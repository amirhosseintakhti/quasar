<template>
  <q-page padding>
    <div class="row q-gutter-md">
      <div class="col-1">
        <q-btn @click="counter> 0? counter --:'' " round icon="remove"></q-btn>
      </div>
      <div class="col"><q-input v-model="counter" label="counter" inputclass="text-center" ></q-input></div>
      <div class="col-1">
        <q-btn @click="counter ++" round icon="add"></q-btn>
      </div>
      <q-btn @click="$router.push('/about')" label="about"></q-btn>
    </div>
  </q-page>
</template>

<script>
import { onMounted } from "vue";
import { reactive,toRefs,ref } from "vue";
import { defineComponent } from "vue";

export default defineComponent({
  name: "IndexPage",
  setup(){
    const myVal = ref('hi')
    console.log(myVal.value + "|seted up|" +new Date);
    const props = reactive({
       counter:0
    });

    onMounted(()=>{
      console.log(myVal.value + "|onMounted|" + new Date);
    });
    // function minus(){
    //   props.counter > 0 ? props.counter -- :''
        
    // }
    // function plus(){
    //   props.counter ++
    // }
    return{
      ...toRefs(props)
      // minus,
      // plus
    }
  }
});
</script>
