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
export default {
  components: {Tweet},
  name: 'timeline',
  data () {
    return {
      tweets: [
        {auteur: 'Roger', tweet: 'This tweet'},
        {auteur: 'JeanMi', tweet: 'MyTweet'}
      ]
    }
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
