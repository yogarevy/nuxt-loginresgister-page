<template>
  <div class="container">
    <div class="row justify-content-around align-items-center my-5">
      <div class="col-md-6">
        <img id="image" src="~/static/svg/queue-red.svg" />
      </div>
      <div class="col-md-6">
        <h1 class="title">
          Q Project
        </h1>
        <h2 class="subtitle">
          Welcome to our be loved Apps
        </h2>
        <div class="row links">
          <div class="col-md-5">
            <b-button
              href="/login"
              class="q_button"
              variant="outline-danger"
              size="lg"
            >
              Login
            </b-button>
          </div>
          <div class="col-md-1">
            <small>OR</small>
          </div>
          <div class="col-md-5">
            <b-button
              href="/register"
              class="q_button"
              variant="outline-secondary"
              size="lg"
            >
              Register
            </b-button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
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

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
  animation: fadein 4s;
  -moz-animation: fadein 4s; /* Firefox */
  -webkit-animation: fadein 4s; /* Safari and Chrome */
  -o-animation: fadein 4s; /* Opera */
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
  animation: fadein 5s;
  -moz-animation: fadein 5s; /* Firefox */
  -webkit-animation: fadein 5s; /* Safari and Chrome */
  -o-animation: fadein 5s; /* Opera */
}

small {
  color: #526488;
}

.links {
  justify-content: center;
  align-items: center;
  text-align: center;
  padding-top: 15px;
  animation: fadein 6s;
  -moz-animation: fadein 6s; /* Firefox */
  -webkit-animation: fadein 6s; /* Safari and Chrome */
  -o-animation: fadein 6s; /* Opera */
}

#image {
  width: 100%;
  animation: fadein 2s;
  -moz-animation: fadein 2s; /* Firefox */
  -webkit-animation: fadein 2s; /* Safari and Chrome */
  -o-animation: fadein 2s; /* Opera */
}

.q_button {
  width: 200px;
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
