<template>
  <div>
    <v-parallax src="/parallax.jpg" style="height: 180px; padding-top: 80px;">
        <p align="center" class="headline">Hotel & Accommodations</p>
    </v-parallax>

        <v-layout row style="max-width: 1280px; margin: 10px auto;">
          <v-flex xs12 md9>
              <v-container grid-list-sm features>          
                      <v-layout wrap>
                        <v-flex xs12 sm6 item lg4 v-for="(item, i) in items" :key="i">
                          <v-card item>
                            <v-container fluid grid-list-md>
                              <v-layout wrap>
                                <v-flex xs4 sm12 img style="background: url('/room.jpg') no-repeat; background-size: cover; height: 185px; margin-bottom: 9px;">
                                  <div class="heart"><v-icon medium color="white">favorite_border</v-icon></div>
                                  <div class="price subheading">$999</div>
                                </v-flex>                  
                                <v-flex xs8 sm12>
                                  <div class="itemDes">
                                      <p class="subheading"><b>Bali Golden Elephant Boutique Villa</b></p>

                                      <p class="stars">
                                          <v-icon small color="orange">star</v-icon>
                                          <v-icon small color="orange">star</v-icon>
                                          <v-icon small color="orange">star</v-icon>
                                          <v-icon small color="orange">star</v-icon>
                                          <v-icon small color="orange">star</v-icon>
                                        </span> <span class="caption"> &nbsp; (<b>192</b> reviews)</span></p>

                                      <p class="body-1 address"><v-icon small>location_on</v-icon>Uluwatu, Bali, ID &nbsp; <code class="viewonmap">view on map</code></p>
                                      
                                      <v-layout row wrap green--text>
                                        <v-flex class="xs3"><v-icon small color="green">wifi</v-icon> wifi</v-flex>
                                        <v-flex class="xs9"><v-icon small color="blue">check</v-icon> <nowrap>order now pay later</nowrap></v-flex>
                                      </v-layout>
                                  </div>                       
                                </v-flex>
                              </v-layout>
                            </v-container>

                              <v-flex footer py-0 px-1 sx12>                      
                                <v-flex py-0 px-0 xs6><v-icon small>grade</v-icon> <em><b class="mr-1">8.8</b></em> Exellent</v-flex>
                                <v-flex xs6 py-0 px-0 mr-0 text-xs-right><v-btn small outline color="blue">Book</v-btn></v-flex>
                              </v-flex>                   
                          </v-card>
                        </v-flex>
                      </v-layout>
              </v-container>

          </v-flex>            
        </v-layout>        
  </div>
</template>

<script>
  export default {
    data: () => ({

      items: [
          {
            title: 'Tinggi k Rendah'
          },
          {
            title: 'Rendah ke TInggi'
          },
          {
            title: 'Lorem ipsum dolor sit amet, mel at clita quando'
          },
          {
            title: 'Click Me 2'
          },
          {
            title: 'Click Me 2'
          },
          {
            title: 'Click Me 2'
          }
        ],
    }),

        methods: {
          gridListing () {

            alert('tes');
          }
        }      
  }
</script>


<style type="text/css">
.subheading{
  color: #555;
}
.img{
  position: relative;
}
.img .heart{
  position: absolute;
  z-index: 1;
}
.img .price{
  position: absolute;
  z-index: 1;
  right: -4px;
  bottom: 10px;
  background-color: #EE595D;
  font-weight: bold;
  padding: 1px 20px;
  color: white;
}

.itemDes i.icon{
  font-size: 16px;
  margin-top: -4px;
}

.subheading,
.stars,
.address{
  margin-bottom: 8px;
}
.address .viewonmap{
  font-size: 10px!important;
  font-weight: bold;
  white-space: nowrap;
  cursor: pointer;
}
nowrap{
  white-space: nowrap;
}
@media only screen and (min-width: 600px) {
  .features .item{
    padding: 8px!important;
  }
  .features .container.grid-list-md{
    padding: 10px;
  }
}

@media only screen and (max-width: 599px) {
  .features .item{
    margin: 6px 0!important;
  }
  .features .img{
    height: auto!important;
  }
  .itemDes{
    margin-left: 8px;
  }
}
</style>