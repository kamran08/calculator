<template>
    <div>
        <mainMenu/>

        <div class="_1content">
            <!-- Top -->
            <div v-if="alldata" class="_resDetails_top">
                <div class="container">
                    <div class="row">
                        <div class="col-12 col-md">
                            <p class="_resDetails_title">From</p>
                            <p v-if="alldata.fromSubDistrict" class="_resDetails_val">{{ alldata.fromSubDistrict.name }}</p>
                        </div>
                        <div class="col-12 col-md">
                            <p class="_resDetails_title">To</p>
                            <p v-if="alldata.toSubDistrict"class="_resDetails_val">{{ alldata.toSubDistrict.name }}</p>
                        </div>
                        <div class="col-12 col-md">
                            <p class="_resDetails_title">Time</p>
                            <p class="_resDetails_val">{{ alldata.pick_up_time }}</p>
                        </div>
                        <div class="col-12 col-md">
                            <p class="_resDetails_title">Pessengers</p>
                            <p class="_resDetails_val">3</p>
                        </div>
                        <div class="col-12 col-md">
                            <p class="_resDetails_title">Date</p>
                            <p class="_resDetails_val">{{ alldata.pick_up_date }}</p>
                        </div>
                        <div class="col-12 col-md-auto">
                            <p class="_resDetails_title">Fair</p>
                            <p class="_resDetails_val">{{ alldata.price }} TK</p>
                        </div>
                    </div>
                </div>
            </div>
            <!-- Top -->

            <!-- Main -->
            <div class="_resDetails_main">
                <div class="container">
                    <div class="_resDetails_info">
                        <p class="_resDetails_info_title">Vehicle information :</p>
                        <p v-if="alldata.fleet" class="_resDetails_info_val"><span>Number :</span> {{ alldata.fleet.vehicle_model }}</p>
                        <p v-if="alldata.driver" class="_resDetails_info_val"><span>Driver Name:</span>  {{ alldata.driver.user_id }}</p>
                        <p v-if="alldata.driver" class="_resDetails_info_val"><span>Driver Number :</span> {{ alldata.driver.user_id }}</p>
                    </div>

                    <div class="_resDetails_det">
                        <div class="row g-0">
                            <div class="col-12 col-md-6">
                                <div class="_resDetails_left">
                                    <img class="_resDetails_left_pic" src="/CAR.png">
                                </div>
                            </div>
                            <div class="col-12 col-md-6">
                                <div class="_resDetails_right">
                                    <h1 class="_resDetails_right_title">BOOK YOUR SEAT</h1>
                                    
                                    <ul class="_resDetails_ava">
                                        <li>Available Seats</li>
                                        <li class="_resDetails_ava_not">Sold Out Seats</li>
                                    </ul>

                                    <div class="_resDetails_form">
                                        <h3 class="_resDetails_form_title">Booking Details</h3>

                                        <ul class="_resDetails_seats">
                                            <li>Selected Seat</li>
                                            <li>
                                                A1 
                                                <span>
                                                    <svg width="9" height="10" viewBox="0 0 9 10" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                        <path d="M6.16667 2.4987V2.16536C6.16667 1.69865 6.16667 1.4653 6.07584 1.28704C5.99594 1.13024 5.86846 1.00275 5.71166 0.922859C5.5334 0.832031 5.30004 0.832031 4.83333 0.832031H4.16667C3.69996 0.832031 3.4666 0.832031 3.28834 0.922859C3.13154 1.00275 3.00406 1.13024 2.92416 1.28704C2.83333 1.4653 2.83333 1.69865 2.83333 2.16536V2.4987M3.66667 4.79036V6.8737M5.33333 4.79036V6.8737M0.75 2.4987H8.25M7.41667 2.4987V7.16536C7.41667 7.86543 7.41667 8.21546 7.28042 8.48285C7.16058 8.71806 6.96936 8.90928 6.73415 9.02912C6.46677 9.16536 6.11673 9.16536 5.41667 9.16536H3.58333C2.88327 9.16536 2.53323 9.16536 2.26585 9.02912C2.03064 8.90928 1.83942 8.71806 1.71958 8.48285C1.58333 8.21546 1.58333 7.86543 1.58333 7.16536V2.4987" stroke="white" stroke-linecap="round" stroke-linejoin="round"/>
                                                    </svg>
                                                </span>
                                            </li>
                                            <li>
                                                A2
                                                <span>
                                                    <svg width="9" height="10" viewBox="0 0 9 10" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                        <path d="M6.16667 2.4987V2.16536C6.16667 1.69865 6.16667 1.4653 6.07584 1.28704C5.99594 1.13024 5.86846 1.00275 5.71166 0.922859C5.5334 0.832031 5.30004 0.832031 4.83333 0.832031H4.16667C3.69996 0.832031 3.4666 0.832031 3.28834 0.922859C3.13154 1.00275 3.00406 1.13024 2.92416 1.28704C2.83333 1.4653 2.83333 1.69865 2.83333 2.16536V2.4987M3.66667 4.79036V6.8737M5.33333 4.79036V6.8737M0.75 2.4987H8.25M7.41667 2.4987V7.16536C7.41667 7.86543 7.41667 8.21546 7.28042 8.48285C7.16058 8.71806 6.96936 8.90928 6.73415 9.02912C6.46677 9.16536 6.11673 9.16536 5.41667 9.16536H3.58333C2.88327 9.16536 2.53323 9.16536 2.26585 9.02912C2.03064 8.90928 1.83942 8.71806 1.71958 8.48285C1.58333 8.21546 1.58333 7.86543 1.58333 7.16536V2.4987" stroke="white" stroke-linecap="round" stroke-linejoin="round"/>
                                                    </svg>
                                                </span>
                                            </li>
                                            <li>
                                                A3
                                                <span>
                                                    <svg width="9" height="10" viewBox="0 0 9 10" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                        <path d="M6.16667 2.4987V2.16536C6.16667 1.69865 6.16667 1.4653 6.07584 1.28704C5.99594 1.13024 5.86846 1.00275 5.71166 0.922859C5.5334 0.832031 5.30004 0.832031 4.83333 0.832031H4.16667C3.69996 0.832031 3.4666 0.832031 3.28834 0.922859C3.13154 1.00275 3.00406 1.13024 2.92416 1.28704C2.83333 1.4653 2.83333 1.69865 2.83333 2.16536V2.4987M3.66667 4.79036V6.8737M5.33333 4.79036V6.8737M0.75 2.4987H8.25M7.41667 2.4987V7.16536C7.41667 7.86543 7.41667 8.21546 7.28042 8.48285C7.16058 8.71806 6.96936 8.90928 6.73415 9.02912C6.46677 9.16536 6.11673 9.16536 5.41667 9.16536H3.58333C2.88327 9.16536 2.53323 9.16536 2.26585 9.02912C2.03064 8.90928 1.83942 8.71806 1.71958 8.48285C1.58333 8.21546 1.58333 7.86543 1.58333 7.16536V2.4987" stroke="white" stroke-linecap="round" stroke-linejoin="round"/>
                                                    </svg>
                                                </span>
                                            </li>
                                        </ul>

                                        <div class="_resDetails_pickPoint">
                                            <p class="_resDetails_pickPoint_title">Choose Boarding Point</p>
                                            
                                            <select class="_2input">
                                                <option>Humayun Rashid Chattar</option>
                                            </select>
                                        </div>

                                        <div class="_resDetails_pickPoint">
                                            <p class="_resDetails_pickPoint_title">Choose Boarding Point</p>
                                            
                                            <div class="row align-items-center">
                                                <div class="col-12 col-md-8">
                                                    <input class="_2input" placeholder="Phone">
                                                </div>

                                                <div class="col-12 col-md">
                                                    <button class="_6btn _btn_long">APPLY</button>
                                                </div>
                                            </div>
                                        </div>
                                    </div>

                                    <div class="_resDetails_form">
                                        <p class="_resDetails_pickPoint_title">Choose Boarding Point</p>
                                            
                                        <RadioGroup class="_payment_type_list">
                                            <Radio label="bKash">
                                                <div class="_payment_type_list_item">
                                                    <p class="_payment_type_name">bKash</p>
                                                    <img class="_bkash_img" src="/bkash.png">
                                                </div>
                                            </Radio>
                                            <Radio label="Bank">
                                                <div class="_payment_type_list_item">
                                                    <p class="_payment_type_name">Bank Transfer</p>
                                                </div>
                                            </Radio>
                                        </RadioGroup>

                                        <div class="_resDetails_pay_button">
                                            <router-link to="/main/ticket"><button class="_6btn _btn_long">PAYMENT</button></router-link>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <!-- Main -->
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
        alldata:{},
    }
  },


  methods:{
    
  },
  
  async created(){
    const res = await this.callApi('get', `/admin/availableFleet/getSingleAvaiFleet/${this.$route.params.id}`)
    if(res.status==200){
        this.alldata = res.data
    }
  }
}
</script>