<template>
  <div>
    <main>
      <div class="container">
        <div class="row m-5 g-2">
          <div class="col-3">
            <Album />
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<script>
import Album from "@/components/Album.vue";
export default {
  name: "Main",
  components: {
    Album,
  },
};
</script>

<style lang="scss">
main {
  height: 100vh;
  background-color: green;
}
</style>