<template >
 <div class="fill" id="WE">
  <b-container class="DarkWhiteColor">
   <b-row align-h="center" align-v="center" class="flex-wrap-reverse py-5">
      <b-col cols="12" sm="10"  md="8" lg="7">
       <div class="bg-imgWE"></div>
      </b-col>
      <b-col cols="12" sm="10"  md="8" lg="5" class="p-4">
        <div  class="d-flex align-items-center">
          <img :src="require(`~/assets/icon/logo.svg`)" class="logo"/>
          <div class="logoText">
            <span>أكاديمية الحوت</span>
            <span>Alhut Academy</span>
          </div>
        </div>
        <h2 class="mt-2 mb-5 font-weight-bold">من نحن</h2>
        <div class="mt-5">
          <div class="d-flex">
            <img :src="require(`~/assets/icon/mess.svg`)" class="icon">
            <h5 class="pr-2 mt-1">الرسالة</h5>
          </div>
          <p class="pr-4">هذا النص هو مثفة إلى زيادة عدد الحروف التى يولدها التطبيق.</p>
        </div>
        <div class="mt-4">
          <div class="d-flex">
            <img :src="require(`~/assets/icon/good-heart.svg`)" class="icon">
            <h5 class="pr-2 mt-1">القيم</h5>
          </div>
          <p class="pr-4">هذا النص هو مثفة إلى زيادة عدد الحروف التى يولدها التطبيق.</p>
        </div>
        <div class="mt-4">
          <div class="d-flex">
            <img :src="require(`~/assets/icon/whale-we.svg`)" class="icon">
            <h5 class="pr-2 mt-1">عن اكاديمية الحوت</h5>
          </div>
          <p class="pr-4">هذا النص هو مثفة إلى زيادة عدد الحروف التى يولدها التطبيق.</p>
        </div>
      </b-col>
   </b-row>
  </b-container>
 </div>
</template>

<style scoped>
.fill{
  background-color: var(--fill);
}
.logo{
  width: 55px;
  margin-left: 5px;
 }
 .logoText{
   display: flex;
   flex-direction: column;
   font-size: 10px;
 }
.bg-imgWE{
  background-image: url('~/assets/img/we2.png');
  background-position: center;
  /* background-clip: content-box; */
  background-repeat: no-repeat;
  background-size: contain;
  height: 500px;
}

@media (max-width:989px) {
  .bg-imgWE{
    height: 400px;
  }
}
@media (max-width:767px) {
  .bg-imgWE{
    height: 350px;
  }
}
@media (max-width:567px) {
  .bg-imgWE{
    height: 300px;
  }
}

.imgMode{
    background-image: url('~/assets/img/we.png');
}
</style>
