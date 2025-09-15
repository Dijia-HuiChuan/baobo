<template>
  <div>
    <section class="h-[300px] md:h-[500px] bg-product bg-cover bg-center">
      <div class="container flex justify-center items-center px-4 h-full">
        <div class="z-10 break-words" data-aos="zoom-in" data-aos-delay="800">
          <p class="z-10 text-center">
            <span
              class="text-white font-['Source_Han_Sans',Geneva,sans-serif] z-10"
            >
              <span class="text-[24px] md:text-[34px] z-10">產 品 介 紹</span>
            </span>
          </p>

          <p class="z-10 mt-2 text-center">
            <span class="font-['Arial_Black'] z-10">
              <span class="z-10 text-white">
                <span class="z-10 text-xs md:text-sm"
                  >Product Introduction</span
                >
              </span>
            </span>
          </p>
        </div>
      </div>
    </section>

    <section class="bg-[#f3f4f5] section py-8 md:py-16">
      <div class="container px-2 md:px-4 mx-auto md:h-[550px] h-max">
        <swiper
          :spaceBetween="30"
          :effect="'fade'"
          :autoplay="{
            delay: 3000,
            disableOnInteraction: false,
          }"
          :pagination="{
            clickable: true,
          }"
          :modules="modules"
          class="mySwiper"
        >
          <swiper-slide class="">
            <div class="pl-4 h-full bg-white md:pl-10 wrap">
              <div
                class="flex pb-10 h-full max-md:flex-col md:justify-between content"
              >
                <div class="p-4 md:p-[50px]">
                  <div class="overflow-hidden z-10">
                    <div class="z-10 h-full">
                      <div class="z-10 h-full break-words">
                        <h2 class="z-10 mb-2 md:mb-4">
                          <span class="font-['Source_Han_Sans'] z-10"
                            ><span class="text-[18px] md:text-[24px] z-10"
                              ><strong class="z-10">企業網絡服務</strong>
                            </span>
                          </span>
                        </h2>

                        <p style="z-index: 1">
                          <span style="font-size: 14px; z-index: 1"
                            ><strong style="z-index: 1"
                              >Enterprise Network Services</strong
                            >
                          </span>
                        </p>

                        <p class="z-10 mb-3 md:mb-4">
                          <span
                            class="leading-[1.4] md:leading-[1.2] z-10 block"
                            ><strong class="z-10"
                              ><span class="text-[12px] md:text-[10.5pt] z-10"
                                ><span class="font-['宋体'] z-10"
                                  >我們的光纖主幹網和網路解決方案旨在提高亞太地區乃至全球關鍵市場的延遲/恢復能力。我們提供非常個性化的一站式解決方案，以滿足您的所有網路和基礎設施需求。</span
                                >
                              </span>
                            </strong>
                          </span>
                        </p>

                        <p class="z-10">&nbsp;</p>

                        <p class="z-10">
                          <span class="leading-[1.2] z-10 block"
                            ><strong class="z-10"
                              ><span class="text-[10.5pt] z-10"
                                ><span class="font-['宋体'] z-10 block"
                                  >Our fiber optic backbone and network
                                  solutions aim to improve latency/recovery
                                  capabilities in key markets in the Asia
                                  Pacific region and even globally. We provide
                                  highly personalized one-stop solutions to meet
                                  all your network and infrastructure
                                  needs.</span
                                >
                              </span>
                            </strong>
                          </span>
                        </p>

                        <br />
                        <p class="z-10 text-left">
                          <span class="leading-[1.2] z-10 block"
                            ><span class="text-[10.5pt] z-10"
                              ><span class="font-['Calibri'] z-10"
                                >1<span class="z-10 text-sm">. WDM</span>
                              </span>
                            </span>
                          </span>
                        </p>

                        <p class="z-10 text-left">
                          <span class="leading-[1.2] z-10 block"
                            ><span class="text-[10.5pt] z-10"
                              ><span class="font-['Calibri'] z-10"
                                >基於光纖骨幹網的WDM服務。這項服務使您能夠擴大您的核心網路覆蓋範圍。波長可以提供1Gbps、10Gbps和100Gbps選項。</span
                              >
                            </span>
                          </span>
                        </p>

                        <p class="z-10 text-left">
                          <span class="leading-[1.2] z-10 block"
                            ><span class="z-10 text-sm"
                              ><span class="font-['Calibri'] z-10">2. EPL</span>
                            </span>
                          </span>
                        </p>
                        <br />
                        <p class="z-10 text-left">
                          <span class="leading-[1.2] z-10 block"
                            ><span class="text-[10.5pt] z-10"
                              ><span class="font-['Calibri'] z-10"
                                >一種專用、可管理的點對點以太網第2層MPLS網路服務，速度高達10Gbps。支持各種MTU、VLAN標記參數。可提供全球多個國家/地區的跨境和本地環路。</span
                              >
                            </span>
                          </span>
                        </p>

                        <p class="z-10 text-left">&nbsp;</p>

                        <p class="z-10 text-left">
                          <span class="leading-[1.2] z-10 block"
                            ><span class="z-10 text-sm"
                              ><span class="font-['Calibri'] z-10"
                                >3. WAVELIGHT & DARK FIBER</span
                              >
                            </span>
                          </span>
                        </p>

                        <p class="z-10 text-left">
                          <span class="leading-[1.2] z-10 block"
                            ><span class="text-[10.5pt] z-10"
                              ><span class="font-['Calibri'] z-10"
                                >客戶端可以根據所需容量在提供的WDM網路上使用自己的複用設備，同時也可選擇租用提供的復用設備。我們在城域網中提供裸光纖服務。</span
                              >
                            </span>
                          </span>
                        </p>
                      </div>
                    </div>
                  </div>
                </div>
                <div
                  class="w-full md:w-[330px] flex-shrink-0 h-[200px] md:h-full bg-product1 bg-cover bg-center"
                ></div>
                <!-- <img src="@/assets/images/product/1.png" alt="" class="w-[330px] h-full" /> -->
              </div>
            </div>
          </swiper-slide>
          <swiper-slide class=""
            ><div class="pl-4 h-full bg-white md:pl-10 wrap">
              <div
                class="flex pb-10 h-full max-md:flex-col md:justify-between content"
              >
                <div class="p-4 md:p-[50px]">
                  <div class="overflow-hidden z-10">
                    <div class="z-10 h-full">
                      <div class="z-10 h-full break-words">
                        <h2 class="z-10 mb-2 md:mb-4">
                          <span class="font-['Source_Han_Sans'] z-10"
                            ><span class="text-[18px] md:text-[24px] z-10"
                              ><strong class="z-10"
                                >高速低延時商業網絡</strong
                              ></span
                            ></span
                          >
                        </h2>

                        <p style="z-index: 6">
                          <span style="font-size: 14px; z-index: 6"
                            ><strong style="z-index: 6"
                              >High speed low latency commercial network</strong
                            ></span
                          >
                        </p>

                        <p class="z-10">
                          <span
                            class="leading-[1.6] md:leading-[1.5] z-10 block"
                            ><span class="text-[12px] md:text-sm z-10"
                              ><span class="font-['Calibri'] z-10"
                                ><span class="font-['宋体'] z-10"
                                  >我們擁有並運營自己的網路，我們能夠為您提供無與倫比的速度、可靠性、性能和服務的定制解決方案。我們的容量選項從1
                                  Mbps到高達10
                                  Gbps的高帶寬服務。我們使用最新的網路技術來幫助我們的客戶滿足他們的所有要求。</span
                                ></span
                              ></span
                            ></span
                          >
                        </p>

                        <p class="z-10">
                          <span
                            class="leading-[1.6] md:leading-[1.5] z-10 block"
                            ><span class="text-[12px] md:text-sm z-10"
                              ><span class="font-['宋体'] z-10"
                                >我們擁有更多的機會幫助客戶開拓亞太市場。基於褒博開發團隊的不斷進取，我們擁有了连接东京、新加坡、香港、臺北、上海、深圳等城市各處金融交易所的頂級綫路資源。</span
                              ></span
                            ></span
                          >
                        </p>

                        <p class="z-10 md:mb-4">
                          <span
                            class="leading-[1.6] md:leading-[1.5] z-10 block"
                            ><span class="text-[12px] md:text-sm z-10"
                              ><span class="font-['Calibri'] z-10"
                                >帶寬端到端硬隔離，專線專用，高可用，可用率不低於99.99%，毫秒級可保證低時延。</span
                              ></span
                            ></span
                          >
                        </p>

                        <p class="z-10">
                          <span class="leading-[1.5] z-10 block"
                            ><span class="z-10 text-sm"
                              ><span class="font-['宋体'] z-10"
                                ><span class="font-['宋体'] z-10 block"
                                  >&nbsp; We own and operate our own network,
                                  and we can provide you with unparalleled
                                  customized solutions for speed, reliability,
                                  performance, and service. Our capacity options
                                  range from 1 Mbps to high bandwidth services
                                  up to 10 Gbps. We use the latest network
                                  technology to help our customers meet all
                                  their requirements.<br class="z-10" />
                                  &nbsp; We have more opportunities to help our
                                  clients expand into the Asia Pacific market.
                                  Based on the continuous progress of the
                                  BAOBO's&nbsp;development team, we have
                                  top-level route resources connecting various
                                  financial exchanges in cities such as Tokyo,
                                  Singapore, Hong Kong, Taipei, Shanghai, and
                                  Shenzhen.<br class="z-10" />
                                  Broadband end-to-end hard isolation, dedicated
                                  line, high availability, with an availability
                                  rate of no less than 99.99%, and millisecond
                                  level to ensure low latency.</span
                                ></span
                              ></span
                            ></span
                          >
                        </p>
                      </div>
                    </div>
                  </div>
                </div>
                <div
                  class="w-full md:w-[330px] flex-shrink-0 h-[200px] md:h-full bg-product2 bg-cover bg-center"
                ></div>
              </div>
            </div>
          </swiper-slide>
        </swiper>
      </div>
    </section>
  </div>
</template>

<script setup>
import { ref, onMounted, computed } from 'vue'

import { Swiper, SwiperSlide } from 'swiper/vue'

import { EffectFade, Navigation, Pagination, Autoplay } from 'swiper/modules'
const modules = [EffectFade, Navigation, Pagination, Autoplay]
import 'swiper/css'
import 'swiper/css/effect-fade'
import 'swiper/css/navigation'
import 'swiper/css/pagination'
import 'swiper/css/autoplay'
</script>
<style scoped>
.mySwiper {
  @apply mx-auto;
  width: 100%;
  height: 100%;
}
.swiper {
  width: 100%;
  height: 100%;
}
@media (max-width: 768px) {
  .mySwiper {
    width: 100%;
    height: auto;
    min-height: 400px;
  }
}
</style>
