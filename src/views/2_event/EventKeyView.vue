<template>
  <div>
    <!-- <input type="search" name="" id="" @keyup="checkEnter($event)" v-model="searchText"> -->
    <input type="search" name="" id="" @keyup.enter="checkEnter($event)" v-model="searchText">
    <button @click="doSearch">조회</button>
    <button type="submit" @click.prevent="doSearch">Submit</button>
  </div>
</template>
<script>
// .stop - event.stopPropagation()
// .prevent - event.preventDefault()
export default {
  components: {},
  data() {
    return {
      searchText: ''
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    doSearch() {
      console.log(this.searchText)
    },
    checkEnter(event) {
      // if (event.keyCode === 13) {
      //   this.doSearch()
      // }
      this.doSearch()
    }
  }
}
</script>
