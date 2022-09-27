<template>
   <main>
      <div class="container">
         <div class="row py-5">
            <div class="col-12">
               <h2>Main Content</h2>
               <PostCard />
            </div>
         </div>
      </div>
   </main>
</template>

<script>
   import PostCard from './PostCard.vue';

   export default {
      components: {
         PostCard
      }
   }
</script>

<style>
   
</style>