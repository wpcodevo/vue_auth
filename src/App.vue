<script setup>
import GoogleLogo from './assets/google.svg';
import { getGoogleUrl } from './utils/getGoogleUrl';

const from = '/';
</script>

<template>
  <div class="container">
    <div class="social-auth">
      <a :href="getGoogleUrl(from)" class="google-auth">
        <img :src="GoogleLogo" alt="Google Logo" />
        <span>Google</span>
      </a>
    </div>
  </div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
a {
  text-decoration: none;
  color: inherit;
}

html {
  font-size: 62.5%;
}

body {
  font-family: Roboto, sans-serif;
  color: #222;
  font-size: 1.6rem;
}

.container {
  background-color: #2363eb;
  height: 100vh;
  width: 100vw;
  display: flex;
  align-items: center;
  justify-content: center;
}

.social-auth {
  max-width: 27rem;
  width: 100%;
  display: flex;
  align-items: center;
  flex-direction: column;
}

.google-auth {
  background-color: #fff;
  border-radius: 5px;
  padding: 0.6rem 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.3s ease-in-out;
}

.google-auth img {
  height: 4rem;
  margin-right: 1rem;
}
.google-auth span {
  font-size: 1.8rem;
}

.google-auth:hover {
  box-shadow: 0 1px 13px 0 rgb(0 0 0 / 15%);
}
</style>
