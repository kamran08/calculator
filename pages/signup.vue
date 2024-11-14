<template>
    <div>
        <div class="_login">
            <router-link to="/" class="_login_logo">
                <img src="/duarecar-logo.png" alt="" title="">
            </router-link>

            <div class="container-fluid">
                <div class="row algin-items-center">
                    <!-- Form -->
                    <div class="col-12 col-md-6 col-lg-6"> 
                        <div class="_login_main">
                            <!-- <ul style="margin-left:100px; display: flex; gap:30px;">
                                <li @click="tab = 1">Customer</li>
                                <li @click="tab = 2">Driver</li>
                            </ul> -->

                            <div v-if="tab == 1"class="_login_form">
                                <h2 class="_log_form_title">Sign Up   👋 </h2>
                                <p class="_log_text">Today is a new day. It's your day. You shape it.  </p>

                                <div class="_log_form">
                                    <div class="row">
                                        <div class="col-12 col-md-12 col-lg-12">
                                            <div class="_1input_group">
                                                <p class="_1label">Name</p>
                                                <input v-model="data.first_name" class="_1input" placeholder="Name" type="text">
                                            </div>
                                        </div>
                                        <div class="col-12 col-md-12 col-lg-12">
                                            <div class="_1input_group">
                                                <p class="_1label">Email</p>
                                                <input v-model="data.email" class="_1input" placeholder="Example@email.com" type="text">
                                            </div>
                                        </div>
                                        <div class="col-12 col-md-12 col-lg-12 col-xl-12">
                                            <div class="_1input_group">
                                                <p class="_1label">Password</p>
                                                <div class="_password_input">
                                                    <span @click="showPassword">
                                                        <svg v-if="isShowPassword == false" width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                            <path d="M8.95245 4.2436C9.29113 4.19353 9.64051 4.16667 10.0003 4.16667C14.2545 4.16667 17.0461 7.9207 17.9839 9.40569C18.0974 9.58542 18.1542 9.67528 18.1859 9.81389C18.2098 9.91799 18.2098 10.0822 18.1859 10.1863C18.1541 10.3249 18.097 10.4154 17.9827 10.5963C17.7328 10.9918 17.3518 11.5476 16.8471 12.1504M5.6036 5.59586C3.80187 6.81808 2.57871 8.51615 2.01759 9.4044C1.90357 9.58489 1.84656 9.67514 1.81478 9.81373C1.79091 9.91783 1.7909 10.082 1.81476 10.1861C1.84652 10.3247 1.90328 10.4146 2.01678 10.5943C2.95462 12.0793 5.74618 15.8333 10.0003 15.8333C11.7157 15.8333 13.1932 15.223 14.4073 14.3972M2.50035 2.5L17.5003 17.5M8.23258 8.23223C7.78017 8.68464 7.50035 9.30964 7.50035 10C7.50035 11.3807 8.61963 12.5 10.0003 12.5C10.6907 12.5 11.3157 12.2202 11.7681 11.7678" stroke="#D2D3D6" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                                                        </svg>
                                                        <svg v-else class="_password_input_open" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                            <path d="M2.42012 12.7132C2.28394 12.4975 2.21584 12.3897 2.17772 12.2234C2.14909 12.0985 2.14909 11.9015 2.17772 11.7766C2.21584 11.6103 2.28394 11.5025 2.42012 11.2868C3.54553 9.50484 6.8954 5 12.0004 5C17.1054 5 20.4553 9.50484 21.5807 11.2868C21.7169 11.5025 21.785 11.6103 21.8231 11.7766C21.8517 11.9015 21.8517 12.0985 21.8231 12.2234C21.785 12.3897 21.7169 12.4975 21.5807 12.7132C20.4553 14.4952 17.1054 19 12.0004 19C6.8954 19 3.54553 14.4952 2.42012 12.7132Z" stroke="black" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                                                            <path d="M12.0004 15C13.6573 15 15.0004 13.6569 15.0004 12C15.0004 10.3431 13.6573 9 12.0004 9C10.3435 9 9.0004 10.3431 9.0004 12C9.0004 13.6569 10.3435 15 12.0004 15Z" stroke="black" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                                                        </svg>
                                                    </span>
                                                    <input v-model="data.password" class="_1input" placeholder="At least 8 characters" :type="isShowPassword? 'text' : 'password'">
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col-12 col-md-12 col-lg-12 col-xl-12">
                                            <div class="_1input_group">
                                                <p class="_1label">Confirm Password</p>
                                                <div class="_password_input">
                                                    <span @click="showConPassword">
                                                        <svg v-if="isShowConPassword == false" width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                            <path d="M8.95245 4.2436C9.29113 4.19353 9.64051 4.16667 10.0003 4.16667C14.2545 4.16667 17.0461 7.9207 17.9839 9.40569C18.0974 9.58542 18.1542 9.67528 18.1859 9.81389C18.2098 9.91799 18.2098 10.0822 18.1859 10.1863C18.1541 10.3249 18.097 10.4154 17.9827 10.5963C17.7328 10.9918 17.3518 11.5476 16.8471 12.1504M5.6036 5.59586C3.80187 6.81808 2.57871 8.51615 2.01759 9.4044C1.90357 9.58489 1.84656 9.67514 1.81478 9.81373C1.79091 9.91783 1.7909 10.082 1.81476 10.1861C1.84652 10.3247 1.90328 10.4146 2.01678 10.5943C2.95462 12.0793 5.74618 15.8333 10.0003 15.8333C11.7157 15.8333 13.1932 15.223 14.4073 14.3972M2.50035 2.5L17.5003 17.5M8.23258 8.23223C7.78017 8.68464 7.50035 9.30964 7.50035 10C7.50035 11.3807 8.61963 12.5 10.0003 12.5C10.6907 12.5 11.3157 12.2202 11.7681 11.7678" stroke="#D2D3D6" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                                                        </svg>
                                                        <svg v-else class="_password_input_open" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                            <path d="M2.42012 12.7132C2.28394 12.4975 2.21584 12.3897 2.17772 12.2234C2.14909 12.0985 2.14909 11.9015 2.17772 11.7766C2.21584 11.6103 2.28394 11.5025 2.42012 11.2868C3.54553 9.50484 6.8954 5 12.0004 5C17.1054 5 20.4553 9.50484 21.5807 11.2868C21.7169 11.5025 21.785 11.6103 21.8231 11.7766C21.8517 11.9015 21.8517 12.0985 21.8231 12.2234C21.785 12.3897 21.7169 12.4975 21.5807 12.7132C20.4553 14.4952 17.1054 19 12.0004 19C6.8954 19 3.54553 14.4952 2.42012 12.7132Z" stroke="black" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                                                            <path d="M12.0004 15C13.6573 15 15.0004 13.6569 15.0004 12C15.0004 10.3431 13.6573 9 12.0004 9C10.3435 9 9.0004 10.3431 9.0004 12C9.0004 13.6569 10.3435 15 12.0004 15Z" stroke="black" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                                                        </svg>
                                                    </span>
                                                    <input v-model="data.password_confirmation" class="_1input" placeholder="At least 8 characters" :type="isShowConPassword ? 'text' : 'password'">
                                                </div>
                                            </div>
                                        </div>
                                        <!-- <div class="col-12 col-md-12 col-lg-12">
                                            <div class="_regi_input_group">
                                                <div class="_log_checkBox">
                                                    <input  v-model="agree" type="checkbox" id="agree">
                                                    <label for="agree">I agree with the <a href="">Terms</a> & <a href="">Privacy</a></label>
                                                </div>
                                            </div>
                                        </div> -->
                                        <div class="col-12 col-md-12 col-lg-12">
                                            <div class="_log_button">
                                                <button @click="registration" :disabled="disable" :loading="loading" class="_1btn _btn_long">SIGN UP</button>
                                            </div>
                                        </div>
                                    </div>
                                </div>

                                <div class="_down">
                                    <p class="_or"><span>Or</span></p>

                                    <button class="_3btn _long">
                                        <span>
                                            <svg width="29" height="28" viewBox="0 0 29 28" fill="none" xmlns="http://www.w3.org/2000/svg">
                                            <g clip-path="url(#clip0_673_1673)">
                                            <path d="M28.227 14.3213C28.227 13.3696 28.1499 12.4128 27.9853 11.4766H14.78V16.8677H22.342C22.0283 18.6065 21.02 20.1446 19.5436 21.122V24.6201H24.0551C26.7044 22.1817 28.227 18.5807 28.227 14.3213Z" fill="#4285F4"/>
                                            <path d="M14.78 28.0009C18.5559 28.0009 21.7402 26.7611 24.0602 24.6211L19.5487 21.1231C18.2935 21.977 16.6731 22.4606 14.7852 22.4606C11.1328 22.4606 8.03596 19.9965 6.92481 16.6836H2.26929V20.2897C4.64592 25.0172 9.48663 28.0009 14.78 28.0009Z" fill="#34A853"/>
                                            <path d="M6.91966 16.6851C6.33322 14.9464 6.33322 13.0636 6.91966 11.3248V7.71875H2.26928C0.283612 11.6747 0.283612 16.3353 2.26928 20.2912L6.91966 16.6851Z" fill="#FBBC04"/>
                                            <path d="M14.78 5.54127C16.776 5.51041 18.7051 6.26146 20.1506 7.64012L24.1477 3.64305C21.6167 1.26642 18.2575 -0.0402103 14.78 0.000943444C9.48663 0.000943444 4.64592 2.98459 2.26929 7.71728L6.91966 11.3234C8.02567 8.00536 11.1276 5.54127 14.78 5.54127Z" fill="#EA4335"/>
                                            </g>
                                            <defs>
                                            <clipPath id="clip0_673_1673">
                                            <rect width="28" height="28" fill="white" transform="translate(0.5)"/>
                                            </clipPath>
                                            </defs>
                                            </svg>
                                        </span>
                                        Sign in with Google
                                    </button>
                                    <button class="_3btn _long">
                                        <span>
                                            <svg width="29" height="28" viewBox="0 0 29 28" fill="none" xmlns="http://www.w3.org/2000/svg">
                                            <g clip-path="url(#clip0_673_662)">
                                            <path d="M28.5 14C28.5 6.26801 22.232 0 14.5 0C6.76801 0 0.5 6.26801 0.5 14C0.5 20.9877 5.61957 26.7796 12.3125 27.8299V18.0469H8.75781V14H12.3125V10.9156C12.3125 7.40687 14.4027 5.46875 17.6005 5.46875C19.1318 5.46875 20.7344 5.74219 20.7344 5.74219V9.1875H18.9691C17.23 9.1875 16.6875 10.2668 16.6875 11.375V14H20.5703L19.9496 18.0469H16.6875V27.8299C23.3804 26.7796 28.5 20.9877 28.5 14Z" fill="#1877F2"/>
                                            <path d="M19.9496 18.0469L20.5703 14H16.6875V11.375C16.6875 10.2679 17.23 9.1875 18.9691 9.1875H20.7344V5.74219C20.7344 5.74219 19.1323 5.46875 17.6005 5.46875C14.4027 5.46875 12.3125 7.40688 12.3125 10.9156V14H8.75781V18.0469H12.3125V27.8299C13.762 28.0567 15.238 28.0567 16.6875 27.8299V18.0469H19.9496Z" fill="white"/>
                                            </g>
                                            <defs>
                                            <clipPath id="clip0_673_662">
                                            <rect width="28" height="28" fill="white" transform="translate(0.5)"/>
                                            </clipPath>
                                            </defs>
                                            </svg>
                                        </span>
                                        Sign in with Facebook
                                    </button>
                                </div>

                                <p class="_donot">Don't you have an account? <router-link to="/login">Sign in</router-link></p>
                            </div>

                            <p class="_all">© 2024 ALL RIGHTS RESERVED</p>
                        </div>
                    </div>
                    <!-- Form -->

                    <!-- Slider -->
                    <div class="col-12 col-md-6 col-lg-6">
                        <div class="_log_slider">
                            <div class="_log_slider_main">
                                <img class="poly_one" src="/polygon1.png" alt="" title="">
                                <img class="poly_two" src="/polygon2.png" alt="" title="">
                                <img class="poly_three" src="/polygon3.png" alt="" title="">

                                <Carousel 
                                class="_log_carousel" 
                                loop
                                :autoplay="setting.autoplay"
                                :autoplay-speed="setting.autoplaySpeed"
                                :dots="setting.dots"
                                :radius-dot="setting.radiusDot"
                                :trigger="setting.trigger"
                                :arrow="setting.arrow"
                                >
                                    <CarouselItem>
                                        <div class="_log_slider_pic">
                                            <img class="_log_slider_img" src="/frame1.png" alt="" title="">
                                        </div>

                                        <div class="_log_bottom">
                                            <!-- <h1 class="_log_slider_title">duare car</h1> -->
                                            <p class="_log_slider_text">Travel<i> comfortably and conveniently</i></p>
                                        </div>
                                    </CarouselItem>
                                    <CarouselItem>
                                        <div class="_log_slider_pic">
                                            <img class="_log_slider_img" src="/frame1.png" alt="" title="">
                                        </div>

                                        <div class="_log_bottom">
                                            <!-- <h1 class="_log_slider_title">duare car</h1> -->
                                            <p class="_log_slider_text">Travel<i> comfortably and conveniently</i></p>
                                        </div>
                                    </CarouselItem>
                                    <CarouselItem>
                                        <div class="_log_slider_pic">
                                            <img class="_log_slider_img" src="/frame1.png" alt="" title="">
                                        </div>

                                        <div class="_log_bottom">
                                            <!-- <h1 class="_log_slider_title">duare car</h1> -->
                                            <p class="_log_slider_text">Travel<i> comfortably and conveniently</i></p>
                                        </div>
                                    </CarouselItem>
                                    <CarouselItem>
                                        <div class="_log_slider_pic">
                                            <img class="_log_slider_img" src="/frame1.png" alt="" title="">
                                        </div>

                                        <div class="_log_bottom">
                                            <!-- <h1 class="_log_slider_title">duare car</h1> -->
                                            <p class="_log_slider_text">Travel<i> comfortably and conveniently</i></p>
                                        </div>
                                    </CarouselItem>
                                </Carousel>
                            </div>
                        </div>
                    </div>
                    <!-- Slider -->
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    // middleware : 'guest',
    components: {
    },

    data(){
        return{
            isShowConPassword: false,
            isShowPassword: false,
            setting: {
                // autoplay: true,
                autoplaySpeed: 2000,
                dots: 'outside',
                radiusDot: true,
                trigger: 'click',
                arrow: 'never'
            },
            tab:1,
            loading: false,
            disable: false,
            agree:false,
            data:{
                first_name:'',
                email:'',
                password_confirmation:'',
                password:'',
                user_type:'user'
            },
            reg: /^(([^<>()\[\]\\.,;:\s@"]+(\.[^<>()\[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,24}))$/,
        }
    },
    methods:{
        async registration(){
            if(!this.data.first_name || this.data.first_name.trim()==''){
               return this.e("Name is required!")
            }
            if (!this.data.email) {
                return this.e("Email is required!")
            }
            if (!this.reg.test(this.data.email)) {
               return this.e("Invalid email format!")
            }
            if(!this.data.password || this.data.password.trim()==''){
                return this.e("Password is required!")
            }
            if(!this.data.password_confirmation || this.data.password_confirmation.trim()==''){
                return this.e("Confirm password is required!")
            }
            if(this.data.password_confirmation != this.data.password){
                return this.e("Password does not match!")
            }
            // if(this.agree != true){
            //     return this.e("Agree with the Terms & Condition!")
            // }

            this.loading = true
            this.disable = true
            
            const res = await this.callApi('post','/auth/register',this.data)
            if(res.status==200){
                // localStorage.setItem('regiEmail', this.data.email);
                this.first_name = ''
                this.email = ''
                this.password_confirmation = ''
                this.password = ''
                this.s(res.data.msg)
                window.location = '/login'
            }
            else if(res.status==401){
                this.loading = false
                this.disable = false 
                return this.e(res.data[0].message)
                // this.e(res.data.msg)
            }
            else if(res.status==402){
                this.loading = false
                this.disable = false
                if(res.data.data.is_active == 0){
                    // localStorage.setItem('regiEmail', res.data.data.email);
                    window.location = '/login'
                    return this.s('You need to verify your account!')
                }else{
                    return this.e(res.data.msg)
                }
            }
            else this.swr()

            this.loading = false
            this.disable = false
        },

        showPassword (){
            this.isShowPassword = !this.isShowPassword
        },
        
        showConPassword (){
            this.isShowConPassword = !this.isShowConPassword
        },
        
        async handleImageUpload(res, file) {
            if (res) {
                this.data.image = res;
            }
        },

        handleRemove(p) {
            this.data.image = ""
        },

        handleFormatError(file) {
            this.$Notice.warning({
                title: "The file format is incorrect",
                desc:
                "File format of " +
                file.name +
                " is incorrect, please select jpg or png."
            });
        },

        handleMaxSize(file) {
            this.$Notice.warning({
                title: "Exceeding file size limit",
                desc: "File  " + file.name + " is too large, no more than 5M."
            });
        },
    },


}
</script>


<style>
.demo-upload-list{
        display: inline-block;
        width: 60px;
        height: 60px;
        text-align: center;
        line-height: 60px;
        border: 1px solid transparent;
        border-radius: 4px;
        overflow: hidden;
        background: #fff;
        position: relative;
        box-shadow: 0 1px 1px rgba(0,0,0,.2);
        margin-right: 4px;
}
.demo-upload-list img{
    width: 100%;
    height: 100%;
}
.demo-upload-list-cover{
    display: none;
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    background: rgba(0,0,0,.6);
}
.demo-upload-list:hover .demo-upload-list-cover{
    display: block;
}
.demo-upload-list-cover i{
    color: #fff;
    font-size: 20px;
    cursor: pointer;
    margin: 0 2px;
}
</style>