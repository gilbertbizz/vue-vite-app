<template>
  <div class="container space-y-10">
    <div>
      <TextField type="text" label_text="Email" />
    </div>
    <div>
      <TextField type="password" label_text="Password" />
    </div>
  </div>
</template>

<script setup>
import TextField from "../components/TextField.vue";
</script>

<style>
* {
  background-color: #004c66;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
