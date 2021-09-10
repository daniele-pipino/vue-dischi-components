<template>
  <div>
    <main>
      <div class="container">
        <div class="row">
          <div
            v-for="(album, index) in filteredAlbums"
            :key="index"
            class="col-3 m-0"
          >
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
      albums: [],
    };
  },
  name: "Main",
  props: ["selectValue"],
  components: {
    Album,
  },
  methods: {},
  computed: {
    filteredAlbums() {
      if (!this.selectValue) return this.albums;
      const searchTerm = this.selectValue.toLowerCase();
      return this.albums.filter((album) =>
        album.genre.toLowerCase().includes(searchTerm)
      );
    },
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