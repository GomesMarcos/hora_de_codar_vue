<script>
const valueArg = ''

export default {
  name: 'InputText',
  props: {
    value: valueArg
  }
}
</script>

<template>
  <input
    style="margin-bottom: 1em"
    class="form-control"
    v-model="valueArg"
    type="text"
    name=""
    id=""
    :value="valueArg"
  />
</template>
