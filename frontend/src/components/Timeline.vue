<template>
  <div class="Timeline">
    <h1>{{ tweets }}</h1>
    <ul>
    <li><v-for="tweet in tweets"></li>
    </ul>

  </div>
</template>

<script>
export default {
  name: 'timeline',
  data () {
    return {
      tweets: ['tweet 1', 'tweet 2', 'tweet 3']
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
