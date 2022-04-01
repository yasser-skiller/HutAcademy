<template>
  <div  id="LastNews" class="bg-color">
    <b-container>
      <b-row align-h="center"  class="WhiteColor p-5">
        <b-col cols="12" sm="10"  md="6" lg="4" class="mt-3 d-flex flex-column justify-content-center align-items-center">
          <p>التواصل الاجتماعي</p>
          <div class="d-flex">
            <div class="d-flex flex-column mt-3">
             <img :src="require(`~/assets/icon/face.svg`)" alt="icon" class="my-2 socialIcon"/>
             <img :src="require(`~/assets/icon/youtube.svg`)" alt="icon" class="my-2 socialIcon"/>
             <img :src="require(`~/assets/icon/tiwter.svg`)" alt="icon" class="my-2 socialIcon"/>
            </div>
            <div class="d-flex flex-column mt-3 mr-4">
             <img :src="require(`~/assets/icon/linked.svg`)" alt="icon" class="my-2 socialIcon"/>
             <img :src="require(`~/assets/icon/ta.svg`)" alt="icon" class="my-2 socialIcon"/>
            </div>
          </div>

        </b-col>
        <b-col cols="12" sm="10"  md="6" lg="4" class="mt-3 d-flex flex-wrap justify-content-around align-items-center">
            <div class="text-center">
            <p>عنوان واحد</p>
            <ul>
              <li>رابط واحد</li>
              <li>رابط واحد</li>
              <li>رابط واحد</li>
              <li>رابط واحد</li>
              <li>رابط واحد</li>
              <li>رابط واحد</li>
              <li>رابط واحد</li>

            </ul>
          </div>
            <div class="text-center">
            <p>عنوان ثاني</p>
            <ul>
              <li>رابط واحد</li>
              <li>رابط واحد</li>
              <li>رابط واحد</li>
              <li>رابط واحد</li>
              <li>رابط واحد</li>
              <li>رابط واحد</li>
              <li>رابط واحد</li>

            </ul>
          </div>
        </b-col>
        <b-col cols="12" sm="10"  md="6" lg="4" class="mt-3 d-flex flex-column justify-content-center align-items-center">
          <img :src="require(`~/assets/icon/whiteLogo.svg`)" alt="icon">
          <p class="mt-3 text-center">هذا النص هو مثال لنص يمكن أن يستبدل في نفس المساحة، لقد تم توليد هذا النص من مولد النصأو العديد </p>
        </b-col>

      </b-row>
    </b-container>
  </div>
</template>

<style scoped>
.bg-color{
  background-color: var(--GrayColor);
}
.socialIcon{
  width: 30px;
}
</style>
