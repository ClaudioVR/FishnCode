<template>
  <div class="black">
    <section id="hero">
      <v-row no-gutters>
        <!-- <v-img
          :min-height="'calc(100vh - ' + $vuetify.application.top + 'px)'"
          src="https://images.unsplash.com/photo-1487017159836-4e23ece2e4cf?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1951&q=80"
        > -->
        <v-img
          :min-height="'calc(100vh - ' + $vuetify.application.top + 'px)'"
          src="https://source.unsplash.com/H4uYCNkNLdM"
        >
        <!-- Dark oslo Yk0tCHUm1-o -->

        <v-container fill-height class="px-0">
          <v-row
            align="center"
            class="white--text mx-auto"
            justify="center"
          >
            <v-col
              class="white--text text-center pa-0"
              cols="12"
            >
              <!-- <span
                :class="[$vuetify.breakpoint.smAndDown ? 'display-3': 'display-4']"
                class="font-weight-black"
              >
                Fish n Code
              </span> -->

              <v-img id="logo" class="pa-0" src="/fishncodelogo.svg">

              </v-img>
              <span
                id="location-text"
                class="font-weight-light"
                :class="[$vuetify.breakpoint.smAndDown ? 'display-1' : 'display-2']"
              >
                Oslo, Norway
              </span>
              <br>
              <v-btn
                class="align-self-end mt-6"
                fab
                outlined
                @click="$vuetify.goTo('#about-me')"
              >
                <v-icon>mdi-chevron-double-down</v-icon>
              </v-btn>

            </v-col>
          </v-row>
        </v-container>
        </v-img>
      </v-row>
    </section>

    <section id="about-me">
      <div class="py-12"></div>

      <v-container class="text-center">
        <h2 class="display-2 font-weight-bold mb-3">ABOUT US</h2>

        <v-responsive
          class="mx-auto mb-8"
          width="56"
        >
          <v-divider class="mb-1"></v-divider>

          <v-divider></v-divider>
        </v-responsive>

        <v-responsive
          class="mx-auto title font-weight-light mb-8"
          max-width="720"
        >
          <p class="headline">Fish n Code offer cutting edge front-end solutions. <br> From simple static websites, to full-stack progressive web applications. We create user-friendly interfaces which deliver the very best user experiences.</p>
          <p>Fish n Code is based in Oslo, but is available for remote project work throughout the world.</p>
        </v-responsive>

        <v-avatar
          class="elevation-12 mb-8"
          size="128"
        >
          <v-img src="/claudio.jpg"></v-img>
        </v-avatar>
        <br>
        <span class="headline font-weight-light">Claudio Rescigno</span>
        <p class="font-weight-thin">Coder and founder</p>

        <div></div>

        <v-btn
          color="grey"
          href="https://www.linkedin.com/in/claudio-rescigno-6b0531177/?originalSubdomain=no"
          target="_blank"
          outlined
          fab
        >
          <!-- <span class="grey--text text--darken-1 font-weight-bold text-capitalize">
            Linked
          </span> -->
          <v-icon large>mdi-linkedin</v-icon>
        </v-btn>
      </v-container>

      <div class="py-12"></div>
    </section>

    <section
      id="services"
      class="grey--text text--lighten-2"
    >
      <div class="py-12"></div>

      <v-container class="text-center">
        <h2 class="display-2 font-weight-bold mb-3 text-uppercase">Our services</h2>

        <v-responsive
          class="mx-auto mb-12"
          width="56"
        >
          <v-divider class="mb-1"></v-divider>

          <v-divider></v-divider>
        </v-responsive>

        <v-row>
          <v-col
            v-for="({ icon, title, text }, i) in services"
            :key="i"
            cols="12"
            md="4"
          >
            <v-card
              class="py-12 px-4 grey lighten-3"
              flat
            >
              <div>
                <v-avatar
                  color="#030d24"
                  size="88"
                >
                  <v-icon
                    large
                    v-text="icon"
                    color="grey lighten-3"

                  ></v-icon>
                </v-avatar>
              </div>

              <v-card-title
                class="justify-center font-weight-black text-uppercase grey--text text--darken-2"
                v-text="title"
              ></v-card-title>

              <v-card-text
                class="subtitle-1 grey--text text--darken-2"
                v-text="text"
              >
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-container>

      <div class="py-12"></div>
    </section>

    <section id="languages">
      <v-parallax
        :height="$vuetify.breakpoint.smAndDown ? 700 : 500"
        src="https://source.unsplash.com/p_wC_T2HUPk"
      >
        <v-container fill-height>
          <v-row class="mx-auto">
            <v-col
              v-for="[value, title, logo] of languages"
              :key="title"
              cols="12"
              md="3"
              class="d-flex flex-column align-center"
            >
              <img class="mb-5" height="60" width="60" :src="logo" :alt="value">
              <div class="text-center">
                <div
                  class="display-3 font-weight-black mb-4"
                  v-text="value"
                ></div>
                <div
                  class="title font-weight-regular text-uppercase"
                  v-text="title"
                ></div>
              </div>
            </v-col>
          </v-row>
        </v-container>
      </v-parallax>
    </section>

    <section id="portfolio">
      <div class="py-12"></div>

      <v-container>
        <h2 class="display-2 font-weight-bold mb-3 text-uppercase text-center">Portfolio</h2>

        <v-responsive
          class="mx-auto mb-12"
          width="56"
        >
          <v-divider class="mb-1"></v-divider>

          <v-divider></v-divider>
        </v-responsive>

        <v-row>
          <v-col
            v-for="({ src, text, title, link }, i) in projects"
            :key="i"
            cols="12"
            md="4"
          >
            <v-img
              :src="src"
              class="mb-4"
              height="285"
              max-width="100%"
            ></v-img>

            <h3
              class="font-weight-black mb-4 text-capitalize"
              v-text="title"
            ></h3>

            <div
              class="title font-weight-light mb-5"
              v-text="text"
            ></div>

            <v-btn
              class="ml-n4 font-weight-black"
              text
              :href="link"
              target="_blank"
            >
              Read more
            </v-btn>
          </v-col>
        </v-row>
      </v-container>

      <div class="py-12"></div>
    </section>

    <!-- <v-sheet
      id="contact"
      color="black"
      tag="section"
      tile
    >
      <div class="py-12"></div>

      <v-container>
        <h2 class="display-2 font-weight-bold mb-3 text-uppercase text-center">Contact Us</h2>

        <v-responsive
          class="mx-auto mb-12"
          width="56"
        >
          <v-divider class="mb-1"></v-divider>

          <v-divider></v-divider>
        </v-responsive>


      </v-container>

      <div class="py-12"></div>
    </v-sheet> -->

    <v-footer
      class="justify-center"
      color="black"
      height="100"
    >
      <div class="title font-weight-light grey--text text--lighten-1 text-center">
        &copy; {{ (new Date()).getFullYear() }} Fish n Code
        <br>
        <span class="caption">Based on a design by John Leider</span>
      </div>
    </v-footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
          {
            src: '/agentpay.png',
            title: 'AgentPay',
            text: 'A PWA accounts and finance app for letting agencies. Dynamic dashbaord and live transaction functionality.',
            link: 'https://agentpay.app/'
          },
          {
            src: 'https://source.unsplash.com/H4uYCNkNLdM',
            title: 'Ongoing project',
            text: 'Currently user testing a multi-functional PWA for the lettings industry.',
            link: ''
          },
          {
            src: 'https://source.unsplash.com/H4uYCNkNLdM',
            title: 'Ongoing project',
            text: 'Working on a AWS Amplify run PWA, using Lambda, DynamoDB and GraphQL.',
            link: ''
          },
        ],
        services: [
          {
            icon: 'mdi-telescope',
            title: 'Innovative technologies',
            text: 'We employ the very latest Javascript frameworks and libraries in order to provide the best tools solutions available on the market.',
          },
          {
            icon: 'mdi-account-circle-outline',
            title: 'UX Design',
            text: 'Users are at the core of everything we do. Human centred design is paramount to providing the best possible digital solutions that solve user requirements.',
          },
          {
            icon: 'mdi-xml',
            title: 'Low code, no code',
            text: 'Reusable components allows us to do more with less. More time to focus on your business logic in order to get the best out of the applications we build.',
          }
        ],
        languages: [
          ['Javascript', 'CSS3 - HTML5', '/javascript_logo.png'],
          ['Vue.js', 'Nuxt.js - Vuetify', 'vue_logo.svg'],
          ['Amplify', 'Amazon Web Services', 'amplify-logo.png'],
          ['UI/UX', 'UXQB Certified', 'adobexd_logo.svg']
        ],
    }
  },
}
</script>

<style>
  #logo {
    height: 300px;
    /* background-color: red; */
  }

</style>
