<template>
  <div class="page">
                <!--======= WELCOME AREA =======-->
        <div id="home" class="welcome-area" data-stellar-background-ratio="0.6" style="background-image: url(src/appAssets/img/intro-bg.jpeg);">
           <div class="welcome-table">
               <div class="welcome-cell">
                    <div class="container">
                        <div class="row">
                            <div class="col-md-12 col-sm-12 col-xs-12">
                                <div class="welcome-text">
                                  <h2 class="theme-color lead">Web Developer. WordPress Wizard.</h2>
                                   <div class="element"></div>
                                    <div class="social-links">
                                        <ul>
                                            <li><a href="https://github.com/e1cerebro" target="_blank"><i class="fa fa-github"></i></a></li>
                                            <li><a href="mailto:nwachukwu16@hotmail.com" ><i class="fa fa-envelope-square"></i></a></li>
                                            <li><a href="https://www.linkedin.com/in/christian-nwachukwu-3847b6131" target="_blank"><i class="fa fa-linkedin"></i></a></li>
                                        </ul>
                                    </div>
                                </div>
                                <div class="home-arrow">
                                    <a href="#about" class="smoth-scroll"><i class="fa fa-angle-double-down"></i></a>
                                </div>
                            </div>
                       </div><!--/.row-->
                    </div><!--/.container-->
                </div>
            </div>
        </div>
        <!--===== END WELCOME AREA =====-->
  </div>
</template>

<script>
export default {
  data() {
    return {
      status: "Critical"
    };
  },
  methods: {
    changeStatus() {
      this.$emit("homeEvent", "This is coming from the home component");
    }
  }
};
</script>
<style scoped>
.lead {
  color: #f27849;
  font-size: 200%;
  font-weight: 500;
}

.element {
}
</style>

