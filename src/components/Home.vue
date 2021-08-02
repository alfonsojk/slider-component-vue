<template>
  <v-app>
    <v-card class="square one">
      <v-img class="cover"
        src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
        width="350px"
        height="200px"
      ></v-img>
      <v-card-title
      class="icons">
        <v-btn
            class="margin-r"
            dark
            v-for="(icon, index) in icons"
            :key="index"
            icon
            outlined
          >
            <v-icon
            color="white"
            small
            icon>{{ icon }}</v-icon>
        </v-btn>
        <div class="spacer">
          <v-dialog
            v-model="dialog"
            width="600px"
          >
            <template v-slot:activator="{ on, attrs }"> 
              <v-btn
              v-bind="attrs"
              v-on="on"
              dark
              v-for="(play, index) in play"
              :key="index"
              icon
              outlined
              >
                <v-icon
                color="white"
                small
                icon>
                  {{ play }}
                </v-icon>
              </v-btn>
            </template>
            <v-card
        color="dark"
        dark>
         
            <v-img class="cover"
        src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
        width="950px"
        height="450px"
      >
            <v-btn
            icon
            dark
            @click="dialog = false"
            class="close"
          >
            <v-icon>mdi-close</v-icon>
          </v-btn>
            </v-img>
            
          <v-row
          class="row">
          <v-col
          class="col-8">
          <v-card-subtitle
          class="d-flex">
              <p
              class="ml-5">
                86% Match
              </p>
              <h2
              class="ml-5">
                2013
              </h2>
              <div>
              <span class="maturity-number ml-3"><h2>TV-14</h2></span>
              </div>
              <div>
              <span class="maturity-number ml-3"><h2>HD</h2></span>
              </div>
            </v-card-subtitle>
          <v-card-subtitle>
              <h2>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita modi cumque omnis harum repellendus voluptatem ducimus praesentium, temporibus voluptatibus sint ea dolores ad illo, doloremque fugit fugiat nisi facilis reiciendis.
              </h2>
          </v-card-subtitle>
          </v-col>
          <v-col>
          <v-card-subtitle>
              <h1>
                Cast:
              </h1>
              <h2>Andre Braeumer, Stephanie Beatriz and more.</h2>
              <br>
              <h1>
                Genres:
              </h1>
              <h2>Show,Comedies, TV</h2>
          </v-card-subtitle>
          </v-col>
          </v-row>
        </v-card>
          </v-dialog>
        </div>
        <div>
          <p>98% Match</p>
        </div>
        <div class="display">
          <span class="maturity-number"><h2>TV-14</h2></span>
          <h2>Movie</h2>
          <span class="maturity-number"><h2>HD</h2></span>
        </div>
          <ul class="list">
          <li><h2>Exciting</h2></li>
          <li><h2>Fantastic</h2></li>
          <li><h2>Thrilling</h2></li>
          </ul>
      </v-card-title>
    </v-card>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      icons: ['mdi-chevron-right', 'mdi-plus', 'mdi-thumb-up','mdi-thumb-down'],
      play:['mdi-chevron-down'],
      dialog: false,
    }
  },
}
</script>

<style>
body,
html {
  margin: 10% 10%;
  width: 100%;
  height: 100%;
}

h1{
  font-family: 'Helvetica Neue',Helvetica,Arial,sans-serif;
  font-weight:500;
  color: #404040;
  font-size:15px;
}
h2{
  font-family: 'Helvetica Neue',Helvetica,Arial,sans-serif;
  font-weight:300;
  color: #ffffff;
  font-size:15px;
}
h3{
  font-family: 'Helvetica Neue',Helvetica,Arial,sans-serif;
  font-weight:300;
  color: #ffffff;
  font-size:15px;
}
.square {
  width: 350px;
  height: 200px;
  transition: transform 400ms ease-out, border-radius 400ms ease-out;
}

.square .cover .text{
  width: 350px;
  height: 200px;
  background-size: cover!important;
  background-position: center!important;

}

.square .icons {
  display: none;
  background: #181818;
  color: #fff;
  width: 100%;
  box-sizing: border-box;
  transition: opacity 500ms ease-out, border-radius 400ms ease-out;
  height: 175px;

}

p{  
  font-family: 'Helvetica Neue',Helvetica,Arial,sans-serif;
  font-weight:700;
  color: #46d369;
  font-size:15px;
}

.square:hover {
  border-radius: 10px;
  transform: scale(1.5);
  box-shadow: 0 0 2px #000a;
}

.square:hover .icons{
  display: block;
}
.maturity-number {
  font-family: 'Helvetica Neue',Helvetica,Arial,sans-serif;
  text-transform: uppercase;
  border: solid 1px white;
  display:inline-flex;
  padding: 0 5px;
  font-size:13px;
}

.test{
  display:flex;
}
.display{
  display:flex;
  margin-top:10px;
  margin-right: 150px;
  justify-content:space-around
}
.list{
  display:flex;
  width: 80%;
  justify-content:space-between;
}
li{
  color: #404040;
}
.spacer{
  float:right;
}
.margin-r{
  margin-right: 10px;
}
</style>