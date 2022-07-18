<template>
  <div dir="rtl">
    <nav
      class="
        container
        px-6
        py-8
        mx-auto
        lg:flex lg:justify-between lg:items-center
      "
    >
    <div class="flex">
     <a href="https://babaeee.ir/">
         <img src="../assets/logos/whiteLogo.png" class="w-[128px] h-[44px] ml-auto mr-5">
    </a>
      <div class="flex items-center mr-auto justify-between">
        <!-- Mobile menu button -->
        <div @click="toggleNav" class="flex lg:hidden">
          <button
            type="button"
            class="
              text-gray-100
              hover:text-gray-400
              focus:outline-none focus:text-gray-400
            "
          >
            <svg viewBox="0 0 24 24" class="w-6 h-6 fill-current">
              <path
                fill-rule="evenodd"
                d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"
              ></path>
            </svg>
          </button>
        </div>
      </div>
    </div>
      <!-- Mobile Menu open: "block", Menu closed: "hidden" -->
      <ul
        :class="state.showMenu ? 'flex' : 'hidden'"
        class="
          flex-col
          mt-8
          space-y-4
          lg:flex lg:space-y-0 lg:flex-row lg:items-center lg:space-x-1 lg:mt-0 xl:space-x-4
        "
      >
            <button class="text-sm text-[#E5E5E5] hover:bg-[#FFFFFF]/5 hover:text-white  lg:px-4 py-2 rounded-[10px]">خانه</button>
            <button class="text-sm text-[#E5E5E5] hover:bg-[#FFFFFF]/5 hover:text-white  lg:px-4 py-2 rounded-[10px]">سایت قدیم</button>
            <Dropdown buttonClass="text-sm text-[#E5E5E5] hover:bg-[#262626] hover:text-white lg:px-4 py-2 rounded-[10px] content-center" name="آموزش المپیاد" :items="['تست ۱','تست ۲']" :mobile="state.showMenu ? true : false " />	   
            <Dropdown buttonClass="text-sm text-[#E5E5E5] hover:bg-[#262626] hover:text-white lg:px-4 py-2 rounded-[10px] content-center" name="آشنایی با المپیاد" :items="['تست ۱','تست ۲']" :mobile="state.showMenu ? true : false "/>	   
            <Dropdown buttonClass="text-sm text-[#E5E5E5] hover:bg-[#262626] hover:text-white lg:px-4 py-2 rounded-[10px] content-center" name="جشنواره سالیانه" :items="['تست ۱','تست ۲']" :mobile="state.showMenu ? true : false"/>	   
            <Dropdown  buttonClass="text-sm text-[#E5E5E5] hover:bg-[#262626] hover:text-white lg:px-4 py-2 rounded-[10px] content-center" name="ببعییی" :items="['تست ۱','تست ۲']" :mobile="state.showMenu ? true : false"/>	   

      </ul>
      <div class="flex ml-5 gap-x-3 invisible lg:visible">
            <a href="">
            <img src="../assets/settingIcon.png" class="w-[28px] h-[28px] cursor-pointer hover:-translate-y-[1px]">
            </a>
            <a href="">
            <img src="../assets/profileIcon.png" class="w-[28px] h-[28px] cursor-pointer hover:-translate-y-[1px]">
            </a>
        </div>
    </nav>
  </div>
</template>
<script setup>
    import { reactive } from 'vue';
    import Dropdown from './Dropdown.vue';
    const state = reactive({showMenu:false})
    const toggleNav = () => (state.showMenu = !state.showMenu);
</script>