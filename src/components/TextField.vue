<template>
  <div class="form__input__container">
    <input
      :type="type"
      class="form__input"
      autocomplete="off"
      placeholder=" "
    />
    <label for="" class="form__label">{{ label_text }}</label>
  </div>
</template>

<script setup>
defineProps({
  type: String,
  label_text: String,
});
</script>

<style scoped>
.form__input__container {
  position: relative;
  width: 20rem;
  height: 1rem;
}

.form__input {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: 2px solid #c1e5ee;
  border-radius: 0.5rem;
  font-family: inherit;
  color: white;
  outline: none;
  padding: 1.2rem;
  background: none;
}

.form__input:hover {
  border-color: #adffff;
}

.form__input:focus {
  border-color: #18ffff;
}

.form__label {
  position: absolute;
  left: 1rem;
  top: 0.8rem;
  padding: 0 0.5rem;
  color: white;
  cursor: text;
  transition: top 200ms ease-in, left 200ms ease-in, font-size 200ms ease-in;
  background-color: #004c66;
}

.form__input:focus ~ .form__label,
.form__input:not(:placeholder-shown).form__input:not(:focus) ~ .form__label {
  top: -0.5rem;
  font-size: 0.8rem;
  left: 0.8rem;
}
</style>
