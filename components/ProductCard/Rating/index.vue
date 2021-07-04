<template>
  <div class="rating">
    <span
      v-for="_ in [1, 2, 3, 4, 5]"
      :key="{ _ }"
      class="rating__circle"
      v-bind:class="{ filled: rating >= _ }"
    />
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  props: {
    rating: {
      type: Number,
      required: false,
      default: 1
    },
    maxRating: {
      type: Array,
      required: false
    }
  }
};
</script>
<style lang="scss" scoped src="./index.scss" />
