<template>
  <textarea :placeholder="taPlaceholder" :name="taName" :cols="taCols" :rows="taRows" v-model="text" @keypress="handleKeyPress"></textarea>
</template>

<script>
export default {
  name: 'MctTextArea',
  props: {
    taName: {
      type: String,
      required: true
    },
    taText: {
      type: String,
      required: true
    },
    taCols: {
      type: Number,
      required: true
    },
    taRows: {
      type: Number,
      required: true
    },
    taPlaceholder: {
      type: String,
      required: true
    },
    taHardLimit: {
      type: Boolean,
      required: false,
      default: false
    },
  },
  data() {
    return {
      text: this.taText, 
      maxRows: this.taHardLimit ? this.taRows : undefined

    };
  },
  methods: {
    handleKeyPress(event) {
      if (event.which === 13) {
        let numberOfLines = this.text.split('\n').length;
        if (numberOfLines >= this.maxRows) {
          event.preventDefault();
        }
      }
    }
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
  resize: none;
}

textarea:focus {
  border-color: var(--primary);
}
</style>
