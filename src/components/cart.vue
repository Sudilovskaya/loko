<template>
   <div class="dialog" @click="hideCart" >
      <div @click.stop class="dialog__content"  >
         <button class="dialog-close" @click="hideCart">
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <g opacity="0.3">
            <path d="M18 6L6 18" stroke="#433D39" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
            <path d="M6 6L18 18" stroke="#433D39" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
            </g>
          </svg>
         </button>
            <slot></slot>
      </div>
   </div>
</template>

<script>
export default {
   props: {
     
  },
   methods:{
     hideCart(){
        this.$emit('hideCart')
     }
  },
}
</script>

<style scoped>
* {
   font-family: 'Alumni Sans', sans-serif;
   color: #433D39;
}
.dialog-close{
   position: absolute;
   right: 20px;
   top: 20px;
   cursor: pointer;
   border: none;
   background: none;
   z-index: 10;   
}
.dialog{
   top: 0;
   left: 0;
   width: 100%;
   height: 100%;
   background-color:rgba(67,61,57, 0.1);
   position: fixed;
   z-index: 1001;
   overflow-y: scroll;
   display: grid;
   grid-template: 1fr / repeat(5, 1fr);
   overflow-x: hidden;
   justify-items: center;
}
.dialog__content{
   background-color:#fff;
   border-radius: 4px;
   position: absolute;
   grid-column: span 5;
   display: flex;
   gap: 130px;
   padding: 30px 20px;
   margin: 50px 150px;
   max-width: 1220px;   
   width: 100%;
   height: auto;
}
</style>
