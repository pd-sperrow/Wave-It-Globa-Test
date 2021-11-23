<template>
  <b-button :size="size" class="icon-button" >
    <div v-if="position === 'left'" class="px-3 py-1" :class="{'button-border': isBorder}">
      <b-icon :icon="icon" :font-scale="scale" aria-hidden="true"></b-icon>
      {{ title }}
    </div>
    <div v-else class="px-3 py-1" :class="{'button-border': isBorder}">
      {{ title }}
      <b-icon :icon="icon" :font-scale="scale" aria-hidden="true"></b-icon>
    </div>
  </b-button>
</template>

<script>
  export default {
    name: 'IconButton',
    props: {
      title: {
        type: String,
        required: true
      },
      icon: {
        type: String,
        required: true
      },
      scale: {
        type: Number,
        default: 1.25
      },
      size: {
        type: String,
        default: 'sm'
      },
      isBorder: {
        type: Boolean,
        default: false
      },
      position: {
        type: String,
        default: 'left'
      }
    }
  }
</script>

<style>
  .icon-button, .icon-button:hover {
    color: #ffffff;
    font-weight: bolder;
    background-color: #6158a7;
    border-radius: 50px;
  }
  .button-border {
    border: 2px solid #ffffff;
    border-radius: 50px;
  }
</style>
