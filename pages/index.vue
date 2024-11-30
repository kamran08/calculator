<template>
  <div>
      <!-- Banner -->
      <div class="_home_banner">
        <mainMenu/>

        <div class="_home_banner_main">
          <div class="container">
            <h1 class="_home_banner_title"><br/>
              Tax  calculator </h1>

              <div class="_home_search">
                <div class="_home_search_top">
                  <ul class="_home_search_top_list">
                    <li><span class="_home_search_top_list_span">Calculate your tax Now (Monthly)</span></li>

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
                         <template>
                          <input type="number" />
                      </template>
                      </div>
                    </div>
                    <div class="col-auto">
                    
                    </div>
                    <div class="col-12 col-md">
                      <div class="_home_search_imput">
              


                      </div>
                    </div>
                    <div class="col-12 col-md">
                     <div class="_home_search_imput">
                     <span class="_home_search_top_list_span"> Total payable tax amount: </span>
                     <span class="_home_search_top_list_span"> </span>
                        
                       <!--   <DatePicker v-model="searchData.pick_up_date" type="date" placeholder="Date" style="width: 100%" /> -->
                      </div>
                    </div>
                    <div class="col-12 col-md">
                      <div class="_home_search_imput">
      
                      </div>
                    </div>

                    <div class="col-12 col-md">
                      <div class="_home_search_imput">
                        <button @click="calculate" class="_6btn _btn_long">SEARCH</button>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
          </div>
        </div>
      </div>
      <!-- Banner -->

   

   

     

      <!-- Footer -->
       <mainFooter/>
      <!-- Footer -->
  </div>
</template>

<script>
import mainMenu from "~/components/main/menu.vue";
import mainFooter from "~/components/main/footer.vue";
// import carousel from 'vue-owl-carousel'

export default {
      data(){
        return{
            valu: 0,
        }
    },

components: {
  mainMenu,
  mainFooter,
},



methods:{
  calculate(){
    console.log("hello",valu)
    
      

   
    

  },
 
},

async created(){

}
}
</script>