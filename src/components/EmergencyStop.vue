<template>
    <button class="emergency-stop-button" @click="onStopClicked">
      <img :src="buttonImage" alt="Emergency Stop All" />
    </button>
  </template>
  
  <script>
  import buttonImage from '../assets/Emergency_Stop_All_Red.png';
  
  export default {
    name: 'EmergencyStopButton',
    props: {
      buttonImage: {
        type: String,
        default: buttonImage
      }
    },
    methods: {
      onStopClicked() {
        this.$emit('stop');
      }
    }
  };
  </script>
  
  <style scoped>
  .emergency-stop-button {
  border: none;
  background-color: transparent;
  padding: 0;
  cursor: pointer;
}
  
  .emergency-stop-button img {
    display: block; 
    width: 100%;
    height: 50px; 
  }
  </style>
  
  
  
  
  