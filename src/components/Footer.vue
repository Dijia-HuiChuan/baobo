<template>
  <footer class="bg-[#343434]">
    <div class="container px-4 h-[149px] flex pb-[20px] mx-auto">
      <div class="text-[#999999] mt-auto">© 2025 Baobo Technology株式会社.</div>
    </div>
  </footer>
</template>

<script>
// ... (script 部分保持不变) ...
import siteConfig from '../config/site.js'

export default {
  name: 'Footer',
  setup() {
    return {
      siteConfig,
    }
  },
}
</script>

<style scoped>
.footer-glass {
  background-color: rgba(255, 255, 255, 0.7); /* 半透明白色背景 */
  backdrop-filter: blur(12px); /* 毛玻璃模糊效果 */
  -webkit-backdrop-filter: blur(12px);
  border-top: 1px solid rgba(255, 255, 255, 0.2); /* 顶部细线，增加层次感 */
}

.social-icon {
  @apply w-9 h-9 rounded-full flex items-center justify-center text-gray-600 bg-gray-100/50 hover:bg-gray-200/70 hover:text-primary-500 transition-all duration-300;
}
</style>
