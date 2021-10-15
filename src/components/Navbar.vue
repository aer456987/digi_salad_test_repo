<template>
  <nav class="navbar" :class="isChecked ? 'background-transparent' : ''">
    <div class="navbar__container">
      <div class="navbar__content">
        <h1>
          <a href="#">
            <img src="@/assets/image/logo/logo.svg" alt="DigiSalad logo-sm">
          </a>
        </h1>

        <div class="navbar__links">
          <button type="button" class="btn fw-bold btn--gradual round-1">
            START YOUR PROJECT
          </button>

          <button type="button" class="navbar__toggler" @click="isChecked = !isChecked">
            <span class="navbar__icon" :class="isChecked ? 'navbar__icon--checked' : ''"></span>
          </button>
        </div>
        <!-- <router-link to="/">Home</router-link> |
        <router-link to="/about">About</router-link> -->
      </div>
      <div class="navbar__menu" :class="isChecked ? navbarMenuChecked : ''">
        <div class="navbar__menu__container">
          <div class="navbar__menu__content">
            <ul class="navbar__menu__items">
              <li
                v-for="item in menuDatas"
                :key="item.id"
                class="navbar__menu__item"
                :class="item.data.classStyle"
                :style="item.data.background"
              >
                <div
                  class="navbar__menu__item__content"
                >
                  <img :src="item.data.iconUrl" :alt="item.data.title" class="navbar__menu__img">
                  <h4 class="navbar__menu__title">
                    <span class="navbar__menu__title__span">
                      {{ item.data.subtitle }}
                    </span>
                    {{ item.data.title }}
                  </h4>
                </div>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      isChecked: false,
      navbarMenuChecked: ['navbar__menu--checked', 'background-transparent'],
      menuDatas: [
        {
          id: 'aboutUs',
          data: {
            title: 'ABOUT US',
            subtitle: 'EMPOWERING BRANDS',
            iconUrl: 'icons/uxDesign.svg',
            classStyle: ['navbar__menu__item__aboutUs'],
            background: {
              backgroundImage: 'url("img/menu/AbuotUs_bg.png")',
            },
          },
        },
        {
          id: 'careers',
          data: {
            title: 'CAREERS',
            subtitle: 'BE COOL WITH US',
            iconUrl: 'icons/websiteDevelopment.svg',
            classStyle: ['navbar__menu__item__careers'],
            background: {
              backgroundImage: 'url("img/menu/careers_bg.png")',
            },
          },
        },
        {
          id: 'services',
          data: {
            title: 'SERVICES',
            subtitle: 'AREAS OF EXPERTISE',
            iconUrl: 'icons/01.svg',
            classStyle: ['navbar__menu__item__services'],
            background: {
              backgroundImage: 'url("img/menu/services_bg.png")',
            },
          },
        },
        {
          id: 'works',
          data: {
            title: 'WORKS',
            subtitle: 'CASE STUDIES',
            iconUrl: 'icons/uiDesign.svg',
            classStyle: ['navbar__menu__item__works'],
            background: {
              backgroundImage: 'url("img/menu/Works_bg.png")',
            },
          },
        },
        {
          id: 'insights',
          data: {
            title: 'INSIGHTS',
            subtitle: 'OUR STRATEGIES',
            iconUrl: 'icons/02.svg',
            classStyle: ['navbar__menu__item__insights'],
            background: {
              backgroundImage: 'url("img/menu/insights_bg.png.png")',
            },
          },
        },
        {
          id: 'contact',
          data: {
            title: 'CONTACT',
            subtitle: 'START YOUR JOURNEY WITH US',
            iconUrl: null,
            classStyle: ['navbar__menu__item__contact'],
            background: {
              backgroundImage: null,
            },
          },
        },
      ],
    };
  },
};
</script>

<style lang="sass">
$primary: #26C6D0
$secondary: #FFBC58
$info: #4EE5EA
$dark-100: #414042
$dark-main: #262626

$pink: #EE6C8A
$blue-dark: #585880
$green-light: #26D0A8
$white: #fff
$gray: #F2F2F2
$black: #000
$white: white
@mixin block-style($bgc, $color: $white)
  color: $color
  background: $bgc
@mixin pad()
  @media (max-width: 992px)
    @content

.navbar
  position: fixed
  width: 100%
  top: 0
  background: $white
  z-index: 1000
  transition-duration: .3s

  &__container
    max-width: 1300px
    margin: 0 auto
    padding-left: 25px
    padding-right: 15px

  &__content
    display: flex
    justify-content: space-between
    align-items: center
    padding-top: 25px
    padding-bottom: 22px

  &__links
    display: flex
    align-items: center

  &__toggler
    width: 30px
    height: 22px
    margin-left: 44px
    padding: 0
    border: none
    background: transparent
    cursor: pointer
    +pad
      margin-left: 30px

  &__icon
    display: block
    position: relative
    width: 100%
    height: 3px
    border: none
    border-radius: 5px
    background: $blue-dark
    transition-duration: .3s
    &::before, &::after
      content: ''
      position: absolute
      height: 3px
      right: 0
      border-radius: 5px
      background: $blue-dark
      transition-duration: .3s
    &::before
      width: 100%
      top: -7px
    &::after
      width: 26px
      bottom: -7px

    &--checked
      background: transparent
      transition-duration: .3s
      &::before
        top: 0
        transform: rotate(-45deg)
      &::after
        width: 100%
        top: 0
        transform: rotate(45deg)

.navbar__menu
  height: 1%
  padding-bottom: 96px
  color: $white
  transition-duration: .3s
  opacity: 0
  display: none

  &--checked
    display: block
    height: 100%
    opacity: 1

  &__container
    max-width: 1194
    margin: 0 auto
    padding: 0 30px

  &__items
    display: flex
    flex-wrap: wrap
    justify-content: space-between

  &__item
    position: relative
    border-radius: 30px
    background-position: center center
    background-size: cover
    overflow: hidden
    margin-bottom: 40px

    &__content
      display: flex
      align-items: center
      justify-content: space-between
      padding: 74px 70px 61px 37px
    &__aboutUs, &__services, &__works, &__contact
      width: 35%
    &__careers, &__insights
      width: 25%

    &__aboutUs
      +block-style($primary)
    &__careers
      +block-style($secondary)
    &__services
      +block-style($blue-dark)
    &__works
      +block-style($pink)
    &__insights
      +block-style($green-light)
    &__contact
      +block-style($white, $dark-main)

  &__title
    margin-left: 27px
    font-size: 32px
    letter-spacing: 3.64px
    &__span
      font-size: 16px
      font-weight: 400
      letter-spacing: 1.8px

.background-transparent
  background: $primary

</style>
