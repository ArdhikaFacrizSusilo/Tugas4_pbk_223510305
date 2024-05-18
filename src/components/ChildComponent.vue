<template>
    <div class="child">
      <h2>Ada yang bisa dibantu?</h2>
      <GrandchildComponent @message-from-grandchild="handleMessageFromGrandchild" />
      <slot name="additionalContent"></slot>
    </div>
  </template>
  
  <script>
  import GrandchildComponent from './GrandchildComponent.vue';
  
  export default {
    components: {
      GrandchildComponent,
    },
    methods: {
      handleMessageFromGrandchild(payload) {
        this.$emit('message-from-child', payload);
      },
    },
  };
  </script>
  
  <style scoped>
  .child {
    padding: 15px;
    background-color: #CDE8E5;
    border: 1px solid #ccc;
    border-radius: 5px;
    margin-top: 10px;
  }
  </style>
  