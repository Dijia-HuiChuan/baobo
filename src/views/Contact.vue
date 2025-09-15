<template>
  <div class="">
    <section class="h-[300px] md:h-[556px] bg-contact bg-cover bg-center">
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
                              >联系我们</span
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
            <div class="overflow-hidden z-[7]">
              <div class="h-full z-[7]">
                <div class="h-full break-words z-[7]">
                  <p class="text-center z-[7]">
                    <span class="tracking-[15px] text-sm font-['Arial_Black'] z-[7]">
                      <span class="text-white">CO</span>
                      <span class="text-[#00FFC0]">N</span>
                      <span class="text-white">TACT </span>
                      <span class="text-[#00FFC0]">U</span>
                      <span class="text-white">S</span>
                    </span>
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="pt-8 pb-24 section">
      <div class="container mx-auto">
        <div class="text-center" data-aos="fade-left">
          <h2 class="text-3xl font-bold font-['Source_Han_Sans'] text-gray-800">
            联系我们，开启合作之旅
          </h2>
          <div
            class="w-[270px] h-[17px] bg-[#00FFC0] mx-auto mt-[-7px]"
            data-aos="fade-right"
          ></div>
        </div>
        <div class="max-w-3xl mx-auto mt-10" data-aos="fade-up">
          <p class="text-center text-gray-600 text-lg leading-relaxed mb-6">
            我们致力于为企业提供专业的技术解决方案和优质服务
          </p>
          <p class="text-center text-gray-600 text-base leading-relaxed mb-4">
            无论您需要咨询服务、技术支持还是商务合作
          </p>
          <p class="text-center text-gray-600 text-base leading-relaxed">
            我们的专业团队都将竭诚为您提供最优质的服务体验
          </p>
        </div>
        <div class="flex justify-evenly mt-6 contact-wrap">
          <a href="tel:090-7518-1818">
            <div
              class="flex flex-col gap-2 items-center cursor-pointer contact-item"
              data-aos="fade-up"
            >
              <div class="">
                <img
                  src="@/assets/images/contact/phone.svg"
                  alt=""
                  class="w-10 h-10"
                />
              </div>
              <div class="text-center max-md:text-[12px]">
                <span>090-7518-1818</span>
              </div>
            </div>
          </a>
          <a href="mailto:tokyo@baobo.co.jp">
            <div
              class="flex flex-col gap-2 items-center cursor-pointer contact-item"
              data-aos="fade-up"
            >
              <div class="">
                <img
                  src="@/assets/images/contact/email.svg"
                  alt=""
                  class="w-10 h-10"
                />
              </div>
              <div class="text-center max-md:text-[12px]">
                <span>tokyo@baobo.co.jp</span>
              </div>
            </div>
          </a>
          <div
            class="flex flex-col gap-2 items-center cursor-pointer contact-item"
            data-aos="fade-up"
          >
            <div class="">
              <img
                src="@/assets/images/contact/location.svg"
                alt=""
                class="w-10 h-10"
              />
            </div>
            <div class="text-center max-md:text-[12px]">
              <span>東京都江東区東雲1-9-31</span>
            </div>
          </div>
        </div>
      </div>
    </section>
    
    <!-- Google Map Section -->
    <section class="py-16 bg-gray-50">
      <div class="container px-4 mx-auto">
        <div class="text-center mb-12" data-aos="fade-up">
          <h3 class="text-2xl font-bold text-gray-800 mb-4">我们的位置</h3>
          <p class="text-gray-600">欢迎您到访我们的办公室，我们期待与您面对面交流</p>
        </div>
        <div class="w-full h-[400px] md:h-[500px] rounded-lg overflow-hidden shadow-lg" data-aos="zoom-in">
           <iframe
              src="https://maps.google.com/maps?width=100%&height=400&hl=ja&q=東京都江東区東雲1-9-31&ie=UTF8&t=&z=16&iwloc=B&output=embed"
              width="100%"
              height="100%"
              class="border-0"
              allowfullscreen=""
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade"
              title="Company Location Map"
            ></iframe>
         </div>
        <div class="mt-6 text-center">
          <a
            href="https://maps.google.com/?q=東京都江東区東雲1-9-31"
            target="_blank"
            rel="noopener noreferrer"
            class="inline-flex items-center px-6 py-3 text-white bg-blue-600 rounded-lg transition-colors duration-300 hover:bg-blue-700"
          >
            <svg class="mr-2 w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"></path>
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"></path>
            </svg>
            在Google地图中查看
          </a>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'Contact',
  data() {
    return {}
  },
}
</script>

<style scoped></style>
