<template>
  <div class="page">

         <!--====== CONTACT INFO AREA ======-->
        <div id="contact" class="contact-info-area section-padding">
            <div class="container">
                <div class="row">
                    <div class="col-md-12 col-sm-12 col-xs-12">
                      <div class="section-title">
                       <h2>contact.</h2>
                       </div>
                    </div>
                </div> <!--/.row-->

                <div class="row contact-margin-bottom">
                    <div class="col-md-8 col-md-offset-2">
                        <div class="row">

                            <app-contact-box v-bind:title="'My Location'" v-bind:icon="'fa fa-rocket'">
                              416 California Avenue, Windsor, ON N9B 2Y9
                            </app-contact-box>
                            <app-contact-box  v-bind:title="'Phone Number'" v-bind:icon="'fa fa-phone'">
                              <a class="custom-link" href="tel:+15199921651">(+1) 519 992 1651</a>
                            </app-contact-box>

                            <app-contact-box  v-bind:title="'Email Address'" v-bind:icon="'fa fa-envelope'">
                               <a class="custom-link" href="mailto:nwachukwu16@hotmail.com">nwachukwu16@hotmail.com</a>
                            </app-contact-box>

                        </div>
                    </div>
                </div><!--/.row-->

                <div class="row">
                    <div class="col-md-8 col-md-offset-2 col-sm-12 col-xs-12">
                      <div class="alert alert-success" v-if="showMessageStatus">
                        <strong>Message Sent!</strong> Your message was successfully sent.
                      </div>

                      <div class="alert alert-warning" v-if="showError">
                        <strong>Warning!</strong> The email could not be sent.
                      </div>

                          <div class="contact-form">
                             <form id="contact-form">
                             <div class="messages"></div>
                                <div class="controls">
                                    <div class="row">
                                        <div class="col-md-6">
                                            <div class="form-group">
                                                <input id="form_name" type="text"   class="form-control" placeholder="Name*"  data-error="Name is required." required="required"  v-model="contact.name">
                                                <div class="help-block with-errors"></div>
                                             </div>
                                        </div>
                                        <div class="col-md-6">
                                            <div class="form-group">
                                                <input id="form_email" type="email" name="email" class="form-control" placeholder="Email*" required="required" data-error="Valid email is required." v-model="contact.email">
                                                <div class="help-block with-errors"></div>
                                            </div>
                                        </div>
                                     </div>

                                    <div class="row">
                                        <div class="col-md-12">
                                            <div class="form-group">
                                                <input id="form_subject" type="text" name="subject" class="form-control" placeholder="Subject*" required="required" data-error="Subject is required." v-model="contact.subject">
                                                <div class="help-block with-errors"></div>
                                            </div>
                                        </div>
                                     </div>
                                    <div class="row">
                                        <div class="col-md-12">
                                            <div class="form-group">
                                                <textarea id="form_message" name="message" class="form-control" placeholder="Message*" rows="7" required="required" data-error="Please,leave us a message." v-model="contact.message"></textarea>
                                                <div class="help-block with-errors"></div>
                                            </div>
                                        </div>
                                        <div class="col-md-12">
                                            <input v-if="valid" type="submit" @click.prevent="sendEmail" class="btn btn-effect btn-sent" value="Send message">
                                            <img v-if="showLoader" :src="'src/appAssets/images/loader.gif'" />
                                        </div>
                                        <h4 class="text-danger text-center" v-if="!valid">Please complete all the fields</h4>
                                    </div>
                                </div>
                            </form>
                          </div>
                     </div>
                    </div>
            </div><!--/.container-->
        </div>
        <!--===== END CONTACT INFO AREA ======-->

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
      contact: {
        name: "",
        email: "",
        subject: "",
        message: ""
      },
      showMessageStatus: false,
      showError: false,
      showLoader: false
    };
  },
  computed: {
    valid() {
      if (
        this.contact.name.length > 3 &&
        this.contact.email.length >= 10 &&
        this.contact.subject.length > 3 &&
        this.contact.message.length > 3
      ) {
        return true;
      }
    }
  },
  methods: {
    sendEmail() {
      this.showLoader = true;
      let vm = this;
      emailjs
        .send("gmail", "chris_email", {
          email: this.contact.email,
          name: this.contact.name,
          subject: this.contact.subject,
          message: this.contact.message
        })
        .then(
          function(response) {
            vm.showLoader = false;
            vm.showMessageStatus = true;
            setTimeout(function() {
              vm.showMessageStatus = false;
            }, 5000);
          },
          function(err) {
            vm.showError = true;
            vm.showLoader = true;
            setTimeout(function() {
              vm.showError = false;
              vm.showLoader = false;
            }, 5000);
          }
        );
    }
  }
};
</script>
<style>
.custom-link {
  color: #f27849 !important;
}
</style>

