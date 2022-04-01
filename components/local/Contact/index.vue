<template >
  <div id="Contact" class="bg-img-gradient">
      <b-container >
        <div class="d-flex flex-wrap">
          <div class="py-1 px-5 m-2 text-white Change bg-GreenColor">
            <p>الفورم رقم واحد</p>
          </div>
          <div class="inputStyle py-1 px-5 m-2 Change">
            <p>الفورم رقم اثنين</p>
          </div>
          <div class="inputStyle py-1 px-5 m-2 Change">
            <p>الفورم رقم ثلاثة</p>
          </div>
        </div>
        <b-row align-h="center" >
            <b-col cols="12" sm="10"  md="8" lg="6" class="px-4 py-5 WhiteColor">
              <h4 class="font-weight-bold">التواصل معنا</h4>
              <p class="line pb-4 mb-4">
                هذا النص هو مثال لنص يمكن أن يستبدل في نفس المساحة، لقد تم توليدزيادة عدد الحروف التى يولدها التطبيق.
              </p>
              <p>
                الفورم رقم واحد
              </p>
              <p>
                  هذا النص هو مثال لنص يمكن أن يستبدل في نفس المساحة، لقد تم توليد هذا النص من مولد النصأو العديد من النصوص الأخرى إضافة إلى زيادة عدد الحروف التى يولدها التطبيق.
              </p>
              <p>
                الفورم رقم اثنين
              </p>
              <p>
                  هذا النص هو مثال لنص يمكن أن يستبدل في نفس المساحة، لقد تم توليد هذا النص من مولد النصأو العديد من النصوص الأخرى إضافة إلى زيادة عدد الحروف التى يولدها التطبيق.
              </p>
              <p>
                الفورم رقم ثلاثة
              </p>
              <p>
                  هذا النص هو مثال لنص يمكن أن يستبدل في نفس المساحة، لقد تم توليد هذا النص من مولد النصأو العديد من النصوص الأخرى إضافة إلى زيادة عدد الحروف التى يولدها التطبيق.
              </p>
            </b-col>
            <b-col cols="12" sm="10"  md="8" lg="6" class="p-5">
              <b-form @submit="onSubmit" @reset="onReset" v-if="show" class="d-flex flex-column align-item-center">

                <b-form-group id="input-group-2"  label-for="input-2">
                  <img :src="require(`~/assets/icon/user.svg`)" alt="icon" class="icon"/>
                  <b-form-input
                    id="input-2"
                    class="inputStyle padding Change"
                    v-model="form.name"
                    placeholder="الأسم ...."
                    required
                  ></b-form-input>
                </b-form-group>

                <b-form-group
                  id="input-group-1"
                  label-for="input-1"
                >
                  <img :src="require(`~/assets/icon/phone-call.svg`)" alt="icon" class="icontwo"/>
                  <b-form-input
                    id="input-1"
                    class="inputStyle padding Change"
                    v-model="form.number"
                    type="number"
                    placeholder="رقم الهاتف ..."
                    required
                  ></b-form-input>
                </b-form-group>

                <b-form-group
                  id="input-group-3"
                  label-for="input-3"
                >
                  <img :src="require(`~/assets/icon/text.svg`)" alt="icon" class="iconthree"/>
                  <b-form-textarea
                    id="input-3"
                    class="inputStyle padding Change"
                    rows="8"
                    v-model="form.message"
                    placeholder=" نص الرسالة ..."
                    required
                  ></b-form-textarea>
                </b-form-group>
                <div class="d-flex justify-content-center">
                  <b-button class="rounded px-5" type="submit" variant="success">ارسال الان</b-button>
                </div>
              </b-form>
            </b-col>
        </b-row>
      </b-container>
  </div>
</template>


<script>
  export default {
    data() {
      return {
        form: {
          number: '',
          name: '',
          message: '',
        },
        show: true
      }
    },
    methods: {
      onSubmit(event) {
        event.preventDefault()
        alert(JSON.stringify(this.form))
      },
      onReset(event) {
        event.preventDefault()
        // Reset our form values
        this.form.number = ''
        this.form.name = ''
        this.form.message =''
        // Trick to reset/clear native browser form validation state
        this.show = false
        this.$nextTick(() => {
          this.show = true
        })
      }
    }
  }
</script>

<style scoped>
.bg-img-gradient{
  /* background-image: url('~/assets/img/Contact.png'); */
  /* background-color: #62AFCB; */
    background-image: linear-gradient(180deg,#2a92a2,#4774AC);
  /* background-position: center; */
  /* background-repeat: no-repeat; */
  /* background-size: cover; */
  /* height: 630px; */
}
/* @media (max-width:989px) {
  .bg-img{
    height: 1150px;
  }
}
@media (max-width:767px) {
  .bg-img{
    height: 1300px;
    background-position: inherit ;
  }
}
@media (max-width:567px) {
  .bg-img{
    height: 1350px;
  }
}
@media (max-width:400px) {
  .bg-img{
    height: 1500px;
  }
} */
.line{
  border-bottom: 2px #fff solid;
}
.padding{
  padding: 15px 50px 15px 9px !important;
  border-radius: 8px !important;
}
.inputStyle{
  background-color: var(--DarkWhiteColor);
}
.inputStyleMode{
  background-color: var(--GrayColor);
  border: none !important ;
  color: var(--DarkWhiteColor);
}
.icontwo{
  position: absolute;
  right: 60px;
  top: 112px;
}
.icon{
  position: absolute;
  right: 60px;
  top: 55px;
}
.iconthree{
  position: absolute;
  right: 60px;
  top: 175px;
}
</style>
