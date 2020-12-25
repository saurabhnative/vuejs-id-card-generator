<template>
  <div id="app">
    <Header :title="title"/>
    <div class="container d-flex container-box">
      <UserInputElements 
        :formData="formData"
        @changeFormData="changeFormData($event)"
      />
      <GeneratedCard :formData="formData"/>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import UserInputElements from "./components/UserInput.vue";
import GeneratedCard from "./components/GeneratedCard.vue";
export default {
  name: "App",
  components: {
    Header,
    UserInputElements,
    GeneratedCard
  },
  data() {
    return {
      title: 'ID Card Generator',
      formData: {
        fullName: "",
        collegeName: "",
        locationName: ""
      }
    }
  },
  methods: {
    changeFormData(keyObject) {
      this.formData = Object.assign(this.formData, keyObject);
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
:root {
  --bg-official: #4047f0;
  --font-body: "Montserrat", sans-serif;
}
.subtitle-section {
  color: var(--bg-official);
  font-family: var(--font-body);
  font-weight: 600;
  font-size: 25px;
}

.subtitle-card {
  font-family: var(--font-body);
  font-weight: 600;
  font-size: 25px;
}

.text-center {
  text-align: center;
}

.container-general {
  display: flex;
  align-items: center;
}

.section-container {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  border: 1px solid #c8c8c8;
}

.section-left {
  border-bottom-left-radius: 16px;
}

.section-right {
  border-bottom-right-radius: 16px;
}

.container-box {
  padding-left: 0;
  padding-right: 0;
}

.form-element {
  margin: 5px;
  min-width: 200px;
}

.form-box {
  width: 100%;
  max-width: 285px;
}

.form-label {
  min-width: 150px;
  display: block;
  font-family: var(--font-body);
  font-weight: 600;
}

.form-input {
  display: block;
  border: 1px solid #c4b4b4;
  border-radius: 10px;
  height: 40px;
  padding: 5px 10px 5px 40px;
}

.font-icon {
  position: relative;
}

.font-icon i {
  position: absolute;
  left: 15px;
  top: 45px;
  color: #000;
}

.btn-generate {
  border: none;
  border-radius: 10px;
  background-color: var(--bg-official);
  color: #fff;
  font-family: var(--font-body);
  font-weight: bold;
  padding: 0.5em;
  margin-top: 1em;
}

.id-card-container {
  display: block;
  width: 100%;
}

.card-container {
  width: 100%;
  height: 300px;
  border-radius: 10px;
  font-family: var(--font-body);
  display: flex;
  align-items: center;
  justify-content: center;
  max-width: 500px;
}

.card-title {
  font-size: 16px;
  color: #babfc9;
  font-weight: bold;
}

.card-input {
  font-size: 16px;
  color: #515a67;
  font-weight: bold;
}

.card-wrapper {
  width: 100%;
  height: 250px;
  background-color: #fff;
  background: linear-gradient(#f8f8f8, #fff);
  box-shadow: 0 8px 16px -8px rgba(0, 0, 0, 0.4);
  border-radius: 10px;
  overflow: hidden;
  position: relative;
  margin: 1.5rem;
  display: flex;
}

.user-card {
  width: 30%;
  height: 100%;
  position: relative;
  background: linear-gradient(to top, var(--bg-official), #8f94fb);
  display: flex;
  justify-content: center;
  align-items: center;
}

.general-information {
  width: 70%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  background-color: #f8f8f8;
}

.user-photo {
  font-size: 6em;
  color: white;
}

.card-element {
  margin-left: 10px;
  margin-bottom: 15px;
}

.card-name {
  font-size: 1.5rem;
}

.college-name {
  font-size: 1.2rem;
}
</style>
