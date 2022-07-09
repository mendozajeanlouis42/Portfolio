<template>
  <v-app id="home" class="bg">
    <nav-bar />
    <v-container fluid>
      <FsLightbox :toggler="toggler" :sources="loadedPhotos" />
      <v-row>
        <v-col cols="12">
          <br />
          <br />
        </v-col>
        <v-col sm="4" md="5" lg="5" style="height: 800px;">
          <v-img class="" src="images/portrait2.png" contain max-height="600"></v-img>
        </v-col>
        <v-col sm="6" md="5" lg="5" offset-sm="1" offset-md="1">
          <h5 class="red--text text--darken-4 top">Hello Im Jean-Louis Mendoza</h5>
          <h1 class="tessss">
            <span class="text-nickname-container">

              <span class="brcus">J</span>
              <span class="brcus">E</span>
              <span class="brcus">A</span>
              <span class="brcus">N</span>

            </span>

          </h1>
          <h1 class="white--text">Web Developer</h1>
          <p class="grey--text" style="">
            Innovative, task-driven professional with 3+ years of
            experience in web development with a strong emphasis
            on "Progressive Enhancement", as I look for creative ways to
            push the boundaries of website without compromise
          </p>


          <div>
            <v-row>
              <v-col md="6" style="text-align: center;">
                <button class="btn btn--light" @click="scroll('about')">
                  <span class="btn__inner">
                    <span class="btn__slide"></span>
                    <span class="btn__content">About me</span>
                  </span>
                </button>
              </v-col>
              <v-col md="6">
                <button class="btn">
                  <span class="btn__inner">
                    <span class="btn__slide"></span>
                    <span class="btn__content">Download Resume</span>
                  </span>
                </button>
              </v-col>
            </v-row>



          </div>
        </v-col>
        <v-col cols="12" class=""></v-col>

        <v-col cols="12" class="">
          <br />
          <v-row>
            <v-col cols="12" style=" height: 100px;">
              <br />
              <br />
            </v-col>
          </v-row>

          <v-row id="projects">
            <br />
            <br />
          </v-row>
          <v-row>
            <v-col class="first" md="12" style="text-align:center; height: 50px;">
              <h4 class="white--text">FEATURED PROJECTS</h4>
            </v-col>
          </v-row>
          <Projects :featureProjects="featuredProjects"></Projects>


        </v-col>
        <v-col cols="12" style="">
          <br />
          <br />
        </v-col>

        <div class="" id="skills">
          <br />
        </div>
        <div class="second" id="">
          <v-col sm="12" md="12" lg="12" class="bgColor1">
            <v-row>
              <v-col sm="12" md="6" lg="6" offset-md="3">
                <div class="skillDiv" style="">
                  <h4 class="white--text">Experiences</h4> <br/>
                  <center>
                    <v-row align="center" justify="center">
                      <v-col xs="1" sm="2" md="2" lg="2">
                        <v-img src="images/skills/html.svg" contain max-height="62" max-width="62"></v-img>
                      </v-col>
                      <v-col xs="1" sm="2" md="2" lg="2">
                        <v-img src="images/skills/css3.svg" contain max-height="62" max-width="62"></v-img>
                      </v-col>
                      <v-col xs="1" sm="2" md="2" lg="2">
                        <v-img src="images/skills/javascript.svg" contain max-height="62" max-width="62"></v-img>
                      </v-col>
                      <v-col xs="1" sm="2" md="2" lg="2">
                        <v-img src="images/skills/jquery.svg" contain max-height="62" max-width="62"></v-img>
                      </v-col>
                      <v-col xs="1" sm="2" md="2" lg="2">
                        <v-img src="images/skills/php.svg" contain max-height="62" max-width="62"></v-img>
                      </v-col>
                      <v-col xs="1" sm="2" md="2" lg="2">
                        <v-img src="images/skills/mysql.svg" contain max-height="62" max-width="62"></v-img>
                      </v-col>
                      <v-col xs="1" sm="2" md="2" lg="2">
                        <v-img src="images/skills/git.svg" contain max-height="62" max-width="62"></v-img>
                      </v-col>
                      <v-col xs="1" sm="2" md="2" lg="2">
                        <v-img src="images/skills/laravel.svg" contain max-height="62" max-width="62"></v-img>
                      </v-col>
                      <v-col xs="1" sm="2" md="2" lg="2">
                        <v-img src="images/skills/react.svg" contain max-height="62" max-width="62"></v-img>
                      </v-col>
                      <v-col xs="1" sm="2" md="2" lg="2">
                        <v-img src="images/skills/vue.svg" contain max-height="62" max-width="62"></v-img>
                      </v-col>
                      <v-col xs="1" sm="2" md="2" lg="2">
                        <v-img src="images/skills/vscode.svg" contain max-height="62" max-width="62"></v-img>
                      </v-col>
                    </v-row>

                  </center>
                </div>
              </v-col>
            </v-row>
            <v-row>
              <v-col xs="1" sm="2" md="6" lg="6">
                <p class="white--text">Service Class Business Logic Application</p>
                <v-img src="images/skills/businesslogic.gif" contain
                  @click="showImage('images/skills/businesslogic.gif')"></v-img>
              </v-col>
              <v-col xs="1" sm="2" md="6" lg="6">
                <p class="white--text">DRY Approach</p>
                <v-img src="images/skills/dry.PNG" contain
                  @click="showImage('images/skills/dry.PNG')"></v-img>
              </v-col>
            </v-row>
          </v-col>
        </div>
        <v-col cols="12" style=" height: 200px;">
          <br />
          <br />
        </v-col>
        <v-col cols="12" id="about">
          <br />
          <br />
        </v-col>

        <div class="">
          <br />
        </div>
        <div class="second" id="">
          <v-col cols="12" class="bgColor1">
            <v-row>
              <v-col sm="12" md="5" style="text-align:left;">
                <v-row>
                  <v-col cols="12" class="mb-0">
                    <h5 class="red--text text--darken-4 ">A BIT ABOUT ME</h5>
                  </v-col>
                  <v-col cols="12" class="mt-0 white--text">
                    <h1 style="font-size: 40px;">I'm Jean-Louis <br /> Mendoza</h1>
                  </v-col>
                  <v-col cols="12" class="mt-0 white--text">
                    <p>
                      I started my web developer career as a System Developer at Synermaxx Corporation,
                      where my tasks strongly involved in the backend development guided by the best team in this
                      company. Also interested
                      in people where I can learn, share, compare, to absorb best approaches in regards to web development.
                    </p>
                    <p>
                      My hobbies are simply watching 🧑🏻‍anime, do 🦸‍♂️cosplay, get few shots for 🏹archery and maybe
                      play 🎮edit/games once in awhile.
                    </p>
                  </v-col>
                  <v-col cols="12" class="ml-16">
                    <button class="btn btn--light" @click="scroll('about')">
                      <span class="btn__inner">
                        <span class="btn__slide"></span>
                        <span class="btn__content">Download Resume</span>
                      </span>
                    </button>
                  </v-col>
                </v-row>
              </v-col>
              <v-col sm="12" md="4" offset-md="2">
                <v-img class="" src="images/portrait1.png" contain max-height="600"></v-img>

              </v-col>
            </v-row>
            <v-row>
              <v-col cols="3">
              </v-col>
            </v-row>
          </v-col>
        </div>

        <div class="" style="height: 900px;" id="">
        </div>

        <v-col cols="12" class="padd topInverse" >
          <div class="second" hidden >
            <div class="secondchild1" id="contact">
              <v-row>
                <v-col cols="7">
                  <h1 class="white--text">
                    Let's work together on<br />your next project
                  </h1>
                  <p class="grey--text">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.

                    Eius nesciunt ducimus natus <br />
                  </p>
                </v-col>
                <v-col cols="5">
                  <v-btn tile color="#A7121D" dark class="mt-16">
                    Contact
                  </v-btn>
                </v-col>
              </v-row>
            </div>
          </div>
          <v-toolbar class="topTolbar" color="#111111" dark flat>
            <div style="
                position: absolute;
                margin-left: auto;
                margin-right: auto;
                left: 0;
                right: 0;
                text-align: left;
              ">
              <p style="padding: 10px; font-size: 9px;">Portfolio in Development 2022 </p>
            </div>
          </v-toolbar>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>
import NavBar from "../components/Navbar.vue";
import Projects from "../components/Projects.vue";
import featuredProjects from "../data/projectsData";
import FsLightbox from "fslightbox-vue";
export default {
  name: "Home",

  data() {
    return {
      featuredProjects: featuredProjects,
      loadedPhotos: this.loadedPhotos,
      toggler: false,
    }
  },
  // data: () => ({
  //   icons: ["mdi-facebook", "mdi-twitter", "mdi-linkedin", "mdi-instagram"],

  // }),
  components: {
    NavBar,
    Projects,
    FsLightbox,

    // Footer,
  },
  methods: {
    scroll(refName) {
      const element = document.getElementById(refName);
      console.log(element)
      element.scrollIntoView({ behavior: "smooth" })
    },
    showImage: function (sources) {
      this.loadedPhotos = [sources]
      this.toggler = !this.toggler
    }
  },
};
</script>
<style scoped>
.skillDiv {
  text-align: center;
  padding: 10px;
  height: 200px;
}

.bg {
  background-image: url("/images/bg.png");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center bottom;
  background-attachment: fixed;
}

.top {
  margin-top: 180px;
}

.topInverse {
  margin-top: -250px;
}

.topTolbar {
  margin-top: 100px;
  text-align: center;
}

.first {
  width: 100%;
  height: 400px;
  background: linear-gradient(to right,
      #181818,
      #181818 50%,
      #111111 50%,
      #111111 50%);
  text-align: center;
  padding: 2rem 2rem;
}

.second {
  width: 100%;
  /* height: 400px; */
  background: #181818;
  text-align: center;
  padding: 2rem 2rem;
}

.secondchild1 {
  display: inline-block;
  background-color: #1e1e1e;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: left;
  margin-top: 250px;
}

.child {
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: left;
  margin-right: 8px;
}

.bgColor1 {
  background-color: #1e1e1e;
}

.bgColor2 {
  background-color: #fe4652;
}

.child1 {
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  margin-right: 5px;
  width: 240px;
}

.child2 {
  display: inline-block;
  width: 245px;
  vertical-align: middle;
}

.mRight {
  margin-right: 8px;
}

.mButton {
  margin-bottom: 8px;
}

.padding {
  padding: 8px 0;
}

.col-12.padd {
  padding: 12px 0 !important;
}

.col-12.childcol {
  padding: 0 !important;
}

h1.number {
  font-size: 50px;
  font-weight: bold;
}

.pimage {
  height: 100px;
  width: 100px;
  border-radius: 100%;
}

.imageme {
  clip-path: polygon(81% 0, 0 0, 0 100%, 20% 100%, 61% 31%);
}

.tessss {
  text-align: center;
  height: 175px;
  width: 50px;
  background-color: #fe4652;
  color: white;
  text-transform: uppercase;
  letter-spacing: 3px;
  margin-left: -65px;
  position: absolute;

  transform-origin: 0 0;
  /* transform: rotate(90deg); */
}

.brcus {
  display: block;
  margin-bottom: -15px;
}

.text-nickname-container {
  top: 10px;
  position: relative;
}









:root {
  --background-color: #0f1923;
}

body {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: var(--background-color);
}

.btn {
  /* Clean style */
  -moz-appearance: none;
  -webkit-appearance: none;
  appearance: none;
  border: none;
  background: none;
  padding: 0;
  color: var(--button-text-color);
  cursor: pointer;
  /* Clean style */

  --button-text-color: var(--background-color);
  --button-text-color-hover: var(--button-background-color);
  --border-color: #7D8082;
  --button-background-color: #ece8e1;
  --highlight-color: #ff4655;
  --button-inner-border-color: transparent;
  --button-bits-color: var(--background-color);
  --button-bits-color-hover: var(--button-background-color);

  position: relative;
  padding: 8px;
  margin-bottom: 20px;
  text-transform: uppercase;
  font-weight: bold;
  font-size: 14px;
  transition: all .15s ease;
}

.btn::before,
.btn::after {
  content: '';
  display: block;
  position: absolute;
  right: 0;
  left: 0;
  height: calc(50% - 5px);
  border: 1px solid var(--border-color);
  transition: all .15s ease;
}

.btn::before {
  top: 0;
  border-bottom-width: 0;
}

.btn::after {
  bottom: 0;
  border-top-width: 0;
}

.btn:active,
.btn:focus {
  outline: none;
}

.btn:active::before,
.btn:active::after {
  right: 3px;
  left: 3px;
}

.btn:active::before {
  top: 3px;
}

.btn:active::after {
  bottom: 3px;
}

.btn__inner {
  position: relative;
  display: block;
  padding: 20px 30px;
  background-color: var(--button-background-color);
  overflow: hidden;
  box-shadow: inset 0px 0px 0px 1px var(--button-inner-border-color);
}

.btn__inner::before {
  content: '';
  display: block;
  position: absolute;
  top: 0;
  left: 0;
  width: 2px;
  height: 2px;
  background-color: var(--button-bits-color);
}

.btn__inner::after {
  content: '';
  display: block;
  position: absolute;
  right: 0;
  bottom: 0;
  width: 4px;
  height: 4px;
  background-color: var(--button-bits-color);
  transition: all .2s ease;
}

.btn__slide {
  display: block;
  position: absolute;
  top: 0;
  bottom: -1px;
  left: -8px;
  width: 0;
  background-color: var(--highlight-color);
  transform: skew(-15deg);
  transition: all .2s ease;
}

.btn__content {
  position: relative;
}

.btn:hover {
  color: var(--button-text-color-hover);
}

.btn:hover .btn__slide {
  width: calc(100% + 15px);
}

.btn:hover .btn__inner::after {
  background-color: var(--button-bits-color-hover);
}

.btn--light {
  --button-background-color: var(--background-color);
  --button-text-color: var(--highlight-color);
  --button-inner-border-color: var(--highlight-color);
  --button-text-color-hover: #ece8e1;
  --button-bits-color-hover: #ece8e1;
}
</style>