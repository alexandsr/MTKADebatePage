<template>
    <MDBNavbar
    container
    expand="lg"
    bg="light"
    class="d-flex justify-content-between rounded-5"
    >
      <MDBNavbarBrand>
        <img src="../assets/debatelogo.png" height="50" alt="Minnetonka Debate Logo" />
      </MDBNavbarBrand>
      <MDBNavbarToggler
        target="#navbarColor01"
        @click="collapse7 = !collapse7"
      ></MDBNavbarToggler>
      <MDBCollapse id="navbarColor01" v-model="collapse7">
        <MDBNavbarNav right class="mb-2 mb-lg-0">
        </MDBNavbarNav>
      </MDBCollapse>
      <MDBNavbarNav center class="mb-2 mb-lg-0 d-flex flex-row">

        <MDBNavbarItem href="#" linkClass="link-secondary"
            ><b>Why Debate?</b></MDBNavbarItem
          >
          <MDBNavbarItem href="#" linkClass="link-secondary"
            >About Us</MDBNavbarItem
          >
          <MDBDropdown v-model="dropdown2">
        <MDBDropdownToggle tag="a" class="nav-link" @click="dropdown2 = !dropdown2"
          >Information</MDBDropdownToggle
        >
        <MDBDropdownMenu>
          <MDBDropdownItem href="#">For Students</MDBDropdownItem>
          <MDBDropdownItem href="#">For Parents</MDBDropdownItem>
          <MDBDropdownItem href="#">Format</MDBDropdownItem>
          <MDBDropdownItem href="#">Competitions</MDBDropdownItem>
          <MDBDropdownItem href="#">Calendar</MDBDropdownItem>
        </MDBDropdownMenu>
      </MDBDropdown>
    </MDBNavbarNav>
      <MDBNavbarNav right class="mb-2 mb-lg-0 d-flex flex-row">
        <MDBDropdown class="nav-item" v-model="dropdown5">
        <MDBDropdownToggle tag="a" class="nav-link" @click="dropdown5 = !dropdown5">
          <Icon :icon="icons.languageIcon" />
        </MDBDropdownToggle>
        <MDBDropdownMenu>
            <MDBDropdownItem href="#"
            ><MDBIcon flag="united-kingdom" />English
              <Icon :icon="icons.checkmarkIcon" />

          </MDBDropdownItem>
          <MDBDropdownItem divider />
          <MDBDropdownItem href="#"><MDBIcon flag="mexico" />Español </MDBDropdownItem>
          <MDBDropdownItem href="#"><MDBIcon flag="somalia" />Soomaali </MDBDropdownItem>
        </MDBDropdownMenu>
      </MDBDropdown>
      <MDBNavbarItem href="#" class="me-3 me-lg-0">
        <Icon :icon="icons.moonStarsFill" />
      </MDBNavbarItem>
      <MDBNavbarItem href="#" class="me-3 me-lg-0">
        <Icon :icon="icons.dividerTall16Filled" class="me-3 me-lg-0" />
      </MDBNavbarItem>
      <MDBNavbarItem href="#" class="me-3 me-lg-0">
        <Icon :icon="icons.baselineFacebook" />
      </MDBNavbarItem>
      <MDBNavbarItem href="#" class="me-3 me-lg-0">
        <Icon :icon="icons.groupmeIcon" />        </MDBNavbarItem >
        <MDBNavbarItem href="#" linkClass="link-secondary"
            ><b>Contact</b></MDBNavbarItem
          >

      </MDBNavbarNav>
    </MDBNavbar>
  </template>
  
  <script>
  import { Icon } from '@iconify/vue';
  import groupmeIcon from '@iconify-icons/simple-icons/groupme';
  import languageIcon from '@iconify-icons/ion/language';
  import moonStarsFill from '@iconify-icons/ph/moon-stars-fill';
  import sunFill from '@iconify-icons/ph/sun-fill';
  import baselineFacebook from '@iconify-icons/ic/baseline-facebook';
  import dividerTall16Filled from '@iconify-icons/fluent/divider-tall-16-filled';
  import checkmarkIcon from '@iconify-icons/ion/checkmark';
    import {
    MDBNavbar,
    MDBNavbarItem,
    MDBNavbarBrand,
    MDBNavbarNav,
    MDBNavbarToggler,
    MDBBadge,
    MDBDropdown,
    MDBDropdownToggle,
    MDBDropdownMenu,
    MDBDropdownItem,
    MDBIcon,
  } from 'mdb-vue-ui-kit';
  import { ref } from "vue";

  export default {
    components: {
        MDBNavbar,
        MDBNavbarItem,
        MDBNavbarBrand,
        MDBNavbarNav,
        MDBNavbarToggler,
        MDBBadge,
        MDBIcon,
        MDBDropdown,
        MDBDropdownToggle,
        MDBDropdownMenu,
        MDBDropdownItem,
        Icon,
    },
    setup() {
      const collapse7 = ref(false);
      const dropdown2 = ref(false);
      const dropdown5 = ref(false);

      return {
        collapse7,
        dropdown2,
        dropdown5,
      }
      
    },
    data() {
		return {
			icons: {
				groupmeIcon,
        baselineFacebook,
        languageIcon,
        moonStarsFill,
        sunFill,
        dividerTall16Filled,
        checkmarkIcon,
			},
		};
	},
  };
</script>