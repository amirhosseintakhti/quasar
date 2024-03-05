<template>
  <q-page padding>
    <q-input v-model="message" />
  <h1>{{ message }}</h1>
  </q-page>
</template>

<script>
export default {
 setup(){
  const props= reactive({
    message:'salam'
  });

  return{
    ...torefs(props)
  }
 }
}
</script>
