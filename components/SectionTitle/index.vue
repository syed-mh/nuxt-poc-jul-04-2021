<template>
  <div v-if="title" class="section-title">
    <div class="boxed">
      <h1 class="section-title__title">
        {{ title }}
      </h1>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    }
  }
};
</script>

<style lang="scss" scoped src="./index.scss" />
