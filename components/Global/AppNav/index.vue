<template>
    <b-navbar toggleable="lg"  class="nav" >

    <b-navbar-brand href="#">
      <div  class="d-flex align-items-center">
        <img :src="require(`~/assets/icon/logo.svg`)" class="logo" alt="icon"/>
        <div class="logoText">
          <span>أكاديمية الحوت</span>
          <span>Alhut Academy</span>
        </div>
      </div>
    </b-navbar-brand>
    <div v-if="ModeCase === true" class="d-lg-block d-none">
        <b-button
          size="sm"
          v-on:click="handelMode(!ModeCase)"
          class="my-2 my-sm-2 mr-3 py-1 px-3 rounded WhiteColor"
          type="button"
          variant="outline-primary"
        >
          <img :src="require(`~/assets/icon/mode.svg`)" class="ml-2" alt="icon">
          نهاري
        </b-button>
    </div>

    <div v-if="ModeCase === false" class="d-lg-block d-none">
        <b-button
          size="sm"
          v-on:click="handelMode(!ModeCase)"
          class="my-2 my-sm-2 mr-3 py-1 px-3 rounded"
          type="button"
          variant="outline-primary"
        >
          <img :src="require(`~/assets/icon/sleep-mode.svg`)" class="ml-2" alt="icon">
          ليلي
        </b-button>
    </div>


    <div v-if="ModeCase === true" class="change">
      <b-navbar-toggle target="nav-collapse">
        <span class="NavIcon"></span>
      </b-navbar-toggle>
    </div>
     <div v-if="ModeCase === false" >
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
    </div>

    <b-collapse id="nav-collapse" class="justify-content-around" is-nav>


      <b-navbar-nav class=" NavBar text-center justify-content-around w-70  align-items-center">
        <NuxtLink  to="/" tag="li" exact class="nav-link">الرئيسية</NuxtLink >
        <NuxtLink to="#WE" class="nav-link"> من نحن</NuxtLink>
        <NuxtLink to="#Qudurat" class="nav-link">قدرات</NuxtLink>
        <NuxtLink to="#Tahasuli" class="nav-link">تحصيلي</NuxtLink>
        <NuxtLink to="#Contact" class="nav-link">الدعم الفني</NuxtLink>
        <NuxtLink to="#LastNews" class="nav-link"> اخر الاخبار</NuxtLink>
      </b-navbar-nav>

      <b-navbar-nav class="pr-0">
        <div v-if="ModeCase === true" class="d-lg-none">
        <b-button
          size="sm"
          v-on:click="handelMode(!ModeCase)"
          class="my-2 my-sm-2 mr-3 py-1 px-3 rounded WhiteColor"
          type="button"
          variant="outline-primary"
        >
          <img :src="require(`~/assets/icon/mode.svg`)" class="ml-2" alt="icon">
          نهاري
        </b-button>
        </div>

        <div v-if="ModeCase === false" class="d-lg-none">
        <b-button
          size="sm"
          v-on:click="handelMode(!ModeCase)"
          class="my-2 my-sm-2 mr-3 py-1 px-3 rounded"
          type="button"
          variant="outline-primary"
        >
          <img :src="require(`~/assets/icon/sleep-mode.svg`)" class="ml-2" alt="icon">
          ليلي
        </b-button>
        </div>
        <b-button size="sm" class="my-2 my-sm-2 mx-2 py-2 px-4 rounded" type="button" variant="primary" >تسجيل دخول</b-button>
        <b-button size="sm" class="my-2 my-sm-2 mx-2 py-2 px-4 rounded" type="button" variant="success">انشاء حساب</b-button>
      </b-navbar-nav>

    </b-collapse>

    </b-navbar>
</template>

<script>
export default {
data() {
    return {
      ModeCase: false,
    };
  },
  methods: {
    handelMode: function (Case) {
      this.ModeCase = Case;
      document.querySelector(".darkMode").classList.toggle('active');
      // document.querySelector('.NavBar').classList.toggle('NavBarMode');
      document.querySelector('.formParent').classList.toggle('formParentMode');
      document.querySelector('.bg-imgWE').classList.toggle('imgMode');

      if(Case === true){
        document.querySelector('body').style.backgroundColor = 'var(--DarkGrayColor)';
        document.querySelector('body').style.color = 'var(--WhiteColor)';
        // document.querySelector('.NavBar').classList.add('NavBarMode');
        document.querySelector('.bg-img-gradient').style.backgroundImage = 'linear-gradient(180deg,#2D727D,#1E324A)';
        document.querySelector('.btn-secondary').style.backgroundImage = 'linear-gradient(90deg,#3D6F77,#3C6292)';
        document.querySelector('#WE').classList.remove('fill');
        document.querySelector('.Alnamudhaj').classList.toggle('bg-img');
        document.querySelector('.Alnamudhaj').classList.toggle('bg-imgMode');
        document.querySelector('.logoText').style.color = '#fff';
        document.documentElement.style.setProperty('--GreenColorTabel', '#63C48A');
        document.documentElement.style.setProperty('--BlueColor', '#2d6375');
        document.documentElement.style.setProperty('--DarkWhiteSceColor', '#d4d4d4');
        document.documentElement.style.setProperty('--GrayNaveActive', '#ffffff');
        document.documentElement.style.setProperty('--GrayNave', '#94969A');
        document.documentElement.style.setProperty('--GreenColor', '#306B48');
        document.documentElement.style.setProperty('--OrangeColor', '#CC5429');
        document.querySelector('.formParent').style.backgroundColor = 'var(--GrayColor)';
        document.querySelector('.inputStyleModeTwo').style.backgroundColor = 'var(--DarkGrayColor)';
        document.querySelector('.inputStyleMode').style.backgroundColor = 'var(--DarkGrayColor)';
        document.querySelector('.inputStyleModeTwo').style.border = 'none';
        document.querySelector('.inputStyleMode').style.border = 'none';
        document.querySelectorAll('.Change').forEach(element => {
          element.classList.toggle('inputStyle');
          element.classList.toggle('inputStyleMode');
        });
      }else{
        document.querySelector('body').style.backgroundColor = 'var(--WhiteColor)';
        document.querySelector('body').style.color = 'var(--BlackColor)';
        document.documentElement.style.setProperty('--GreenColorTabel', '#48AB70');
        // document.querySelector('.NavBar').classList.remove('NavBarMode');
        document.querySelector('.bg-img-gradient').style.backgroundImage = 'linear-gradient(180deg,#2D727D,#1E324A)';

        document.querySelector('.btn-secondary').style.backgroundImage = 'linear-gradient(90deg,#2a92a2,#4677AD)';
        document.querySelector('#WE').classList.add('fill');
        document.querySelector('.Alnamudhaj').classList.toggle('bg-img');
        document.querySelector('.Alnamudhaj').classList.toggle('bg-imgMode');
        document.querySelector('.logoText').style.color = '#000';
        document.documentElement.style.setProperty('--BlueColor', '#37B9CE');
        document.documentElement.style.setProperty('--GreenColor', '#48AB70');
        document.documentElement.style.setProperty('--OrangeColor', '#FF6B35');
        document.documentElement.style.setProperty('--DarkWhiteSceColor', '#000');
        document.documentElement.style.setProperty('--GrayNaveActive', '#363848');
        document.documentElement.style.setProperty('--GrayNave', '#868891');
        document.querySelector('.formParent').style.backgroundColor = 'var(--WhiteColor)';
        document.querySelector('.inputStyleModeTwo').style.backgroundColor = 'var(--WhiteColor)';
        document.querySelector('.inputStyleMode').style.backgroundColor = 'var(--WhiteColor)';
        document.querySelector('.inputStyleModeTwo').style.border = '1px solid #ced4da';
        document.querySelector('.inputStyleMode').style.border = '1px solid #ced4da';
        document.querySelectorAll('.Change').forEach(element => {
          element.classList.toggle('inputStyle');
          element.classList.toggle('inputStyleMode');
        });


      }
    }
  }

};

</script>

<style scoped>
 .nav{
  border-bottom: 2px solid var(--mainColor);
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
 .nav-link{
  color: var(--GrayNave) !important;
  cursor: pointer;
 }
 .nav-link:hover{
  color: var(--BlackColor) !important;
 }
 .nuxt-link-active{
   color: var(--GrayNaveActive) !important;
   position: relative;
   display: flex;
   flex-direction: column;
   align-items: center;
 }
 .NavBar .nuxt-link-active::after{
   content: url('~/assets/icon/whale.svg');
   position: absolute;
   bottom: -20px;
 }

.NavIcon{
  background-image: url('~/assets/img/menu.png') !important;
  width: 40px;
    height: 40px;
    background-size: contain;
    display: flex;
}
</style>
