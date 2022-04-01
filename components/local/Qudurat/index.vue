<template >
 <div id="Qudurat">
  <b-container class="DarkWhiteColor">
    <h2 class="mt-5 text-center font-weight-bold"> قدرات</h2>
    <p class="text-center m-0">هذا النص هو مثال لنص يمكن أن يستبدقد تم توليد هذا النص لتى يولدها التطبيق.</p>
    <p class="text-center m-0">هذا النص هو مثال لنص يمكن أن يستبدل في نفس المساحة، لقد تم تولة التى يولدها التطبيق.</p>

   <b-row align-h="center"  class="flex-wrap-reverse py-5 mt-4">

      <b-col cols="12" sm="10"  md="8" lg="5" class="px-4">

        <div class="">
          <div class="d-flex">
            <img :src="require(`~/assets/icon/webpage.svg`)" class="icon">
            <h5 class="pr-3 mt-1 font-weight-bold">نماذج الكترونية</h5>
          </div>
          <p class="pr-5 mt-2">هذا النص هو مثفة إلى زيادة عدد الحروف التى يولدها التطبيق.</p>
          <b-button size="sm" class="py-2 px-5 rounded mr-5" type="button" variant="primary" >معرفة المزيد</b-button>

        </div>
        <div class="my-5">
          <div class="d-flex">
            <img :src="require(`~/assets/icon/pdf.svg`)" class="icon">
            <h5 class="pr-3 mt-1 font-weight-bold"> تجميعات بصيغه بي دي اف</h5>
          </div>
          <p class="pr-5 mt-2">هذا النص هو مثفة إلى زيادة عدد الحروف التى يولدها التطبيق.</p>
          <b-button size="sm" class="py-2 px-5 rounded mr-5" type="button" variant="danger" >معرفة المزيد</b-button>

        </div>
        <div class="">
          <div class="d-flex">
            <img :src="require(`~/assets/icon/laptop.svg`)" class="icon">
            <h5 class="pr-3 mt-1 font-weight-bold"> تجميعات بصيغه بي دي اف</h5>
          </div>
          <p class="pr-5 mt-2">هذا النص هو مثفة إلى زيادة عدد الحروف التى يولدها التطبيق.</p>
          <b-button size="sm" class="py-2 px-5 rounded mr-5" type="button" variant="success" >معرفة المزيد</b-button>

        </div>
      </b-col>

      <b-col cols="12" sm="10"  md="8" lg="7">
       <div class="bg-img"></div>
      </b-col>

   </b-row>
  </b-container>
 </div>
</template>

<style scoped>
.logo{
  width: 55px;
  margin-left: 5px;
 }
 .logoText{
   display: flex;
   flex-direction: column;
   font-size: 10px;
 }
.bg-img{
  background-image: url('~/assets/img/Qudurat.png');
  background-position: center;
  /* background-clip: content-box; */
  background-repeat: no-repeat;
  background-size: contain;
  height: 500px;
}
@media (max-width:989px) {
  .bg-img{
    height: 400px;
  }
}
@media (max-width:767px) {
  .bg-img{
    height: 350px;
  }
}
@media (max-width:567px) {
  .bg-img{
    height: 300px;
  }
}


</style>
