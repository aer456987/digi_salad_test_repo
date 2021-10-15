<template>
  <ul class="service__lists">
    <li v-for="service in serviceDatas" :key="service.id" class="service__lists__item">
      <div class="service__lists__icon">
        <img :src="service.imgUrl" :alt="`${service.id} icon`">
      </div>
      <h4 v-if="service.isalign"
        :style="service.alignStyle"
        class="service__lists__title"
      >
        {{ service.title }}
      </h4>
      <h4 v-else
        class="service__lists__title"
        v-html="service.title"
      ></h4>
      <p class="service__lists__contentText">
        {{ service.contentText }}
      </p>
      <MoreBtn is-round="true" :btn-text="'VIEW MORE'" />
    </li>
  </ul>
</template>

<script>
import MoreBtn from '../MoreBtn.vue';

export default {
  data() {
    return {
      serviceDatas: [
        {
          id: 'uxDesign',
          title: 'UX DESIGN',
          contentText: 'Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare.',
          imgUrl: 'icons/uxDesign.svg',
          isalign: true,
          alignStyle: 'line-height: 40px;',
        },
        {
          id: 'uiDesign',
          title: 'UI DESIGN',
          contentText: 'Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare.',
          imgUrl: 'icons/uiDesign.svg',
          isalign: true,
          alignStyle: 'line-height: 40px;',
        },
        {
          id: 'websiteDevelopment',
          title: 'WEBSITE<br>DEVELOPMENT',
          contentText: 'Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare.',
          imgUrl: 'icons/websiteDevelopment.svg',
          isalign: false,
        },
        {
          id: 'mobileAppDevelopment',
          title: 'MOBILE APP<br>DEVELOPMENT',
          contentText: 'Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare.',
          imgUrl: 'icons/mobileAppDevelopment.svg',
          isalign: false,
        },
        {
          id: 'ecommerce',
          title: 'ECOMMERCE',
          contentText: 'Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare.',
          imgUrl: 'icons/ecommerce.svg',
          isalign: true,
          alignStyle: 'line-height: 40px;',
        },
        {
          id: 'customerLoyalty',
          title: 'CUSTOMER<br>LOYALTY',
          contentText: 'Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare.',
          imgUrl: 'icons/customerLoyalty.svg',
          isalign: false,
        },
        {
          id: 'digitalTransformation',
          title: 'DIGITAL<br>TRANSFORMATION',
          contentText: 'Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare.',
          imgUrl: 'icons/digitalTransformation.svg',
          isalign: false,
        },
        {
          id: 'digitalMarketing',
          title: 'DIGITAL<br>MARKETING',
          contentText: 'Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare.',
          imgUrl: 'icons/digitalMarketing.svg',
          isalign: false,
        },
        {
          id: 'branding',
          title: 'BRANDING',
          contentText: 'Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare.',
          imgUrl: 'icons/branding.svg',
          isalign: true,
          alignStyle: 'line-height: 40px;',
        },
      ],
    };
  },
  components: { MoreBtn },
};
</script>

<style lang="sass">
$white: white
$round: 100%
@mixin pad()
  @media (max-width: 992px)
    @content
@mixin moblie()
  @media (max-width: 766px)
    @content

.service
  &__lists
    display: flex
    flex-wrap: wrap
    justify-content: space-between
    align-items: start
    margin: 85px 0 42px
    color: $white
    +moblie
      margin-bottom: 0
  &__lists__item
    width: 32%
    display: flex
    flex-direction: column
    justify-content: center
    align-items: center
    margin-bottom: 60px
    +pad
      width: 48%
    +moblie
      width: 100%

  &__lists__icon
    width: 108px
    height: 108px
    display: flex
    justify-content: center
    align-items: center
    border-radius: $round
    background: $white
  &__lists__title
    height: 40px
    margin: 20px 0 15px
    text-align: center
    font-size: 20px
    font-weight: 700
    letter-spacing: 2px
  &__lists__contentText
    margin-bottom: 20px
    line-height: 1.75
    text-align: center
    font-size: 16px

</style>
