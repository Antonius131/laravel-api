<template>
   <main>
      <div class="container">
         <div class="row py-5">
            <div class="col-12">
               <div class="row">
                  <div class="col-12">
                     <h2>Main Content</h2>
                  </div>
               </div>
               <div class="row">
                  <div class="col-4">
                     <PostCard />
                  </div>
               </div>
            </div>
         </div>
      </div>
   </main>
</template>

<script>
   import PostCard from './PostCard.vue';
   import Axios from 'axios';

   export default {
      components: {
         PostCard
      },
      data: function(){
         return {
            posts: [],
         }
      },
      methods: {
         getPosts(postPage = 1){
            Axios.get('/api/posts', {
               page: postPage
            }).then((response) => {
               this.posts = response.data.results;
            });
         }
      },
      created() {
         this.getPosts();
      }
   }
</script>

<style>
   
</style>