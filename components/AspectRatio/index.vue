<template>
  <figure class="aspect-ratio" :aspect-ratio="aspectRatio">
    <img :src="image" :alt="title" />
  </figure>
</template>

<script>
export default {
  props: {
    aspectRatio: {
      type: String,
      required: true
    },
    image: {
      type: String,
      required: true
    },
    title: {
      type: String,
      required: true
    }
  }
};
</script>

<style lang="scss" scoped src="./index.scss" />
