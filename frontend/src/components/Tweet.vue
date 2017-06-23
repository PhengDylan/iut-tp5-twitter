<template>
  <div class="Tweet">
   {{ tweet.auteur }} : {{ tweet.contenu }}
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
