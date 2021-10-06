<template>
    <div class="article-card w-50">
      <NuxtLink  :to= "`/products/${article.id}`">
        <div class="image-container w-25">
            <img :src="article.images_url[0]" alt="">
             <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Repellendus quam magni beatae possimus debitis.</p>
        </div>

      </NuxtLink>

        <div class="text-container" >

        </div>
    </div>
</template>

<script>
    export default {
        props: ['article'],
    }
</script>

<style scoped>

  .article-card {
  width: 31.5%;
  display: flex;
  flex-direction: row;
  height: 30rem;
  border: none;
  overflow: hidden;
  padding: 0;
  cursor: pointer;
  }

  .image-container {
    object-fit: cover;
    height: 65%;
    border-radius: 0.5rem;
  }
  .image-container:hover {
    transform: scale(.7);
  }

  .header {
    color: #111;
    font-size: 1.15rem;
    margin-top: 0.4rem;
  }
  a {
    text-decoration: none;
  }
  .snippet {
    color: grey;
  }


  @media(max-width:980px) {
  .card {
    width: 100%;
    }
    .image {
      width: 100%;
      object-fit: cover;
    }
  }
  @media(max-width:480px) {

    .image {
      width: 100%;
      object-fit: cover;
    }
  }

</style>
