<script setup>
  import Dropdown from './Dropdown.vue'
</script>

<template>
    <header class="flex flex-row gap-x-5 p-4 items-center">
  	<div class="flex ml-5 gap-x-3">
  	 <a href="">
	   <img src="../assets/settingIcon.png" class="w-[28px] h-[28px] cursor-pointer hover:-translate-y-[1px]">
  	 </a>
  	 <a href="">
	   <img src="../assets/profileIcon.png" class="w-[28px] h-[28px] cursor-pointer hover:-translate-y-[1px]">
  	 </a>
  	</div>
   <div class="flex mx-auto space-x-1" dir="rtl">
	   <button class="text-[#E5E5E5] hover:bg-[#FFFFFF]/5 hover:text-white px-6 py-2 rounded-[10px]">خانه</button>
	   <button class="text-[#E5E5E5] hover:bg-[#FFFFFF]/5 hover:text-white px-6 py-2 rounded-[10px]">سایت قدیم</button>
       <Dropdown class="dropdown" name="آموزش المپیاد" :items="['تست ۱','تست ۲']"/>	   
       <Dropdown class="dropdown" name="آشنایی با المپیاد" :items="['تست ۱','تست ۲']"/>	   
       <Dropdown class="dropdown" name="جشنواره سالیانه" :items="['تست ۱','تست ۲']"/>	   
       <Dropdown class="dropdown" name="ببعییی" :items="['تست ۱','تست ۲']"/>	   


   </div>
	 <a href="https://babaeee.ir/">
		<img src="../assets/logos/whiteLogo.png" class="w-[128px] h-[44px] ml-auto mr-5">
		</a>
   </header>
</template>