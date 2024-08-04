<script>
export default {
  name: 'ChangeProfilePicture',
  emits: ['changeImage']
}
</script>

<template>
  <div>
    <button @click="$emit('changeImage')">Chande profile pic</button>
  </div>
</template>
