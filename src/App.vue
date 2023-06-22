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
  <section class="wrapper p-2">
    <div id="over-flow" class="container-fluid my-5 py-3 fs-5 mx-4 px-4">

      <div class="btn card record px-4 py-3 my-4" v-for="(item, index) in store.array" :key="index">
        <a :href="item.link">
          {{ item.name }}
        </a>
      </div>

    </div>
  </section>
</template>

<style lang="scss">
#over-flow {
  overflow-y: hidden;
}
</style>
