<template>
  <div>
    <section class="h-[600px] md:h-[750px] lg:h-[900px] bg-cover bg-center">
      <div
        class="relative bg-home h-[600px] md:h-[750px] lg:h-[900px] bg-cover bg-center flex justify-center items-center"
      >
        <div class="container px-4 mx-auto sm:px-6 lg:px-8">
          <div class="flex flex-col items-center">
            <span
              class="text-[32px] md:text-[42px] lg:text-[54px] font-bold text-white text-center"
              data-aos="zoom-in"
            >
              BAOBO TECHNOLOGY
            </span>
            <span
              class="text-white text-[16px] md:text-[18px] lg:text-[22px] mt-2 text-center"
              data-aos="zoom-in"
            >
              褒博機電科技有銀公司
            </span>
            <div
              class="line h-[50px] md:h-[65px] lg:h-[80px] w-[1px] mt-[25px] md:mt-[32px] lg:mt-[40px] bg-white"
              data-aos="fade-up"
            ></div>
          </div>
        </div>
        <img
          src="../assets/images/home/down.gif"
          alt=""
          class="w-[21px] h-[34px] absolute bottom-9"
          data-aos="fade-down"
        />
      </div>
    </section>

    <section class="bg-[#fafafa] py-12 md:py-16 lg:py-20">
      <div class="container px-4 mx-auto sm:px-6 lg:px-8">
        <div
          class="flex mb-8 max-md:flex-col lg:flex-row lg:justify-between lg:items-center text md:mb-12 lg:mb-16"
        >
          <div
            class="w-full lg:w-[300px] flex-shrink-0 text-center lg:text-left mb-6 lg:mb-0"
          >
            <h2
              class="mb-4 text-[24px] md:text-[28px] lg:text-[32px] font-bold"
              style="font-family: 'Source Han Sans,Geneva,sans-serif'"
            >
              我们的故事
            </h2>
            <span style="font-family: Arial Black"
              ><span class="text-xs md:text-sm"
                >O<span style="color: #00ffc0">U</span>R STO<span
                  style="color: #00ffc0"
                  >R</span
                >Y</span
              ></span
            >
          </div>
          <div
            class="flex-1 editableContent lg:ml-8"
            data-aos="zoom-in"
            style="height: 100%; word-wrap: break-word"
          >
            <p style="text-align: justify">
              <span style="line-height: 1.5"
                ><span class="text-sm md:text-base"
                  >&nbsp; &nbsp; Founded in 2011&nbsp;(Hong
                  Kong,China).Headquartered in Hong Kong with branches in
                  Shanghai,The team consists of a highly spirited team of
                  entrepreneurs and foreign educated employees from a variety of
                  backgrounds ranging from global telecom leaders companies to
                  China incumbent carriers.</span
                ></span
              >
            </p>

            <p style="text-align: justify">
              <span style="line-height: 1.5"
                ><span class="text-sm md:text-base"
                  >&nbsp; &nbsp;
                  &nbsp;公司在中國香港成立於2011年。團隊總部位於香港，在上海設有分支機構，我們的團隊由一支充滿活力的企業家和受過國內外高等教育的員工組成，他們來自全球電信領導者公司和中國現有運營商等不同背景。</span
                ></span
              >
            </p>

            <p style="text-align: justify">&nbsp;</p>
          </div>
        </div>
        <div
          class="grid grid-cols-2 gap-2 w-full lg:flex sm:gap-3 lg:gap-4 lg:justify-between cards"
        >
          <div
            class="flex h-[200px] md:h-[250px] lg:h-[310px] pt-[40px] md:pt-[50px] lg:pt-[60px] hover:pt-[35px] md:hover:pt-[45px] lg:hover:pt-[55px] cursor-pointer group transition-all duration-300 bg-white flex-1 flex-col justify-center items-center"
            v-for="value in Story"
            :key="value.text"
            :data-aos="value.aos"
          >
            <div
              class="w-[60px] h-[60px] md:w-[75px] md:h-[75px] lg:w-[90px] lg:h-[90px]"
            >
              <img
                :src="value.icon"
                alt=""
                class="object-contain w-full h-full"
              />
            </div>
            <div class="text-center mt-[15px] md:mt-[18px] lg:mt-[20px] px-2">
              <p class="text-[16px] md:text-[18px] lg:text-[20px] font-bold">
                {{ value.text }}
              </p>
            </div>
            <div
              class="fade group-hover:h-[5px] transition-all duration-300 w-full mt-auto h-0 bg-[#06dfbc] z-10"
            ></div>
          </div>
        </div>
      </div>
    </section>

    <section class="bg-gray-50">
      <div class="flex flex-col w-full lg:flex-row">
        <div
          class="w-full lg:w-1/2 h-[300px] md:h-[400px] lg:h-[630px] bg-bot bg-cover bg-center"
        ></div>
        <div
          class="w-full lg:w-1/2 h-auto lg:h-[630px] bg-white px-4 sm:px-8 md:px-12 lg:px-20 py-8 lg:pt-[160px] order-1 lg:order-1"
        >
          <div
            class="editableContent"
            id="txtc_con_167_17"
            style="height: 100%; word-wrap: break-word"
          >
            <p>
              <strong
                ><span
                  class="tracking-[1.5px] text-[#333333] font-['Source_Han_Sans'] text-xl sm:text-2xl lg:text-[32px]"
                  >高速企業專綫</span
                ></strong
              >
            </p>

            <p>
              <span class="text-base tracking-[1.5px] font-['Arial_Black']"
                >High<span class="text-[#33ff00]">-</span>Speed EPL/PLC</span
              >
            </p>

            <p>&nbsp;</p>

            <p>
              <span class="leading-[1.5] text-[10.5pt] font-['宋体']"
                >褒博科技作為資深的數據網路運營者，擁有10多年的運營管理經驗，向用戶提供最先進，最安全，最可靠的高速、短時延專網解決方案，實現高速率，低延遲，超安全的專線傳輸。</span
              >
            </p>

            <p>&nbsp;</p>

            <p>
              <span class="leading-[1.2] text-xs"
                >As a senior data network operator with over 10 years of
                operational management experience, Baobo Technology provides
                users with the most advanced, secure, and reliable high-speed
                and short-term dedicated network solutions, achieving
                high-speed, low latency, and ultra secure dedicated line
                transmission.</span
              >
            </p>
          </div>
        </div>
      </div>
      <div class="flex flex-col w-full lg:flex-row">
        <div
          class="w-full lg:w-1/2 h-auto lg:h-[630px] md:bg-white px-4 sm:px-8 md:px-12 lg:px-20 py-8 lg:pt-[160px] order-1 lg:order-1"
        >
          <div id="txt_con_170_40" style="height: 100%">
            <div
              class="h-full break-words editableContent"
              id="txtc_con_170_40"
            >
              <p>
                <span
                  class="text-[#333333] font-['Source_Han_Sans'] text-lg md:text-xl lg:text-2xl xl:text-[32px]"
                  ><strong>專業IDC業務</strong></span
                >
              </p>

              <p class="mt-2">
                <span
                  class="tracking-[1.5px] text-xs md:text-sm font-['Arial_Black']"
                  ><span class="text-[#00ffc0]">I</span
                  ><span class="text-black">DC Business</span></span
                >
              </p>

              <p class="mt-4">&nbsp;</p>

              <p>
                <span class="leading-[1.5] text-sm md:text-base font-['宋体']"
                  >為客戶提供中國及亞太地區的IDC租賃和托管服務。以高速可靠的內外部網路環境和系統化的監控管理支持手段，為客戶集中式收集、存儲、處理和發送數據的設備提供專業託管空間、高端數據傳輸和高速接入服務。</span
                >
              </p>

              <p class="mt-4">&nbsp;</p>

              <p>
                <span
                  class="leading-[1.5] text-sm md:text-base font-['Calibri']"
                  >Provide IDC leasing and hosting services for customers in
                  China and the Asia Pacific region. With a high-speed and
                  reliable internal and external network environment and
                  systematic monitoring and management support, we provide
                  professional hosting space, high-end data transmission, and
                  high-speed access services for centralized data collection,
                  storage, processing, and transmission equipment for
                  customers.</span
                >
              </p>
            </div>
          </div>
        </div>
        <div
          class="w-full lg:w-1/2 h-[300px] md:h-[400px] lg:h-[630px] bg-hands bg-cover bg-center order-2 lg:order-2"
        ></div>
      </div>
    </section>

    <section
      class="my-8 md:my-12 lg:my-16 xl:my-20 bg-center h-[250px] md:h-[300px] lg:h-[354px] bg-cover bg-home_last"
    >
      <div
        class="container flex justify-center items-center px-4 mx-auto h-full sm:px-6 md:px-8 lg:px-12 xl:px-20"
      >
        <div
          class="text-center text-white"
          data-aos="fade-down"
          data-aos-delay="100"
        >
          <span
            style="font-family: Source Han Sans, Geneva, sans-serif"
            class="text-base sm:text-lg md:text-xl lg:text-2xl xl:text-[36px] font-semibold block mb-2"
            >期待與您的合作</span
          >
          <span
            style="font-family: Arial Black"
            class="text-xs sm:text-sm md:text-base"
            ><span style="color: #ffffff">SE</span
            ><span style="color: #00ffc0">R</span
            ><span style="color: #ffffff">VICE P</span
            ><span style="color: #00ffc0">R</span
            ><span style="color: #ffffff">OVIDER R</span
            ><span style="color: #00ffc0">E</span
            ><span style="color: #ffffff">CRUIT</span
            ><span style="color: #00ffc0">M</span
            ><span style="color: #ffffff">ENT</span></span
          >
        </div>
      </div>
    </section>
  </div>
</template>

<script lang="ts">
import siteConfig from '../config/site'
import Team from '@/assets/images/home/team.png'
import Support from '@/assets/images/home/support.png'
import Setting from '@/assets/images/home/setting.png'
import Index from '@/assets/images/home/index.png'

export default {
  name: 'Home',
  setup() {
    const Story = [
      {
        icon: Team,
        text: '優秀的技術團隊',
        aos: 'fade-left',
        aosDelay: 100,
      },
      {
        icon: Support,
        text: '專業的技術支持',
        aos: 'fade-down',
        aosDelay: 200,
      },
      {
        icon: Setting,
        text: '專業的技術服務',
        aos: 'fade-right',
        aosDelay: 300,
      },
      {
        icon: Index,
        text: '獨有的核心資源',
        aos: 'fade-down',
        aosDelay: 400,
      },
    ]
    return {
      featuredProjects: siteConfig.featuredProjects,
      latestArticles: siteConfig.latestArticles,
      socialLinks: siteConfig.socialLinks,
      siteConfig,
      Story,
    }
  },
}
</script>

<style scoped>
/* 暗色模式适配 */
:deep(.dark .card) {
  @apply bg-gray-800 hover:bg-gray-750 shadow-lg shadow-gray-900/10;
}

:deep(.dark .card h3) {
  @apply text-white;
}

:deep(.dark .card p) {
  @apply text-gray-300;
}

:deep(.dark .btn-outline) {
  @apply border-primary-400 text-primary-400 hover:bg-primary-500 hover:border-primary-500;
}

/* 总之就是非常可爱按钮样式 */
.kawaii-btn {
  @apply inline-flex items-center justify-center px-6 py-3 rounded-full font-medium transition-all duration-300;
  background: linear-gradient(to right, #ffb7c5, #d8aef2);
  color: #fff;
  border: 2px solid #fff;
  box-shadow: 0 4px 10px rgba(255, 183, 197, 0.5);
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.1);
  transform: translateY(0);
}

.kawaii-btn:hover {
  background: linear-gradient(to right, #ff9eb2, #c89ce0);
  transform: translateY(-2px);
  box-shadow: 0 6px 12px rgba(255, 183, 197, 0.6);
}

.kawaii-btn:active {
  transform: translateY(0);
  box-shadow: 0 2px 6px rgba(255, 183, 197, 0.4);
}
</style>
