<template>
  <div class="container">
    <div
      class="row justify-content-around flex-md-row-reverse align-items-center my-5"
    >
      <div class="col-md-6">
        <img id="image" src="~/static/svg/authentication.svg" />
      </div>
      <div class="col-md-6">
        <a href="/">
          <h1 class="title">
            Q Project
          </h1>
        </a>
        <h2 class="subtitle">
          Login
        </h2>
        <div class="login_form">
          <div class="form-group">
            <label for="login_email">Email address</label>
            <input
              id="login_email"
              type="email"
              class="form-control"
              aria-describedby="emailHelp"
              placeholder="Type email here"
            />
            <small id="emailHelp" class="form-text text-muted"
              >We'll never share your email with anyone else.</small
            >
          </div>
          <div id="form_password" class="form-group form-icon-append">
            <label for="login_password">Password</label>
            <input
              id="login_password"
              v-model="password"
              :type="type"
              class="form-control"
              placeholder="Type password here"
            />
            <i @click="switchVisibility"><font-awesome-icon :icon="icon"/></i>
          </div>
          <div class="links">
            <b-button block type="submit" variant="danger" size="lg">
              Login
            </b-button>
          </div>
          <div class="mt-1">
            <small class="form-text text-muted option-text">
              <b-link href="/forgot-password">
                Forgot Password ?
              </b-link>
            </small>
            <small class="form-text text-muted option-text float-right">
              <b-link href="/register">
                Create Account
              </b-link>
            </small>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      password: '',
      type: 'password',
      icon: ['far', 'eye']
    }
  },
  methods: {
    switchVisibility() {
      if (this.type === 'password') {
        this.type = 'text'
        this.icon = ['far', 'eye-slash']
      } else {
        this.type = 'password'
        this.icon = ['far', 'eye']
      }
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.login_form {
  text-align: left;
  animation: fadein 3s;
  -moz-animation: fadein 3s; /* Firefox */
  -webkit-animation: fadein 3s; /* Safari and Chrome */
  -o-animation: fadein 3s; /* Opera */
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 50px;
  color: #35495e;
  letter-spacing: 1px;
  animation: fadein 3s;
  -moz-animation: fadein 3s; /* Firefox */
  -webkit-animation: fadein 3s; /* Safari and Chrome */
  -o-animation: fadein 3s; /* Opera */
}

.subtitle {
  font-weight: 300;
  font-size: 22px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
  animation: fadein 4s;
  -moz-animation: fadein 4s; /* Firefox */
  -webkit-animation: fadein 4s; /* Safari and Chrome */
  -o-animation: fadein 4s; /* Opera */
}

.links {
  padding-top: 15px;
  animation: fadein 5s;
  -moz-animation: fadein 5s; /* Firefox */
  -webkit-animation: fadein 5s; /* Safari and Chrome */
  -o-animation: fadein 5s; /* Opera */
}

#image {
  width: 100%;
  animation: fadein 2s;
  -moz-animation: fadein 2s; /* Firefox */
  -webkit-animation: fadein 2s; /* Safari and Chrome */
  -o-animation: fadein 2s; /* Opera */
}

a:link {
  text-decoration: none;
}

.option-text {
  display: inline;
}

.form-icon-append {
  position: relative;
}

.form-icon-append > input {
  padding-right: 32px;
}

.form-icon-append > i {
  position: absolute;
  color: rgba(0, 0, 0, 0.54);
  right: 15px;
  bottom: calc(0.375rem - 1px);
}
.form-icon-append > i:hover {
  cursor: pointer;
}

@keyframes fadein {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@-moz-keyframes fadein {
  /* Firefox */
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@-webkit-keyframes fadein {
  /* Safari and Chrome */
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@-o-keyframes fadein {
  /* Opera */
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>
