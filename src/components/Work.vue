<template>
      <div v-bind:class="category" class="col-md-4 col-sm-12 col-xs-12 mix category">
          <div class="single-work">
              <img v-bind:src="icon" alt="">
              <div class="item-hover">
                  <div class="work-table">
                      <div class="work-tablecell">
                          <div class="hover-content">
                              <h4>{{title}}</h4>
                               <a class="work-popup" v-bind:href="icon"><i class="fa fa-search-plus"></i></a>
                              <a class="work-link" target="_blank" v-bind:href="link"><i class="fa fa-link"></i></a>
                          </div>
                      </div>
                  </div>
              </div>
          </div>
      </div>
</template>

<script>
export default {
  props: {
    icon: {
      type: String
    },
    title: {
      type: String
    },
    description: {
      type: String
    },
    link: {
      type: String
    },
    category: {
      type: String
    }
  },
  data() {
    return {};
  },
  methods: {}
};
</script>
<style>

</style>

