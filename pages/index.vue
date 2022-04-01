<template>
 <div>
    <div class="containerMode">
      <div class="darkMode"></div>
    </div>
    <AppNav/>
    <Header/>
    <WE/>
    <Qudurat/>
    <Tahasuli/>
    <Alnamudhaj/>
    <Contact/>
    <LastNews/>
 </div>
</template>

<script>
import AppNav from '@/components/Global/AppNav';
import Header from '@/components/local/Header';
import WE from '@/components/local/WE';
import Qudurat from '@/components/local/Qudurat';
import Tahasuli from '@/components/local/Tahasuli';
import Alnamudhaj from '@/components/local/Alnamudhaj';
import Contact from '@/components/local/Contact';
import LastNews from '@/components/Global/LastNews';

export default {
  components:{
    AppNav,
    Header,
    WE,
    Qudurat,
    Tahasuli,
    Alnamudhaj,
    Contact,
    LastNews,
  },
}
</script>
