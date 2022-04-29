<template>
  <div class="home">
    <HeaderComponents />
    <img alt="Home Logo" src="../assets/HomeLogo.png"/>
    <div>
      <router-link :to="{name: 'AboutPage'}">
        <button>소개 페이지로 이동하기</button>
      </router-link>
    </div>
  </div>
</template>

<script>
import HeaderComponents from '../components/Header.vue'
export default {
  name: 'HomePage',
  components: {
    HeaderComponents,
  },
};
</script>
