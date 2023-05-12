<template>
  <div class="blog-div">
    <swiper :modules="modules" :slides-per-view="sPrev" :space-between="sBtw"
      :autoplay="{ 'delay': 2500, 'disableOnInteraction': false }">
      <swiper-slide v-for="post in posts" :key="post.key" class="slide">
        <div class="blog-box">
          <img :src="post.image"
            style="width: 100%;border-top-left-radius: 10px;border-top-right-radius: 10px;height: inherit;" />
          <a :href="post.link" target="_blank" class=" card-title">
            {{ post.title }}
          </a>
        </div>
      </swiper-slide>
      ...
    </swiper>
  </div>
</template>
<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Autoplay } from 'swiper';
import 'swiper/css';
import axios from 'axios'
import { ref } from 'vue'

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  async setup() {
    const sPrev = ref(2);
    const sBtw = ref(30);
    if (window.innerWidth < 900) {
      sPrev.value = 1;
      sBtw.value = 1;
    }
    const posts = ref(null)
    const res = await axios.get("https://mediumpostsapi.vercel.app/api/destrex271");
    var data = await res.data['dataMedium'];
    data = data.map((dt, index) => { dt['key'] = index; return dt; })
    posts.value = data;
    return {
      posts,
      modules: [Autoplay],
      sPrev,
      sBtw
    };
  },
};
</script>
<style>
.blog-div {
  margin-top: 4rem;
  width: 85%;
  height: 60vh;
  border-radius: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  padding-left: 3rem;
  padding-right: 3rem;
}

.blog-box {
  width: 30rem;
  height: 25rem;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  color: white;
}

.slide {
  display: flex;
  justify-content: center;
  align-items: center;
}

.card-title {
  color: white;
  width: inherit;
  height: 5rem;
  font-size: 1.3rem;
  font-family: 'Share Tech Mono', monospace;
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
  border: 0.2px solid #333;
  text-decoration: none;
}

.card-title:hover {
  background-color: #222;
  transition: background 0.3s ease-in;
}

@media screen and (max-width: 900px) {
  .blog-box {
    width: 20rem;
  }
}
</style>
