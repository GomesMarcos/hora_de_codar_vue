<script>
import FormComponent from './form/Form.vue'
import Info from './Info.vue'
import PictureComponent from './Picture.vue'

export default {
  components: { Info, FormComponent, PictureComponent },
  name: 'PersonComponent',

  data() {
    return {
      name: 'Marcos',
      emai: 'qwe@asd.zxc'
    }
  }
}
</script>

<template>
  <div>
    <PictureComponent></PictureComponent>
    <h2>The person name's is: {{ name }}</h2>
    <Info :email="emai" />
    <FormComponent />
  </div>
</template>
