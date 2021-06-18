<template>
  <div id="generator" class="generator">
    <div class="container generator--container">
      <header class="d-flex justify-content-between align-items-center">
        <h4 class="fw-bold">Generate Briefing</h4>
        <x-icon></x-icon>
      </header>
      <main class="generator--main">
        <div
          class="generator--controls generator--controls-left d-flex justify-content-between align-items-center"
        >
          <arrow-left-icon></arrow-left-icon>
        </div>
        <div class="generator--steps">

        <component v-bind:is="steps[step]"></component>
        </div>
        <div
          class="generator--controls generator--controls-right d-flex justify-content-between align-items-center"
        >
          <arrow-right-icon></arrow-right-icon>
        </div>
      </main>
    </div>
  </div>
</template>

<script>
import { ArrowLeftIcon, ArrowRightIcon, XIcon } from "vue-feather-icons";
import StepMeta from "@/components/steps/StepMeta";

export default {
  name: "Generator",
  components: {
    ArrowLeftIcon,
    ArrowRightIcon,
    XIcon,
    StepMeta,
  },
  data() {
    return {
      step: 0,
      steps: ["StepMeta"]
    };
  },
};
</script>

<style lang="less">
.generator {
  position: absolute;
  width: 100vw;
  height: 100vh;
  top: 0px;
  left: 0;
  background-color: #353535;
  color: #fff;

  &--main {
    display: grid;
    grid-template-columns: 80px 1fr 80px;
  }
}
</style>
