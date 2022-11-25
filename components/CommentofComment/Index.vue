<template>

    <div v-for="(i, index) in data.user_comentario[0].coment_from_coment.length" class="py-2">
      <div class="flex flex-col w-[full] md:max-lg top-[284px] left-[1260px] px-2.5 py-2 gap-[10px] bg-[#2d64ef] rounded-[20px] items-start ">
        <div class="flex flex-row ">
          <div class="p-2">
            <div class=" w-[20px] h-[20px] rounded-[50%] ">
                <img class=" w-[20px] h-[20px] rounded-[50%]" v-bind:src="data.user_comentario[0].coment_from_coment[index].userR2.profile" alt="">
            </div>
          </div>
          <div >
            <h1 class=" w-[100px] h-[20px] font-semibold text-sm text-start text-white ">{{data.user_comentario[0].coment_from_coment[index].userR2.username}}: </h1>
          </div>
          <div class=" w-[140px]  pt-1  font-semibold text-xs text-white pl-[10px]">
          <p>
            {{data.user_comentario[0].coment_from_coment[index].comment}}
          </p>
        </div>
        <div class="flex flex-row pl-[50px]">
            <p class="w-[80px] h-[10px] pt-3 font-semibold text-xs text-start text-[#C8DEFF]">{{data.user_comentario[0].coment_from_coment[index].fecha.substr(0, 24 - 14)}}</p>
            <p class="w-[100px] h-[10px] pt-3 font-semibold text-xs text-start text-[#C8DEFF]  ">{{data.user_comentario[0].coment_from_coment[index].fecha.substr(11, 13 - 8)}}</p>
           </div>
        </div>
        
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
      const muestra = false;
      const {data} =  useFetch(url)

     

      
</script>
