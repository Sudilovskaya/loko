<template>
   <popUp v-if="dialogVisible" @hideDialog="hideDialog" @cartCounter="cartCounter" @showDialog="showDialog" v-bind:slug="slug" >
        <div class="image__group" >
            <div class="popup__image">
              <img v-bind:src="item.image.image"  alt="">
          </div>
          <div class="popup__image">
              <img v-bind:src="item.image.image"  alt="">
              <img v-bind:src="item.image.image"  alt="">
          </div>
          <div class="popup__image">
              <img v-bind:src="item.image.image"  alt="">
          </div>
         </div>
          <div class="product__col popup">
            <div class="product__title"> {{item.name}}</div>
            <div class="product__subtitle">
              <div class="product__cost">
                {{item.price}}₽
              </div>
              <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M10.2443 13.0909V12.554C10.2443 12.1828 10.3205 11.843 10.473 11.5348C10.6288 11.2232 10.8542 10.9747 11.1491 10.7891C11.4474 10.6001 11.8087 10.5057 12.233 10.5057C12.6638 10.5057 13.0251 10.6001 13.3168 10.7891C13.6084 10.9747 13.8288 11.2232 13.978 11.5348C14.1271 11.843 14.2017 12.1828 14.2017 12.554V13.0909C14.2017 13.4621 14.1255 13.8035 13.973 14.1151C13.8239 14.4233 13.6018 14.6719 13.3068 14.8608C13.0152 15.0464 12.6572 15.1392 12.233 15.1392C11.8021 15.1392 11.4392 15.0464 11.1442 14.8608C10.8492 14.6719 10.6255 14.4233 10.473 14.1151C10.3205 13.8035 10.2443 13.4621 10.2443 13.0909ZM11.2585 12.554V13.0909C11.2585 13.3991 11.3314 13.6759 11.4773 13.9212C11.6231 14.1631 11.875 14.2841 12.233 14.2841C12.581 14.2841 12.8262 14.1631 12.9688 13.9212C13.1146 13.6759 13.1875 13.3991 13.1875 13.0909V12.554C13.1875 12.2457 13.1179 11.9706 12.9787 11.7287C12.8395 11.4834 12.5909 11.3608 12.233 11.3608C11.8849 11.3608 11.6347 11.4834 11.4822 11.7287C11.3331 11.9706 11.2585 12.2457 11.2585 12.554ZM5.1733 7.2642V6.72727C5.1733 6.35606 5.24953 6.01634 5.40199 5.7081C5.55777 5.39654 5.78314 5.14796 6.07812 4.96236C6.37642 4.77344 6.73769 4.67898 7.16193 4.67898C7.5928 4.67898 7.95407 4.77344 8.24574 4.96236C8.53741 5.14796 8.75781 5.39654 8.90696 5.7081C9.05611 6.01634 9.13068 6.35606 9.13068 6.72727V7.2642C9.13068 7.63542 9.05445 7.9768 8.90199 8.28835C8.75284 8.59659 8.53078 8.84517 8.2358 9.03409C7.94413 9.2197 7.58617 9.3125 7.16193 9.3125C6.73106 9.3125 6.36813 9.2197 6.07315 9.03409C5.77817 8.84517 5.55445 8.59659 5.40199 8.28835C5.24953 7.9768 5.1733 7.63542 5.1733 7.2642ZM6.1875 6.72727V7.2642C6.1875 7.57244 6.26042 7.8492 6.40625 8.09446C6.55208 8.33641 6.80398 8.45739 7.16193 8.45739C7.50994 8.45739 7.75521 8.33641 7.89773 8.09446C8.04356 7.8492 8.11648 7.57244 8.11648 7.2642V6.72727C8.11648 6.41903 8.04688 6.14394 7.90767 5.90199C7.76847 5.65672 7.51989 5.53409 7.16193 5.53409C6.81392 5.53409 6.56368 5.65672 6.41122 5.90199C6.26207 6.14394 6.1875 6.41903 6.1875 6.72727ZM5.55114 15L12.5511 4.81818H13.6847L6.68466 15H5.55114Z" fill="#433D39"/>
                  <path d="M12.332 2.31997L12.4641 2.41633L12.6276 2.41602L15.5141 2.41052L16.4008 5.15743L16.4511 5.31303L16.5835 5.40889L18.922 7.10108L18.0248 9.84459L17.9739 10L18.0248 10.1554L18.922 12.8989L16.5835 14.5911L16.4511 14.687L16.4008 14.8426L15.5141 17.5895L12.6276 17.584L12.4641 17.5837L12.332 17.68L10 19.3811L7.66802 17.68L7.53592 17.5837L7.3724 17.584L4.48592 17.5895L3.59918 14.8426L3.54894 14.687L3.41648 14.5911L1.07804 12.8989L1.97523 10.1554L2.02606 10L1.97523 9.84459L1.07804 7.10108L3.41648 5.40889L3.54894 5.31303L3.59918 5.15743L4.48592 2.41052L7.3724 2.41602L7.53592 2.41633L7.66802 2.31997L10 0.618891L12.332 2.31997Z" stroke="#433D39"/>
              </svg>
              <div class="product__discount">Скидка на первый заказ </div>
            </div>
            <div class="product__devider"></div>
            <div class="product__description">
                {{item.short_description}}
            </div>
            <div class="cart__btn btn" @click="cartCounter" v-bind:data-articul="item.id">
              <svg width="27" height="10" viewBox="0 0 27 10" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M1 9.25L6 4.25L11 9.25L16 4.25L21 9.25L26 4.25" stroke="#433D39"/>
                  <path d="M1 5.75L6 0.75L11 5.75L16 0.75L21 5.75L26 0.75" stroke="#433D39"/>
                </svg>
                  купить
                <svg width="27" height="10" viewBox="0 0 27 10" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M1 9.25L6 4.25L11 9.25L16 4.25L21 9.25L26 4.25" stroke="#433D39"/>
                    <path d="M1 5.75L6 0.75L11 5.75L16 0.75L21 5.75L26 0.75" stroke="#433D39"/>
                </svg>
            </div>
           <div class="product__devider"></div>
            <div v-html="slug.description" class="slug__description"></div>
         </div>
  </popUp >
  
    <div  class="product">
      <div class="product__image">
              <img v-bind:src="item.image.image"  alt="">
          </div>
          <div class="product__col">
            <div class="product__title"> {{item.name}}</div>
            <div class="product__subtitle">
              <div class="product__cost">
                {{item.price}}₽  
              </div>
              <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M10.2443 13.0909V12.554C10.2443 12.1828 10.3205 11.843 10.473 11.5348C10.6288 11.2232 10.8542 10.9747 11.1491 10.7891C11.4474 10.6001 11.8087 10.5057 12.233 10.5057C12.6638 10.5057 13.0251 10.6001 13.3168 10.7891C13.6084 10.9747 13.8288 11.2232 13.978 11.5348C14.1271 11.843 14.2017 12.1828 14.2017 12.554V13.0909C14.2017 13.4621 14.1255 13.8035 13.973 14.1151C13.8239 14.4233 13.6018 14.6719 13.3068 14.8608C13.0152 15.0464 12.6572 15.1392 12.233 15.1392C11.8021 15.1392 11.4392 15.0464 11.1442 14.8608C10.8492 14.6719 10.6255 14.4233 10.473 14.1151C10.3205 13.8035 10.2443 13.4621 10.2443 13.0909ZM11.2585 12.554V13.0909C11.2585 13.3991 11.3314 13.6759 11.4773 13.9212C11.6231 14.1631 11.875 14.2841 12.233 14.2841C12.581 14.2841 12.8262 14.1631 12.9688 13.9212C13.1146 13.6759 13.1875 13.3991 13.1875 13.0909V12.554C13.1875 12.2457 13.1179 11.9706 12.9787 11.7287C12.8395 11.4834 12.5909 11.3608 12.233 11.3608C11.8849 11.3608 11.6347 11.4834 11.4822 11.7287C11.3331 11.9706 11.2585 12.2457 11.2585 12.554ZM5.1733 7.2642V6.72727C5.1733 6.35606 5.24953 6.01634 5.40199 5.7081C5.55777 5.39654 5.78314 5.14796 6.07812 4.96236C6.37642 4.77344 6.73769 4.67898 7.16193 4.67898C7.5928 4.67898 7.95407 4.77344 8.24574 4.96236C8.53741 5.14796 8.75781 5.39654 8.90696 5.7081C9.05611 6.01634 9.13068 6.35606 9.13068 6.72727V7.2642C9.13068 7.63542 9.05445 7.9768 8.90199 8.28835C8.75284 8.59659 8.53078 8.84517 8.2358 9.03409C7.94413 9.2197 7.58617 9.3125 7.16193 9.3125C6.73106 9.3125 6.36813 9.2197 6.07315 9.03409C5.77817 8.84517 5.55445 8.59659 5.40199 8.28835C5.24953 7.9768 5.1733 7.63542 5.1733 7.2642ZM6.1875 6.72727V7.2642C6.1875 7.57244 6.26042 7.8492 6.40625 8.09446C6.55208 8.33641 6.80398 8.45739 7.16193 8.45739C7.50994 8.45739 7.75521 8.33641 7.89773 8.09446C8.04356 7.8492 8.11648 7.57244 8.11648 7.2642V6.72727C8.11648 6.41903 8.04688 6.14394 7.90767 5.90199C7.76847 5.65672 7.51989 5.53409 7.16193 5.53409C6.81392 5.53409 6.56368 5.65672 6.41122 5.90199C6.26207 6.14394 6.1875 6.41903 6.1875 6.72727ZM5.55114 15L12.5511 4.81818H13.6847L6.68466 15H5.55114Z" fill="#433D39"/>
                  <path d="M12.332 2.31997L12.4641 2.41633L12.6276 2.41602L15.5141 2.41052L16.4008 5.15743L16.4511 5.31303L16.5835 5.40889L18.922 7.10108L18.0248 9.84459L17.9739 10L18.0248 10.1554L18.922 12.8989L16.5835 14.5911L16.4511 14.687L16.4008 14.8426L15.5141 17.5895L12.6276 17.584L12.4641 17.5837L12.332 17.68L10 19.3811L7.66802 17.68L7.53592 17.5837L7.3724 17.584L4.48592 17.5895L3.59918 14.8426L3.54894 14.687L3.41648 14.5911L1.07804 12.8989L1.97523 10.1554L2.02606 10L1.97523 9.84459L1.07804 7.10108L3.41648 5.40889L3.54894 5.31303L3.59918 5.15743L4.48592 2.41052L7.3724 2.41602L7.53592 2.41633L7.66802 2.31997L10 0.618891L12.332 2.31997Z" stroke="#433D39"/>
              </svg>
              <div class="product__discount">Скидка на первый заказ</div>
            </div>
            <div class="product__devider"></div>
            <div class="product__description">
                {{item.short_description}}
            </div>
            <div class="product__btn btn" @click="makeFetch" >
              <svg width="27" height="10" viewBox="0 0 27 10" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M1 9.25L6 4.25L11 9.25L16 4.25L21 9.25L26 4.25" stroke="#433D39"/>
                  <path d="M1 5.75L6 0.75L11 5.75L16 0.75L21 5.75L26 0.75" stroke="#433D39"/>
                </svg>
                  подробнее
                <svg width="27" height="10" viewBox="0 0 27 10" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M1 9.25L6 4.25L11 9.25L16 4.25L21 9.25L26 4.25" stroke="#433D39"/>
                    <path d="M1 5.75L6 0.75L11 5.75L16 0.75L21 5.75L26 0.75" stroke="#433D39"/>
                </svg>
            </div>
         </div>
    </div>
   
</template>


<script>
import popUp from '@/components/popUp'

export default {
    components: {
      popUp
    },
    props: {
       item: {
         type: Object,
         required: true
       },
       cart: []
    },
    data() {
      return{
         dialogVisible: false,
         itemCount: 0,
         slug: {
         type: Object,
         required: true,
       },
      }
    },
    methods:{
      showDialog(){
        this.dialogVisible = true;
        this.$emit('showDialog')
      },
      makeFetch(item){
        this.showDialog()
        item = this.item.slug
        fetch(`http://5.181.254.199/api/products/${item}`)
        .then(res => res.json())
        .then(data => this.slug = data)
      },
      hideDialog(){
        this.dialogVisible = false;
        this.$emit('hideDialog')
      },
      cartCounter(){
        this.itemCount += 1
        this.$emit('cartCounter')
        this.updateParentCounter()
        this.updateParentItem()
        this.cartCounter = function(){}
      },
      updateParentItem(){
        this.$emit('updateItem', {
          item: this.item,
        })
      },
      updateParentCounter(){
        this.$emit('updateCounter', {
          itemCount: this.itemCount,
        })
      }
    }
}
</script>

<style scoped>
.image__group{
   display: flex;
   flex-direction: column;
   grid-column: 1;
   gap: 20px;
}
.popup__image img{
  width: 460px;
  height: 580px;
  object-fit: cover;
}
.popup__image:nth-child(2){
  display: flex;
  gap: 20px;
}
.popup__image:nth-child(2) img{
  width: 220px; 
  height: 280px;
  object-fit: cover;
}
.product{
  display: flex;
  margin: 60px 0;
  gap: 130px;
  position: relative;
   background: url(@/assets/Rectangle29.png) no-repeat top right;
}
.product:nth-child(even){
  flex-direction: row-reverse;
  text-align: right;
  left: 0;
  background: url(@/assets/Rectangle29.png) no-repeat top left;
}
.product__image img {
  width: 460px;
  height: 600px;
  object-fit: cover;
}
.product__col{
  max-width: 590px;
  max-height: 605px;
  position: relative;
  padding-top: 60px;
  width: 100%;
}
.product__col.popup{
  grid-column: span 4;
  margin-left: 130px;
  padding-top: 0;
}
.product__title {
  text-transform: uppercase;
  font-size: 60px;
  line-height: 60px;
  height: 120px;
}
.product__col.popup>.product__title{
  height: auto;
  max-width: 550px;
}
.product__subtitle {
  display: inline-block;
  margin-top: 93px;
  padding-bottom: 25px;
  position: relative;
}
.product__col.popup>.product__subtitle{
  margin-top: 33px;
}
.product__cost {
  font-size: 20px;
  line-height: 20px;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  margin-right: 30px;
  display: inline;
}
.product__subtitle svg{
  vertical-align: middle;
}
.product__discount {
  margin-left: 8px;
  font-family: 'Futura PT';
  display: inline;
}
.product__devider{
  position: relative;
  border: 1px solid rgba(67, 61, 57, 0.1);
  max-width: 590px;
  width: 100%;
}
.product__description {
  display: inline-block;
  margin-top: 45px;
  max-width: 500px;
  font-family: 'Futura PT';
}
.product__col.popup>.product__description{
  margin-top: 25px;
}
.btn {
  display: inline-block;
  cursor: pointer;
  margin-top: 85px;
  padding: 14px 19px;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  border: 1px solid #433D39;
  font-size: 20px;
  transition: all .3s ease-in-out;
}
.product__col.popup>.btn{
  margin-top: 35px;
  margin-bottom: 40px;
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
.product__decoration {
  position: absolute;
  z-index: -10;
  right: 0;
}
</style>
