<template>
  <div class="page">
       <div class="col-md-4 col-sm-4 text-center wow fadeInUp" data-wow-delay="0.2s">
          <div class="single-address">
              <i v-bind:class="icon"></i>
              <h4>{{title}}:</h4>
              <p><slot></slot></p>
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
    content: {
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

