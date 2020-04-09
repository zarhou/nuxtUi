<template>
  <div class="flex justify-center items-center min-h-screen bg-gray-200">
    <div class="content bg-white rounded-lg">
     <nav class="mt-10 mx-8">

       <nuxt-link :to="{name: 'dashboard'}"
        class="text-2xl text-green-300 pl-4 border-b-2 border-green-200 w-full inline-block"
        >Dashboard</nuxt-link>

      <nuxt-link :to="{name: 'store'}"
        class="text-2xl text-green-300 mt-4 pl-4 border-b-2 border-green-200 w-full inline-block"
        >store</nuxt-link>

      <nuxt-link :to="{name: 'landing'}"
        class="text-2xl text-green-300 mt-4 pl-4 border-b-2 border-green-200 w-full inline-block"
        >Landing page</nuxt-link>
      
      <nuxt-link :to="{name: 'store'}"
        class="text-2xl text-green-300 mt-4 opacity-25 pl-4 border-b-2 border-green-200 w-full inline-block"
        >store</nuxt-link>
        
        
     </nav>
    </div>
  </div>  
</template>

<style lang="scss" scoped>

.content {
  min-height: 40rem;
  width: 40rem;
}

</style>
