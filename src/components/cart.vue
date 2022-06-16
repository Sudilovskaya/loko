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
            <button class="cta-btn btn">
               <svg width="27" height="10" viewBox="0 0 27 10" fill="none" xmlns="http://www.w3.org/2000/svg">
                     <path d="M1 9.25L6 4.25L11 9.25L16 4.25L21 9.25L26 4.25" stroke="#433D39"/>
                     <path d="M1 5.75L6 0.75L11 5.75L16 0.75L21 5.75L26 0.75" stroke="#433D39"/>
                  </svg>
                     оформить заказ
                  <svg width="27" height="10" viewBox="0 0 27 10" fill="none" xmlns="http://www.w3.org/2000/svg">
                     <path d="M1 9.25L6 4.25L11 9.25L16 4.25L21 9.25L26 4.25" stroke="#433D39"/>
                     <path d="M1 5.75L6 0.75L11 5.75L16 0.75L21 5.75L26 0.75" stroke="#433D39"/>
                  </svg>
            </button>
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
*{
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
}
.dialog__content{
   background-color:#fff;
   border-radius: 4px;
   position: relative;
   grid-column: span 5;
   height: 420px;
   display: flex;
   gap: 130px;
   padding: 30px 20px;
   margin: 50px 150px;
   max-width: 1220px;   
   width: 100%;
}
.btn {
  display: inline-block;
  cursor: pointer;
  margin-top: 85px;
  padding: 14px 19px;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  border: 1px solid #433D39;
  background-color: #fff;
  font-size: 20px;
  transition: all .3s ease-in-out;
  position: absolute;
  bottom: 30px;
  right: 20px;

}
.btn svg path{
  transition: all .3s ease-in-out;
}
.btn:hover{
  background-color: #433D39;
  color: #FFFFFF;
}
.btn:hover svg path {
  stroke: #FFFFFF;
}
</style>
