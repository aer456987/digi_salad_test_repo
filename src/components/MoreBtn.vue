<template>
  <a v-if="isRound"
    href="#"
    class="moreBtnStyleBtn__round"
  >
    {{ btnText }}
  </a>

  <template v-else>
    <a href="#"
      class="moreBtnStyleBtn" :class="btnClass"
    >
      {{ btnText }}
      <span class="moreBtnStyleBtn__line"></span>
    </a>
  </template>
</template>

<script>
export default {
  props: ['btnText', 'btnClass', 'isRound'],
};
</script>

<style lang="sass">
$white: white
$base-font-size: 10px
@mixin moblie()
  @media (max-width: 766px)
    @content

.moreBtnStyleBtn
  display: flex
  justify-content: center
  align-items: center
  padding: 33px 25px
  border: none
  font-size: $base-font-size*1.6
  font-weight: 700
  letter-spacing: 2.2px
  color: $white
  cursor: pointer

  &__line
    display: block
    width: 52px
    height: 1.5px
    margin-left: 15px
    background: $white
    +moblie
      margin-left: 0px

.moreBtnStyleBtn__round
  display: flex
  justify-content: center
  padding: 20px 35px
  border: solid 2px
  border-radius: 30px
  font-weight: 700
  font-size: $base-font-size*1.4
  letter-spacing: 2.2px
  color: $white
  cursor: pointer

</style>
