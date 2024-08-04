<script>
export default {
  name: 'ProfilePicture',

  data() {
    return {
      avatar: '/img/profile.jpg',
      alt: 'Profile pic'
    }
  }
}
</script>

<template>
  <img :src="avatar" style="width: 256px" :alt="alt" />
</template>
