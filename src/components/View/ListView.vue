<template>
  <div class="profile">
    <b-row no-gutters>
      <b-col cols="10">
        <div class="d-flex justify-content-between">
          <div class="profile-info d-flex">
            <b-avatar :src="profile.avatar" rounded size="60px"></b-avatar>
            <div class="ml-2">
              <h5>{{ profile.name }}</h5>
              <h6>{{ profile.address }}, {{ profile.age }}, {{ profile.religion }}</h6>
            </div>
          </div>
          <div class="profile-tags">
            <tag class="ml-1" title="Shortlist" icon="star-fill" />
            <tag class="ml-1" title="Teamlist" icon="diagram3" />
            <tag class="ml-1" title="Contact" icon="diagram3" />
            <tag class="ml-1" title="Block" icon="slash-circle" bg-color="danger" />
          </div>
        </div>
      </b-col>
      <b-col cols="2">
        <div class="profile-action text-white cursor-pointer text-center bg-primary"><a href="#" class="text-white">View Profile</a></div>
      </b-col>
    </b-row>
  </div>
</template>

<script>
import IconButton from '../IconButton.vue'
import Tag from '../Tag.vue'
export default {
components: { IconButton, Tag },
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
    box-shadow: 0 0 5px 3px #d1d0d0;
  }
  .profile:focus {
    box-shadow: 0 0 5px 3px #739abb;
  }
  .profile-tags {
    padding-top: 16px;
  }
  .profile-action {
    border-bottom-right-radius: 5px;
    border-top-right-radius: 5px;
    height: 58px;
    padding-top: 16px;
  }
</style>
