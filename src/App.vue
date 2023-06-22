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
  <section id="over-flow" class="wrapper pt-4 px-5">



    <div class="container-fluid  fs-5 ">

      <div class="btn card record px-4 py-3 my-4" v-for="(item, index) in store.array" :key="index">
        <a :href="item.link">
          {{ item.name }}
        </a>
      </div>

      <!-- <div class="btn card record px-4 py-3 my-4" v-for="(item, index) in store.array" :key="index">
        <a :href="item.link">
          {{ item.name }}
        </a>
      </div> -->

    </div>




  </section>
</template>

<style lang="scss">
#over-flow {
  overflow-y: auto;
}
</style>
