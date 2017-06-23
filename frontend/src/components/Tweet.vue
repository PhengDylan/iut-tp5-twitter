<template>
  <div class="Tweet">

    <ul>
    {{ tweets.Auteur }} : {{ tweets.tweet }}
    </ul>

  </div>
</template>

<script>
export default {
  name: 'tweet',
  props: ['tweet']
  }
}
</script>

<style scoped>

}
 </style>
