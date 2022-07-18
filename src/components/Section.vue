<script setup>
    import {reactive} from 'vue'
    const state = reactive({
        hover : '',
        ishovered : false
    })

    function onmouseenter(e){
        state.hover = e.srcElement.id;
    }
    function onmouseleave(){
        state.hover = '';
    }
    function hovered(){
        state.ishovered = !state.ishovered;
    }

</script>


<template >

    <div class="">
        <section class="bg-[#E5E5E5] pt-60 pb-40 pr-10" dir="rtl">
                <img class=" h-[10rem] md:h-[17rem] lg:h-[21rem] xl:h-[26rem] w-auto float-left ml-20" src="../assets/holder.png" alt="">
                <div class="flex place-items-center gap-2">
                    <span class="w-6 h-[1px] rounded-full mr-2 bg-[#808080] inline-block"></span>
                    <h3 class="text-sm text-[#808080]">آموزش جذاب و رایگان</h3>
                </div>
                <h2 class="text-3xl blackText font-black mt-5 ">
                    آموزش المپیاد کامپیوتر
                </h2>
                <div class="space-y-4">
                    <a href="" class="relative flex dark:text-[#E5E5E5] mt-10 w-[22rem] lg:w-fit"  @mouseenter="onmouseenter" @mouseleave="onmouseleave" id="1">
                            <div class="absolute bg-[#FF5E5E] rounded-[50px] w-[8px] h-10 self-center transition right-[5px]"
                            :class=" state.hover==='1' ? 'scale-y-150':'' "
                                ></div>
                            <div
                            class="bg-white dark:bg-[#3A3A3A] rounded-[20px] space-y-4 p-5 hover:shadow-xl mr-[6px] w-[28rem] h-[65px] lg:px-6">
                            <div 
                            class="font-bold "
                            :class = " state.hover==='1' && 'text-[#FF5E5E]'">
                            آموزش
                            <span class="text-[#FF5E5E]">مرحله اول</span>
                            المپیاد کامپیوتر
                            </div>
                            </div>
                    </a>
                     <a href="" class="relative flex dark:text-[#E5E5E5] mt-10 w-[22rem] lg:w-fit"  @mouseenter="onmouseenter" @mouseleave="onmouseleave" id="2">
                            <div class="absolute bg-[#FF5E5E] rounded-[50px] w-[8px] h-10 self-center transition right-[5px]"
                            :class=" state.hover==='2' ? 'scale-y-150':'' "
                                >  </div>
                            <div
                            class="bg-white dark:bg-[#3A3A3A] rounded-[20px] space-y-4 p-5 hover:shadow-xl mr-[6px] w-[28rem] h-[65px] lg:px-6">
                            <div 
                            class="font-bold "
                            :class = " state.hover==='2' && 'text-[#FF5E5E]'">
                            آموزش
                            <span class="text-[#FF5E5E]">مرحله اول</span>
                            المپیاد کامپیوتر
                            </div>
                            </div>
                    </a>
                    <a href="#" class="flex w-fit" @mouseenter="hovered" @mouseleave="hovered">
                        <h3 class="mt-8 mr-2 font-bold" >همکاری در تولید محتوا</h3>
                        <svg
                        class="transition float-left pr-1 h-5 text-black rotate-90 mt-9 dark:text-white pt-1"
                        :class="state.ishovered ? '-translate-x-1' : '' "
                        xmlns="http://www.w3.org/2000/svg"
                        viewBox="0 0 20 20"
                        fill="currentColor"
                        >
                        <path
                            fill-rule="evenodd"
                            d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
                            clip-rule="evenodd"
                        />
                        </svg>
                    </a>
                
                </div>
            
        </section>
    </div>
</template>