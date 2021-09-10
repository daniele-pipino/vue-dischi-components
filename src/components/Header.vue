<template>
  <div>
    <header class="header d-flex justify-content-between align-items-center">
      <img src="@/assets/logo.png" alt="" class="" />
      <div class="p-2">
        <select
          v-model.trim="Searchedalbum"
          class="px-3"
          name=""
          id="filter"
          @change="$emit('findValue', Searchedalbum)"
        >
          <option value="All">All</option>
          <option value="Pop">Pop</option>
          <option value="Rock">Rock</option>
          <option value="Metal">Metal</option>
          <option value="Jazz">Jazz</option>
        </select>
      </div>
    </header>
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      Searchedalbum: "",
    };
  },
};
</script>

<style lang="scss">
header {
  height: 50px;
  background-color: grey;
  img {
    height: 50px;
  }
}
</style>