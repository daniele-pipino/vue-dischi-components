<template>
  <div>
    <main>
      <div class="container">
        <div class="row">
          <div v-for="(album, index) in albums" :key="index" class="col-3">
            <Album :album="album" />
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<script>
import axios from "axios";
import Album from "@/components/Album.vue";
export default {
  data() {
    return {
      albums: "",
    };
  },
  name: "Main",
  components: {
    Album,
  },
  created() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((res) => {
        this.albums = res.data.response;
      });
  },
};
</script>

<style lang="scss">
</style>