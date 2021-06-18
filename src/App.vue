<template>
  <div id="app">
    <header></header>
    <main>
      <div class="px-4 py-5 my-5 text-center">
        <h1 class="display-5 fw-bold">Briefingerator</h1>
        <div class="col-lg-6 mx-auto">
          <p class="lead mb-4">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
            ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
            aliquip ex ea commodo consequat.
          </p>
          <div class="d-grid gap-2 d-sm-flex justify-content-sm-center">
            <button
              v-on:click="showGenerator = true"
              type="button"
              class="btn btn-primary btn-lg px-4 gap-3"
            >
              Generate Briefing
            </button>
            <button
              type="button"
              class="btn btn-outline-secondary btn-lg px-4"
              disabled
            >
              Scan Media Plan
            </button>
          </div>
        </div>
      </div>

      <Generator v-if="showGenerator"></Generator>
    </main>
    <footer></footer>
  </div>
</template>

<script>
import Generator from "./components/Generator.vue";

export default {
  name: "App",
  components: { Generator },
  data() {
    return {
      showGenerator: false,
    };
  },
};
</script>
