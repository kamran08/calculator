<template>
    <div>
        <div :class="(scrollY>150)? '_1menu_scroll': ''" class="_menu">
            <div class="container">
                <div class="_menu_con">
                    <div class="row align-items-center">
                        <div class="col-12 col-md col-lg">
                            <ul class="_menu_left_list">
                                <li>
                                    <router-link :class="$route.path == '/'? '_menu_left_list_text _active':'_menu_left_list_text'" to="/">Home</router-link>
                                </li>
                                <li>
                                    <router-link :class="$route.path == '/main/aboutUs'? '_menu_left_list_text _active':'_menu_left_list_text'" to="/main/aboutUs">About</router-link>
                                </li>
                                <li>
                                    <router-link :class="$route.path == '/main/contact'? '_menu_left_list_text _active':'_menu_left_list_text'" to="/main/contact">Contact</router-link>
                                </li>
                            </ul>
                        </div>

                        <div class="col-12 col-md-auto col-lg-auto">
                            <router-link class="_menu_logo" to="/">
                                
                                <img class="_two" src="/driver_logo.png" alt="" title="">
                            </router-link>
                        </div>
                        <div v-if="!authUser" class="col-12 col-md col-lg">
                            <div class="_menu_right">
                                <router-link class="_menu_right_list" to="/login">Login</router-link>
                                <router-link class="_menu_right_list" to="/signup">Sign up</router-link>
                            </div> 
                        </div>
                        <div v-else class="col-12 col-md col-lg">
                            <div class="_menu_right">
                                <a class="_menu_right_list" href="">History</a>
                                <a class="_menu_right_list" href="">Payment</a>
                                <Dropdown trigger="click" style="margin-left: 20px">
                                <a href="javascript:void(0)">
                                    <div class="_menu_pro">
                                        <div v-if="authUser" class="_menu_pro_pic">
                                            <img :src="authUser.image">                            
                                        </div>
                                        <p class="_menu_pro_name">{{ authUser.first_name }} {{ authUser.last_name }}</p>
                                        <span>
                                            <svg width="12" height="8" viewBox="0 0 12 8" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                <path d="M1 1.5L6 6.5L11 1.5" stroke="#181C32" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                                            </svg>
                                        </span>
                                    </div>
                                    </a>
                                    <template #list>
                                        <DropdownMenu>
                                            <DropdownItem v-if="(authUser.user_type == 'driver') || (authUser.user_type == 'admin')"><router-link class="" to="/admin"><p>Admin Penel</p></router-link></DropdownItem>
                                            <DropdownItem><p @click="logout" class="" href="">Log out</p></DropdownItem>
                                        </DropdownMenu>
                                    </template>
                                </Dropdown>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>


<script>
// import auth from '~/middleware/auth';
import { mapGetters } from "vuex";
export default {
    data(){
        return{
            scrollY: 0,
        }
    },

    methods:{
        handleScroll(){
            this.scrollY = window.scrollY
        },

        async logout(){
            const res = await this.callApi('get', '/auth/logout')
            if(res.status==200){
                this.$store.commit('loginUser', false)
                // window.location = '/'
            }
        },
    },

    computed: {
       
    },

    async created(){
        
    },
    
    mounted(){
        window.addEventListener('scroll', this.handleScroll);
    },
}
</script>