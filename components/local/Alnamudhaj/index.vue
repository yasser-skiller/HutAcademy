<template>
  <div class="mt-5 ">
    <h3 class="text-center my-4 font-weight-bold">نماذج اكاديمية الحوت</h3>
    <div  class="bg-img Alnamudhaj">
      <b-container>
        <div class="table-responsive-md">
          <table class="table table-borderless ">
            <thead class="mt-5">
              <tr>
                <th scope="col"></th>
                <th scope="col">اسم النموذج</th>
                <th scope="col">درجة النموذج</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <th scope="row"><img :src="require(`~/assets/icon/gold-medal.svg`)" alt="icon" class="icon"/></th>
                <td>الجبر والهندسة</td>
                <td class="GreenColorTabel"> 88%</td>
              </tr>
              <tr>
                <th scope="row"><img :src="require(`~/assets/icon/silver-medal.svg`)" alt="icon" class="icon"/></th>
                <td>اللغة العربية الفصحي</td>
                <td class="GreenColorTabel"> 99%</td>
              </tr>
              <tr>
                <th scope="row"><img :src="require(`~/assets/icon/bronze-medal.svg`)" alt="icon" class="icon"/></th>
                <td>الفلسفة وعلم الاجتماع</td>
                <td class="GreenColorTabel">98% </td>
              </tr>
              <tr>
                <th scope="row"></th>
                <td>الجبر والهندسة</td>
                <td class="GreenColorTabel">98% </td>
              </tr>
              <tr>
                <th scope="row"></th>
                <td>علم النفس</td>
                <td class="GreenColorTabel">98% </td>
              </tr>
            </tbody>
          </table>
        </div>

        <div class="d-flex justify-content-center">
          <b-button size="md" class="mx-auto py-2 px-5 rounded border-0 " > المزيد من النماذج</b-button>
        </div>
      </b-container>
    </div>
  </div>
</template>


<style scoped>

.bg-img{
  background-image: url('~/assets/img/alnamudhaj.png');
  background-position: center;
  background-clip: content-box;
  background-repeat: no-repeat;
  background-size: cover;
  height: 425px;
}
.bg-imgMode{
  background-color: var(--GrayColor);
  padding: 20px 0;
}
.bg-imgMode .table{
  color: var(--DarkWhiteColor) !important;
}
@media (max-width:989px) {
  .bg-img{
    height: 400px;
  }
}

@media (max-width:567px) {
  .bg-img{
    height: 450px;
  }
}
@media (max-width:400px) {
  .bg-img{
    height: 550px;
  }
}
.icon{
  width: 30px;
}
</style>
