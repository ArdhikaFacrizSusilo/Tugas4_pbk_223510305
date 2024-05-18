<template>
    <div class="grandchild">
      <h3>Tekan Button Berikut</h3>
      <button @click="sendMessageToParent">Send Message to Parent</button>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      sendMessageToParent() {
        this.$emit('message-from-grandchild', 'Hubungi saya, noTelp : 081388822887, Instagram : ardhikafacriz');
      },
    },
  };
  </script>
  
  <style scoped>
  .grandchild {
    padding: 10px;
    background-color: #EEF7FF;
    border: 1px solid #bbb;
    border-radius: 5px;
    margin-top: 10px;
  }
  button {
    padding: 5px 10px;
    border: none;
    border-radius: 3px;
    background-color: #007bff;
    color: white;
    cursor: pointer;
  }
  button:hover {
    background-color: #0056b3;
  }
  </style>
  