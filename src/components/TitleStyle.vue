<template>
  <h3 class="titleStyle" :class="titleData.color">
    {{ titleData.title }}
  </h3>
</template>

<script>
export default {
  props: ['titleData'],
};
</script>

<style lang="sass">
.titleStyle
  font-size: 28px
  font-weight: 700
  letter-spacing: 3.64px
</style>
