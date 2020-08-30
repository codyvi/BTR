<template>
  <div class="wrapper">
    <div class="section page-header header-filter" :style="headerStyle">
      <div class="container">
        <div class="md-layout">
          <div
            class="md-layout-item md-size-33 md-small-size-66 md-xsmall-size-100 md-medium-size-40 mx-auto"
          >
            <login-card header-color="green">
              <h4 slot="title" class="card-title">Register</h4>
              <md-field class="md-form-group" slot="inputs">
                <md-icon>face</md-icon>
                <label>Full Name...</label>
                <md-input v-model="fullName"></md-input>
              </md-field>
                <md-field class="md-form-group" slot="inputs">
                <md-icon>account_circle</md-icon>
                <label>Username...</label>
                <md-input v-model="username"></md-input>
              </md-field>
            <md-field class="md-form-group" slot="inputs">
                <md-icon>account_balance</md-icon>
                <label>University...</label>
                <md-input v-model="university"></md-input>
              </md-field>
                <md-field class="md-form-group" slot="inputs">
                <md-icon>book</md-icon>
                <label>Major...</label>
                <md-input v-model="major"></md-input>
              </md-field>
              <md-field class="md-form-group" slot="inputs">
                <md-icon>email</md-icon>
                <label>Email...</label>
                <md-input v-model="email" type="email"></md-input>
              </md-field>
              <md-field class="md-form-group" slot="inputs">
                <md-icon>lock_outline</md-icon>
                <label>Password...</label>
                <md-input v-model="password"></md-input>
              </md-field>
                <md-field class="md-form-group" slot="inputs">
                <md-icon>lock_outline</md-icon>
                <label>Confirm Password...</label>
                <md-input v-model="confpassword"></md-input>
              </md-field>
              <md-button slot="footer" class="md-simple md-success md-lg">
                Get Started
              </md-button>
            </login-card>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { LoginCard } from "@/components";

export default {
  components: {
    LoginCard
  },
  bodyClass: "register-page",
  data() {
    return {
      firstname: null,
      email: null,
      password: null
    };
  },
  props: {
    header: {
      type: String,
      default: require("@/assets/img/bg9.jpg")
    }
  },
  computed: {
    headerStyle() {
      return {
        backgroundImage: `url(${this.header})`
      };
    }
  }
};
</script>

<style lang="css"></style>
