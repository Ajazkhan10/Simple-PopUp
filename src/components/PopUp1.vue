<template>
    <div class="popup">
      <div class="inner-popup">
        <slot />
        <button @click="closePopUp">close PopUp</button>
      </div>
    </div>
  </template>
  <script>
  export default {
    props: {
      closePopUp: {
        type: Function,
      },
  
    },
  };
  </script>
  <style scoped>
  .popup {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    z-index: 99;
    background-color: rgba(0, 0, 0, 0.2);
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .inner-popup {
    background: #fff;
    padding: 32px;
    width: 400px;
    height: fit-content;
    box-shadow: rgb(38, 57, 77) 0px 20px 30px -10px;
    border-radius: 3px solid black;
  
  }
  </style>