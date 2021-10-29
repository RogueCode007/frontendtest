<template>
  <div class=" relative px-3 py-10 lg:py-20 leftbox lg:px-10">
      <h1 class="text-2xl font-black lg:w-4/5">Grow your business with real-time reviews</h1>
      <p class="mt-4 text-xs leadingtext lg:w-4/5">Find out more on what people and saying about your company, with real time reveiw and data.</p>
      <div class="mt-8 flex p-1 pl-3 justify-between items-center gap-2 bg-white rounded input ">
          <input type="text" class="text-xs w-full lg:text-base focus:outline-none" placeholder="Search for Companies">
          <button class="text-white text-sm p-2 lg:px-4 lg:py-3 rounded">Search</button>
      </div>
      <p class="mt-6 text-xs lg:text-sm act">Already have an account? <span class="font-bold">Sign In</span></p>
      <div class="quote">
          <div class="mt-14 px-6 relative lg:w-3/5">
                <div class="absolute topsvg gap-1">
                    <svg width="10" height="18" viewBox="0 0 10 18" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M10 18L0.0499992 18L0.0500001 8.04L4.04 0.0599989L9 0.0599994L5.03 8.04L10 8.04L10 18Z" fill="#FF6634"/>
                        </svg>
                    <svg width="10" height="18" viewBox="0 0 10 18" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M10 18L0.0499992 18L0.0500001 8.04L4.04 0.0599989L9 0.0599994L5.03 8.04L10 8.04L10 18Z" fill="#FF6634"/>
                        </svg>
                </div>
                <p class="text-xs" style="color:#8D8D8D">A life spent making mistakes is not only more honorable, but more useful than a life spent doing nothing.</p>
                <div class="absolute bottomsvg gap-1">
                    <svg width="10" height="18" viewBox="0 0 10 18" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M0 0H9.95V9.96L5.96 17.94H1L4.97 9.96H0V0Z" fill="#FF6634"/>
                        </svg>
                    <svg width="10" height="18" viewBox="0 0 10 18" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M0 0H9.95V9.96L5.96 17.94H1L4.97 9.96H0V0Z" fill="#FF6634"/>
                        </svg>
                </div>
            </div>
      </div>
      
  </div>
</template>

<script>

export default {
    
}
</script>

<style scoped>
.leftbox{
    min-height: 400px;
    overflow-x: hidden;
}
h1{
    color: #303030;
    z-index: 100;
}
.leadingtext{
    z-index: 100;
}
.input{
    z-index: 100;
    /* left: 0; */
    width: 90%;
}
.act{
    
    z-index: 100
}
input::placeholder{
    color: #DEDEDE
}
button{
    background: #FF6634;
}
span{
    color: #FF6634;
}
.quote{
    top: 250px;
    z-index: 100;
}
.topsvg{
    display: flex;
    top: -8px;
    left: -10px
}
.bottomsvg{
    display: flex;
    bottom: -8px;
    right: 15px
}
@media only screen and (min-width: 1024px){
    .leftbox{
        width: 100%;
    }
    h1{
        font-size: 2.5em;
        line-height: 50px
    }
    .leadingtext{
        font-size: 1em;
        line-height: 25px
    }
    .input{
        max-width: 450px;
        padding: 10px
    }
}
</style>