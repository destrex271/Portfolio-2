
<template>
  <div class="main-box-dev center">
    <div class="head-box-dev">
      <div class="head-blog-text">
        Blogs
        <img src="@/assets/pen.png" class="pen" />
      </div>
    </div>
    <Suspense>
      <template #default>
        <BlogCards />
      </template>
      <template #fallback>
        <div class="blog-div" style="border: 1px solid white;">
        </div>
      </template>
    </Suspense>
  </div>
</template>

<script>
import BlogCards from './BlogCards.vue';
import { Suspense } from 'vue';

export default {
  components: {
    BlogCards,
    Suspense
  }
}
</script>

<style>
.center {
  align-items: center;
  flex-direction: column;
}

.head-blog-text {
  font-size: 5rem;
  font-family: 'Architects Daughter', cursive;
}

.pen {
  width: 5rem;
  margin-left: -1.5rem;
}
</style>
