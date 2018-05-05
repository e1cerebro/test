<template>
  <div class="page">
      <!--====== FOOTER AREA ======-->
          <footer class="footer">
              <div class="container">
                  <div class="row wow zoomIn" data-wow-delay="0.4s">
                      <div class="col-md-12 text-center">
                          <p>&copy;{{date}} <a href="/"><strong>Christian</strong></a>. All Rights Reserved</p>
                      </div>
                  </div>
              </div>
          </footer>
        <!--====== END FOOTER AREA ======-->
  </div>
</template>

<script>
import ContactBox from "./ContactBox.vue";

export default {
  components: {
    "app-contact-box": ContactBox
  },
  data() {
    return {
      date: ""
    };
  },
  methods: {},
  created() {
    var d = new Date();
    this.date = d.getFullYear();
  },
  updated() {
    var d = new Date();
    this.date = d.getFullYear();
  }
};
</script>
<style>

</style>

