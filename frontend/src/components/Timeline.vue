<template>
  <div class="Timeline">

    <ul>
    <li v-for="tweet in tweets">
     <tweet :tweet='tweet'/>
    </li>
    </ul>

  </div>
</template>

<script>
import Tweet from './Tweet'
import Vue from 'vue'
import Resource from 'vue-resource'
Vue.use(Resource)

export default {
  components: {Tweet},
  name: 'timeline',
  data () {
    return {
      tweets: []
    }
  },
  methods: {
    fetchTweets: function () {
      this.$http.get('http://localhost:8080/list').then(response => {
        this.tweets = response.body
        console.log(response.body)
      }, response => {
      })
    }
  },
  created () {
    this.fetchTweets()
  }
}
</script>

<style scoped>
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: block;
  margin: 0 10px;
}
 </style>
