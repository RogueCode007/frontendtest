<template>
  <div class="absolute py-4 pb-6 bg-white mobilemenu">
      <div class="px-4 flex justify-between items-center">
            <div></div>
            <svg @click="$emit('close')" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M17.59 5L12 10.59L6.41 5L5 6.41L10.59 12L5 17.59L6.41 19L12 13.41L17.59 19L19 17.59L13.41 12L19 6.41L17.59 5Z" fill="#2E3A59"></path>
            </svg>
        </div>
        <u-animate-container class="mt-6 px-4">
            <u-animate
                name="fadeInRight"
                delay="0s"
                duration="1s"
                :iteration="1"
                :offset="20"
                animateClass="animated"
                :begin="true"
            >
                <router-link to="/" class="text-black text-sm block">Timeline</router-link>
            </u-animate>
            <u-animate
                name="fadeInRight"
                delay="0s"
                duration="1.2s"
                :iteration="1"
                :offset="20"
                animateClass="animated"
                :begin="true"
            >
                <router-link to="/" class="text-black text-sm mt-4 block">Peer Review</router-link>
            </u-animate>
            <u-animate
                name="fadeInRight"
                delay="0s"
                duration="1.4s"
                :iteration="1"
                :offset="20"
                animateClass="animated"
                :begin="true"
            >
                <router-link to="/" class="text-black text-sm mt-4 block">Login</router-link>
            </u-animate>
            <u-animate
                name="fadeInRight"
                delay="0s"
                duration="1.6s"
                :iteration="1"
                :offset="20"
                animateClass="animated"
                :begin="true"
            >
                <router-link to="/" class="rounded p-2 signup text-center text-sm mt-4 block">SignUp</router-link>
            </u-animate>
        </u-animate-container>
  </div>
</template>

<script>
import "animate.css"
export default {

}
</script>

<style scoped>
.mobilemenu{
  top: 0;
  width: 100%;
  left: 0;
  box-shadow: 0px 9px 45px #00000090;
  z-index: 1002
}
.signup{
    border: 1px solid #FF6634;
    color: #FF6634;
    width: 100px
}
</style>