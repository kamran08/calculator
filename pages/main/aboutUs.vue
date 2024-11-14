<template>
    <div>
        <mainMenu/>

        <div class="_1content">
            <!-- Banner -->
             <div class="_con_banner">
              <div class="_con_banner_pic">
                <img class="_con_banner_img" src="/car-three.jpg" alt="" title="">
              </div>

              <div class="_con_banner_content">
                <h4 class="_con_banner_title">About Us</h4>
                <h1 class="_con_banner_text">Unleash Your  Comfortable Journey with Quick Rentals</h1>
              </div>
             </div>
            <!-- Banner -->

            <!-- Main section -->
            <div class="_about_who">
                <div class="container">
                    <div class="_about_who_main">
                        <div class="row align-items-center g-0">
                            <div class="col-12 col-md-6">
                                <div class="_about_who_left">
                                    <h1 class="_about_who_title">Who We Are</h1>

                                    <p class="_about_who_subTitle">Wide Range of Vehicles</p>
                                    <p class="_about_who_text">
                                        From compact cars and sedans to SUVs and luxury vehicles, our extensive fleet caters to all your needs and preferences. Whether you need a car for a day, a week, or a month, we have the perfect vehicle for you.
                                    </p>

                                    <p class="_about_who_subTitle">Competitive Pricing</p>
                                    <p class="_about_who_text _mar_b0">
                                        We offer transparent and competitive pricing with no hidden fees. Our flexible rental plans are designed to suit your budget and duration of rental
                                    </p>
                                </div>
                            </div>
                            <div class="col-12 col-md-6">
                                <div class="_about_who_right">
                                    <img src="/about_img.png">
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="_about_dri">
                <div class="container">
                    <div class="row g-3">
                        <div class="col-12 col-md-3">
                            <div class="_about_dri_left">
                                <div class="_about_dri_img">
                                    <img src="/toyota-offer-2 1.png">
                                </div>
                            </div>
                        </div>

                        <div class="col-12 col-md-9">
                            <div class="_about_dri_right">
                                <h1 class="_about_dri_right_text">Do You Want To Earn With Us?<br/> So Don't Be Late.</h1>
                                
                                <div class="_about_dri_button">
                                    <button class="_6btn">Become a Driver</button>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="_about_faq">
                <div class="container">
                    <h1 class="_about_faq_title">Frequently asked questions</h1>
                    <p class="_about_faq_text">Get your queries cleared and have a hassle free rental journey!</p>

                    <div class="row justify-content-center">
                        <div class="col-12 col-md-8 col-lg-6">
                            <div class="_collapse">
                                <Collapse accordion>
                                    <Panel name="1">
                                        How can I make a reservation with Duare Car
                                        <template #content>o make a reservation with Duare Car, simply visit our website and create an account. Once logged in, you can browse our available vehicles, select your desired dates and times, and complete the booking process online. Alternatively, you can also contact our customer service team for assistance with your reservation.</template>
                                    </Panel>
                                    <Panel name="2">
                                        What is Quick Rentals' policy?
                                        <template #content>o make a reservation with Duare Car, simply visit our website and create an account. Once logged in, you can browse our available vehicles, select your desired dates and times, and complete the booking process online. Alternatively, you can also contact our customer service team for assistance with your reservation.</template>
                                    </Panel>
                                    <Panel name="3">
                                        How can I make a reservation with Duare Car
                                        <template #content>o make a reservation with Duare Car, simply visit our website and create an account. Once logged in, you can browse our available vehicles, select your desired dates and times, and complete the booking process online. Alternatively, you can also contact our customer service team for assistance with your reservation.</template>
                                    </Panel>
                                    <Panel name="4">
                                        What is Quick Rentals' cancellation policy?
                                        <template #content>o make a reservation with Duare Car, simply visit our website and create an account. Once logged in, you can browse our available vehicles, select your desired dates and times, and complete the booking process online. Alternatively, you can also contact our customer service team for assistance with your reservation.</template>
                                    </Panel>
                                </Collapse>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <!-- Main section -->
        </div>

        <!-- Footer -->
         <mainFooter/>
        <!-- Footer -->
    </div>
</template>

<script>
import mainMenu from "~/components/main/menu.vue";
import mainFooter from "~/components/main/footer.vue";

export default {
  // middleware:'auth',
  components: {
    mainMenu,
    mainFooter,
  },

  data(){
    return{
      
    }
  },


  methods:{
    
  },
  
  created(){
    
  }
}
</script>