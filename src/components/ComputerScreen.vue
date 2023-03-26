<script setup>
import { Navigation, Autoplay } from 'swiper'
</script>

<template>
  <div class="fl-box">
    <div class="computer-div">
      <div class="main-scr">
        <swiper :modules="[Navigation, Autoplay]" :spaceBetween="10" :centeredSlides="true" :slides-per-view="1"
          :space-between="10" @slideChange="onSlideChange" :loop="true"
          :autoplay="{ 'delay': 1000, 'disableOnInteraction': false }" style="width:100%;height: 100%;">
          <swiper-slide v-for="url in urls" :key="url.id">
            <div class="slide">
              <img :src="url.url" class="imgt" />
              <h3>{{ url.title }}</h3>
            </div>
          </swiper-slide>
          ...
        </swiper>
      </div>
    </div>
    <div class="desk-div">
      SKILLSET
    </div>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue'
import 'swiper/css';

export default {
  name: 'ComputerScreen',
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      urls: [
        { url: "https://upload.wikimedia.org/wikipedia/commons/1/19/C_Logo.png?20201023095457", id: 1, title: "C" },
        { url: "https://upload.wikimedia.org/wikipedia/commons/thumb/1/18/ISO_C%2B%2B_Logo.svg/306px-ISO_C%2B%2B_Logo.svg.png?20170928190710", id: 2, title: "C++" },
        { url: "https://cdn.icon-icons.com/icons2/2415/PNG/512/csharp_original_logo_icon_146578.png", id: 1, title: "C#" },
        { url: "https://upload.wikimedia.org/wikipedia/commons/thumb/d/d5/CSS3_logo_and_wordmark.svg/363px-CSS3_logo_and_wordmark.svg.png?20160530175649", id: 3, title: "CSS" },
        { url: "https://raw.githubusercontent.com/destrex271/destrex271/main/Icons/django1.png", id: 4, title: "Django & Django Rest Framework" },
        { url: "https://www.vectorlogo.zone/logos/flutterio/flutterio-icon.svg", id: 5, title: "Flutter" },
        { url: "https://upload.wikimedia.org/wikipedia/commons/thumb/6/61/HTML5_logo_and_wordmark.svg/512px-HTML5_logo_and_wordmark.svg.png?20170517184425", id: 6, title: "HTML" },
        { url: "https://upload.wikimedia.org/wikipedia/en/thumb/3/30/Java_programming_language_logo.svg/121px-Java_programming_language_logo.svg.png", id: 7, title: "Java" },
        { url: "https://upload.wikimedia.org/wikipedia/commons/thumb/6/6a/JavaScript-logo.png/600px-JavaScript-logo.png?20120221235433", id: 8, title: 'Javascript' },
        { url: "https://upload.wikimedia.org/wikipedia/commons/thumb/3/35/Tux.svg/506px-Tux.svg.png?20220320193426", id: 9, title: 'Linux & Linux Tools' },
        { url: "https://git-scm.com/images/logos/downloads/Git-Icon-White.png", id: 10, title: 'Git' },
        { url: "https://upload.wikimedia.org/wikipedia/commons/thumb/d/d9/Node.js_logo.svg/590px-Node.js_logo.svg.png?20170401104355", id: 11, title: "Node.Js" },
        { url: "https://upload.wikimedia.org/wikipedia/commons/c/c3/Python-logo-notext.svg", id: 12, title: "Python" },
        { url: "https://upload.wikimedia.org/wikipedia/commons/a/a7/React-icon.svg", id: 13, title: "React.JS" },
        { url: "https://upload.wikimedia.org/wikipedia/commons/thumb/2/20/Rustacean-orig-noshadow.svg/1024px-Rustacean-orig-noshadow.svg.png", id: 15, title: "Rust" },
        { url: "https://www.docker.com/wp-content/uploads/2022/03/Moby-logo.png", id: 15, title: "Docker" },
        { url: "https://www.oracle.com/a/ocom/img/pl-sql.svg", id: 16, title: "SQL & PL/SQL" },
        { url: "https://kelvinfan001.github.io/assets/img/actix/logo-large.png", id: 17, title: "Actix Web" },
      ]
    }
  },
  setup() {
    /* const onSwiper = (swiper) => { */
    /*   console.log(swiper); */
    /* }; */
    const onSlideChange = () => {
      console.log('slide change');
    };
    return {
      onSlideChange,
    };
  }
}
</script>

<style>
.fl-box {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.computer-div {
  width: 35rem;
  height: 20rem;
  background-color: black;
  border: 1px solid #fff;
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.slide {
  width: inherit;
  height: inherit;
  background-color: black;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}

.main-scr {
  width: 33rem;
  height: 18rem;
  background-color: black;
  border: 1px solid #fff;
  border-top-left-radius: 5px;
  border-top-right-radius: 5px;
}

.imgt {
  width: 8rem;
}

.desk-div {
  width: 40rem;
  height: 3rem;
  color: white;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  border: 1px solid #fff;
  box-shadow: 0px -7px 4px #ffffffa2;
}

@media screen and (max-width: 900px) {
  .fl-box {
    width: 70vw;
  }

  .computer-div {
    width: 21rem;
    height: 15rem;
    border-radius: 10px;
  }

  .main-scr {
    width: 19rem;
    height: 13rem;
    border-radius: 10px;
  }

  .desk-div {
    display: none;
  }

  .imgt {
    width: 5rem;
  }

  .slide {
    font-size: 1rem;
  }
}
</style>
