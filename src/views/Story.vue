<template>
  <div>
    <section class="bg-cover bg-story h-[500px] bg-right">
      <div class="container flex justify-center items-center px-4 h-full">
        <div
          class="editableContent break-words z-10 text-center relative top-8 md:top-12 lg:top-[50px]"
        >
          <p class="z-10 text-center">
            <span class="z-10 text-white"
              ><strong class="z-10"
                ><span class="text-[34px] z-10"
                  ><span class="font-['Source_Han_Sans'] z-10"
                    >我们的故事</span
                  ></span
                ></strong
              ></span
            >
          </p>

          <p class="z-10 text-center">
            <span class="tracking-[7px] z-10"
              ><span class="font-['Arial_Black'] z-10"
                ><span class="z-10 text-white"
                  ><span class="z-10 text-sm">O</span></span
                ><span class="text-[#00ffc0] z-10"
                  ><span class="z-10 text-sm">U</span></span
                ><span class="z-10 text-white"
                  ><span class="z-10 text-sm">R S</span></span
                ><span class="text-[#00ffc0] z-10"
                  ><span class="z-10 text-sm">T</span></span
                ><span class="z-10 text-white"
                  ><span class="z-10 text-sm">ORY</span></span
                ></span
              ></span
            >
          </p>
        </div>
      </div>
    </section>
    <section
      class="mt-10 h-max max-md:px-2 section"
      style="background-image: url('/src/assets/story-bg.png')"
    >
      <div
        class="container flex flex-col gap-4 justify-between items-center mx-auto space-y-6 md:flex-row sm:px-6 md:space-y-0"
      >
        <img
          src="/src/assets/images/story/2.png"
          alt=""
          class="h-full w-full max-w-[426px]"
          data-aos="fade-left"
        />
        <div
          class="md:h-[534px] w-full md:w-[706px] z-[7] border-[#03ffc0] border-[4px] pt-24 pb-12 max-md:px-4 md:pl-[32px]"
        >
          <div class="overflow-visible">
            <div class="w-container" data-effect-name="enterTop">
              <div class="md:h-[290px] md:w-[636px] z-[6]" ctrl-location="main">
                <div class="overflow-hidden">
                  <div class="h-full break-words">
                    <p>
                      <span class="text-[30px]"
                        ><strong
                          ><span class="font-['Source_Han_Sans']"
                            >智勝危機&nbsp;思變未來</span
                          ></strong
                        ></span
                      >
                    </p>
                  </div>
                  <div class="h-[50px] w-[143px] z-[3]">
                    <div class="overflow-hidden">
                      <div class="h-full break-words editableContent">
                        <span
                          class="text-[#888888] leading-[1.5] font-['Arial'] text-sm"
                          >Outsmart the crisis, think about the future.</span
                        >
                      </div>
                    </div>
                  </div>
                  <div class="md:h-[292px] md:w-[610px] z-[4]">
                    <div class="overflow-hidden">
                      <div class="h-full break-words">
                        <p class="text-justify">
                          <span class="leading-[1.5] text-sm font-['宋体']"
                            >公司在中國香港成立於2011年。團隊總部位於香港，在上海設有分支機構。我們的團隊由一支充滿活力的企業家和受過國內外高等教育的員工組成，他們來自全球電信領導者公司和中國現有運營商等不同背景。我們致力于为国内外企业提供高品质端到端通信解决方案、IT集成服务。帮助客户优化网络基础架构和管理能力，提高IT投资效率，增强企业的核心竞争力。以优质的产品、卓越的服务为各类用户提供全面专业的行业解决方案以满足企业高端信息服务需求。</span
                          >
                        </p>

                        <p class="text-justify">&nbsp;</p>

                        <p class="text-justify">
                          <span
                            class="leading-[1.5] text-[12px] md:text-[10px] md:text-xs block"
                            >The company was established in Hong Kong, China in
                            2011. The team is headquartered in Hong Kong and has
                            a branch in Shanghai. Our team consists of a dynamic
                            team of entrepreneurs and highly educated employees
                            from various backgrounds, including global
                            telecommunications leaders and existing Chinese
                            operators. We are committed to providing
                            high-quality end-to-end communication solutions and
                            IT integration services for domestic and foreign
                            enterprises. Assist clients in optimizing network
                            infrastructure and management capabilities,
                            improving IT investment efficiency, and enhancing
                            the core competitiveness of the enterprise. To
                            provide comprehensive and professional industry
                            solutions for various users with high-quality
                            products and excellent services to meet the high-end
                            information service needs of enterprises.</span
                          >
                        </p>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import { ref, computed, onMounted } from 'vue'
import { getArticleList, formatDate } from '../utils/markdown'

export default {
  name: 'Articles',
  setup() {
    const searchQuery = ref('')
    const articleList = ref([])
    const loading = ref(true)

    // --- 新增的状态 ---
    const activeCategory = ref('all') // 当前选中的分类
    const activeTag = ref(null) // 当前选中的标签

    const fetchArticles = async () => {
      loading.value = true
      try {
        const { articleList: list } = await getArticleList()
        articleList.value = list.value
      } catch (error) {
        console.error('加载文章列表失败:', error)
      } finally {
        loading.value = false
      }
    }

    // --- 新增的计算属性 ---
    // 从所有文章中自动计算出不重复的分类列表
    const categories = computed(() => {
      const allCategories = articleList.value.map((article) => article.category)
      // 使用 Set 去重并转换为数组，然后在前面加上“全部”选项
      return ['all', ...new Set(allCategories)].filter(Boolean)
    })

    // 从所有文章中自动计算出不重复的标签列表
    const tags = computed(() => {
      const allTags = articleList.value.flatMap((article) => article.tags)
      return [...new Set(allTags)].filter(Boolean)
    })

    // --- 升级后的过滤逻辑 ---
    const filteredArticles = computed(() => {
      let articles = articleList.value

      // 1. 按分类过滤
      if (activeCategory.value !== 'all') {
        articles = articles.filter(
          (article) => article.category === activeCategory.value
        )
      }

      // 2. 按标签过滤
      if (activeTag.value) {
        articles = articles.filter(
          (article) => article.tags && article.tags.includes(activeTag.value)
        )
      }

      // 3. 按搜索框内容过滤
      if (searchQuery.value) {
        const query = searchQuery.value.toLowerCase()
        articles = articles.filter((article) => {
          return (
            article.title.toLowerCase().includes(query) ||
            (article.summary && article.summary.toLowerCase().includes(query))
          )
        })
      }

      return articles
    })

    // --- 新增的点击事件处理函数 ---
    const selectCategory = (category) => {
      activeCategory.value = category
      activeTag.value = null // 选择分类时清空已选标签
      searchQuery.value = '' // 选择分类时清空搜索框
    }

    const selectTag = (tag) => {
      // 如果再次点击同一个标签，则取消选择
      if (activeTag.value === tag) {
        activeTag.value = null
      } else {
        activeTag.value = tag
        activeCategory.value = 'all' // 选择标签时，分类重置为“全部”
        searchQuery.value = '' // 选择标签时清空搜索框
      }
    }

    const formatArticleDate = (dateString) => {
      return formatDate(dateString)
    }

    onMounted(() => {
      fetchArticles()
    })

    return {
      searchQuery,
      articleList,
      filteredArticles,
      loading,
      formatArticleDate,
      categories,
      tags,
      activeCategory,
      activeTag,
      selectCategory,
      selectTag,
    }
  },
}
</script>
