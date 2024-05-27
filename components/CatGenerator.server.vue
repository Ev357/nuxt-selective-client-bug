<script setup lang="ts">
import type Bun from "bun";

// @ts-ignore
const file = Bun.file("./data/cats.txt");
const cats = (await file.text()).split("\n");

const randomCat = cats[Math.floor(Math.random() * cats.length)];
</script>

<template>
  <div>
    <RevealButton nuxt-client :cat-name="randomCat" />
  </div>
</template>
