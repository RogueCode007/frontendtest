<template>
  <div class=" py-10">
      <div class="box">
      <div v-for="(review, index) in reviews" :key="index" class="bg-white rounded p-3 mb-6 card">
          <div class="flex items-end">
              <star-rating :value="review.rating" :disabled="true"></star-rating>
              <span class="ml-2 font-bold">{{review.rating}}.0</span>
          </div>
            <p class="mt-2 text-gray-500 text-sm">{{review.text}}</p>
            <div class="mt-4 flex items-center justify-between">
                <p class="tag font-bold text-center p-1 rounded">{{review.tag}}</p>
                <div class="flex items-center">
                    <svg width="10" height="9" viewBox="0 0 10 9" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M4.0625 0.625C3.81386 0.625 3.5754 0.723772 3.39959 0.899587C3.22377 1.0754 3.125 1.31386 3.125 1.5625V1.875H0.9375C0.68886 1.875 0.450403 1.97377 0.274587 2.14959C0.098772 2.3254 0 2.56386 0 2.8125L0 7.8125C0 8.06114 0.098772 8.2996 0.274587 8.47541C0.450403 8.65123 0.68886 8.75 0.9375 8.75H9.0625C9.31114 8.75 9.5496 8.65123 9.72541 8.47541C9.90123 8.2996 10 8.06114 10 7.8125V2.8125C10 2.56386 9.90123 2.3254 9.72541 2.14959C9.5496 1.97377 9.31114 1.875 9.0625 1.875H6.875V1.5625C6.875 1.31386 6.77623 1.0754 6.60041 0.899587C6.4246 0.723772 6.18614 0.625 5.9375 0.625H4.0625ZM4.0625 1.25H5.9375C6.02038 1.25 6.09987 1.28292 6.15847 1.34153C6.21708 1.40013 6.25 1.47962 6.25 1.5625V1.875H3.75V1.5625C3.75 1.47962 3.78292 1.40013 3.84153 1.34153C3.90013 1.28292 3.97962 1.25 4.0625 1.25ZM5.24125 5.57125L9.375 4.46938V7.8125C9.375 7.89538 9.34208 7.97487 9.28347 8.03347C9.22487 8.09208 9.14538 8.125 9.0625 8.125H0.9375C0.85462 8.125 0.775134 8.09208 0.716529 8.03347C0.657924 7.97487 0.625 7.89538 0.625 7.8125V4.46875L4.75875 5.57125C4.91683 5.61335 5.08317 5.61335 5.24125 5.57125ZM0.9375 2.5H9.0625C9.14538 2.5 9.22487 2.53292 9.28347 2.59153C9.34208 2.65013 9.375 2.72962 9.375 2.8125V3.8225L5.08062 4.9675C5.0278 4.98161 4.9722 4.98161 4.91937 4.9675L0.625 3.8225V2.8125C0.625 2.72962 0.657924 2.65013 0.716529 2.59153C0.775134 2.53292 0.85462 2.5 0.9375 2.5Z" fill="#FF6634"/>
                    </svg>
                    <p class="company ml-2 font-bold text-xs">{{review.company}}</p>
                </div>
            </div>
            <div class="mt-6 flex">
                <img :src="review.image" alt="avatar">
                <div class="ml-3">
                    <p class="text-gray-600 name font-semibold">{{review.name}}</p>
                    <p class="text-gray-500 role">{{review.role}}</p>
                </div>
            </div>
      </div>
      </div>
      <div class="mt-8 flex justify-center">
            <svg class="block mx-2" width="13" height="13" viewBox="0 0 13 13" fill="#8A8A8A" xmlns="http://www.w3.org/2000/svg">
                <circle cx="6.5" cy="6.5" r="5.5" stroke="#E9E9E9" stroke-width="2"/>
            </svg>
            <svg class="block mx-2" width="13" height="13" viewBox="0 0 13 13" fill="none" xmlns="http://www.w3.org/2000/svg">
                <circle cx="6.5" cy="6.5" r="5.5" stroke="#E9E9E9" stroke-width="2"/>
            </svg>
            <svg class="block mx-2" width="13" height="13" viewBox="0 0 13 13" fill="none" xmlns="http://www.w3.org/2000/svg">
                <circle cx="6.5" cy="6.5" r="5.5" stroke="#E9E9E9" stroke-width="2"/>
            </svg>
      </div>
  </div>
</template>

<script>
import image2 from "@/assets/Ellipse 1.png"
import StarRating from './RightBox/StarRating.vue'
export default {
    components:{StarRating},
    data(){
        return {
            reviews: [
                {
                    text: "Great place to work with the good work culture and people skills.",
                    rating: 4,
                    tag: "sexual assault",
                    image: image2,
                    company: "Facebook",
                    name: "Anonymous",
                    role: "Business Analysis"
                },
                {
                    text: "Great place to work with the good work culture and people skills.",
                    rating: 3,
                    tag: "sexual assault",
                    image: image2,
                    company: "Google",
                    name: "Anonymous",
                    role: "Consumer Satisfaction"
                },
                {
                    text: "Great place to work with the good work culture and people skills.",
                    rating: 5,
                    tag: "racism",
                    image: image2,
                    company: "Netflix",
                    name: "Anonymous",
                    role: "Customer Success"
                },
                {
                    text: "Great place to work with the good work culture and people skills.",
                    rating: 4,
                    tag: "sexual assault",
                    image: image2,
                    company: "Amazon",
                    name: "Anonymous",
                    role: "Business Analysis"
                },
                {
                    text: "Great place to work with the good work culture and people skills.",
                    rating: 2,
                    tag: "nepotism",
                    image: image2,
                    company: "Apple",
                    name: "Anonymous",
                    role: "Business Analysis"
                },
                {
                    text: "Great place to work with the good work culture and people skills.",
                    rating: 3,
                    tag: "sexual assault",
                    image: image2,
                    company: "Google",
                    name: "Anonymous",
                    role: "Business Analysis"
                },
            ]
        }
    }
}
</script>

<style scoped>
.card{
    border: 1px solid red;
    box-shadow: 0px 5px 10px 2px rgba(0, 0, 0, 0.04);
    border: 1px solid #FBFBFB;
}
.tag{
    background: rgba(255, 102, 52, 0.05);
    color: #FF6634
}
.company, .role{
    font-size: 10px
}
.name{
    font-size: 12px;
}
@media only screen and (min-width: 1024px){
    .box{
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
    }
    .card{
        flex: 0 1 30%
    }
}
</style>