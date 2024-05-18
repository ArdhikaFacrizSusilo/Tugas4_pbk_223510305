<template>
    <div class="parent">
      <h1>Welcome to Website</h1>
      <p>{{ message }}</p>
      <ChildComponent @message-from-child="handleMessageFromChild">
        <template v-slot:additionalContent>
          <p>Ardhika Facriz Susilo | 223510305 | 4D</p>
        </template>
      </ChildComponent>
    </div>
  </template>
  
  <script>
  import ChildComponent from './ChildComponent.vue';
  
  export default {
    components: {
      ChildComponent,
    },
    data() {
      return {
        message: 'Tidak Ada Pesan Yang Masuk.',
      };
    },
    methods: {
      handleMessageFromChild(payload) {
        this.message = payload;
      },
    },
  };
  </script>
  
  <style scoped>
  .parent {
    padding: 20px;
    background-color: #7AB2B2;
    border: 1px solid #ddd;
    border-radius: 5px;
  }
  </style>
  