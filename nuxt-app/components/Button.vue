<script setup></script>

<template>
  <button class="button">
    <slot></slot>
  </button>
</template>

<style lang="scss" scoped>
.button {
  background-color: #9fcbaa;
  border: none;
  color: black;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  border-radius: 16px;
  font-family: "Courier New", Courier, monospace;
}

.button:hover {
  background-color: #1c3422;
  color: white;
  cursor: pointer;
}
</style>
