<template>
  <div id="app">
    <img alt="temp" src="./assets/Google.png">
    <Header></Header>
        <Logo></Logo>
        <SearchSection></SearchSection>
        <Languages></Languages>
        <Footer></Footer>
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Header from './components/Header.vue';
import Logo from './components/Logo.vue';
import SearchSection from './components/SearchSection.vue';
import Languages from './components/Languages.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    Logo,
    SearchSection,
    Languages,
    Footer
  },
  data(){
    return {
      tempBackgroundImage:{backgroundImage:"./assets/Google.png"}
    };
  }
}
</script>

<style>
body{
  margin: 0;
}
#app {
  width: 100vw;
  height: 100vh;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;  
  margin: 0 0 0 0 !important;
  padding:0;
   display: flex;
      flex-direction: column;
      justify-content: center;
}

.google-container{
  width: 100vw;
  height: 100vh;
  background-color: red;
}

#app img {
  width: 100vw;
  height: 100vh;
  opacity: 50%;
  position: fixed;
  z-index: +1;
  /* transform: translateX(-50%); */
}



  /* .container {
      display: flex;
      flex-direction: column;
      justify-content: center;
  } */

.header {
    padding: 6px;
    height: 60px;
    box-sizing: border-box;
    display: flex;
    justify-content: flex-end;
}

.header-content {
    width: auto;
    display: flex;
    justify-content: center;
    align-items: center;
}

.header-content p {
    display: inline;
    height: auto;
    text-align: center;
    line-height: 24px;
    font-size: 13px;
    font-family: sans-serif;
    margin: 0 7.5px;
    color: rgba(0, 0, 0, 0.87);
    cursor: pointer;
}

.header-content .dots-container {
    box-sizing: border-box;
    padding: 12px;
    width: 48px;
    height: 48px;
}

.header-content .dots-container .dots {
    box-sizing: border-box;
    width: 24px;
    height: 24px;
    cursor: pointer;
}

.header-content .dots-container .dots:hover {
    box-shadow: 1px 1px 15px rgba(255, 0, 0, 0.8);
    background-color: rgba(255, 0, 0, 0.3);
}

.header-content .profile-image-container {
    width: 48px;
    padding: 8px;
    box-sizing: border-box;
    height: 48px;
    display: flex;
    justify-content: center;
    align-content: center;
}

.profile-image {
    cursor: pointer;
    width: 32px;
    height: 32px;
    border-radius: 150px;
    background-image: url("./assets/1_mk1-6aYaf_Bes1E3Imhc0A.jpeg");
    background-repeat: no-repeat;
    background-size: cover;
    overflow: visible;
}

.profile-image:hover {
    box-shadow: 1px 1px 15px rgba(255, 0, 0, 0.8);
}

.logo-container {
    width: 100%;
    height: 25%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-end;
}

.logo-container .google-logo {
    width: 50%;
    max-width: 300px;
    max-height: 125px;
}

.search-container {
    width: 100%;
    padding: 20px;
    min-height: 160px;
    height: auto;
    box-sizing: border-box;
    display: flex;
    justify-content: center;
}

.search-bar {
    display: flex;
    width: 100%;
    justify-content: space-between;
    flex: 1;
    padding: 8px 8px 8px 16px;
    border-radius: 28px;
    border: 1px solid rgba(0, 0, 0, 0.2);
    box-sizing: border-box;
}

.search-bar input[type="text"] {
    width: 50vw;
    max-width: 400px;
    outline: none;
    border: none;
}

.search-icon {
    background-image: url("./assets/R.png");
    background-size: contain;
    background-repeat: no-repeat;
    height: 16px;
    width: 16px;
}

.search-bar .keyboard-icon {
    background-image: url("./assets/keyboard1600.png");
    background-size: contain;
    background-repeat: no-repeat;
    height: 16px;
    width: 16px;
    margin: 0 5px;
    cursor: pointer;
}

.search-bar .google_mic {
    background-image: url("./assets/google_mic.png");
    background-size: contain;
    background-repeat: no-repeat;
    height: 16px;
    width: 16px;
    margin: 0 5px;
    cursor: pointer;
}

.search-bar:hover {
    box-shadow: 0.5px 0.5px 15px rgba(0, 0, 0, 0.2);
}

.search-buttons {
    height: 90px;
    padding-top: 17px;
    box-sizing: border-box;
    display: flex;
    justify-content: center;
    align-items: center;
}

.search-buttons button {
    width: auto;
    height: 36px;
    min-width: 54px;
    text-align: center;
    cursor: pointer;
    margin: 5px;
    font-size: 14px;
    padding: 0 16px;
    border-radius: 4px;
    color: #3c4043;
    background-color: #f8f9fa;
    line-height: 27px;
    box-sizing: border-box;
    border: 1px solid rgba(0, 0, 0, 0);
}

.search-buttons button:hover {
    border: 1px solid rgba(0, 0, 0, 0.2);
}

.available-languages-container {
    width: 100%;
    height: 100%;
    max-height: 300px;
    display: flex;
    align-items: flex-start;
    justify-content: center;
}

.available-languages-container .language-list {
    width: 40vw;
    height: 28px;
    display: flex;
    justify-content: space-evenly;
    line-height: 28px;
    color: #3c4043;
    font-family: sans-serif;
    font-size: small;
    flex-wrap: wrap;
}

.available-languages-container .language-list a {
    padding: 0 3px;
    font: 13px;
    color: #1a0dab;
    text-decoration: none;
}

.footer .real-footer,
.footer .country {
    border-bottom: 1px solid #dadce0;
    font-size: 15px;
    color: rgba(0, 0, 0, 0.54);
}

.footer {
    background: #f2f2f2;
}

.footer .real-footer {
    display: flex;
    width: 100%;
    height: auto;
    box-sizing: border-box;
    padding: 0 20px;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
}

.footer .real-footer a {
    text-decoration: none;
    color: rgba(0, 0, 0, 0.54);
    padding: 15px;
    font-size: 14px;
    font-family: sans-serif;
}

.footer .real-footer div {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
}

.footer .country {
    padding: 15px 30px;
    font-size: 15px;
    font-family: sans-serif;
}

@media only screen and (max-width: 340px) {
    .footer .country {
        font-size: 10px;
        padding: 10px 25px;
    }
    .footer .real-footer div a {
        padding: 10px;
        font-size: 9px;
    }
    .search-buttons {
        flex-wrap: wrap;
    }
}
</style>
