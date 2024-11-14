<template>
    <div>
        <div class="_login">
            <div class="container-fluid">
                <div class="row">
                    <!-- Form -->
                    <div class="col-12 col-md-6 col-lg-6"> 
                        <div class="_login_main">
                            <a href="" class="_login_logo">
                                <img src="/duarecar-logo.png" alt="" title="">
                            </a>
                            <div class="_login_form">
                                <h2 class="_log_form_title">Verification </h2>
                                <p class="_log_text">A verification code sent to {{ regiEmail }} </p>

                                <div class="_log_form">
                                    <div class="row">
                                        <div class="col-12 col-md-12 col-lg-12">
                                            <div class="_1input_group">
                                                <p class="_1label">Confirm Code</p>
                                                <input v-model="data.confirm_code" class="_1input" placeholder="Confirm Code" type="text">
                                            </div>
                                        </div>
                                        <div class="col-12 col-md-12 col-lg-12">
                                            <div class="_log_button _log_button_group">
                                                <p :disabled="disable" :loading="loading" @click="sendAgain" class="_send_again">Send again</p>
                                                <button :disabled="disable" :loading="loading" @click="submit" class="_1btn">Submit</button>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>

                            <p class="_all">© 2024 ALL RIGHTS RESERVED</p>
                        </div>
                    </div>
                    <!-- Form -->

                    <!-- Slider -->
                    <div class="col-12 col-md-6 col-lg-6">
                        <div class="_log_slider">
                            <div class="_log_slider_main">
                                <div class="_log_slider_pic">
                                    <img class="_log_slider_img" src="/loginArt.png" alt="" title="">
                                </div>

                                <div class="_log_bottom">
                                    <h1 class="_log_slider_title">duare car</h1>
                                    <p class="_log_slider_text">Travel comfortably and conveniently</p>
                                </div>
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
    data(){
        return{
            loading: false,
            disable: false,
            data:{
                email:'',
                confirm_code:''
            },
            regiEmail: ''
        }
    },
    methods:{
        async submit(){
            if(!this.data.confirm_code || this.data.confirm_code.trim()==''){
               return this.e("Verification code is required!")
            }

            this.data.email = this.regiEmail
            this.loading = true
            this.disable = true

            const res = await this.callApi('post','/auth/verificationCode',this.data)
            if(res.status==200){
                this.s(res.data.msg)
                window.location = '/login'
            }
            else if(res.status==401){
                this.loading = false
                this.disable = false
                this.e(res.data.msg)
            }
            else this.swr()
            this.loading = false
            this.disable = false
        },

        async sendAgain(){
            this.data.email = this.regiEmail
            const res = await this.callApi('post','/auth/sendVerificationCodeAgain',this.data)
            this.loading = true
            this.disable = true
            if(res.status==200){
                this.s("Check your email")
            }
            else if(res.status==401){
                this.loading = false
                this.disable = false
                this.e(res.data.msg)
            }
            else this.swr()
            this.loading = false
            this.disable = false
        },

        storage(){
            this.regiEmail = localStorage.getItem('regiEmail')
        },

    },
    
    async created(){
        
    },

    mounted() {
        this.storage();
    },
}
</script>