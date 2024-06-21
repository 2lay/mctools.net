<template>
  <textarea :placeholder="taPlaceholder" :name="taName" :cols="taCols" :rows="taRows" v-model="text"></textarea>
</template>

<script>
export default {
  name: 'MctTextArea',
  props: {
    taName: {
      type: String,
      required: true
    },
    taCols: {
      type: String,
      required: true
    },
    taRows: {
      type: String,
      required: true
    },
    taText: {
      type: String,
      required: true
    },
    taPlaceholder: {
      type: String,
      required: true
    },
  },
  data() {
    return {
      text: this.taText  // init the text prop
    };
  }
}
</script>

<style scoped>
textarea {
  border-radius: 9px;
  font-size: 16px;
  transition: background-color 0.2s, transform 0.05s, box-shadow 0.1s, border 0.2s;
  outline: none;
}


textarea {
  border: 1px solid #252529;
  color: white;
  background-color: #161618;
  padding: 5px 15px;
}

textarea:focus {
  border-color: var(--primary);
}
</style>
