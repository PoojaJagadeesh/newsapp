<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <v-card>
     <div v-if="$auth.loggedIn">
     Hi {{ $auth.user.name}}
     </div>
      <div v-else>
        <v-card-title class="headline">
         Please register if you are a new user.
        </v-card-title>
         <v-card-actions>
          <v-spacer />
          <v-btn
            color="primary"
            nuxt
            to="/register"
          >
            Register
          </v-btn>
           <v-btn
            color="primary"
            nuxt
            to="/login"
          >
            Login
          </v-btn>
        </v-card-actions>
    
       </div>
       </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>
