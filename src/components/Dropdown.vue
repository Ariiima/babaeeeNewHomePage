<template>
  <div>
    <div  
    :class=" mobile ? 'flex justify-center' : 'relative' "
    @click="isOpen" v-click-outside="onClickOutside">
      <!-- Dropdown toggle button -->
      <button
        class = "px-[5rem]"
        :class="buttonClass"
      >
        <span>{{name}}</span>
        <svg
          class="float-left pr-1 h-5 text-indigo-100 dark:text-white pt-1"
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
      </button>

      <!-- Dropdown menu -->
      <div
        
        v-show="show"
        class="transition absolute right-0 py-2 mt-2 rounded-md shadow-xl w-44 bg-[#1A1A1A]/[95%]"
      >
        <a
        href='#'
        v-for="item of items"
          to="/"
          class="block px-4 py-2 text-[#E5E5E5] hover:bg-[#262626] hover:text-white px-6 py-2 rounded-[10px] "
        >
          {{item}}
        </a>


      </div>
    </div>
  </div>
</template>
<script>
  import vClickOutside from 'click-outside-vue3'
  import { ref } from 'vue';
  export default {
     directives: {
      clickOutside: vClickOutside.directive
    },
   methods: {
      onClickOutside (event) {
        this.show=false;
      }
    },
    props: {
    mobile : '',
    buttonClass:'',
    name:'',
    items:[]
  },
    setup(props) {
      let show = ref(false);
      const isOpen = () => (show.value = !show.value);
      return { show, isOpen };
    },
  };
</script>
