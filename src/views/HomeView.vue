<template>
  <div>
    <h1>Book Worms</h1>
    <img alt="Vue logo" src="../assets/external-apple-back-to-school-fill-outline-pongsakorn-tan.png">
    <HelloWorld msg="Welcome to Book Worms"/>
     <v-form id="form">
    <v-container fluid >
      <v-alert v-if="isAlert" type="error"> Wrong username or password</v-alert>
      <v-alert v-if="isLoggedIn" type="success">
        Login successful , welcome {{email}}
      </v-alert>
      <v-col
          cols="8"
          md="8" >
          <v-text-field class="text"
            v-model= "email"
            label="E-mail"
            
          ></v-text-field>
        </v-col>
      <v-col
          cols="12"
          sm="6"
        >
           <v-text-field
            v-model="password"
            :append-icon="show3 ? 'mdi-eye' : 'mdi-eye-off'"
            :type="show3 ? 'text' : 'password'"
            name="input-10-2"
            label="Password"
            class="input-group--focused"
            @click:append="show3 = !show3"
          ></v-text-field>
        </v-col>

      <v-btn
      elevation="2"
      color="yellow"
      @click="login"
       > 
      Log in 
      </v-btn>
      <v-container id="signup">
          New to Book Worms? Sign up with us now
        <router-link  tag="button"  to="/signup" >Sign Up</router-link>
        </v-container>
        </v-container>

    </v-form>

    </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  }
}
</script>
