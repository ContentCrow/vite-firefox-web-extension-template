<template>
  <img :src="imageUrl" height="45" alt="" class="w-10 h-10" /> <!-- tailwindcss test -->
  <h1 class="m-2">
    <slot></slot>
  </h1>
  <button class="mt-5" type="button" @click="increment">Clicks: {{ count }}</button>
  <svg-icon type="mdi" :path="path"></svg-icon> <!-- icon test-->
</template>

<script>
import logo from "~/assets/logo.svg";
import SvgIcon from '@jamescoyle/vue-icon';
import { mdiAccount } from '@mdi/js';
export default {
  components: {
    SvgIcon
  },
  data() {
    return {
      imageUrl: new URL(logo, import.meta.url).href,
      count: 0,
      path: mdiAccount
    };
  },
  methods: {
    increment() {
      this.count += 1;
    },
  }

};
</script>

<style></style>
