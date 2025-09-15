<template>
  <header
    class="top-0 z-50 bg-transparent shadow-sm"
    :class="{ '!bg-[#000]': !isHomePage || isMenuOpen }"
  >
    <nav class="container flex justify-between items-center px-4 py-3 mx-auto">
      <!-- Logo -->
      <router-link to="/" class="flex items-center space-x-2">
        <div class="overflow-hidden w-[53px] h-[53px] rounded-full">
          <img
            :src="siteConfig.site.logo"
            :alt="siteConfig.site.title"
            class="object-cover w-full h-full"
          />
        </div>
        <span class="text-xl font-bold kawaii-gradient-text">{{
          siteConfig.site.title
        }}</span>
      </router-link>

      <!-- 移动端菜单按钮 -->
      <button
        @click="toggleMenu"
        class="p-2 text-lg text-gray-500 rounded-full md:hidden focus:outline-none"
      >
        <i :class="isMenuOpen ? 'fa-solid fa-xmark' : 'fa-solid fa-bars'"></i>
      </button>

      <!-- 桌面端导航链接 -->
      <div
        class="hidden relative items-center space-x-1 md:flex"
        ref="navContainer"
      >
        <router-link
          v-for="(item, index) in siteConfig.navItems"
          :key="item.path"
          :to="item.path"
          :ref="(el) => setNavItemRef(el, index)"
          class="transition-colors duration-300 nav-link w-[138px] px-[15px] text-center text-sm text-white block relative"
          :class="[
            $route.path === item.path
              ? 'text-primary-600 font-medium'
              : 'text-gray-600 hover:text-primary-600',
          ]"
          @mouseenter="handleNavHover(index)"
          @mouseleave="handleNavLeave"
        >
          {{ item.name }}
        </router-link>

        <!-- 全局小圆点 -->
        <div
          class="nav-dot-global"
          :class="{
            'nav-dot-visible': dotVisible,
            'nav-dot-active': isActiveDot,
          }"
          :style="dotStyle"
        ></div>
      </div>
    </nav>

    <!-- 移动端导航菜单 -->
    <div
      v-if="isMenuOpen"
      class="absolute inset-0 top-[76px] bg-black bg-opacity-95 h-max md:hidden"
    >
      <div class="container py-2 pr-4 pl-10 mx-auto">
        <router-link
          v-for="item in siteConfig.navItems"
          :key="item.path"
          :to="item.path"
          class="block px-6 py-4 text-lg font-medium text-white border-b border-white border-dashed transition-colors duration-300"
          :class="[
            $route.path === item.path
              ? 'text-primary-400 bg-gray-800'
              : 'text-white',
          ]"
          @click="isMenuOpen = false"
        >
          {{ item.name }}
        </router-link>
      </div>
    </div>
  </header>
</template>

<script>
import { ref, computed, onMounted, nextTick, watch } from 'vue'
import { useRoute } from 'vue-router'
import siteConfig from '../config/site.js'

export default {
  name: 'Navbar',
  setup() {
    const isMenuOpen = ref(false)
    const navItems = ref({})
    const navContainer = ref(null)
    const dotVisible = ref(false)
    const dotStyle = ref({})
    const hoveredIndex = ref(-1)
    const currentActiveIndex = ref(-1)

    // 设置导航项ref
    const setNavItemRef = (el, index) => {
      if (el) {
        navItems.value[index] = el
      }
    }
    const route = useRoute()

    // 检测是否是"总之就是非常可爱"页面
    const isKawaiiPage = computed(() => {
      return route.path === '/kawaii'
    })

    const isHomePage = computed(() => {
      return route.path === '/'
    })
    // 判断小圆点是否为active状态
    const isActiveDot = computed(() => {
      return hoveredIndex.value === -1 && currentActiveIndex.value !== -1
    })

    // 获取当前active导航项的索引
    const getActiveIndex = () => {
      return siteConfig.navItems.findIndex((item) => item.path === route.path)
    }

    // 计算小圆点位置
    const calculateDotPosition = (index) => {
      if (!navItems.value[index] || !navContainer.value) {
        return {}
      }

      const navItem = navItems.value[index].$el || navItems.value[index]
      const containerRect = navContainer.value.getBoundingClientRect()
      const itemRect = navItem.getBoundingClientRect()

      const left = itemRect.left - containerRect.left + itemRect.width / 2 - 3 // 3px是圆点半径

      return {
        left: `${left}px`,
        transition: 'all 0.3s cubic-bezier(0.4, 0, 0.2, 1)',
      }
    }

    // 更新小圆点位置
    const updateDotPosition = () => {
      const targetIndex =
        hoveredIndex.value !== -1
          ? hoveredIndex.value
          : currentActiveIndex.value

      if (targetIndex !== -1) {
        dotStyle.value = calculateDotPosition(targetIndex)
        dotVisible.value = true
      } else {
        dotVisible.value = false
      }
    }

    // 处理导航项hover
    const handleNavHover = (index) => {
      hoveredIndex.value = index
      updateDotPosition()
    }

    // 处理鼠标离开
    const handleNavLeave = () => {
      hoveredIndex.value = -1
      updateDotPosition()
    }

    // 初始化小圆点位置
    const initializeDot = async () => {
      await nextTick()
      await nextTick() // 双重nextTick确保DOM完全渲染

      currentActiveIndex.value = getActiveIndex()
      updateDotPosition()
    }

    // 监听路由变化
    watch(
      () => route.path,
      () => {
        currentActiveIndex.value = getActiveIndex()
        updateDotPosition()
      }
    )

    onMounted(() => {
      initializeDot()
    })

    return {
      isMenuOpen,
      toggleMenu: () => {
        isMenuOpen.value = !isMenuOpen.value
      },
      siteConfig,
      navContainer,
      navItems,
      dotVisible,
      dotStyle,
      isActiveDot,
      handleNavHover,
      handleNavLeave,
      setNavItemRef,
      isHomePage,
    }
  },
  watch: {
    $route() {
      this.isMenuOpen = false
    },
  },
}
</script>

<style>
.nav-link {
  @apply px-4 py-2 rounded-md;
}

/* 全局小圆点样式 */
.nav-dot-global {
  position: absolute;
  bottom: -8px;
  width: 6px;
  height: 6px;
  border-radius: 50%;
  background: linear-gradient(135deg, #ffb7c5, #ff9eb2);
  opacity: 0;
  z-index: 10;
  box-shadow: 0 2px 4px rgba(255, 183, 197, 0.3);
  pointer-events: none;
}

/* 小圆点可见状态 */
.nav-dot-visible {
  opacity: 1;
}

/* active状态的小圆点 */
.nav-dot-active {
  background: linear-gradient(135deg, #ff9eb2, #ff8fa3);
  box-shadow: 0 0 12px rgba(255, 183, 197, 0.8),
    0 0 20px rgba(255, 183, 197, 0.4);
  transform: scale(1.1);
}

/* hover状态的小圆点 */
.nav-dot-global:not(.nav-dot-active) {
  box-shadow: 0 0 8px rgba(255, 183, 197, 0.6);
}

/* 总之就是非常可爱文本样式 */
.kawaii-text {
  color: #ffb7c5 !important;
}

/* 渐变文本样式，用于kawaii页面的网站标题 */
.kawaii-gradient-text {
  background: linear-gradient(to right, #ffb7c5, #d8aef2);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  color: transparent;
}

/* 总之就是非常可爱导航链接特殊样式 */
.kawaii-nav-link {
  background: linear-gradient(
    to right,
    rgba(255, 183, 197, 0.1),
    rgba(216, 174, 242, 0.1)
  );
  position: relative;
}

.kawaii-nav-link::after {
  content: '❤';
  position: absolute;
  top: -2px;
  right: -2px;
  font-size: 10px;
  color: #ffb7c5;
}

.kawaii-nav-link:hover {
  background: linear-gradient(
    to right,
    rgba(255, 183, 197, 0.2),
    rgba(216, 174, 242, 0.2)
  );
  color: #ffb7c5 !important;
}

.nav-link:hover {
  color: #ffb7c5 !important;
}

.kawaii-nav-link.text-primary-600,
.kawaii-nav-link.text-primary-500 {
  background: linear-gradient(
    to right,
    rgba(255, 183, 197, 0.3),
    rgba(216, 174, 242, 0.3)
  );
  color: #ff9eb2 !important;
}
</style>
