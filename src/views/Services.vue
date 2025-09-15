<template>
  <div class="">
    <section class="h-[300px] md:h-[556px] bg-service bg-cover bg-center">
      <div class="container flex justify-center items-center px-4 h-full">
        <div class="z-10 break-words" data-aos="zoom-in" data-aos-delay="800">
          <div class="smAreaC z-16">
            <div class="h-[35px] w-[280px] md:w-[360px] z-20 mx-auto">
              <div class="overflow-hidden z-16">
                <div class="h-full z-16">
                  <div class="h-full break-words editableContent z-16">
                    <p class="w-full text-center z-16">
                      <span class="text-white z-16"
                        ><strong class="z-16"
                          ><span class="text-[24px] md:text-[34px] z-16"
                            ><span class="font-['Source_Han_Sans'] z-16"
                              >褒博服務</span
                            ></span
                          ></strong
                        ></span
                      >
                    </p>
                  </div>
                </div>
              </div>
            </div>
            <br />
            <div class="esmartMargin smartAbs h-[35px] w-full z-21">
              <div
                class="overflow-hidden yibuFrameContent con_12_32 text_Style1 z-16"
              >
                <div class="h-full z-16">
                  <div class="h-full break-words editableContent z-16">
                    <p class="text-center z-16">
                      <span class="tracking-[4px] z-16"
                        ><span class="text-[#33ffcc] z-16"
                          ><span class="font-['Arial_Black'] z-16"
                            ><span class="text-xs md:text-sm z-16"
                              >B</span
                            ></span
                          ></span
                        ><span class="text-white font-['Arial_Black'] z-16"
                          ><span class="text-xs md:text-sm z-16"
                            >AOBO
                          </span></span
                        ><span class="text-[#33ffcc] z-16"
                          ><span class="font-['Arial_Black'] z-16"
                            ><span class="text-xs md:text-sm z-16"
                              >S</span
                            ></span
                          ></span
                        ><span class="text-white font-['Arial_Black'] z-16"
                          ><span class="text-xs md:text-sm z-16"
                            >ERVICES</span
                          ></span
                        ></span
                      >
                    </p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="py-8 bg-gray-50 section md:py-16">
      <div class="container px-2 md:px-4">
        <div
          class="flex justify-center mx-auto mb-14 h-[79px] w-[280px] md:w-[360px] z-2"
        >
          <div class="overflow-hidden yibuFrameContent con_95_41 text_Style1">
            <div id="txt_con_95_41" class="h-full">
              <div
                class="h-full break-words editableContent"
                id="txtc_con_95_41"
              >
                <p class="text-center">
                  <span class="leading-[1.5]"
                    ><span class="text-[28px] md:text-[36px]"
                      ><span class="font-['Source_Han_Sans']"
                        ><strong
                          ><span class="text-black"
                            >我们提供的服务</span
                          ></strong
                        ></span
                      ></span
                    ></span
                  >
                </p>

                <p class="text-center">
                  <span class="text-base"
                    ><span class="font-['Trebuchet_MS']"
                      ><span class="text-gray-500"
                        ><span class="leading-[1.5]">OUR SERVICE</span></span
                      ></span
                    ></span
                  >
                </p>
              </div>
            </div>
          </div>
        </div>

        <div class="container px-2 md:px-4">
          <div class="flex flex-wrap gap-y-8 justify-evenly md:gap-y-14">
            <div
              class="flex w-full md:flex-row item md:w-auto"
              v-for="value in serviceItems"
            >
              <div
                class="icon w-[35px] h-[35px] md:w-[45px] md:h-[45px] bg-cover bg-center mb-2 md:mb-0 mx-auto md:mx-0"
                :class="value.class"
              ></div>
              <div
                style="
                  height: 81px;
                  width: 285px;
                  left: 55px;
                  top: 0px;
                  z-index: 3;
                "
              >
                <div
                  class="overflow-hidden yibuFrameContent con_82_41 text_Style1"
                >
                  <div id="txt_con_82_41" class="h-full">
                    <div
                      class="h-full break-words editableContent"
                      id="txtc_con_82_41"
                    >
                      <p>
                        <span class="font-['Microsoft_YaHei']"
                          ><span class="text-lg md:text-xl">{{
                            value.title
                          }}</span></span
                        >
                      </p>

                      <p>
                        <span class="text-xs md:text-sm"
                          ><span class="text-gray-500"
                            ><span class="leading-[1.75]">{{
                              value.description
                            }}</span></span
                          ></span
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
    </section>
    <section
      class="bg-service_bg2 h-auto md:h-[554px] bg-cover bg-center pb-8 md:pb-0 bg-scroll"
    >
      <div class="container mx-auto">
        <div class="py-12 mx-auto w-max md:py-20">
          <div class="smAreaC" cid="con_71_49">
            <div class="h-[42px] w-[320px] md:w-[431px] z-2 mx-auto">
              <div
                class="overflow-hidden yibuFrameContent con_72_49 text_Style1"
              >
                <div class="h-full">
                  <div class="h-full break-words editableContent">
                    <p class="text-center">
                      <span class="text-[28px] md:text-[40px]"
                        ><span class="font-['Arial']"
                          ><strong
                            ><span class="text-white"
                              >OUR ADVANTAGE</span
                            ></strong
                          ></span
                        ></span
                      >
                    </p>
                  </div>
                </div>
              </div>
            </div>
            <div class="h-[30px] w-[140px] z-9 mx-auto mt-4">
              <div
                class="overflow-hidden yibuFrameContent con_73_49 text_Style1"
              >
                <div class="h-full">
                  <div class="h-full break-words editableContent">
                    <p class="text-center">
                      <span class="text-lg md:text-2xl"
                        ><span class="text-white">我們的優勢</span></span
                      >
                    </p>
                  </div>
                </div>
              </div>
            </div>
            <div class="h-[20px] w-[85px] z-8 mx-auto mt-2">
              <div
                class="overflow-visible yibuFrameContent con_74_49 line_Style1"
              >
                <!-- w-line -->
                <div class="relative h-full">
                  <div class="w-line absolute top-1/2 w-[85px]"></div>
                </div>
              </div>
            </div>
            <div class="h-[20px] w-[83px] z-8 mx-auto mt-2">
              <div
                class="overflow-visible yibuFrameContent con_75_49 line_Style1"
              >
                <!-- w-line -->
                <div class="relative h-full">
                  <div
                    class="w-line absolute top-1/2 w-[83px]"
                    linetype="horizontal"
                  ></div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div
          class="flex flex-wrap gap-8 justify-evenly px-4 md:gap-0 service-wrap"
        >
          <div
            class="flex flex-col justify-center items-center w-full service-item sm:w-1/2 md:w-auto"
            :data-aos="value.aos"
            :data-aos-delay="value.aosDelay"
            v-for="value in advantage"
          >
            <div
              class="icon border-[1px] border-solid border-[#666] rounded-full w-[70px] h-[70px] md:w-[98px] md:h-[98px] flex justify-center items-center mb-4"
            >
              <img
                :src="value.class"
                alt=""
                class="w-[35px] h-[35px] md:w-[50px] md:h-[50px]"
              />
            </div>
            <div
              style="
                height: 49px;
                width: 160px;
                left: 30px;
                top: 168px;
                z-index: 6;
              "
            >
              <div
                class="overflow-hidden yibuFrameContent con_59_49 text_Style1"
              >
                <div id="txt_con_59_49" class="h-full">
                  <div
                    class="h-full break-words editableContent"
                    id="txtc_con_59_49"
                  >
                    <p class="text-center">
                      <span class="text-3xl md:text-5xl"
                        ><span class="text-white"
                          ><span class="font-['Arial_Black']">{{
                            value.title
                          }}</span></span
                        ></span
                      >
                    </p>
                  </div>
                </div>
              </div>
            </div>

            <div class="overflow-hidden yibuFrameContent con_60_49 text_Style1">
              <div id="txt_con_60_49" class="h-full">
                <div class="h-full break-words editableContent">
                  <p class="text-center">
                    <span class="text-sm md:text-base"
                      ><span class="text-white font-['Arial']">{{
                        value.desc
                      }}</span></span
                    >
                  </p>
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
import service1 from '@/assets/images/service/1.svg'
import service2 from '@/assets/images/service/2.svg'
import service3 from '@/assets/images/service/3.svg'
import service4 from '@/assets/images/service/4.svg'

export default {
  name: 'service',
  setup() {
    const serviceItems = [
      {
        class: 'bg-service1',
        title: '訂製服務',
        description:
          '工程、機電及網絡團隊隨時與運維團隊緊密配合，按客戶實際需求靈活定制服務',
      },
      {
        class: 'bg-service2',
        title: '多語種支持',
        description: '提供中文、英文、韓文、日文多語種在綫技術支持',
      },
      {
        class: 'bg-service3',
        title: '網管數據監控',
        description:
          '7*24在綫的網管服務，實時為用戶提供最即時的故障統計和技術支持',
      },
      {
        class: 'bg-service4',
        title: '運輸倉儲服务',
        description:
          '幫助客戶高效運輸和通關普通和高價值貨物，在多地區擁有可靠的倉儲空間供客戶周轉存儲。',
      },
      {
        class: 'bg-service5',
        title: 'IDC現場服務',
        description:
          '根據客戶的授權，提供Remote Hands、Smart Hands智能手服務。',
      },
      {
        class: 'bg-service6',
        title: '快速響應',
        description: '專業團隊24小時待命，5分鐘響應，2小時内抵達城市任意IDC',
      },
    ]

    const advantage = [
      {
        class: service1,
        title: '12+',
        aos: 'fade-left',
        aosDelay: 600,
        desc: '年行業經驗',
      },
      {
        class: service2,
        title: '100%',
        aos: 'fade-left',
        aosDelay: 300,
        desc: '客戶滿意度',
      },
      {
        class: service3,
        title: '100+',
        aos: 'fade-right',
        aosDelay: 300,
        desc: '建立合作關係',
      },
      {
        class: service4,
        title: '25+',
        aos: 'fade-right',
        aosDelay: 600,
        desc: '城市駐點服務團隊',
      },
    ]
    return { serviceItems, advantage }
  },
}
</script>

<style></style>
