<template>
<NuxtLink :to= "`/products/${card.id}`" class="card ">
  <img :src="require(`@/assets/images/${card.image }`)" alt="" class="image">
  <div>
    <h3 class="header">
    {{card.title}}
  </h3>
  <p class="snippet">
    {{card.snippet}}
  </p>
  </div>
</NuxtLink>
</template>

<script>
export default {
  props : ['card']

}
</script>

<style  scoped>
.card {
  width: 31.5%;
  height: 30rem;
  border: none;
  overflow: hidden;
  padding: 0;
  cursor: pointer;
}

.image {
  object-fit: cover;
  height: 65%;
  border-radius: 0.5rem;
}
.image:hover {
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

