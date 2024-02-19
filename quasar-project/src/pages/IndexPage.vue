<template>
  <q-page padding>
    <div class="row q-gutter-md">
      <div class="col-1">
        <q-btn @click="minus " round icon="remove"></q-btn>
      </div>
      <div class="col"><q-input v-model="props.counter" label="counter" inputclass="text-center" ></q-input></div>
      <div class="col-1">
        <q-btn @click="plus" round icon="add"></q-btn>
      </div>
    </div>
  </q-page>
</template>

<script>
import { reactive } from "vue";
import { defineComponent } from "vue";

export default defineComponent({
  name: "IndexPage",
  setup(){
    const props = reactive({
       counter:0
    })
    function minus(){
      if(props.counter>0){
        props.counter --
      }
      
    }
    function plus(){
      props.counter ++
    }
    return{
      props,
      minus,
      plus
    }
  }
});
</script>
