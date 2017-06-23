<template>
  <div class="Tweet">
   {{ tweet.auteur }} : {{ tweet.tweet }}
  </div>
</template>

<script>
export default {
  name: 'tweet',
  props: ['tweet']
}

</script>
<style scoped>

 </style>
