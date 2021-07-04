<template>
  <article class="category-card">
    <div class="category-card__thumbnail">
      {{ `${category[0]}` }}
    </div>
    <h3 class="category-card__title">
      <NuxtLink :to="`category/${category}`">
        {{ `${category.split("_").join(" ")}` }}
      </NuxtLink>
    </h3>
  </article>
</template>

<script>
export default {
  props: {
    category: {
      type: String,
      required: true
    }
  }
};
</script>

<style lang="scss" scoped src="./index.scss" />
