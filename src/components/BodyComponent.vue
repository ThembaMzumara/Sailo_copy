<template>
  <div class="body-container">
    <div class="backgroud-image">
      <header class="body-header">
        <div class="logo">
          <img src="" alt="sailo." />
        </div>

        <nav class="nav-links">
          <div class="dropdown">
            <button class="dropbtn">Home</button>
            <div class="dropdown-content">
              <a href="#">Option 1</a>
              <a href="#">Option 2</a>
              <a href="#">Option 3</a>
            </div>
          </div>

          <div class="dropdown">
            <button class="dropbtn">About</button>
            <div class="dropdown-content"></div>
          </div>

          <div class="dropdown">
            <button class="dropbtn">Service</button>
            <div class="dropdown-content">
              <a href="#">Choice 1</a>
              <a href="#">Choice 2</a>
              <a href="#">Choice 3</a>
            </div>
          </div>

          <div class="dropdown">
            <button class="dropbtn">Project</button>
            <div class="dropdown-content">
              <a href="#">Choice 1</a>
              <a href="#">Choice 2</a>
              <a href="#">Choice 3</a>
            </div>
          </div>

          <div class="dropdown">
            <button class="dropbtn">Pages</button>
            <div class="dropdown-content">
              <a href="#">Choice 1</a>
              <a href="#">Choice 2</a>
              <a href="#">Choice 3</a>
            </div>
          </div>

          <div class="dropdown">
            <button class="dropbtn">Blog</button>
            <div class="dropdown-content">
              <a href="#">Choice 1</a>
              <a href="#">Choice 2</a>
              <a href="#">Choice 3</a>

              <div class="nested-dropdown">
                <a href="#">Choice 4 &#x25B6;</a>
                <div class="nested-dropdown-content">
                  <a href="#">Sub Choice 1</a>
                  <a href="#">Sub Choice 2</a>
                  <a href="#">Sub Choice 3</a>
                  <a href="#">Sub Choice 4</a>
                  <a href="#">Sub Choice 5</a>
                </div>
              </div>
            </div>
          </div>

          <div class="dropdown">
            <button class="dropbtn">Contact</button>
            <div class="dropdown-content"></div>
          </div>
        </nav>

        <div class="action-buttons">
          <button class="inherit">cart</button>
          <button class="inherit">search</button>
          <button class="get-in-touch">Get in Touch</button>
        </div>
      </header>

      <div class="centered-text">
        <h4>Welcome to Sailo</h4>
        <h1>Modern Way To Lead The Future World</h1>
        <p class="par">
          Dapibus aliquet lacus sem egestas netus vestibulum sit turpis scelerisque pharetra pelque
          diam pharetra curabitur.
        </p>
        <router-link to="/" class="discover-more" @click="toggleMenu"> Discover More </router-link>
      </div>

      <div class="bar">
        <ul>
          <li v-for="item in barItems" :key="item.id">
            <div>
              <img :src="item.imgSrc" :alt="item.imgAlt" />
              <p>
                <span id="number">{{ item.number }}</span> <br />
                {{ item.description }}
              </p>
            </div>
          </li>
        </ul>
      </div>
    </div>

    <div class="about-section">
      <div class="about-image">
        <img src="" alt="About Us Image" />
      </div>
      <div class="about-text">
        <h5>About Company</h5>
        <h1>We Are Solving All of Your Business Problem</h1>
        <p>
          Our industry's business policy encompasses the strategies, guidelines, and practices that
          technology companies use to achieve their goals and objectives. The policies may vary
          depending on the company's size, market position, and competitive landscape. Commodo erat
          amet vitae consectetur consectetur feugiat.
        </p>
        <p>
          Tellus viverra eu risus ut ipsum magna sed odio elit. Sed sem purus tincidunt condimentum
          amet condimentum massa. Nunc vel nascetur id cras.
        </p>
        <span> </span>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const barItems = ref([
  {
    id: 1,
    imgSrc: 'path/to/your/image1.jpg',
    imgAlt: 'Specialized Employees',
    number: '500+',
    description: 'Highly specialised employees'
  },
  {
    id: 2,
    imgSrc: 'path/to/your/image2.jpg',
    imgAlt: 'Countries Around the World',
    number: '500+',
    description: 'Countries around the world'
  },
  {
    id: 3,
    imgSrc: 'path/to/your/image3.jpg',
    imgAlt: 'Award Winning',
    number: '500+',
    description: 'Historical Award Winning'
  },
  {
    id: 4,
    imgSrc: 'path/to/your/image4.jpg',
    imgAlt: 'Completed Projects',
    number: '500+',
    description: 'Successfully completed projects'
  }
])
</script>

<style scoped>
.body-container {
  height: 120vh;
  position: relative;
  text-align: center;
  padding: 3px 40px;
  color: white;
  font-family: 'Roboto', sans-serif;
}

.background-image {
  background: url('https://source.unsplash.com/blue-and-black-robot-figurine-S-vkpXA3os8') no-repeat center center;
  background-size: cover;
  min-height: 100vh;
  position: relative;
}

.body-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: inherit;
}

.nav-links {
  display: flex;
  margin: 0;
  padding: 0;
}

a {
  text-decoration: none;
}

.dropbtn {
  background-color: inherit;
  color: white;
  font-size: 18px;
  border: none;
  cursor: pointer;
  padding-top: 30px;
  margin: -50px 0 0 0;
  width: 90px;
  position: relative;
  transition: color 0.3s ease;
}

.dropbtn::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 4px;
  background-color: transparent;
  transition: background-color 0.3s ease;
}

.dropbtn:hover::before {
  background-color: #ff5e14;
}

.dropbtn:hover {
  color: #ff5e14;
}

.dropdown {
  position: relative;
  display: inline-block;
  margin: 0 10px;
}

.dropdown-content {
  display: none;
  position: absolute;
  background-color: #f9f9f9;
  min-width: 190px;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
  z-index: 1;
  margin-top: 3px;
}

.dropdown-content a {
  color: black;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
  width: 150px;
  text-align: left;
}

.dropdown-content a:hover {
  text-decoration: underline;
  text-decoration-color: #ff5e14;
  transition: background-color 0.3s ease;
}

.dropdown:hover {
  border-top: #ff5e14;
}

.dropdown:hover .dropdown-content {
  display: block;
}

.nested-dropdown {
  position: relative;
}

.nested-dropdown-content {
  display: none;
  position: absolute;
  left: 100%;
  top: 0;
  background-color: #f9f9f9;
  min-width: 190px;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
  z-index: 1;
}

.nested-dropdown:hover .nested-dropdown-content {
  display: block;
}

.inherit {
  margin-left: 10px;
  color: #fff;
  background-color: inherit;
  border: none;
}

.get-in-touch,
.discover-more {
  border: none;
  cursor: pointer;
  background-color: #ff5e14;
  padding: 20px 30px;
  margin: 8px;
  color: white;
  font-weight: 600;
  transition: background-color 0.3s ease;
}

.get-in-touch {
  padding: 20px 50px;
}

.par {
  margin-bottom: 50px;
}

.centered-text {
  margin: 180px 210px;
  width: 600px;
  z-index: 1;
  position: relative;
  text-align: left;
}

h4 {
  font-size: 26px;
  color: #ff5e14;
}

h1 {
  font-size: 60px;
}

.bar {
  position: absolute;
  left: 0;
  right: 0;
  top: 900px;
  height: 300px;
  z-index: 2;
  margin: 10px 55px;
  background-color: #f9f9f9;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);

  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

ul {
  list-style: none;
  display: flex;
  flex-wrap: wrap;
  margin: 0;
  padding: 0;
  justify-content: center;
  align-items: center;
  color: black;
  max-width: 100%;
}

li {
  width: 330px;
  margin: 10px;
  padding: 40px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.bar p {
  font-size: 22px;
  text-align: left;
}

#number {
  font-size: 34px;
  font-weight: 700;
}

.about-section {
  margin-top: 500px;
  height: 110vh;
  display: flex;
  justify-content: space-between;
  align-items: center;
  /* background-color: #f9f9f9; */
  color: black;
}

.about-image {
  flex: 1;
  padding-right: 20px;
}

.about-image img {
  width: 100%;
  height: auto;
  border-radius: 10px;
}

.about-text {
  flex: 1;
  padding-left: 20px;
  text-align: left;
}

.about-text h2 {
  font-size: 32px;
  margin-bottom: 20px;
}

.about-text p {
  font-size: 18px;
  line-height: 1.6;
}
</style>
