<template>
  <div class="about-page">
    <HeaderComponents/>
    <main>
      <div class="w3-container">
        <ul class="item-title">
          <li v-for="item in AboutInfo[0].items" :key="item">
            주요 연구:{{item.itemTitle}} || 상세내용: {{item.itemDescription}}
          </li>
        </ul>
      </div>
    </main>
  </div>
</template>

<script>
import HeaderComponents from "../components/Header.vue";
export default {
  name: "AboutPage",
  components: {
    HeaderComponents,
  },
  data() {
    return {
      AboutInfo: [{
        title: 'JOACE',
        description: '하고 싶은 것을 전부 올릴 웹페이지입니다!',
        items: [
          {
            itemTitle: 'Virtual Reality',
            itemDescription: '완전 몰입형 가상현실 기획'
          },
          {
            itemTitle: 'Augmented Reality',
            itemDescription: '자비스 같은 인공지능 IOT 서비스 제공'
          },
          { itemTitle: '논문 연구',
            itemDescription: '영상처리, 컴퓨터 비전, 그래픽스 논문 연구' 
          }
        ]
      }]
    }
  },
  methods: {
    isDataExist() { if (this.items) { return true; } return false; },
  }
};
</script>

<style scoped>
.item-title {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}
</style>