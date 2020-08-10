<template>

<div>
  <!-- Header -------------------------------------------------->
    <div>
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

    <!--Body----------------------------------------------------->
    <div class="row q-pt-md body">
        <div class="col-12 col-md">
            <div>
                <q-list separator>
                    <q-item clickable>
                        <q-item-section>
                            <div class="row">
                                <div class="col-12 col-md-5">
                                    <div class="">
                                        <q-carousel
                                        swipeable
                                        animated
                                        arrows
                                        v-model="slide"
                                        thumbnails
                                        infinite
                                        >
                                        <q-carousel-slide :name="1" img-src='~/assets/florida1.png'/>
                                        <q-carousel-slide :name="2" img-src='~/assets/florida2.png'/>
                                        <q-carousel-slide :name="3" img-src='~/assets/florida3.png'/>
                                        </q-carousel>
                                    </div>
                                </div>
                                <div class="col-12 col-md-7 listingDetails">
                                    <div class="text-h6 detailPrimary">Top Floor Penthouse Panoramic View</div>
                                    <div class="text-h6 detailSecondary">8 Guests<br>3 Bedrooms<br>7 Beds<br>3 Baths</div>
                                    <div class="text-h6 detailPrimary price"><span class="text-weight-bolder">$570</span> / night</div>
                                </div>
                            </div>
                        </q-item-section>
                    </q-item>

                    <q-item clickable>
                        <q-item-section>
                            <div class="row">
                                <div class="col-12 col-md-5">
                                    <div class="">
                                        <q-carousel
                                        swipeable
                                        animated
                                        arrows
                                        v-model="slide"
                                        thumbnails
                                        infinite
                                        >
                                        <q-carousel-slide :name="1" img-src='~/assets/florida1.png'/>
                                        <q-carousel-slide :name="2" img-src='~/assets/florida2.png'/>
                                        <q-carousel-slide :name="3" img-src='~/assets/florida3.png'/>
                                        </q-carousel>
                                    </div>
                                </div>
                                <div class="col-12 col-md-7 q-pa-md listingDetails">
                                    <div class="text-h6 detailPrimary">Top Floor Penthouse Panoramic View</div>
                                    <div class="text-h6 detailSecondary">8 Guests<br>3 Bedrooms<br>7 Beds<br>3 Baths</div>
                                    <div class="text-h6 detailPrimary price"><span class="text-weight-bolder">$570</span> / night</div>
                                </div>
                            </div>
                        </q-item-section>
                    </q-item>

                    <q-item clickable>
                        <q-item-section>
                            <div class="row">
                                <div class="col-12 col-md-5">
                                    <div class="">
                                        <q-carousel
                                        swipeable
                                        animated
                                        arrows
                                        v-model="slide"
                                        thumbnails
                                        infinite
                                        >
                                        <q-carousel-slide :name="1" img-src='~/assets/jersey1.png'/>
                                        <q-carousel-slide :name="2" img-src='~/assets/jersey2.png'/>
                                        <q-carousel-slide :name="3" img-src='~/assets/jersey3.png'/>
                                        </q-carousel>
                                    </div>
                                </div>
                                <div class="col-12 col-md-7 q-pa-md listingDetails">
                                    <div class="text-h6 detailPrimary">Top Floor Penthouse Panoramic View</div>
                                    <div class="text-h6 detailSecondary">8 Guests<br>3 Bedrooms<br>7 Beds<br>3 Baths</div>
                                    <div class="text-h6 detailPrimary price"><span class="text-weight-bolder">$570</span> / night</div>
                                </div>
                            </div>
                        </q-item-section>
                    </q-item>
                </q-list>
            </div>   
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
      lorem: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
      slide:1
    }
  }
}
</script>

<style lang="scss">
.listingDetails {
    text-decoration:none;
    position:relative;

    .detailPrimary{
        color:black;
    }

    .detailSecondary {
        color:rgb(117, 117, 117);
    }

    .price {
        position: absolute;
        bottom: 8px;
        right: 16px;
        font-size: 18px;
    }
}

.listing {
    height:200px;
}

.map{
    background:black;
    height:100px;
}
</style>