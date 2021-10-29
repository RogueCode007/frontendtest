<template>
  <div class="bg-white py-6 lg: py-10 px-3 lg:px-16">
      <div>
          <h1 class="font-bold text-center text-xl">Featured Reviews</h1>
          <p class="text-center mt-4">Here are some from the review been done by some of the employees on this platform.</p>
          <Reviews />
      </div>
  </div>
</template>

<script>
import Reviews from "./Reviews.vue"
export default {
    components:{Reviews}
}
</script>

<style>

</style>