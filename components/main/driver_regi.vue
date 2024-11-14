<template>
    <div>
        <div class="">
            <h2 class="_log_form_title">Welcome Back  👋 </h2>
            <p class="_log_text">Today is a new day. It's your day. You shape it. </p>

            <div class="_log_form">
                <div class="row g-3">
                    <div class="col-12 col-md-6 col-lg-6">
                        <div class="_regi_input_group">
                            <input v-model="data.first_name" class="_1input" placeholder="First name" type="text">
                        </div>
                    </div>

                    <div class="col-12 col-md-6 col-lg-6">
                        <div class="_regi_input_group">
                            <input v-model="data.last_name" class="_1input" placeholder="Last name" type="text">
                        </div>
                    </div>
                    <div class="col-12 col-md-12 col-lg-12">
                        <div class="_regi_input_group">
                            <div v-show="data.image" class="demo-upload-list">
                                <img :src="data.image" alt="" title="">
                                <div class="demo-upload-list-cover">
                                    <Icon type="ios-trash-outline" @click="handleRemove"></Icon>
                                </div>
                            </div>
                            <div>
                                <Upload
                                    ref="file"
                                    type="drag"
                                    :format="['jpg', 'jpeg', 'png']"
                                    :max-size="20480"
                                    :show-upload-list="false"
                                    :on-format-error="handleFormatError"
                                    :on-exceeded-size="handleMaxSize"
                                    :on-success="handleImageUpload"
                                    :action="`${apiUrl}/auth/uploadImage`">
                                    <div style="padding: 32px 0">
                                        <Icon type="ios-cloud-upload" size="52" style="color: #3399ff"></Icon>
                                        <p>Click or drag files here to upload</p>
                                    </div>
                                </Upload>
                            </div>
                        </div>
                    </div>
                    <div class="col-12 col-md-12 col-lg-12">
                        <div class="_regi_input_group">
                            <input v-model="data.email" class="_1input" placeholder="Email" type="text">
                        </div>
                    </div>
                    <div class="col-12 col-md-12 col-lg-12">
                        <div class="_regi_input_group">
                            <input v-model="data.phone" class="_1input" min="0" placeholder="Phone number" type="number">
                        </div>
                    </div>
                    <div class="col-12 col-md-6 col-lg-6">
                        <div class="_regi_input_group">
                            <input v-model="data.password" class="_1input" type="password" placeholder="Password">
                        </div>
                    </div>
                    <div class="col-12 col-md-6 col-lg-6">
                        <div class="_regi_input_group">
                            <input v-model="data.password_confirmation" class="_1input" type="password" placeholder="Confirm password">
                        </div>
                    </div>
                    <div class="col-12 col-md-6 col-lg-6">
                        <div class="_regi_input_group">
                            <input v-model="data.license" class="_1input" type="text" placeholder="License No">
                        </div>
                    </div>
                    <div class="col-12 col-md-12 col-lg-12">
                        <div class="_regi_input_group">
                            <h1 class="_addPage_from_title">Payment Information </h1>

                            <RadioGroup v-model="data.payment_type" class="_payment_type_list">
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

                            <div v-if="data.payment_type === 'bKash'" class="_account_details_baksh">
                                <h1 class="_addPage_from_title">Enter Your bKash Account</h1>
                                <div class="row g-4">
                                    <div class="col-12 col-md-6 col-lg-6">
                                        <label class="_2label"><span>*</span> Account Number</label>
                                        <Input v-model="data.b_account_num" type="number" size="large" placeholder="Account Number"/>
                                    </div>
                                    <div class="col-12 col-md-6 col-lg-6">
                                        <label class="_2label"><span>*</span> Account Name</label>
                                        <Input v-model="data.b_account_name" size="large" placeholder="Account Name"/>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="col-12 col-md-12 col-lg-12">
                        <div class="_regi_input_group">
                            <h1 class="_addPage_from_title">Upload License Photo</h1>

                            <div class="row g-4">
                                <div class="col-12 col-md-4 col-lg-4">
                                    <div v-if="data.image_one" class="_license_img_remove">
                                        <img :src="data.image_one" alt="" title="">
                                        <div class="_license_img_remove_icon">
                                            <Icon type="ios-trash-outline" @click="handleRemoveOne"></Icon>
                                        </div>
                                    </div>

                                    <Upload
                                        v-if="!data.image_one"
                                        ref="file"
                                        type="drag"
                                        :format="['jpg', 'jpeg', 'png']"
                                        :max-size="20480"
                                        :show-upload-list="false"
                                        :on-format-error="handleFormatError"
                                        :on-exceeded-size="handleMaxSize"
                                        :on-success="handleImageOneUpload"
                                        :action="`${apiUrl}/auth/uploadImage`">
                                        <div style="padding: 25px 0">
                                            <Icon type="ios-cloud-upload" size="35" style="color: #3399ff"></Icon>
                                            <p style="font-size:12px">Click or drag file</p>
                                        </div>
                                    </Upload>
                                </div>
                                <div class="col-12 col-md-4 col-lg-4">
                                    <div v-if="data.image_two" class="_license_img_remove">
                                        <img :src="data.image_two" alt="" title="">
                                        <div class="_license_img_remove_icon">
                                            <Icon type="ios-trash-outline" @click="handleRemoveTwo"></Icon>
                                        </div>
                                    </div>

                                    <Upload
                                        v-if="!data.image_two"
                                        ref="file"
                                        type="drag"
                                        :format="['jpg', 'jpeg', 'png']"
                                        :max-size="20480"
                                        :show-upload-list="false"
                                        :on-format-error="handleFormatError"
                                        :on-exceeded-size="handleMaxSize"
                                        :on-success="handleImageTwoUpload"
                                        :action="`${apiUrl}/auth/uploadImage`">
                                        <div style="padding: 25px 0">
                                            <Icon type="ios-cloud-upload" size="35" style="color: #3399ff"></Icon>
                                            <p style="font-size:12px">Click or drag file</p>
                                        </div>
                                    </Upload>
                                </div>
                                <div class="col-12 col-md-4 col-lg-4">
                                    <div v-if="data.image_three" class="_license_img_remove">
                                        <img :src="data.image_three" alt="" title="">
                                        <div class="_license_img_remove_icon">
                                            <Icon type="ios-trash-outline" @click="handleRemoveThree"></Icon>
                                        </div>
                                    </div>

                                    <Upload
                                        v-if="!data.image_three"
                                        ref="file"
                                        type="drag"
                                        :format="['jpg', 'jpeg', 'png']"
                                        :max-size="20480"
                                        :show-upload-list="false"
                                        :on-format-error="handleFormatError"
                                        :on-exceeded-size="handleMaxSize"
                                        :on-success="handleImageThreeUpload"
                                        :action="`${apiUrl}/auth/uploadImage`">
                                        <div style="padding: 25px 0">
                                            <Icon type="ios-cloud-upload" size="35" style="color: #3399ff"></Icon>
                                            <p style="font-size:12px">Click or drag file</p>
                                        </div>
                                    </Upload>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="col-12 col-md-12 col-lg-12">
                        <div class="_regi_input_group">
                            <div class="_log_checkBox">
                                <input  v-model="agree" type="checkbox" id="agree">
                                <label for="agree">I agree with the <a href="">Terms</a> & <a href="">Privacy</a></label>
                            </div>
                        </div>
                    </div>
                    <div class="col-12 col-md-12 col-lg-12">
                        <div class="_log_button">
                            <button @click="driverRegistration" :disabled="disable" :loading="loading" class="_1btn _btn_long">Submit</button>
                        </div>
                    </div>
                </div>
            </div>

            <p class="_donot">Already have an account? <a href="">Sign in</a></p>
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
            agree:false,
            data:{
                image:'',
                email:'',
                phone:'',
                first_name:'',
                last_name:'',
                license:'',
                password:'',
                password_confirmation:'',
                user_type:'driver',
                payment_type:'',
                b_account_num:'',
                b_account_name:'',
                image_one:'',
                image_two:'',
                image_three:'',
                authUserType:'',
            },
            reg: /^(([^<>()\[\]\\.,;:\s@"]+(\.[^<>()\[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,24}))$/,
        }
    },
    methods:{
        async driverRegistration(){
            // if(this.authUser){
            //     this.data.authUserType = this.authUser.user_type
            // }
            // console.log( this.data.authUserType )
            // if(!this.data.image || this.data.image.trim()==''){
            //    return this.e("Image is required!")
            // }
            // if (!this.data.email) {
            //     return this.e("Email is required!")
            // }
            // if(!this.data.phone || this.data.phone.trim()==''){
            //    return this.e("Phone number is required!")
            // }
            // if(!this.data.first_name || this.data.first_name.trim()==''){
            //    return this.e("First name is required!")
            // }
            // if(!this.data.last_name || this.data.last_name.trim()==''){
            //    return this.e("Last name is required!")
            // }
            // if (!this.reg.test(this.data.email)) {
            //    return this.e("Invalid email format!")
            // }
            // if(!this.data.license || this.data.license.trim()==''){
            //     return this.e("License number is required!")
            // }
            // if(!this.data.password || this.data.password.trim()==''){
            //     return this.e("Password is required!")
            // }
            // if(!this.data.password_confirmation || this.data.password_confirmation.trim()==''){
            //     return this.e("Confirm password is required!")
            // }
            // if(this.data.password_confirmation != this.data.password){
            //     return this.e("Password does not match!")
            // }
            // if(!this.data.payment_type || this.data.payment_type.trim()==''){
            //     return this.e("Select payment type!")
            // }
            // if(this.data.payment_type === 'bKash'){
            //     if(!this.data.b_account_num || this.data.b_account_num.trim()==''){
            //         return this.e("Account number is required!")
            //     }

            //     if(!this.data.b_account_name || this.data.b_account_name.trim()==''){
            //         return this.e("Account name is required!")
            //     }
            // }
            // if(!this.data.image_one || this.data.image_one.trim()==''){
            //     return this.e("License file is required!")
            // }
            // if(!this.data.image_two || this.data.image_two.trim()==''){
            //     return this.e("License file is required!")
            // }
            // if(!this.data.image_three || this.data.image_three.trim()==''){
            //     return this.e("License file is required!")
            // }
            // if(this.agree != true){
            //     return this.e("Agree with the Terms & Condition!")
            // }

            this.loading = true
            this.disable = true

            const res = await this.callApi('post','/admin/driver/createDriver',this.data)
            if(res.status==200){
                localStorage.setItem('regiEmail', this.data.email);
                console.log("email", this.data.email)
                console.log("testemail")
                window.location = '/verification'
                this.data.image = ''
                this.data.email = ''
                this.data.phone = ''
                this.data.first_name = ''
                this.data.last_name = ''
                this.data.password_confirmation = ''
                this.data.password = ''
                this.data.license = ''
                this.data.payment_type = ''
                this.data.b_account_num = ''
                this.data.b_account_name = ''
                this.data.image_one = ''
                this.data.image_two = ''
                this.data.image_three = ''
                this.s(res.data.msg)
            }
            else if(res.status==401){
                this.loading = false
                this.disable = false
                return this.e(res.data[0].message)
            }
            else if(res.status==402){
                this.loading = false
                this.disable = false
                return this.e(res.data.msg)
            }
            else this.swr()
            this.loading = false
            this.disable = false
        },
        
        async handleImageUpload(res, file) {
            if (res) {
                this.data.image = res;
            }
        },
        async handleImageOneUpload(res, file) {
            if (res) {
                this.data.image_one = res;
            }
        },
        async handleImageTwoUpload(res, file) {
            if (res) {
                this.data.image_two = res;
            }
        },
        async handleImageThreeUpload(res, file) {
            if (res) {
                this.data.image_three = res;
            }
        },

        handleRemove(p) {
            this.data.image = ""
        },
        handleRemoveOne(p) {
            this.data.image_one = ""
        },
        handleRemoveTwo(p) {
            this.data.image_two = ""
        },
        handleRemoveThree(p) {
            this.data.image_three = ""
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