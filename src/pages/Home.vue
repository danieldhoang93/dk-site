<template>

<div>
  <!-- Header -------------------------------------------------->
  <div class="">
    <div class="parallaxHeader">
      <q-parallax
      :height="600"
      :speed=".8"
        src='~/assets/dk-header.jpg'
        class="backgroundTint"
      >
      </q-parallax>
      <div class="headerText text-center">
        <h1 class="text-white">Find Your Luxury</h1>
      <searchBox></searchBox>
      </div>
    </div>
  </div>

  <!--body ----------------------------------------------------->

    <div class="row q-pt-xl body">
      <div class="col-12 col-md q-px-sm q-pt-sm">
        <q-card class="cityPictures" flat bordered>
          <div class="">
            <q-carousel
              animated
              v-model="slide"
              navigation
              infinite
              :autoplay="autoplay"
              arrows
              transition-prev="slide-right"
              transition-next="slide-left"
              @mouseenter="autoplay = false"
              @mouseleave="autoplay = true"
            >
              <q-carousel-slide :name="1" img-src='~/assets/florida1.png'/>
              <q-carousel-slide :name="2" img-src='~/assets/florida2.png'/>
              <q-carousel-slide :name="3" img-src='~/assets/florida3.png'/>
            </q-carousel>
          </div>

          <q-card-section>
            <div class="text-h5 q-mt-sm q-mb-xs">Florida <span class="text-overline text-orange-9">6 Listings Available</span></div>
            <div class="text-caption text-grey">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
            </div>
          </q-card-section>

          <q-card-actions>
            <q-btn flat color="dark" label="Explore" v-bind:to="listingsLink"/>
            <q-space />
          </q-card-actions>
        </q-card>
      </div>
      <div class="col-12 col-md q-px-sm q-pt-sm">
        <q-card class="cityPictures" flat bordered>
          <div class="">
            <q-carousel
              animated
              v-model="slide"
              navigation
              infinite
              :autoplay="autoplay"
              arrows
              transition-prev="slide-right"
              transition-next="slide-left"
              @mouseenter="autoplay = false"
              @mouseleave="autoplay = true"
            >
              <q-carousel-slide :name="1" img-src='~/assets/jersey1.png'/>
              <q-carousel-slide :name="2" img-src='~/assets/jersey2.png'/>
              <q-carousel-slide :name="3" img-src='~/assets/jersey3.png'/>
            </q-carousel>
          </div>

          <q-card-section>
            <div class="text-h5 q-mt-sm q-mb-xs">New Jersey <span class="text-overline text-orange-9">12 Listings Available</span></div>
            <div class="text-caption text-grey">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
            </div>
          </q-card-section>

          <q-card-actions>
            <q-btn flat color="dark" label="Explore" v-bind:to="listingsLink"/>
            <q-space />
          </q-card-actions>
        </q-card>
      </div>
    </div>

    <!-- footer -------------------------------------------------->
    <div class="q-pt-xl">
      <div class="footer">
        <div class="text-center">
          <q-parallax
          :height="100"
          :speed=".8"
          src='~/assets/dk-header.jpg'
          class="backgroundTint"
          >
          <div class="text-white"></div>
          </q-parallax>
          <div class="headerText text-center">
            <div class="text-white">© Untitled. All rights reserved.</div>
          </div>
        </div>
      </div>
    </div>
</div>
</template>

<script>
import searchBox from 'components/searchBox.vue'
export default {
  components: {
    searchBox
  },
  data () {
    return {
      checkIn: '',
      checkOut: '',
      location: 'Select a location',
      locations: [
        'Florida', 'New Jersey'
      ],
      guests:0,
      slide: 1,
      autoplay: true,
      listingsLink:'/listings'
    }
  },
  methods: {
        addGuest: function() {
            this.guests += 1;
        },
        minusGuest: function() {
            if (this.guests != 0) {
              this.guests -= 1;
            }
        }
    }
}
</script>

<style lang="scss">
.container {
 height: 100%;
  margin: 0;
  position: relative;
}

body {
  background:rgb(240, 240, 240);
}

.backgroundSaturate {
  filter: saturate(130%);
}

.cities {
  width:100%;
  margin-left:auto;
  margin-right:auto;
}

.cityPictures {
   width: 100%;
   position:relative;
}

.footer {
  background:black;
  height:100%;
  position:relative;
}
</style>
