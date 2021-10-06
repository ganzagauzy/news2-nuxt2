<template>
  <div>
     <!-- <navigation /> -->

      <h1>
        News To Know
      </h1>
     <lgcarddisplay
        v-for="cardinfo in lgcardinfo.slice(0,3)"
        :key="cardinfo.id"
        :cardssection="cardinfo"
      />

      <articles />



  </div>
</template>

<script>
import { lgcardsections } from "@/assets/data.js";
import Articles from '/components/Articles.vue';


// import navigation from "@/components/nav.vue";
export default {
  components: { Articles },

  // components: {  navigation },

   data() {
    return {
      lgcardinfo: lgcardsections,

    };
  },

}
</script>

<style scoped>
  h1 {
    display: flex;
    justify-content: center;
    padding-top: 2rem;
  }
</style>




