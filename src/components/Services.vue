<template>
  <div class="page">
          <!--===== SERVICES AREA =====-->
        <div id="services" class="services-area section-padding">
            <div class="container">
               <div class="row">
                   <div class="col-md-12 col-sm-12 col-xs-12">
                      <div class="section-title">
                       <h2>what i do.</h2>
                       </div>
                   </div>
               </div> <!--/.row-->

                <div class="row">
                    <div class="row">
                      <app-service-single  v-bind:title="'Web Design'" v-bind:icon="'src/appAssets/img/service/1.png'">
                        I can help you have the website that look great both you and your target audience.
                      </app-service-single>
                      <app-service-single  v-bind:title="'WordPress Development'" v-bind:icon="'src/appAssets/img/service/2.png'">
                        I create wordpress websites and plugins. Easily edit pages, images and content with no programming required.
                      </app-service-single>
                      <app-service-single  v-bind:title="'Custom Email & Web Hosting'" v-bind:icon="'src/appAssets/img/service/4.png'">
                        I can help you configure email and web hosting available on a domain of your choosing for one low yearly cost.
                      </app-service-single>
                    </div>
                   <div class="row">
                      <app-service-single v-bind:title="'Business Consulting'" v-bind:icon="'src/appAssets/img/service/3.png'">
                       I can help you put your best foot forward online with a professional website designed with your target audience in mind.
                      </app-service-single>
                      <app-service-single v-bind:title="'Seo Freindly'" v-bind:icon="'src/appAssets/img/service/5.png'">
                        I can help you earn the type of top 3 ranking your websites deserves on the search engines.
                      </app-service-single>
                      <app-service-single v-bind:description="'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Non vel, sint nisi possimus sunt veritatis.'" v-bind:title="'Support'" v-bind:icon="'src/appAssets/img/service/6.png'">
                        Complete Business solution for companies and small scale businesses.
                      </app-service-single>
                   </div>

                </div><!--/.row-->
            </div><!--/.container-->
        </div>
        <!--====== END SERVICES AREA ======-->
  </div>
</template>

<script>
import ServiceSingle from "./ServiceSingle.vue";

export default {
  components: {
    "app-service-single": ServiceSingle
  },
  data() {
    return {
      status: "Critical",
      services: [{ title: "", icon: "", content: "" }]
    };
  },
  methods: {
    changeStatus() {
      this.$emit("homeEvent", "This is coming from the home component");
    }
  }
};
</script>
<style>

</style>

