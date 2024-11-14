<template>
    <div>
        <mainMenu/>

        <div class="_1content">
            <div class="_ticket">
                <div class="container">
                    <h1 class="_ticket_title">
                        <span>
                            <svg xmlns="http://www.w3.org/2000/svg" width="6" height="10" viewBox="0 0 6 10" fill="none">
                                <path d="M4.66602 9.16797L1.33268 5.0013L4.66602 0.834635" stroke="white" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                            </svg>
                        </span>
                        Trip Details
                    </h1>
                    <div class="row">
                        <div class="col-12 col-md">
                            <div class="_ticket_info">
                                <div class="row g-4">
                                    <div class="col-12 col-md-6">
                                        <p class="_trip_title">Car Name</p>
                                        <p class="_trip_val">Sedan AC</p>
                                    </div>
                                    <div class="col-12 col-md-6">
                                        <p class="_trip_title">Car Model</p>
                                        <p class="_trip_val">TXN45454</p>
                                    </div>
                                    <div class="col-12 col-md-6">
                                        <p class="_trip_title">Pick-up</p>
                                        <p class="_trip_val">01 Jun 2023, 02:00 PM</p>
                                    </div>
                                    <div class="col-12 col-md-6">
                                        <p class="_trip_title">Drop-up</p>
                                        <p class="_trip_val">01 Jun 2023, 02:00 PM</p>
                                    </div>
                                    <div class="col-12 col-md-6">
                                        <p class="_trip_title">Pick-up Location</p>
                                        <p class="_trip_val">Sylhet</p>
                                    </div>
                                    <div class="col-12 col-md-6">
                                        <p class="_trip_title">Drop Location</p>
                                        <p class="_trip_val">Dhaka</p>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="col-12 col-md-auto">
                            <div class="_ticket_info">
                                <h1 class="_ticket_head_title">Driver Details</h1>

                                <div class="_driver_drop_pro">
                                    <div class="_driver_drop_Pro_pic">
                                        <img src="/car-three.jpg">
                                    </div>
                                    <p class="_driver_drop_name">Jhon David</p>
                                </div>

                                <p class="_driver_drop_info">Tips <span>13</span></p>
                                <p class="_driver_drop_info">Ratings <span>3.5</span></p>
                                <div class="_driver_drop_button">
                                    <button class="_6btn _btn_sm _btn_long">Make a Call</button>
                                </div>
                            </div>
                        </div>

                        <div class="col-12 col-md">
                            <div class="_ticket_info">
                                <h1 class="_ticket_head_title">Price Details</h1>

                                <p class="_price_info">Car Rent fees <span>13121TK</span></p>
                                <p class="_price_info">Taxes & Fees <span>00TK</span></p>
                                <p class="_price_info">Services fees <span>21TK</span></p>

                                <p class="_price_info_total">Total <span>2121313TK</span></p>
                            </div>
                        </div>
                    </div>

                    <div class="_ticket_card_all">
                        <div class="_ticket_card">
                            <div class="row g-0">
                                <div class="col-12 col-md-9">
                                    <div class="_ticket_card_top">
                                        <p class="_ticket_card_top_one">One Way</p>

                                        <p class="_ticket_card_logo">Duare car</p>
                                    </div>

                                    <div class="_ticket_card_main">
                                        <div class="row align-items-center">
                                            <div class="col-12 col-md-3">
                                                <h1 class="_searchRes_card_name">Sedan <span>ac</span></h1>
                                                <div class="_searchRes_card_pic">
                                                    <img src="/car-two.png">
                                                </div>
                                            </div>

                                            <div class="col-12 col-md-auto">
                                                <div class="_searchRes_card_move_time">
                                                    <p class="_searchRes_card_move_title">Time</p>
                                                    <p class="_searchRes_card_move_val _searchRes_card_time">6:30 AM</p>
                                                    <p class="_searchRes_card_move_title _searchRes_card_move">Move to</p>
                                                    <p class="_searchRes_card_move_val">Sylhet</p>
                                                </div>
                                            </div>

                                            <div class="col-12 col-md">
                                                <div class="_searchRes_road">
                                                    <p class="_searchRes_road_time">8h 30m</p>

                                                    <div class="_searchRes_road_icon">
                                                        <svg width="210" height="3" viewBox="0 0 210 3" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                            <line y1="1.5" x2="210" y2="1.5" stroke="white" stroke-width="3" stroke-dasharray="12 12"/>
                                                        </svg>
                                                    </div>
                                                </div>
                                            </div>

                                            <div class="col-12 col-md-auto">
                                                <div class="_searchRes_card_move_time">
                                                    <p class="_searchRes_card_move_title">Time</p>
                                                    <p class="_searchRes_card_move_val _searchRes_card_time">8:00 PM</p>
                                                    <p class="_searchRes_card_move_title">Destination</p>
                                                    <p class="_searchRes_card_move_val _searchRes_card_move">Dhaka</p>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>

                                <div class="col-12 col-md-3">
                                    <div class="_ticket_card_right">
                                        <div class="_ticket_card_top _ticket_card_top_right">
                                            <p class="_ticket_card_top_one">E-Ticket</p>
                                        </div>
                                        
                                        <div class="_ticket_card_main_right">
                                            <p class="_ticket_pass">Passenger Name</p>
                                            <p class="_ticket_pass_val">Jack Dawnson</p>

                                            <div class="row g-2">
                                                <div class="col-auto">
                                                    <p class="_ticket_info_title">Departure Time</p>
                                                    <p class="_ticket_info_val">6:30 AM</p>
                                                </div>
                                                <div class="col-auto">
                                                    <p class="_ticket_info_title">Seats</p>
                                                    <p class="_ticket_info_val">A1, A2, A3</p>
                                                </div>
                                                <div class="col-auto">
                                                    <p class="_ticket_info_title">Type</p>
                                                    <p class="_ticket_info_val">One Way</p>
                                                </div>
                                            </div>

                                            <div class="_ticket_qr">
                                                <img src="/qr.png">

                                                <p class="_ticket_qr_no">No:346566578488948744545444554546578</p>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="row justify-content-center">
                        <div class="col-12 col-md-5 col-lg-4">
                            <div class="_ticket_button">
                                <button class="_6btn _btn_long">Download Ticket Now</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
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