<template>
  <div class="profile">
    <b-row no-gutters>
      <b-col cols="11">
        <div class="d-flex justify-content-between">
          <div class="profile-info">
            asfasd
          </div>
          <div class="profile-tags">
            <icon-button class="ml-1" title="Advance Search" icon="search" size="xs" />
          </div>
        </div>
      </b-col>
      <b-col cols="1" class="bg-primary">
        <div class="profile-action text-white cursor-pointet text-center">View Profile</div>
      </b-col>
    </b-row>
  </div>
</template>

<script>
import IconButton from '../IconButton.vue'
  export default {
  components: { IconButton },
    props: {
      profile: {
        type: Object,
        required: true
      }
    },
    name: 'ListView',
  }
</script>

<style>
  .profile {
    width: 100%;
    border-radius: 10px;
    box-shadow: 0 0 5px 3px #efefef;
  }
</style>
