<template>
  <Header />

  <main>
    <section class="aboutOurs">
      <div class="aboutOurs__container">
        <div class="aboutOurs__content">
          <TitleStyle :title-data="aboutOurs" />

          <div class="aboutOurs__video__size">
            <iframe
              class="aboutOurs__video"
              src="https://www.youtube.com/embed/IeIRJ9jZ5Ro"
              allowfullscreen="true"
            ></iframe>
          </div>

          <p class="aboutOurs__text__content">
            Cras quis nulla commodo, aliquam lectus sed, blandit augue.
            Cras ullamcorper bibendum bibendum.
            Duis tincidunt urna non pretium porta.
            Nam condimentum vitae ligula vel ornare.
            Phasellus at semper turpis.
            Nunc eu tellus tortor.
            Etiam at condimentum nisl, vitae sagittis orci.
            Donec id dignissim nunc.
            Donec elit ante, eleifend a dolor et, venenatis facilisis dolor.
            In feugiat orci odio, sed lacinia sem elementum quis.
            Aliquam consectetur, eros et vulputate euismod,
            nunc leo tempor lacus, ac rhoncus neque eros nec lacus.
            Cras lobortis molestie faucibus.
          </p>
          <MoreBtn :btn-text="aboutOurs.btnText" :btn-class="aboutOurs.btnClass" />
        </div>
      </div>
    </section>

    <section class="awards">
      <div class="awards__content">
        <div class="awards__text">
          <TitleStyle :title-data="awards" />
          <p>
            Cras quis nulla commodo, aliquam lectus sed, blandit augue.
            Cras ullamcorper bibendum bibendum. Duis tincidunt urna non pretium porta.
            Nam condimentum vitae ligula vel ornare.
            Phasellus at semper turpis. Nunc eu tellus tortor.
            Etiam at condimentum nisl, vitae sagittis orci.
            Donec id dignissim nunc.
            </p>
        </div>
        <ul class="awards__lists">
          <li class="awards__lists__item mb-10">
            <img src="@/assets/image/awards_img.jpg" alt="awards img">
          </li>
          <li class="awards__lists__item mb-10">
            <img src="@/assets/image/awards_img.jpg" alt="awards img">
          </li>
          <li class="awards__lists__item">
            <img src="@/assets/image/awards_img.jpg" alt="awards img">
          </li>
          <li class="awards__lists__item">
            <img src="@/assets/image/awards_img.jpg" alt="awards img">
          </li>
        </ul>
      </div>
    </section>

    <section class="ourIngradients">
      <div class="ourIngradients__container">
        <div class="ourIngradients__content">
          <TitleStyle :title-data="ourIngradients" />
          <p class="ourIngradients__text mb-15">
            Cras quis nulla commodo, aliquam lectus sed, blandit augue.
            Cras ullamcorper bibendum bibendum.
            Duis tincidunt urna non pretium porta.
            Nam condimentum vitae ligula vel ornare.
            Phasellus at semper turpis.
            Nunc eu tellus tortor.
            Etiam at condimentum nisl, vitae sagittis orci.
            Donec id dignissim nunc.
            Donec elit ante, eleifend a dolor et, venenatis facilisis dolor.
            In feugiat orci odio, sed lacinia sem elementum quis.
            Aliquam consectetur,
            eros et vulputate euismod, nunc leo tempor lacus, ac rhoncus neque eros nec lacus.
            Cras lobortis molestie faucibus.
          </p>
          <MoreBtn :btn-text="ourIngradients.btnText" :btn-class="ourIngradients.btnClass" />
          <ServiceItems />
          <a href="#" class="ourIngradients__more__link">
            VIEW MORE DIGISALAD’S INGRADIENTS
          </a>
        </div>
      </div>
    </section>

    <section class="leaderIdeal">
      <div class="leaderIdeal__content" :style="leaderIdeal.background">
        <div class="leader__data">
          <div class="leader__data__img">
            <img src="@/assets/image/leader.png" alt="leader pic">
          </div>
          <h4 class="leader__data__name">
            Tony Ng <br>
            <span class="leader__data__position">
              Founder & Creative Director
            </span>
          </h4>
        </div>
        <div class="leaderIdeal__text__content">
          <div class="leaderIdeal__icons">
            <img src="icons/leader.svg" alt="leaderIdeal__icon" class="leaderIdeal__icon">
            <img src="icons/leader.svg" alt="leaderIdeal__icon" class="leaderIdeal__icon">
          </div>
          <p class="leaderIdeal__text__content__text">
            A great digital work isn’t about designing beautiful pages purely.
            It is about context - how do we deliver the right experience to the
            <span class="leaderIdeal__text__content--mark">
              right person at the right time.
            </span>
            The most important thing is that your work can engage customers at anytime,
            anywhere and let users experience an entire amazing digital journey.
          </p>
        </div>

      </div>
    </section>

    <section class="brandExperience">
      <div class="brandExperience__content">
        <TitleStyle :title-data="brandExperience" />
        <p class="brandExperience__text">
          Cras quis nulla commodo, aliquam lectus sed, blandit augue.
          Cras ullamcorper bibendum bibendum.
          Duis tincidunt urna non pretium porta.
          Nam condimentum vitae ligula vel ornare.
          Phasellus at semper turpis.
          Nunc eu tellus tortor.
          Etiam at condimentum nisl, vitae sagittis orci.
          Donec id dignissim nunc.
          Donec elit ante, eleifend a dolor et, venenatis facilisis dolor.
          In feugiat orci odio, sed lacinia sem elementum quis.
          Aliquam consectetur, eros et vulputate euismod,
          nunc leo tempor lacus, ac rhoncus neque eros nec lacus.
          Cras lobortis molestie faucibus.
        </p>
        <img src="@/assets/image/brandExperience_items.jpg" alt="brandExperience"
          class="brandExperience__items"
        >
      </div>
    </section>

    <section class="projects" :style="projects.background">
      <div class="projects__container">
        <div class="projects__content">
          <button type="button" class="projects__navigation projects__navigation__start"></button>
          <button type="button" class="projects__navigation projects__navigation__end"></button>

          <div class="projects__imgs">
            <div class="projects__imgs__img">
              <img src="@/assets/image/projects/project.jpg" alt="project">
            </div>
            <MoreBtn :btn-text="projects.btnText" :btn-class="projects.btnClass"/>
          </div>

          <div class="projects__text__content">
            <div>
              <h4 class="projects__title">
                <span class="projects__subtitle">HIGHLIGHTED SHOWCASE</span>
                LP CLUB MOBILE APP
              </h4>
              <p class="projects__text">
                Cras quis nulla commodo, aliquam lectus sed, blandit augue.
                Cras ullamcorper bibendum bibendum.
                Duis tincidunt urna non pretium porta.
                Nam condimentum vitae ligula vel ornare.
                Phasellus at semper turpis.
                Nunc eu tellus tortor.
                Etiam at condimentum nisl, vitae sagittis orci.
                Donec id dignissim nunc.
                Donec elit ante, eleifend a dolor et, venenatis facilisis dolor.
                In feugiat orci odio, sed lacinia sem elementum quis.
                Aliquam consectetur, eros et vulputate euismod,
                nunc leo tempor lacus, ac rhoncus neque eros nec lacus.
                Cras lobortis molestie faucibus.
              </p>
            </div>
            <div>
              <span class="projects__date projects__date__momth">01</span>
              <span></span>
              <span class="projects__date projects__date__day">04</span>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import Header from '../components/blocks/Header.vue';
import TitleStyle from '../components/TitleStyle.vue';
import MoreBtn from '../components/MoreBtn.vue';
import ServiceItems from '../components/blocks/ServiceItems.vue';

export default {
  data() {
    return {
      aboutOurs: {
        title: 'ABOUT DIGISALAD',
        color: ['text-dark-main', 'mb-45', 'mb-md-20'],
        btnText: 'VIEW MORE',
        btnClass: 'btn-primary',
      },
      awards: {
        title: 'AWARDS',
        color: ['text-dark-main', 'mb-25', 'mb-md-15'],
      },
      ourIngradients: {
        title: 'OUR INGRADIENTS',
        color: ['text-white', 'mb-29', 'mb-md-20'],
        btnText: 'OUR SERVICES',
        btnClass: 'btn-blue-dark',
      },
      leaderIdeal: {
        background: {
          backgroundImage: 'url("img/leader_bg.png")',
        },
      },
      brandExperience: {
        title: 'OUR BRAND EXPERIENCE',
        color: ['text-dark-main', 'mb-37', 'mb-md-15'],
      },
      projects: {
        // title: 'OUR INGRADIENTS',
        // color: ['text-white', 'mb-29', 'mb-md-20'],
        btnText: 'VIEW PROJECT',
        btnClass: ['btn-primary', 'projects__btn'],
        background: {
          backgroundImage: 'url("./img/project_bg.jpg")',
        },
      },
    };
  },
  components: {
    Header,
    TitleStyle,
    MoreBtn,
    ServiceItems,
  },
};
</script>
