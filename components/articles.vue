<template>
  <div>
    <!-- <h3>Articles</h3> -->
     <div>
       <articlecard
        v-for="article in articles.articles"
        :key="article.id"
        :article="article"
        />
    </div>
  </div>

</template>

<script>
import Articlecard from '@/components/Articlecard.vue';
export default {
  components: { Articlecard },
  data() {
    return {
      articles: []
    }
  },
  async fetch() {
    this.articles = await fetch(
      'https://nk-studio-api.herokuapp.com/api/v1/articles/'
    ).then(res => res.json())
  }

}
</script>

<style scoped>
  .header {
    display: flex;
    justify-content: center;
    margin-top: 70px;
    font-weight: 700;
    font-size: 1.5rem;
  }
  .snippet {
    display: flex;
    justify-content: center;
    color: grey;
    margin-bottom: 1rem;

  }
  .cards-container {

    display: flex;
    justify-content: space-between;
  }
  @media (max-width:980px) {
    .cards-container {
      flex-direction: column;
    }
  }
  @media (max-width:480px) {
    .cards-container {
      flex-direction: column;
    }
  }
</style>
