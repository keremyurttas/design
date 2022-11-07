<template>
  <div
    class="container max-w-[1440px] lg:p-2 mx-auto font-mont"
    :class="{ 'overflow-hidden h-screen': isHeaderActive }"
  >
    <button
      @click="isHeaderActive = true"
      v-if="!isHeaderActive"
      class="lg:hidden w-10 h-10 absolute top-10 right-10"
    >
      <img src="../assets/options-lines-svgrepo-com.svg" alt="" />
    </button>
    <img
      src="../assets/background.png"
      class="absolute hidden lg:block"
      alt=""
    />
    <div
      class="lg:w-[1322px] hidden lg:flex w-screen pt-10 lg:p-4 z-20 justify-between items-center h-[6%] mx-[4.5%] px-[9%] pb-8 mb-[10%] lg:relative"
    >
      <a>
        <button><h3 class="text-2xl">Brandname</h3></button>
      </a>
      <div
        class="lg:flex items-center gap-[21px] lg:w-[20%] text-base lg:mr-64"
      >
        <a class="block lg:inline mb-20 lg:mb-0"> Home </a>
        <a class="block lg:inline mb-20 lg:mb-0"> Product </a>
        <a class="block lg:inline mb-20 lg:mb-0"> Pricing </a>
        <a class="block lg:inline mb-20 lg:mb-0"> Contact </a>
      </div>
      <div class="flex justify-between gap-[45px] items-center lg:mr-12">
        <a class="text-primary">Login</a>
        <button class="primary-button flex justify-evenly items-center">
          <a>JOIN US</a>
          <img src="../assets/icn-arrow-right.png" alt="" />
        </button>
      </div>
    </div>
    <div
      v-if="isHeaderActive"
      class="lg:w-[1322px] bg-gray-600 flex lg:hidden fixed flex-col justify-evenly w-screen pt-10 lg:p-4 z-20 items-center h-full pb-8 mb-[10%] lg:relative"
    >
      <button
        @click="isHeaderActive = !isHeaderActive"
        class="absolute top-8 right-8 font-bold text-xl"
      >
        x
      </button>
      <a>
        <button><h3 class="text-2xl mb-10">Brandname</h3></button>
      </a>
      <div
        class="lg:flex items-center gap-[21px] lg:w-[20%] text-base lg:mr-64"
      >
        <a class="block lg:inline mb-10"> Home </a>
        <a class="block lg:inline mb-10"> Product </a>
        <a class="block lg:inline mb-10"> Pricing </a>
        <a class="block lg:inline mb-10"> Contact </a>
      </div>
      <div class="flex justify-between gap-[45px] items-center lg:mr-12">
        <a class="text-primary">Login</a>
        <button
          class="bg-primary flex justify-evenly items-center py-4 px-5 text-sm gap-4 tracking-wide text-white rounded-md"
        >
          <a>JOIN US</a>
          <img src="../assets/icn-arrow-right.png" alt="" />
        </button>
      </div>
    </div>
    <div
      class="container w-[73%] h-[973px] mx-auto py-20 mb-[800px] relative lg:mb-0"
    >
      <div class="w-full font-bold mb-20 z-10 relative">
        <div class="text-base tracking-widest text-primary mb-[3%]">
          For better Future
        </div>
        <h1 class="text-6xl w-[80%] mb-[3%] leading-[80px]">
          HIGH QUALITY <br />
          COURSES
        </h1>
        <h5
          class="text-xl leading-[30px] tracking-[0.2px] font-normal text-[#737373] mb-[3%]"
        >
          Every day brings with it a fresh <br />
          set of learning possibilities.
        </h5>
        <div>
          <button class="primary-button px-10 py-4 mr-2.5 mb-2 sm:mb-0">
            Get Quote Now
          </button>
          <button
            class="px-10 py-4 text-primary border-primary border bg-white rounded-[5px] text-sm tracking-[0.2px] font-bold"
          >
            Learn More
          </button>
        </div>
      </div>
      <div class="w-full lg:flex block">
        <div
          v-for="card in firstCards"
          class="py-[35px] px-[40px] lg:px-[40px] shadow-lg mb-10 z-10 relative lg:mr-8 bg-white"
        >
          <img
            class="w-[70px] h-[76px] mb-5"
            :src="require(`../assets/${card.img}`)"
            alt=""
          />

          <h3 class="text-xl lg:text-2xl mb-5 font-bold w-[259px]">
            {{ card.header }}
          </h3>
          <div class="w-[50px] bg-primary h-0.5 mb-5"></div>
          <span class="text-sm tracking-[0.2px] text-[#737373] font-normal">
            The gradual accumulation of <br />
            information about atomic and <br />
            small-scale behaviour...</span
          >
        </div>
      </div>
    </div>
    <div class="container w-[73%] mx-auto py-10 lg:py-40">
      <div class="w-full lg:flex items-center">
        <img
          class="w-1/2 mx-auto mr-40 hidden lg:block"
          src="../assets/col-md-6.png"
          alt=""
        />
        <div class="">
          <div class="bg-primary w-[94px] h-[7px] mb-9"></div>
          <h3 class="lg:text-6xl text-4xl w-max font-bold mb-[35px]">
            Get Quality <br />
            Education
          </h3>
          <div class="text-sm tracking-[0.2px] text-[#737373] font-normal mb-9">
            Problems trying to resolve the conflict between <br />
            the two major realms of Classical physics: <br />
            Newtonian mechanics
          </div>
          <button class="flex items-center">
            <span class="text-sm font-bold text-primary mr-2.5"
              >Learn More</span
            >
            <img class="w-[9] h-4" src="../assets/iconarrow-next.png" alt="" />
          </button>
        </div>
      </div>
    </div>
    <div
      class="container lg:w-[73%] lg:py-20 pb-20 mx-auto flex flex-wrap justify-between items-center"
    >
      <img class="w-[153px] h-[34px]" src="../assets/col-md-2sec-.png" alt="" />
      <img
        class="w-[146px] h-[59px]"
        src="../assets/col-md-2sec-(1).png"
        alt=""
      />
      <img
        class="w-[152px] h-[75px]"
        src="../assets/col-md-2sec-(2).png"
        alt=""
      />
      <img
        class="w-[151px] h-[42px]"
        src="../assets/col-md-2sec-(3).png"
        alt=""
      />
      <img
        class="w-[151px] h-[62px]"
        src="../assets/col-md-2sec-(4).png"
        alt=""
      />
      <img
        class="w-[151px] h-[72px]"
        src="../assets/col-md-2sec-(5).png"
        alt=""
      />
    </div>
    <div class="w-full pb-20 bg-[#26335D]">
      <div class="container w-[73%] mx-auto py-40">
        <div class="w-full mb-20">
          <span class="text-sm font-bold text-primary mb-2.5"
            >Practice Advice</span
          >
          <h2 class="text-[40px] text-white mb-2.5">Our Popular Courses</h2>
          <span class="text-sm text-white mb-2.5">
            Problems trying to resolve the conflict between <br />
            the two major realms of Classical physics: Newtonian mechanics
          </span>
        </div>
        <!-- HEREE -->
        <div class="w-full flex-col lg:flex-row items-center flex">
          <div v-for="card in secondCards" :class="{'mr-3':!card.last}" class=" mb-10 lg:mb-0">
            <div class="relative max-w-[250px] lg:max-w-[340px] h-[300px]">
              <div
                class="text-sm px-2.5 font-bold bg-primary text-white inline absolute top-4 left-3"
              >
                Sale
              </div>
              <img
                class="w-full h-full"
                :src="require(`../assets/${card.img}`)"
                alt=""
              />
              <div
                class="flex absolute w-40 bottom-0 left-1/2 translate-x-[-50%] translate-y-[-50%]"
              >
                <img
                  class="p-2.5 rounded-[45px] bg-white mr-2.5"
                  src="../assets/icnfavorite.png"
                  alt=""
                />
                <img
                  class="p-2.5 rounded-[45px] bg-white mr-2.5"
                  src="../assets/icnfavorite1.png"
                  alt=""
                />
                <img
                  class="p-2.5 rounded-[45px] bg-white"
                  src="../assets/icnfavorite2.png"
                  alt=""
                />
              </div>
            </div>
            <div class="bg-white pt-6 pb-9 px-6 max-w-[250px] lg:max-w-[340px]">
              <div class="flex items-center justify-between mb-2.5">
                <span class="text-sm font-bold text-primary">{{
                  card.smHeader
                }}</span>
                <div
                  class="flex bg-[#26335D] rounded-[20px] items-center p-1.5"
                >
                  <img
                    class="w-[15px] h-[15px]"
                    src="../assets/iconemojione-star.png"
                    alt=""
                  />
                  <span class="text-[12px] text-white">4.9</span>
                </div>
              </div>
              <h3 class="text-base font-bold text-[#26335D] mb-2.5">
                {{ card.header }}
              </h3>
              <div
                class="text-sm leading-5 tracking-wide text-[#737373] font-normal mb-2.5"
              >
                We focus on ergonomics and meeting <br />
                you where you work. It's only a <br />
                keystroke away.
              </div>
              <div class="flex items-center mb-2.5">
                <img
                  class="mr-2.5 w-[15px] h-[16px]"
                  src="../assets/Framesec-.png"
                  alt=""
                />
                <span class="font-bold text-sm text-[#737373]">15 Sales</span>
              </div>
              <div class="flex mb-2.5">
                <span
                  class="font-bold text-base tracking-[0.1px] text-[#BDBDBD] mr-1"
                  >$16.48</span
                >
                <span
                  class="font-bold text-base tracking-[0.1px] text-[#26335d]"
                  >$6.48</span
                >
              </div>
              <button
                class="border-primary flex items-center border rounded-[37px] px-5 py-2.5"
              >
                <span class="font-bold text-sm text-primary mr-2.5"
                  >Learn More</span
                >
                <img
                  class="w-[9px] h-4"
                  src="../assets/icnarrow-right.icn-xs.png"
                  alt=""
                />
              </button>
            </div>
          </div>


        </div>
      </div>
    </div>
    <div class="container w-[73%] mx-auto py-40">
      <div class="text-sm font-bold text-primary mb-2.5">Practice Advice</div>
      <h3 class="text-base font-bold text-[#26335D] mb-2.5">
        Watch our Courses
      </h3>
      <span
        class="text-sm leading-5 tracking-wide text-[#737373] font-normal mb-20 block"
      >
        Problems trying to resolve the conflict between <br />
        the two major realms of Classical physics: Newtonian mechanics
      </span>
      CAREFUL THERE
      <div class="w-full lg:flex">
        <!-- Price cards -->

        <div
          v-for="card in freeCards"
          :class="{ 'mr-8': !card.last }"
          class="py-12 px-10 shadow-md mb-6 lg:mb-0 relative"
        >
          <div v-if="card.new">
            <div
              class="bg-[#E77C40] hidden absolute top-[-10px] lg:top-[-29px] right-[-34.5px] w-24 h-24 rounded-full lg:flex items-center justify-center text-white font-bold text-2xl"
            >
              New
            </div>
          </div>
          <img
            class="p-6 rounded-full bg-primary mb-9"
            src="../assets/iconcool-icon-25.png"
            alt=""
          />
          <h3 class="text-2xl font-bold mb-9">FREE</h3>
          <h6 class="mb-9">
            Organize across all apps by <br />
            hand
          </h6>
          <div class="mb-9">
            <h2 class="font-bold text-4xl tracking-[0.2px] text-primary">
              19$
            </h2>
            <h6 class="font-bold tracking-[0.2px] text-[#8EC2F2]">Per Month</h6>
          </div>
          <p class="text-sm font-normal text-[#737373] mb-9">
            Slate helps you see how <br />
            many more days you need...
          </p>

          <button class="primary-button py-4 mb-9 px-10 lg:px-20 ">
            Try for free
          </button>
          <ul>
            <li
              class="font-bold text-sm flex items-center tracking-[0.2px] mb-4"
            >
              <img
                class="py-2.5 px-2 bg-[#2DC071] rounded-full mr-2.5"
                src="../assets/check.icn-xs.png"
                alt=""
              />
              <h6>Unlimited product updates</h6>
            </li>
            <li
              class="font-bold text-sm flex items-center tracking-[0.2px] mb-4"
            >
              <img
                class="py-2.5 px-2 bg-[#2DC071] rounded-full mr-2.5"
                src="../assets/check.icn-xs.png"
                alt=""
              />
              <h6>Unlimited product updates</h6>
            </li>
            <li
              class="font-bold text-sm flex items-center tracking-[0.2px] mb-4"
            >
              <img
                class="py-2.5 px-2 bg-[#2DC071] rounded-full mr-2.5"
                src="../assets/check.icn-xs.png"
                alt=""
              />
              <h6>Unlimited product updates</h6>
            </li>
            <li
              class="font-bold text-sm flex items-center tracking-[0.2px] mb-4"
            >
              <img
                class="py-2.5 px-2 bg-[#BDBDBD] rounded-full mr-2.5"
                src="../assets/check.icn-xs.png"
                alt=""
              />
              <h6>1GB Cloud Storage</h6>
            </li>
            <li class="font-bold text-sm flex items-center tracking-[0.2px]">
              <img
                class="py-2.5 px-2 bg-[#BDBDBD] rounded-full mr-2.5"
                src="../assets/check.icn-xs.png"
                alt=""
              />
              <h6>
                Email and community <br />
                support
              </h6>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div class="container w-[73%] mx-auto py-40">
      <div class="text-sm font-bold text-primary mb-2.5">Practice Advice</div>
      <h3 class="text-4xl font-bold text-[#26335D] mb-2.5">
        Approdable Packages
      </h3>
      <span
        class="text-sm leading-5 tracking-wide text-[#737373] font-normal mb-20 block"
      >
        Problems trying to resolve the conflict between <br />
        the two major realms of Classical physics: Newtonian mechanics
      </span>
      <div class="w-full lg:flex">
        <!-- comment Boxs -->
        <div
          v-for="comment in comments"
          class="lg:px-16 lg:py-6 flex flex-col items-center lg:mr-8"
        >
          <div class="p-8">
            <div class="flex items-center mb-4">
              <img class="mr-1.5" src="../assets/Vector.png" alt="" />
              <img class="mr-1.5" src="../assets/Vector.png" alt="" />
              <img class="mr-1.5" src="../assets/Vector.png" alt="" />
              <img class="mr-1.5" src="../assets/Vector.png" alt="" />
              <img src="../assets/icnbx-star.png" alt="" />
            </div>
            <p class="text-center text-sm text-[#737373]">
              Slate helps you see <br />
              how many more days <br />
              you need to work to<br />
              reach your financial <br />
              goal for the month <br />
              and year.
            </p>
          </div>
          <div class="flex items-center">
            <img
              class="mr-4"
              :src="require(`../assets/${comment.img}`)"
              alt=""
            />
            <div class="py-1">
              <h6 class="text-primary text-sm font-bold leading-[24px]">
                Regina Miles
              </h6>
              <span class="text-[12px] font-normal">Designer</span>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="container w-[73%] mx-auto py-40">
      <div class="text-sm font-bold text-primary mb-2.5 text-center">
        Newsletter
      </div>
      <h3 class="text-base font-bold text-[#26335D] mb-2.5 text-center">
        Most Popular Courses
      </h3>
      <span
        class="text-sm leading-5 tracking-wide text-[#737373] font-normal mb-20 block text-center"
      >
        Problems trying to resolve the conflict between <br />
        the two major realms of Classical physics: Newtonian mechanics
      </span>
      <!---------Careful the button-------------->
      <div class="flex justify-center">
        <input
          class="px-4 py-4 w-[54%] bg-[#E6E6E6] placeholder:text-sm font-normal"
          type="text"
          placeholder="Your email"
        />
        <button class="primary-button rounded-none">
          <span class="font-light"> Subscribe </span>
        </button>
      </div>
    </div>
    <!-- footer -->
    <div class="container w-[73%] mx-auto py-[50px] lg:flex justify-between">
      <div class="mr-8">
        <h5 class="mb-5 font-bold text-base">Company Info</h5>
        <a class="mb-2.5 block font-bold text-sm text-[#737373]"> About Us</a>
        <a class="mb-2.5 block font-bold text-sm text-[#737373]"> Carrier</a>
        <a class="mb-2.5 block font-bold text-sm text-[#737373]">
          We are hiring</a
        >
        <a class="mb-2.5 block font-bold text-sm text-[#737373]"> Blog</a>
      </div>
      <div class="mr-8">
        <h5 class="mb-5 font-bold text-base mr-8">Legal</h5>
        <a class="mb-2.5 block font-bold text-sm text-[#737373]"> About Us</a>
        <a class="mb-2.5 block font-bold text-sm text-[#737373]"> Carrier</a>
        <a class="mb-2.5 block font-bold text-sm text-[#737373]">
          We are hiring</a
        >
        <a class="mb-2.5 block font-bold text-sm text-[#737373]"> Blog</a>
      </div>
      <div class="mr-8">
        <h5 class="mb-5 font-bold text-base">Features</h5>
        <a
          class="mb-2.5 block font-bold text-sm tracking-[0.2px] text-[#737373]"
        >
          Business Marketing</a
        >
        <a class="mb-2.5 block font-bold text-sm text-[#737373]">
          User Analytic</a
        >
        <a class="mb-2.5 block font-bold text-sm text-[#737373]"> Live Chat</a>
        <a class="mb-2.5 block font-bold text-sm text-[#737373]">
          Unlimited Support</a
        >
      </div>
      <div class="mr-8">
        <h5 class="mb-5 font-bold text-base">Resources</h5>
        <a class="mb-2.5 block font-bold text-sm text-[#737373]">
          IOS & Android</a
        >
        <a class="mb-2.5 block font-bold text-sm text-[#737373]">
          Watch a Demo</a
        >
        <a class="mb-2.5 block font-bold text-sm text-[#737373]"> Customers</a>
        <a class="mb-2.5 block font-bold text-sm text-[#737373]"> API</a>
      </div>
      <div>
        <h5 class="mb-5 font-bold text-base">Get In Touch</h5>
        <a class="mb-2.5 block font-bold text-sm text-[#737373]">
          <img class="inline mr-2.5" src="../assets/bx_bx-phone.png" alt="" />
          <span>(480) 555-0103</span>
        </a>
        <a
          class="mb-2.5 block font-bold text-sm text-[#737373] flex items-center"
        >
          <img class="mr-2.5" src="../assets/bx_bx-map.png" alt="" />
          <span
            >4517 Washington Ave. Manchester, <br />
            Kentucky 39495</span
          ></a
        >
        <a class="mb-2.5 block font-bold text-sm text-[#737373]">
          <img
            class="inline mr-2.5"
            src="../assets/carbon_send-alt.png"
            alt=""
          />
          <span>debra.holt@example.com</span></a
        >
      </div>
    </div>
    <div class="lg:w-[1440px] bg-[#FAFAFA] lg:px-[195px] px-4">
      <div class="container items-center flex py-6 justify-between">
        <h6 class="font-bold text-sm text-[#737373]">
          Made With Love By Figmaland All Right Reserved
        </h6>
        <div class="px-16 ml-15 flex">
          <img class="mr-4" src="../assets/facebook.png" alt="" />
          <img class="mr-4" src="../assets/instagram.png" alt="" />
          <img class="" src="../assets/twitter.png" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      isHeaderActive: false,
      firstCards: [
        {
          img: "fixed-widthsec-.png",
          header: "Expert Instruction",
          text: "The gradual accumulation of <br /> information about atomic and <br />small-scale behaviour...",
        },
        {
          img: "fixed-width1.png",
          header: "Training Courses",
          text: "The gradual accumulation of <br /> information about atomic and <br />small-scale behaviour...",
        },
        {
          img: "fixed-width2.png",
          header: "Lifetime Acess",
          text: "The gradual accumulation of <br /> information about atomic and <br />small-scale behaviour...",
        },
      ],
      secondCards: [
        {
          img: "product-cover-124sec-.png",
          smHeader: "training Courses",
          header: "Video in Live Action",
          text: `We focus on ergonomics and meeting
          you where you work. It's only a
          keystroke away.`,
        },
        {
          img: "product-cover-125sec-.png",
          smHeader: "Books Library",
          header: "Every Client Matters",
          text: `We focus on ergonomics and meeting
          you where you work. It's only a
          keystroke away.`,
        },
        {
          img: "product-cover-126sec-.png",
          smHeader: "Certified Teacher",
          header: "Get Quality Education",
          text: `We focus on ergonomics and meeting
          you where you work. It's only a
          keystroke away.`,
          last:true,
        },
      ],
      comments: [
        {
          img: "testimonial-user-cover-167.png",
        },
        {
          img: "circle.png",
        },
        {
          img: "circle1.png",
        },
      ],
      freeCards: [{ new: false }, { new: true }, { new: false, last: true }],
    };
  },
};
</script>
