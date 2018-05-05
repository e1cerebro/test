<template>
  <div class="page">

        <!--====== WORK AREA ======-->
        <div id="work" class="work-area section-padding">
            <div class="container">
                <div class="row">
                    <div class="col-md-12 col-sm-12 col-xs-12">
                      <div class="section-title">
                           <h2>recent work.</h2>
                           <p>Here are some of the projects that I contributed to.</p>
                       </div>
                    </div>
                </div> <!--/.row-->

                 <div class="row">
                    <ul class="work-list text-center">
                        <li class="filter" data-filter="all">all</li>
                        <li class="filter" data-filter=".blogs">Blogs</li>
                        <li class="filter" data-filter=".company-website">Company Website</li>
                        <li class="filter" data-filter=".gyms">Gyms</li>
                        <li class="filter" data-filter=".imagery">Imagery</li>
                        <li class="filter" data-filter=".school-management">School Management</li>
                        <li class="filter" data-filter=".social-connect">Social Connections</li>
                    </ul>
                </div>
                <!--/.row-->

                <div class="work-inner">
                    <div class="row">

                      <div class="row">
                        <app-single-work v-bind:category = "'school-management'" v-bind:icon="'static/img/work/prodigy.PNG'" v-bind:title="'Prodigy Reseller Platform'" v-bind:link="'https://prodigy.com.ng/'"></app-single-work>
                        <app-single-work v-bind:category = "'company-website'" v-bind:icon="'static/img/work/rydox.PNG'" v-bind:title="'Rydox Technologies'" v-bind:link="'http://rydoxtech.com/ '"></app-single-work>
                        <app-single-work v-bind:category = "'company-website'" v-bind:icon="'static/img/work/krisbel.PNG'" v-bind:title="'Krysbel Energy'" v-bind:link="'http://krysbelenergy.com/'"></app-single-work>
                      </div>

                        <div class="row">
                          <app-single-work v-bind:category = "'blogs'" v-bind:icon="'static/img/work/expounding.PNG'" v-bind:title="'Expounding Christ'" v-bind:link="'http://expoundingchrist.com/'"></app-single-work>
                          <app-single-work v-bind:category = "'blogs'" v-bind:icon="'static/img/work/nibcraft.PNG'" v-bind:title="'NibCraft'" v-bind:link="'http://nibcraft.com/'"></app-single-work>
                          <app-single-work v-bind:category = "'social-connect'" v-bind:icon="'static/img/work/windsor.PNG'" v-bind:title="'Windsor Connect'" v-bind:link="'https://windsorconnect.ca/'"></app-single-work>
                        </div>

                         <div class="row">
                          <app-single-work v-bind:category = "'gyms'" v-bind:icon="'static/img/work/jsfitness.PNG'" v-bind:title="'JS Fitness'" v-bind:link="'http://jsfitness.ca/'"></app-single-work>
                          <app-single-work v-bind:category = "'gyms'" v-bind:icon="'static/img/work/refine.PNG'" v-bind:title="'Refine Fitness'" v-bind:link="'http://refinefitness.ca/'"></app-single-work>
                          <app-single-work v-bind:category = "'imagery'" v-bind:icon="'static/img/work/chezimagery.PNG'" v-bind:title="'Chez Imagery'" v-bind:link="'http://chezimagery.com/'"></app-single-work>
                        </div>

                    </div> <!--/.row-->

                </div>
            </div><!--/.container-->
        </div>
        <!--====== END WORK AREA ======-->
  </div>
</template>

<script>
import Work from "./Work.vue";

export default {
  components: {
    "app-single-work": Work
  },
  data() {
    return {};
  },
  methods: {}
};
</script>
<style>

</style>

