<script>
import { store } from '../store';

export default {
  name: "App",

  data() {
    return {
      store,
    }
  }
}
</script>

<template>
  <section class="wrapper p-4">



    <div class="container-fluid">

      <div class="btn card record px-4 py-3 my-4" v-for="(item, index) in store.array" :key="index">
        <a class="fs-5" :href="item.link">
          {{ item.name }}
        </a>
      </div>

      <!-- <div class="btn card record px-4 py-3 my-4" v-for="(item, index) in store.array" :key="index">
        <a class="fs-5" :href="item.link">
          {{ item.name }}
        </a>
      </div> -->

    </div>




  </section>
</template>

<style lang="scss" scoped></style>
