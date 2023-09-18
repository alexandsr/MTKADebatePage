<template>
    <!-- Footer -->
    <MDBFooter :text="['center', 'lg-start', 'muted']">
      <!-- Section: Social media -->
      <section class="
          d-flex
          justify-content-center justify-content-lg-between
          p-4
          border-bottom
        ">
        <!-- Left -->
        <div class="me-5 d-none d-lg-block">
          <span>Ask questions, connect and get involved on social media:</span>
        </div>
        <!-- Left -->
        <!-- Right -->
        <div>
        <a href="" class="me-4 text-reset">
            <Icon :icon="icons.groupmeIcon" />
          </a>
          <a href="" class="me-4 text-reset">
            <Icon :icon="icons.baselineFacebook" />
          </a>
        </div>
        <!-- Right -->
      </section>
      <!-- Section: Social media -->
      <!-- Section: Links  -->
      <section class="">
        <MDBContainer class="text-center text-md-start mt-5">
          <!-- Grid row -->
          <MDBRow class="mt-3">
            <!-- Grid column -->
            <MDBCol md="3" lg="4" xl="3" class="mx-auto mb-4">
              <!-- Content -->
              <h6 class="text-uppercase fw-bold mb-4">
                <i class="fas fa-gem me-3"></i>Minnetonka Speech & Debate
              </h6>
              <p>
                Minnetonka Speech & Debate has been speaking
                and debating for many years. Colleges like debate so you should like debate.

            </p>
            </MDBCol>
            <!-- Grid column -->
            <!-- Grid column -->
            <MDBCol md="2" lg="2" xl="2" class="mx-auto mb-4">
              <!-- Links -->
              <h6 class="text-uppercase fw-bold mb-4">Formats</h6>
              <p>
                <a href="#!" class="text-reset">Congress</a>
              </p>
              <p>
                <a href="#!" class="text-reset">Lincoln-Douglass</a>
              </p>
            </MDBCol>
            <!-- Grid column -->
            <!-- Grid column -->
            <MDBCol md="3" lg="2" xl="2" class="mx-auto mb-4">
              <!-- Links -->
              <h6 class="text-uppercase fw-bold mb-4">Useful links</h6>
              <p>
                <a href="#!" class="text-reset">Tabroom</a>
              </p>
              <p>
                <a href="#!" class="text-reset">Google</a>
              </p>
            </MDBCol>
            <!-- Grid column -->
            <!-- Grid column -->
            <MDBCol md="4" lg="3" xl="3" class="mx-auto mb-md-0 mb-4">
              <!-- Links -->
              <h6 class="text-uppercase fw-bold mb-4">Contact</h6>
              <p>
                <i class="fas fa-envelope me-3"></i>
                contact@mtkadebate.org
              </p>
            </MDBCol>
            <!-- Grid column -->
          </MDBRow>
          <!-- Grid row -->
        </MDBContainer>
      </section>
      <!-- Section: Links  -->
      <!-- Copyright -->
      <div class="text-center p-4" style="background-color: rgba(0, 0, 0, 0.05)">
        © 2023 Copyright:
        <a class="text-reset fw-bold" href="https://alexander.systems">bals</a>
      </div>
      <!-- Copyright -->
    </MDBFooter>
    <!-- Footer -->
  </template>
  <script>
  import {
    MDBFooter,
    MDBContainer,
    MDBRow,
    MDBCol,
    MDBIcon
  } from 'mdb-vue-ui-kit';
  import { Icon } from '@iconify/vue';
  import groupmeIcon from '@iconify-icons/simple-icons/groupme';
  import baselineFacebook from '@iconify-icons/ic/baseline-facebook';


  export default {
    components: {
      MDBFooter,
      MDBContainer,
      MDBRow,
      MDBCol,
      MDBIcon,
      Icon,

    },
    data() {
		return {
			icons: {
				groupmeIcon,
                baselineFacebook,
			},
		};
	},

  };
</script>