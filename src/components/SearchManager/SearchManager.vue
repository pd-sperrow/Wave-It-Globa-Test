<template>
  <div class="search-manger">
    <div class="bg-primary text-center search-header text-white font-weight-normal">
      <tag class="ml-1 back" title="Back" icon="caret-left-fill" bg-color="white" />
      <h5 class="pt-2">Search Manger</h5>
      <b-icon class="right-back bg-primary color-white" icon="caret-left-fill" font-scale="1.5" aria-hidden="true"></b-icon>
    </div>
    <div class="d-flex justify-content-center mt-3">
      <icon-button class="mx-1" title="Save Search" icon="search" size="sm"/>
      <icon-button class="mx-1" title="Load Saved Search" icon="arrow-counterclockwise" />
    </div>
    <hr>
    <div class="mt-3">
      <div class="d-flex">
        <label class="mr-2">Age:</label>
        <b-form-input id="age-min" v-model="age.low" type="range" min="0" :max="age.high"></b-form-input>
        <b-form-input id="age-max" v-model="age.high" type="range" min="0" max="100"></b-form-input>
      </div>
      {{ age.low }} {{ age.high }}
    </div>

  </div>
</template>

<script>
import IconButton from '../IconButton.vue'
import Tag from '../Tag.vue'
export default {
  components: { Tag, IconButton },
  name: 'SearchManager',
  data() {
    return {
      age: {
        low: 27,
        high: 40,
      },
    }
  }
}
</script>

<style scoped>
  .search-manger {
    width: 30%;
    text-align: center;
    box-shadow: 0 0 5px 3px #d1d0d0;
    border-radius: 10px;
    height: min-content;
  }
  .search-header {
    height: 40px;
    border-top-right-radius: 10px;
    border-top-left-radius: 10px;
    position: relative;
  }
  .back {
    position: absolute;
    left: -5px;
    top: 12px;
  }
  .right-back {
    position: absolute;
    right: 0px;
    top: 20px;
    height: 35px;
    border-left: 1px solid #fff;
    border-top: 1px solid #fff;
    border-bottom: 1px solid #fff;
    border-top-left-radius: 100%;
    border-bottom-left-radius: 100%;
    border-top-right-radius: 0px;
    border-bottom-right-radius: 0px;

  }
</style>
