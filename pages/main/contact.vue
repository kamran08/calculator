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
                <h4 class="_con_banner_title">Contact Us</h4>
                <h1 class="_con_banner_text">We value your inquiries, feedback, and concerns</h1>
              </div>
             </div>
            <!-- Banner -->

            <!-- Main section -->
             <div class="_contact">
              <div class="container">
                <div class="_contact_row">
                  <!-- Form -->
                  <div class="_contact_form">
                    <h1 class="_contact_form_title">Get In Touch</h1>

                    <div class="row g-3">
                      <div class="col-12 col-md-6 col-lg-6">
                        <input class="_2input" placeholder="Name">
                      </div>
                      <div class="col-12 col-md-6 col-lg-6">
                        <input class="_2input" placeholder="Phone">
                      </div>
                      <div class="col-12 col-md-6 col-lg-6">
                        <input class="_2input" placeholder="Email">
                      </div>
                      <div class="col-12 col-md-6 col-lg-6">
                        <input class="_2input" placeholder="Address">
                      </div>
                      <div class="col-12 col-md-12 col-lg-12">
                        <textarea class="_1textarea" rows="6" placeholder="I'm interested in"></textarea>
                      </div>
                      <div class="col-12 col-md-12 col-lg-12">
                        <div class="_button_group">
                          <button class="_6btn _btn_long">SUBMIT</button>
                        </div>
                      </div>
                    </div>
                  </div>
                  <!-- Form -->

                  <!-- Map -->
                   <div class="_contact_map">
                    <img src="/map.png">
                   </div>
                  <!-- Map -->
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