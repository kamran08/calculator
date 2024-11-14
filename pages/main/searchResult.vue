<template>
    <div>
        <mainMenu/>

        <div class="_1content">
            <div class="_searchRes">
                <div class="_searchRes_sea">
                    <div class="container">
                        <div class="_home_search _searchRes_sea_main">
                            <div class="_home_search_top">
                                <ul class="_home_search_top_list">
                                    <li><span class="_home_search_top_list_span">Book  a car Now</span></li>

                                    <li>
                                    <RadioGroup>
                                        <Radio label="oneWay">
                                            <span>One Way</span>
                                        </Radio>
                                        <Radio label="return">
                                            <span>Return</span>
                                        </Radio>
                                    </RadioGroup>
                                    </li>
                                </ul>
                            </div>

                            <div class="_home_search_main">
                                <div class="row g-2 align-items-center">
                                    <div class="col-12 col-md">
                                    <div class="_home_search_imput">
                                        <Select v-model="searchData.from_sub_district_id" size="large" filterable placeholder="City">
                                            <Option v-for="(item, index) in subDistricts" :value="item.id" :key="index">{{ item.name }}</Option>
                                        </Select>
                                    </div>
                                    </div>
                                    <div class="col-auto">
                                        <svg width="20" height="17" viewBox="0 0 20 17" fill="none" xmlns="http://www.w3.org/2000/svg">
                                            <path opacity="0.3" d="M19.2499 12.4367H2.61992L4.05992 10.9967C4.18946 10.8625 4.26185 10.6832 4.26185 10.4967C4.26185 10.3102 4.18946 10.1309 4.05992 9.99668C3.9193 9.85623 3.72867 9.77734 3.52992 9.77734C3.33117 9.77734 3.14055 9.85623 2.99992 9.99668L0.279922 12.6867C0.158949 12.8252 0.0922852 13.0028 0.0922852 13.1867C0.0922852 13.3706 0.158949 13.5482 0.279922 13.6867L2.99992 16.6967C3.07166 16.7732 3.15844 16.834 3.25482 16.8753C3.35119 16.9166 3.45507 16.9375 3.55992 16.9367C3.74579 16.9352 3.92429 16.8638 4.05992 16.7367C4.19798 16.5948 4.27522 16.4046 4.27522 16.2067C4.27522 16.0087 4.19798 15.8186 4.05992 15.6767L2.52992 13.9967H19.2499C19.4488 13.9967 19.6396 13.9177 19.7803 13.777C19.9209 13.6364 19.9999 13.4456 19.9999 13.2467C19.9999 13.0478 19.9209 12.857 19.7803 12.7164C19.6396 12.5757 19.4488 12.4967 19.2499 12.4967V12.4367Z" fill="#3E97FF"/>
                                            <path d="M19.78 3.20818L17 0.358177C16.8658 0.228641 16.6865 0.15625 16.5 0.15625C16.3135 0.15625 16.1342 0.228641 16 0.358177C15.877 0.495682 15.809 0.673694 15.809 0.858177C15.809 1.04266 15.877 1.22067 16 1.35818L17.48 2.85818H0.790007C0.607292 2.87938 0.43874 2.96699 0.316401 3.10435C0.194061 3.24171 0.126465 3.41924 0.126465 3.60318C0.126465 3.78712 0.194061 3.96464 0.316401 4.102C0.43874 4.23936 0.607292 4.32697 0.790007 4.34818H17.56L16.07 5.84818C15.9658 5.95246 15.8947 6.08512 15.8655 6.2296C15.8363 6.37408 15.8503 6.52397 15.9057 6.66053C15.9612 6.7971 16.0557 6.91429 16.1774 6.99746C16.2991 7.08063 16.4426 7.1261 16.59 7.12818C16.7704 7.15284 16.9534 7.1062 17.1 6.99818L19.78 4.30818C19.8533 4.23508 19.9108 4.14758 19.9486 4.0512C19.9865 3.95483 20.004 3.85165 20 3.74818C19.9982 3.54671 19.9195 3.35354 19.78 3.20818Z" fill="#3E97FF"/>
                                        </svg>
                                    </div>
                                    <div class="col-12 col-md">
                                    <div class="_home_search_imput">
                                        <Select v-model="searchData.to_sub_district_id" size="large" filterable placeholder="City">
                                            <Option v-for="(item, index) in subDistricts" :value="item.id" :key="index">{{ item.name }}</Option>
                                        </Select>
                                    </div>
                                    </div>
                                    <div class="col-12 col-md">
                                    <div class="_home_search_imput">
                                        <DatePicker v-model="searchData.pick_up_date" type="date" placeholder="Date" style="width: 100%" />
                                    </div>
                                    </div>
                                    <div class="col-12 col-md">
                                    <div class="_home_search_imput">
                                        <Select v-model="searchData.passengers" placeholder="Passenger">
                                            <Option value="1">1</Option>
                                            <Option value="2">2</Option>
                                            <Option value="3">3</Option>
                                            <Option value="4">4</Option>
                                            <Option value="5">5</Option>
                                            <Option value="6">6</Option>
                                            <Option value="7">7</Option>
                                            <Option value="8">8</Option>
                                            <Option value="9">9</Option>
                                            <Option value="10">10</Option>
                                        </Select>
                                    </div>
                                    </div>

                                    <div class="col-12 col-md">
                                    <div class="_home_search_imput">
                                        <button @click="getSearchData" class="_6btn _btn_long">SEARCH</button>
                                    </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Cards -->
                <div class="_searchRes_main">
                    <div class="container">
                        <div class="_searchRes_top align-items-center">
                            <!-- <p class="_searchRes_res_num">{{ availableFleet.data.length }} result found</p> -->
                            <p class="_searchRes_res_num"><span v-if="availableFleet.meta">{{ availableFleet.meta.total }}</span> result found</p>

                            <div class="_filter">
                                <div class="_filter_one">
                                    <svg width="12" height="10" viewBox="0 0 12 10" fill="none" xmlns="http://www.w3.org/2000/svg">
                                        <path d="M0 1C0 0.447715 0.447715 0 1 0H11C11.5523 0 12 0.447715 12 1C12 1.55228 11.5523 2 11 2H1C0.447715 2 0 1.55228 0 1Z" fill="#171D27"/>
                                        <path d="M2 5C2 4.44772 2.44772 4 3 4H9C9.55229 4 10 4.44772 10 5C10 5.55228 9.55229 6 9 6H3C2.44772 6 2 5.55228 2 5Z" fill="#171D27"/>
                                        <path d="M5 8C4.44772 8 4 8.44771 4 9C4 9.55229 4.44772 10 5 10H7C7.55228 10 8 9.55229 8 9C8 8.44771 7.55228 8 7 8H5Z" fill="#171D27"/>
                                    </svg>
                                </div>
                                <p class="_filter_text">Filters</p>
                                <div class="_filter_two">1</div>
                            </div>
                        </div>

                        <div class="_searchRes_card_all">
                            <template v-if="availableFleet && availableFleet.data && availableFleet.data.length">
                                <!-- Item -->
                                <div v-for="(item, index) in availableFleet.data" :value="item.id" :key="index" class="_searchRes_card">
                                    <div class="row align-items-center">
                                        <div class="col-12 col-md-3">
                                            <h1 class="_searchRes_card_name">{{ item.fleet.vehicle_name }}  
                                                <span v-if="item.fleet.vehicle_features == 'air_conditioner'">ac</span>
                                                <span v-if="item.fleet.vehicle_features == 'non_air_conditioner'">non ac</span>
                                            </h1>
                                            
                                            <Carousel 
                                                class="_secThree_slider_main" 
                                                loop
                                                :autoplay="setting.autoplay"
                                                :autoplay-speed="setting.autoplaySpeed"
                                                :dots="setting.dots"
                                                :radius-dot="setting.radiusDot"
                                                :trigger="setting.trigger"
                                                :arrow="setting.arrow"
                                                >
                                                <CarouselItem  v-for="(item2, index2) in item.fleet_images" :value="item.id" :key="index2" fleet_images>
                                                    <div class="_searchRes_card_pic">
                                                        <img :src="item2.image">
                                                    </div>
                                                </CarouselItem>
                                            </Carousel>
                                        </div>
    
                                        <div class="col-12 col-md-auto">
                                            <div class="_searchRes_card_move_time _text_right">
                                                <p class="_searchRes_card_move_title">Time</p>
                                                <p class="_searchRes_card_move_val _searchRes_card_time">{{ item.pick_up_time }}</p>
                                                <p class="_searchRes_card_move_title _searchRes_card_move">Move to</p>
                                                <p class="_searchRes_card_move_val">{{ item.fromSubDistrict.name }}</p>
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
                                                <p class="_searchRes_card_move_val _searchRes_card_time">{{ item.drop_up_time }}</p>
                                                <p class="_searchRes_card_move_title">Destination</p>
                                                <p class="_searchRes_card_move_val _searchRes_card_move">{{ item.toSubDistrict.name }}</p>
                                            </div>
                                        </div>
    
                                        <div class="col-12 col-md">
                                            <div class="_searchRes_card_date_day">
                                                <p class="_searchRes_card_date">{{ item.pick_up_date }}</p>
                                                <p class="_searchRes_card_day">Thursday</p>
                                            </div>
                                        </div>
    
                                        <div class="col-12 col-md-2">
                                            <div class="_searchRes_card_details">
                                                <h1 class="_searchRes_card_price">{{ item.price }} <span>TK</span></h1>
                                                    <ul class="_rating _searchRes_card_rating">
                                                        <li>
                                                            <svg width="27" height="27" viewBox="0 0 27 27" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                            <path d="M13.5258 21.0857L21.7876 26.0722L19.5951 16.6741L26.8944 10.3507L17.2824 9.53524L13.5258 0.671875L9.76924 9.53524L0.157227 10.3507L7.45647 16.6741L5.26402 26.0722L13.5258 21.0857Z" fill="#F8A401"/>
                                                            </svg>
                                                        </li>
                                                        <li>
                                                            <svg width="27" height="27" viewBox="0 0 27 27" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                            <path d="M13.5258 21.0857L21.7876 26.0722L19.5951 16.6741L26.8944 10.3507L17.2824 9.53524L13.5258 0.671875L9.76924 9.53524L0.157227 10.3507L7.45647 16.6741L5.26402 26.0722L13.5258 21.0857Z" fill="#F8A401"/>
                                                            </svg>
                                                        </li>
                                                        <li>
                                                            <svg width="27" height="27" viewBox="0 0 27 27" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                            <path d="M13.5258 21.0857L21.7876 26.0722L19.5951 16.6741L26.8944 10.3507L17.2824 9.53524L13.5258 0.671875L9.76924 9.53524L0.157227 10.3507L7.45647 16.6741L5.26402 26.0722L13.5258 21.0857Z" fill="#F8A401"/>
                                                            </svg>
                                                        </li>
                                                        <li>
                                                            <svg width="27" height="27" viewBox="0 0 27 27" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                            <path d="M13.5258 21.0857L21.7876 26.0722L19.5951 16.6741L26.8944 10.3507L17.2824 9.53524L13.5258 0.671875L9.76924 9.53524L0.157227 10.3507L7.45647 16.6741L5.26402 26.0722L13.5258 21.0857Z" fill="#F8A401"/>
                                                            </svg>
                                                        </li>
                                                        <li>
                                                            <svg width="28" height="27" viewBox="0 0 28 27" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                            <path d="M27.3265 10.3507L17.7145 9.52188L13.9579 0.671875L10.2014 9.53524L0.589355 10.3507L7.8886 16.6741L5.69615 26.0722L13.9579 21.0857L22.2197 26.0722L20.0406 16.6741L27.3265 10.3507ZM13.9579 18.5858L8.93135 21.6204L10.2682 15.8987L5.82984 12.0485L11.6853 11.5405L13.9579 6.15299L16.244 11.5539L22.0994 12.0619L17.661 15.9121L18.9979 21.6338L13.9579 18.5858Z" fill="#F8A401"/>
                                                            </svg>
                                                        </li>
                                                    </ul>
    
                                                <div class="_searchRes_card_button">
                                                    <button  @click="$router.push(`/main/resultDetails/${item.id}`)" class="_6btn _btn_long">BOOK</button>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                <!-- Item -->
                            </template>

                            <div v-else class="_text_center">
                                No data found!
                            </div>
                        </div>
                    </div>
                </div>
                <!-- cards -->
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
            setting: {
                // autoplay: true,
                autoplaySpeed: 2000,
                dots: 'none',
                // radiusDot: false,
                trigger: 'click',
                // arrow: 'never'
            },
            availableFleet: {},
            subDistricts : {},
            searchData: {
                page:1,
                pageSize:10,
                from_sub_district_id : '',
                to_sub_district_id : '',
                pick_up_date : '',
                passengers : '',
            }
        }
    },


    methods:{
        async getSearchData(){
            this.getAvailableFleetBySearch()
            // this.$route.query.location = this.searchData.from_sub_district_id
            // this.$route.query.dropup = this.searchData.to_sub_district_id
            // this.searchData.pick_up_date = this.$route.query.pickupdate
            // this.searchData.passengers = this.$route.query.passengers
        },

        async getAvailableFleetBySearch(){
            // const res = await this.callApi('get', `/admin/availableFleet/getAvailableFleetBySearch?location=${this.searchData.from_sub_district_id}&dropup=${this.searchData.to_sub_district_id}&date=${this.searchData.pick_up_date}&passengers=${this.searchData.passengers}`)
            const res = await this.callApi('post','/admin/availableFleet/getAvailableFleetBySearch',this.searchData)
            if(res.status == 200){
                this.availableFleet = res.data
            }
            else this.swr();
        }
    },
  
    async created(){
        const [res1, res2] = await Promise.all([
            this.callApi('get',`/admin/availableFleet/getAllSubDistrict`),
            this.callApi('get',`/admin/availableFleet/getDistricts`),
        ]);
        if(res1.status == 200 && res2.status ==200 ){
            this.subDistricts = res1.data
            this.districts = res2.data
            // this.bloodGroups = res3.data
        }
        else this.swr();

        this.searchData.from_sub_district_id = this.$route.query.location
        this.searchData.to_sub_district_id = this.$route.query.dropup
        this.searchData.pick_up_date = this.$route.query.pickupdate
        this.searchData.passengers = this.$route.query.passengers

        console.log("Vehicle name is required!", this.searchData)
        this.getAvailableFleetBySearch()

    }
}
</script>