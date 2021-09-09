<template>
  <div class="album-card text-center">
    <img :src="album.poster" alt="album.title" class="img-fluid" />
    <p class="m-0 title">{{ album.title }}</p>
    <p class="m-0 artist">{{ album.author }}</p>
    <p class="m-0 year">{{ album.year }}</p>
  </div>
</template>

<script>
export default {
  name: "Album",
  props: ["album"],
};
</script>

<style lang="scss">
.album-card {
  margin: 3px;
  padding: 5px;
  width: 200px;
  height: 300px;
  background-color: rgb(43, 58, 75);
  padding: 5px;
  p {
    color: grey;
  }
  .title {
    color: antiquewhite;
  }
  img {
    width: 100%;
  }
}
</style>