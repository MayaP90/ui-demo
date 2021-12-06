<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">
        <v-img
          :src="require('@/assets/scribi.png')"
          class="my-3"
          contain
          height="200"
        />
      </v-col>

      <v-col class="mb-4">
        <h1 class="display-2 font-weight-bold mb-3">
          Welcome to Scribi
        </h1>

      </v-col>

      <v-col
        class="mb-5"
        cols="12"
      >
        <v-row justify="center">
    <v-dialog
      v-model="signin"
      persistent
      max-width="600px"
    >
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          color="blue"
          dark
          v-bind="attrs"
          v-on="on"
        >
          Sign In
        </v-btn>
      </template>
      <v-card>
        <v-card-title>
          <span class="text-h5">Sign In</span>
        </v-card-title>
        <v-card-text>
          <v-container>
            <v-row>
              <v-col
                cols="12"
                sm="6"
                md="4"
              >
              </v-col>
              <v-col
                cols="12"
                sm="6"
                md="4"
              >
              </v-col>
              <v-col
                cols="12"
                sm="6"
                md="4"
              >
              </v-col>
              <v-col cols="12">
                <v-text-field
                  label="Email*"
                  required
                ></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-text-field
                  label="Password*"
                  type="password"
                  required
                ></v-text-field>
              </v-col>
              <v-col
                cols="12"
                sm="6"
              >
              </v-col>
            </v-row>
          </v-container>
          <small>*indicates required field</small>
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="blue darken-1"
            text
            @click="signin = false"
          >
            Sign In
          </v-btn>
          <v-btn
            color="blue darken-1"
            text
            @click="signin = false"
          >
            Cancel
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-row>
      </v-col>

      <v-col
        class="mb-5"
        cols="12"
      >
        <v-row justify="center">
    <v-dialog
      v-model="signup"
      persistent
      max-width="600px"
    >
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          color="primary"
          dark
          v-bind="attrs"
          v-on="on"
        >
          Sign Up
        </v-btn>
      </template>
      <v-card>
        <v-card-title>
          <span class="text-h5">User Profile</span>
        </v-card-title>
        <v-card-text>
          <v-container>
            <v-row>
              <v-col
                cols="12"
                sm="6"
                md="4"
              >
                <v-text-field
                  label="Legal first name*"
                  required
                ></v-text-field>
              </v-col>
              <v-col
                cols="12"
                sm="6"
                md="4"
              >
                <v-text-field
                  label="Legal middle name"
                  hint="example of helper text only on focus"
                ></v-text-field>
              </v-col>
              <v-col
                cols="12"
                sm="6"
                md="4"
              >
                <v-text-field
                  label="Legal last name*"
                  hint="example of persistent helper text"
                  persistent-hint
                  required
                ></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-text-field
                  label="Email*"
                  required
                ></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-text-field
                  label="Password*"
                  type="password"
                  required
                ></v-text-field>
              </v-col>
              <v-col
                cols="12"
                sm="6"
              >
              </v-col>
              <v-col
                cols="12"
                sm="6"
              >
              </v-col>
            </v-row>
          </v-container>
          <small>*indicates required field</small>
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="blue darken-1"
            text
            @click="signup = false"
          >
            Sign Up
          </v-btn>
          <v-btn
            color="blue darken-1"
            text
            @click="signup = false"
          >
            Cancel
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-row>
      </v-col>

      <v-col
        class="mb-5"
        cols="12"
      >
        <div class="text-center">
    <v-dialog
      v-model="terms"
      width="500"
    >
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          color="black"
          dark
          v-bind="attrs"
          v-on="on"
        >
          Terms and Conditions
        </v-btn>
      </template>

      <v-card>
        <v-card-title class="text-h5 grey lighten-2">
          Terms and Conditions
        </v-card-title>

        <v-card-text>
          <div>
            <br>
            <p>Agreement to Terms</p>
            <p>These Tems of Use constitute a legally binding agreement made between you, whether personally or on behalf on entity</p>
            <p>("you") and Scribi concerning your access to and ue of the Scribi application website as</p>
            <p> well as any other media from, media channel, mobile application related, linked, or otherwise connected</p>
            <p> thereto (collectively, the "Site"). You agree that by accessing the Site, you have read, understood, and agreed to be bound by all</p>
            <p> of these Terms of Use. IF YOU DO NOT AGREE WITH ALL OF THESE TERMS OF USE, THEN YOU ARE EXPRESSLY</p>
            <p> PROHIBTED FROM USING THE SITE AND YOU MUST DISCONTINUE USE IMEDIATELY. </p>
            </div>
        </v-card-text>

        <v-divider></v-divider>

      </v-card>
    </v-dialog>
  </div>
  <br>
  <p>While using this application you agree to the Terms and Conditions</p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'HelloWorld',

  data: () => ({
    signin: false,
    terms: false,
    signup: false,
    ecosystem: [
      {
        text: 'vuetify-loader',
        href: 'https://github.com/vuetifyjs/vuetify-loader'
      },
      {
        text: 'github',
        href: 'https://github.com/vuetifyjs/vuetify'
      },
      {
        text: 'awesome-vuetify',
        href: 'https://github.com/vuetifyjs/awesome-vuetify'
      }
    ],
    importantLinks: [
      {
        text: 'Documentation',
        href: 'https://vuetifyjs.com'
      },
      {
        text: 'Chat',
        href: 'https://community.vuetifyjs.com'
      },
      {
        text: 'Made with Vuetify',
        href: 'https://madewithvuejs.com/vuetify'
      },
      {
        text: 'Twitter',
        href: 'https://twitter.com/vuetifyjs'
      },
      {
        text: 'Articles',
        href: 'https://medium.com/vuetify'
      }
    ],
    whatsNext: [
      {
        text: 'Explore components',
        href: 'https://vuetifyjs.com/components/api-explorer'
      },
      {
        text: 'Select a layout',
        href: 'https://vuetifyjs.com/getting-started/pre-made-layouts'
      },
      {
        text: 'Frequently Asked Questions',
        href: 'https://vuetifyjs.com/getting-started/frequently-asked-questions'
      }
    ]
  })
}
</script>

<style>
    h2 {
        color: black;
        padding: 30px;
    }
</style>
