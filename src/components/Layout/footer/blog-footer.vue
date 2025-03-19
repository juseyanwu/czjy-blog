<template>
  <!-- 最外层 div 是占位置的 -->
  <div
    v-if="route.path !== '/message/chat'"
    class="footer_box flex flex-col items-center justify-center"
  >
    <!-- eslint-disable-next-line -->
    <div class="footer-color">&copy 陈子进的博客 2024</div>
    <a class="footer-color change-color mt-[5px]" href="http://beian.miit.gov.cn/" target="_blank"
      >赣ICP备2024032778号</a
    >
  </div>
</template>

<script setup>
import { useRoute } from "vue-router";
const route = useRoute();
</script>

<style lang="scss" scoped>
.footer-color {
  color: var(--font-color);
  text-align: center;
}

.change-color {
  text-decoration: none;
  transition: all 0.3s;

  &:hover {
    color: var(--global-black);
  }
}
</style>
