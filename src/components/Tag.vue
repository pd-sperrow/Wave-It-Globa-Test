<template>
  <b-badge pill class="mx-2" :class="{'bg-primary': bgColor === 'default', 'bg-danger': bgColor === 'danger', 'bg-white': bgColor === 'white'}">
    <div v-if="position === 'left'" :class="{'color-primary': bgColor === 'white'}">
      <b-icon :icon="icon" :font-scale="scale" aria-hidden="true"></b-icon>
      {{ title }}
    </div>
    <div v-else>
      {{ title }}
      <b-icon :icon="icon" :font-scale="scale" aria-hidden="true"></b-icon>
    </div>
  </b-badge>
</template>

<script>
export default {
  name: 'Tag',
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
      default: 1
    },
    position: {
      type: String,
      default: 'left'
    },
    bgColor: {
      type: String,
      default: 'default'
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
