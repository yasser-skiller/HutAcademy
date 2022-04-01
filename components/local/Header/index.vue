<template>
  <div class="bg-img">
    <h1 class="my-4 font-weight-bold">
      اكاديمية الحوت
    </h1>
    <p class="mt-2 px-5 text-center">
      هذا النص هو مثال لنص يمكن أن يستبدل في نفس المساحة ق.
    </p>
     <p class="px-5 text-center">
   في نفس ال تم توليد هذا النص من مولد النصأو العديد من النصوص الأخرى إضافة إلى زيادة عدد الحروف التى يولدها التطبيق.
    </p>
    <div class="d-flex flex-wrap mt-4 justify-content-center">
        <b-button size="sm" class="my-2 my-sm-2 mx-2 py-2 px-5 rounded" type="button" variant="primary" >تسجيل دخول</b-button>
        <b-button size="sm" class="my-2 my-sm-2 mx-2 py-2 px-5 rounded" type="button" variant="success">انشاء حساب</b-button>
    </div>
    <b-form
       @submit="onSubmit"
       @reset="onReset"
       v-if="show"
       class="formParent  d-flex flex-wrap align-items-center justify-content-around shadow p-2 rounded w-75"
      >

        <b-form-group id="input-group-2"  class="mb-0"  label-for="input-2">
          <b-form-input
            id="input-2"
            class="inputStyle inputStyleModeTwo"
            v-model="form.TextOne"
            placeholder="بحث عن النص الأول ..."
            required
          ></b-form-input>
        </b-form-group>

        <b-form-group
          id="input-group-1"
          label-for="input-1"
          class="mb-0"
        >
          <b-form-input
            id="input-1"
            class="inputStyle inputStyleMode"
            v-model="form.TextTwo"
            placeholder="بحث عن النص الثاني ..."
            required
          ></b-form-input>
        </b-form-group>

          <b-button class="rounded px-5" type="submit" variant="success"> ابحث الان</b-button>
    </b-form>

  </div>
</template>

<script>
  export default {
    data() {
      return {
        form: {
          TextOne: '',
          TextTwo: '',
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
        this.form.TextOne = ''
        this.form.TextTwo = ''
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
.bg-img{
  position: relative;
  background-image: url('~/assets/img/header.png');
  background-position: center;
  background-clip: content-box;
  background-repeat: no-repeat;
  background-size: cover;
  height: 95vh;
  color: var(--WhiteColor);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.formParent{
  position: absolute;
  bottom: -10px;
  background-color: var(--WhiteColor);
}
.inputStyle{
  width: 350px;
  background-color: var(--WhiteColor);
}
.formParentMode .btn-success{
  border-color: var(--BlueColor) !important;
  background-image: linear-gradient(90deg,#3D6F77,#3C6292) !important;

}
@media (max-width:1200px) {
  .inputStyle{
    width: 250px;
  }
}
@media (max-width:967px) {
  .inputStyle{
    width: 200px;
  }
}

@media (max-width:780px) {
  .inputStyle{
    margin-bottom: 10px;
  }
}

@media (max-width:558px) {
  .inputStyle{
    width: 280px;
  }
  .formParent{
   position: absolute;
   bottom: -60px;
  }
}

@media (max-width:400px) {
  .bg-img{
   height: 120vh;
  }
  .inputStyle{
    width: 200px;
  }
  .formParent{
   position: absolute;
   bottom: -40px;
  }
}
@media (max-width:350px) {
  .formParent{
   position: absolute;
   bottom: -55px;
  }
}
</style>
