<template>

  <div id="app">
    <main>

      <div class="search-box">
        <input
              type="text"
              placeholder="Search..."
              class="search-bar"
        />
      </div>

      <div class="weather-wrap">
        <div class="location-box">
          <div class="location">Madrid, ES</div>
          <div class="date">Friday, 01 July 2022</div>
        </div>
      </div>

      <div class="weather-box">
        <div class="temp">30°C</div>
        <div class="weather">Sunny</div>
      </div>

    </main>
  </div>

</template>

<script>

export default {
  name: 'app',
  data() {
    return {
      api_key: '0bc0b273c04a7177a5d047aed297b692',
      url_base: 'https://api.openweathermap.org/data/2.5/',
      query: '',
      weather: {}
    }
  },
  methods: {

  }
}
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'montserrat', sans-serif;
}

#app {
  background-image: url('./assets/cold-bg.jpg');
  background-position: bottom;
  background-size: cover;
  transition: 0.4;
}

#app.warm { background-image: url('./assets/warm-bg.jpg'); }

main {
  background-image: linear-gradient(to bottom, rgba(0, 0, 0, 0.25), rgba(0, 0, 0, 0.75));
  min-height: 100vh;
  padding: 25px;
}

.search-box {
  margin-bottom: 30px;
  width: 100%;
}

.search-box .search-bar {
  color: #313131;
  display: block;
  font-size: 20px;
  padding: 15px;
  width: 100%;

  appearance: none;
  background: none;
  border: none;
  outline: none;

  background-color: rgba(255, 255, 255, 0.5);
  border-radius: 0px 16px 0px 16px;
  box-shadow: 0px 0px 8px rgba(0, 0, 0, 0.25);
  transition: 0.4s;
}

.search-box .search-bar:focus {
  background-color: rgba(255, 255, 255, 0.75);
  border-radius: 16px 0px 16px 0px;
  box-shadow: 0px 0px 16px rgba(0, 0, 0, 0.25);
}

.location-box .location {
  color: #fff;
  font-size: 32px;
  font-weight: 500;
  text-align: center;
  text-shadow: 1px 3px rgba(0, 0, 0, 0.25);
}

.location-box .date {
  color: #fff;
  font-size: 20px;
  font-style: italic;
  font-weight: 300;
  text-align: center;
}

.weather-box { text-align: center; }

.weather-box .temp {
  background-color:rgba(255, 255, 255, 0.25);
  border-radius: 16px;
  box-shadow: 3px 6px rgba(0, 0, 0, 0.25);
  color: #fff;
  display: inline-block;
  font-size: 102px;
  font-weight: 900;
  margin: 30px 0px;
  padding: 10px 25px;
  text-shadow: 3px 6px rgba(0, 0, 0, 0.25);
}

.weather-box .weather {
  color: #fff;
  font-size: 48px;
  font-style: italic;
  font-weight: 700;
  text-shadow: 3px 6px rgba(0, 0, 0, 0.25);
}
</style>
