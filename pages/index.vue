<template>
  <div class="grid">
    <NuxtLink v-for="_ in a" :key="_.i" :to="`/${_.i}`">
      {{ _.n }}
    </NuxtLink>
  </div>
</template>

<script>
export default {
  data() {
    return {
      a: []
    };
  },
  async fetch() {
    let _ = await fetch("https://skincare-api.herokuapp.com/products", {
      mode: "no-cors"
    });
    _ = await _.json();
    const _z = [];
    _.forEach(_x => {
      _z.push({
        i: _x.id,
        n: _x.name
      });
    });
    this.a = [..._z];
  }
};
</script>

<style lang="scss" scoped src="./index.scss" />
