<template>
  <!--===== SERVICES AREA =====-->
    <div class="col-md-4 col-sm-12">
        <div class="single-service text-center wow fadeInUp" data-wow-delay="0.4s">
            <div class="service-img" v-bind:style="{ backgroundImage: 'url(' + icon + ')' }"></div>
            <h3>{{title}}</h3>
            <p><slot></slot></p>
        </div>
    </div>
<!--====== END SERVICES AREA ======-->
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
    }
  },
  data() {
    return {};
  },
  methods: {}
};
</script>
<style scoped>
.single-service {
  max-height: 300px;
  min-height: 300px;
}
</style>

