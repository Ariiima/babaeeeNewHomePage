<script setup>
  import Section from './components/Section.vue'
  import Header from './components/Header.vue'
  import Footer from './components/Footer.vue'
  import Swiper from './components/Swiper.vue'
  import Navbar from './components/Navbar.vue'
</script>

<template>
  <div class='bg-[#1A1A1A]'>
    <Navbar class="mb-10" />
    <section class="max-w-md sm:max-w-lg md:max-w-xl xl:max-w-3xl space-y-6 mx-auto flex flex-col items-center" dir="rtl">
        <span class="text-white font-bold text-4xl blackText sm:text-5xl sm:mb-4 xl:text-7xl mt-10">
            المپیاد را
            <span class="text-[#FF5E5E] blackText">جذاب</span>
            بیاموزید!
        </span>
        <p class="text-sm max-w-[23rem] sm:max-w-[30rem] sm:text-lg lg:max-w-[40rem] xl:max-w-[45rem] text-[#E5E5E5] text-justify">
            نزدیک به چهل سال از نخستین مسابقات المپیاد کشوری میگذرد. با وجود محبوبیت یافتن این مسابقات در میان تمام اقشار دانش آموزی، همچنان کمبود منابع معتبر آموزشی خصوصا درمیان طبقات محروم جامعه به چشم می آید. لذا، اکثریت مدال آوران المپیاد در دهه های گذشته را دانش آموزان استان های بزرگ کشوری تشکیل داده اند. در این راستا، گروه ببعییی تلاش کرده است تا با در اختیار قرار دادن آموزش های رایگان، دانش آموزان دبیرستانی از تمامی اقشار اجتماعی و اقتصادی را با مراجع به روز المپیادهای کشوری آشنا سازد. گروه ببعییی با فراهم کردن فیلم و انیمیشن های آموزشی و مشاوره ای، بخش های تعاملی و تمرین های درسی سعی براین دارد که شعله اشتیاق یادگیری را درمیان دانش آموزان مستعد برافروزد، از پیچیدگی های مسیر المپیاد بکاهد و تنوع فرهنگی را در جامعه المپیاد توسعه دهد.
        </p>
    </section>
    <Swiper class="w-[28rem] sm:w-[35rem] lg:w-[50rem] xl:w-[80rem] translate-y-[7rem]"/>
    <Section/>
    
    <Section/>
    <Footer/>
  </div>
</template>

<style scoped>
		@font-face{
			font-family: 'IranianSans';
			src:url(assets/fonts/IRANSans/IRANSans.ttf);
			}
		@font-face{
			font-family: 'IranianSansBold';
			src:url(assets/fonts/IRANSans/IRANSans_Bold.ttf);
			font-weight: bold;
			}
		@font-face{
			font-family: 'IranianSansBlack';
			src:url(assets/fonts/IRANSans/IRANSans_Black.ttf);
			font-weight: bold;
			}
		*{
			font-family: 'IranianSans';
		}
		.bigText{
			
			font-family: 'IranianSansBold';
		}
		.blackText{
			font-family: 'IranianSansBlack';
		}
</style>
