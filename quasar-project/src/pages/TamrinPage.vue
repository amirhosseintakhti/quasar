<template>
  <q-page padding>
    <div>{{ message }}</div>
  </q-page>
</template>

<script>
export default {
 setup(){
  const message = 'salam';

  return{
    message
  }
 }
}
</script>
