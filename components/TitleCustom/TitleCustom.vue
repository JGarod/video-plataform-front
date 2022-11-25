<template>
    <div class="flex flex-col ">
        <div class="flex flex-row ">
            <div class="p-2">
            <div class="bg-[#C8DEFF] w-[50px] h-[50px] rounded-[50%] ">
                <img class="  w-[50px] h-[50px] rounded-[50%]"  v-bind:src="data.user_A.profile" alt="">
            </div>
          </div>
    <div class=" py-3">
            <h1 class=" w-[480px] h-[20px] font-semibold text-sm text-start text-white">{{data.title}}</h1>
            <p class="w-[250px] h-[20px] font-semibold text-xs text-start text-[#C8DEFF]">{{data.user_A.username}}</p>
          </div>
        </div>
    <div class="px-4 w-[480px] h-[20px] font-semibold text-xl text-white">
        <h1>{{data.title}}</h1>
    </div>
</div>

</template>

<script setup>
      import {useFetch} from "nuxt/app";
      import {ubicacion} from "../../index"
      // var URLactual = window.location.href;
      // var num2= [... URLactual]
      // console.log(num2)
      const url = ubicacion
      const {data} =  useFetch(url)

      
</script>