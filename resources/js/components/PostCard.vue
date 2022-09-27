<template>
   <div class="card my-4 p-3">
      <h4 class="card-title">
         {{ post.title }}
      </h4>
   </div>
</template>

<script>
   export default {
      props: [
         'post'
      ]
   }
</script>

<style>
   
</style>