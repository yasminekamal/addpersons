<template>
  <div class="container">
    <div class="row mt-2 ">
      <div class="col">
        <Header></Header>
      </div>
    </div>
    <div class="row mt-2" >
      <div class="col-4">
        <Aside></Aside>
      </div>
      <div class="col-8 overflow-auto" style="height:500px">
        <Main></Main>
      </div>
    </div>
    <div class="row mt-5">
      <div class="col">
        <Footer></Footer>
      </div>
    </div>
  </div>
</template>

<script>
import Header from "./components/headerComponent.vue";
import Aside from "./components/asideComponent.vue";
import Main from "./components/mainComponent.vue";
import Footer from "./components/footerComponent.vue";

export default {
  
  components: {
    Header,
    Aside,
    Main,
    Footer,
  },
};
</script>