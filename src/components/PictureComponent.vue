<script>
import ChangeProfilePicture from './ChangeProfilePicture.vue'

export default {
  name: 'ProfilePicture',

  components: { ChangeProfilePicture },
  methods: {
    changeImage() {
      this.avatar =
        this.avatar === '/img/profile_cartoon.jpg' ? '/img/profile.jpg' : '/img/profile_cartoon.jpg'
    }
  },

  data() {
    return {
      avatar: '/img/profile.jpg',
      alt: 'Profile pic'
    }
  }
}
</script>

<template>
  <div>
    <img :src="avatar" style="width: 256px" :alt="alt" />
    <br />
    <ChangeProfilePicture @change-image="changeImage" />
  </div>
</template>
