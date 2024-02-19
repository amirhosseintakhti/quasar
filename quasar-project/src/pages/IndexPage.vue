<template>
  <q-page padding>
    <div class="row q-gutter-md">
      <div class="col-1">
        <q-btn round icon="remove"></q-btn>
      </div>
      <div class="col"><q-input v-model="props.counter" label="counter" inputclass="text-center" ></q-input></div>
      <div class="col-1">
        <q-btn round icon="add"></q-btn>
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
       counter:0;
    })
    return{
      props
    }
  }
});
</script>
