<template>
  <div>
    <!-- <navigation /> -->


    <div class="container">
      <h1>News To Know </h1>
      <lgcarddisplay
        v-for="cardinfo in lgcardinfo.slice(0,3)"
        :key="cardinfo.id"
        :cardssection="cardinfo"
      />


    </div>
  </div>
</template>

<script>
import { lgcardsections } from "@/assets/data.js";

// import navigation from "../components/nav.vue";

export default {
  // components: {navigation},


  data() {
    return {
      lgcardinfo: lgcardsections,

    };
  },
};
</script>
<style  scoped>
  h1 {
    display: flex;
    justify-content: center;
    padding-top: 2rem;
  }

</style>


