<template>
  <div class="search-details">
    <b-container fluid>
      <b-row>
        <b-col md="12">
            <h1 class="color-gray font-weight-bolder mb-3">Search result</h1>
            <div class="d-flex justify-content-between mb-3">
              <p class="font-weight-bolder total-result mb-0">Matches for your requirements: {{ profiles.length }} results</p>
              <div class="d-flex">
                <icon-button class="mx-1" title="Manage Filters" icon="blockquote-left" :is-border="true" position="right" />
                <icon-button class="ml-1" title="Advance Search" icon="search" :is-border="true" position="right" />
              </div>
            </div>
            <b-row class="mb-4">
              <b-col>
                <div class="color-primary">
                  <b-iconstack font-scale="2" class="cursor-pointer" @click="changeGridType('grid')">
                    <b-icon v-if="gridType == 'grid'" stacked icon="square-fill"></b-icon>
                    <b-icon v-if="gridType == 'grid'" stacked icon="grid-fill" scale=".75" variant="white"></b-icon>
                    <b-icon v-if="gridType == 'list'" stacked icon="grid-fill" scale=".75"></b-icon>
                  </b-iconstack>

                  <b-iconstack font-scale="2" class="cursor-pointer"  @click="changeGridType('list')">
                    <b-icon v-if="gridType == 'list'" stacked icon="square-fill"></b-icon>
                    <b-icon v-if="gridType == 'list'" stacked icon="list" scale="1" variant="white"></b-icon>
                    <b-icon v-if="gridType == 'grid'" stacked icon="list" scale=".75"></b-icon>
                  </b-iconstack>
                </div>
              </b-col>
              <b-col class="tags">
                <b-form-tags
                  input-id="tags-pills"
                  v-model="tags"
                  tag-variant="primary"
                  tag-pills
                  size="md"
                  placeholder="See More"
                >
                </b-form-tags>
              </b-col>
            </b-row>
            <template v-if="gridType === 'grid'">
              <div>
                <template v-for="(profile, index) in profiles">
                  <grid-view :profile="profile" :key="index" class="mb-3" />
                </template>
              </div>
            </template>
            <template v-if="gridType === 'list'">
              <div>
                <template v-for="(profile, index) in profiles">
                  <list-view :profile="profile" :key="index" class="mb-3" />
                </template>
              </div>
            </template>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import IconButton from '../IconButton.vue'
import GridView from '../View/GridView.vue'
import ListView from '../View/ListView.vue'
  export default {
    name: 'SearchDetails',
    components: { IconButton, ListView, GridView },
    data() {
      return {
        gridType: 'list',
        tags: ['Male', 'London', '27-40Yrs', 'Islam', 'Pakistani'],
        profiles: [
          {
            name: 'Justin Webb',
            address: 'London, UK',
            age: 27,
            religion: 'Islam'
          },
          {
            name: 'Justin Webb',
            address: 'London, UK',
            age: 27,
            religion: 'Islam'
          },
          {
            name: 'Justin Webb',
            address: 'London, UK',
            age: 27,
            religion: 'Islam'
          },
          {
            name: 'Justin Webb',
            address: 'London, UK',
            age: 27,
            religion: 'Islam'
          },
          {
            name: 'Justin Webb',
            address: 'London, UK',
            age: 27,
            religion: 'Islam'
          },
          {
            name: 'Justin Webb',
            address: 'London, UK',
            age: 27,
            religion: 'Islam'
          },
          {
            name: 'Justin Webb',
            address: 'London, UK',
            age: 27,
            religion: 'Islam'
          },
          {
            name: 'Justin Webb',
            address: 'London, UK',
            age: 27,
            religion: 'Islam'
          },
          {
            name: 'Justin Webb',
            address: 'London, UK',
            age: 27,
            religion: 'Islam'
          },
          {
            name: 'Justin Webb',
            address: 'London, UK',
            age: 27,
            religion: 'Islam'
          },
          {
            name: 'Justin Webb',
            address: 'London, UK',
            age: 27,
            religion: 'Islam'
          },
          {
            name: 'Justin Webb',
            address: 'London, UK',
            age: 27,
            religion: 'Islam'
          },
          {
            name: 'Justin Webb',
            address: 'London, UK',
            age: 27,
            religion: 'Islam'
          },
          {
            name: 'Justin Webb',
            address: 'London, UK',
            age: 27,
            religion: 'Islam'
          },
          {
            name: 'Justin Webb',
            address: 'London, UK',
            age: 27,
            religion: 'Islam'
          },
          {
            name: 'Justin Webb',
            address: 'London, UK',
            age: 27,
            religion: 'Islam'
          },
          {
            name: 'Justin Webb',
            address: 'London, UK',
            age: 27,
            religion: 'Islam'
          },
          {
            name: 'Justin Webb',
            address: 'London, UK',
            age: 27,
            religion: 'Islam'
          },
          {
            name: 'Justin Webb',
            address: 'London, UK',
            age: 27,
            religion: 'Islam'
          },
          {
            name: 'Justin Webb',
            address: 'London, UK',
            age: 27,
            religion: 'Islam'
          },
          {
            name: 'Justin Webb',
            address: 'London, UK',
            age: 27,
            religion: 'Islam'
          },
          {
            name: 'Justin Webb',
            address: 'London, UK',
            age: 27,
            religion: 'Islam'
          },
          {
            name: 'Justin Webb',
            address: 'London, UK',
            age: 27,
            religion: 'Islam'
          },
          {
            name: 'Justin Webb',
            address: 'London, UK',
            age: 27,
            religion: 'Islam'
          },
          {
            name: 'Justin Webb',
            address: 'London, UK',
            age: 27,
            religion: 'Islam'
          }
        ]
      }
    },
    methods: {
      changeGridType (type) {
        this.gridType = type
      }
    },
  }
</script>

<style>
  .search-details {
    width: 80%;
  }
  .total-result {
    color: #787878;
  }
  .badge-primary {
    background-color: #b1abd3 !important;
  }
  .tags .form-control, .tags .form-control:focus {
    border: 1px solid #fbfbfd;
    box-shadow: none;
    background-color: #fbfbfd;
  }
  .tags .b-form-tags-input::placeholder {
      color: #e00f0f;
      text-decoration: underline;
  }
</style>
