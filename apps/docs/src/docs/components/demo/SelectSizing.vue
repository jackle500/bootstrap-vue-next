<template>
  <BFormSelect
    v-model="selected"
    :options="ex1Options"
    :select-size="4"
  />

  <div class="mt-3">
    Selected: <strong>{{ selected }}</strong>
  </div>
</template>

<script setup lang="ts">
import {ref} from 'vue'

const ex1Options = [
  {value: null, text: 'Please select an option'},
  {value: 'a', text: 'This is First option'},
  {value: 'b', text: 'Selected Option'},
  {value: {C: '3PO'}, text: 'This is an option with object value'},
  {value: 'd', text: 'This one is disabled', disabled: true},
]

const selected = ref()
</script>
