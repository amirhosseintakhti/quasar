<template>
  <q-page padding>
      <div v-for="(message, index) in messages" :key="'message-' + index">
        {{ message.fullName }}|{{ message.email }}<br />
        {{ message.topic }}<br />
        {{ message.message }}
        <hr />
      </div>
  </q-page>
</template>

<script>
import axios from "axios";
import { ref, defineComponent } from "vue";

export default defineComponent({
  name: "IndexPage",
  setup() {
    const messages = ref([]);
    function fetchMessages() {
      axios.get("http://localhost:8000/api/contact").then((r) => {
        console.log(r.data);
        messages.value = r.data.messages;
      });
    }
    fetchMessages();
    return {
      messages,
    };
  },
});
</script>
