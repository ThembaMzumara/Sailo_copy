<template>
  <div class="body-container">
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
          </div>
        </div>

        <div class="dropdown">
          <button class="dropbtn">Contact</button>
          <div class="dropdown-content"></div>
        </div>
      </nav>

      <div class="action-buttons">
        <button class="inherit">search</button>
        <button class="inherit">cart</button>
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
        <li>
          <div>
            <img src="" alt="" />
            <p>
              <span id="number"> 500+ </span> <br />
              Highly specialised employees
            </p>
          </div>
        </li>

        <li>
          <div>
            <img src="" alt="" />
            <p>
              <span id="number"> 500+ </span> <br />
              Countries around the world
            </p>
          </div>
        </li>

        <li>
          <div>
            <img src="" alt="" />
            <p>
              <span id="number"> 500+ </span> <br />
              Historical Award Winning
            </p>
          </div>
        </li>

        <li>
          <div>
            <img src="" alt="" />
            <p>
              <span id="number"> 500+ </span> <br />
              Successfully completed projects
            </p>
          </div>
        </li>
      </ul>
    </div>

    <div class="below"></div>
  </div>
</template>

<script setup></script>

<style scoped>
.body-container {
  height: 120vh;
  position: relative;
  text-align: center;
  background-color: black;
  padding: 70px 40px;
  color: white;
  font-family: 'Roboto', sans-serif;

  /* background:url('https://source.unsplash.com/blue-and-black-robot-figurine-S-vkpXA3os8'); */
  background-position: center;
  background-repeat: no-repeat;
  background-origin: content-box;
  background-size: cover;
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
}

a {
  text-decoration: none;
}

.dropbtn {
  background-color: inherit;
  color: white;
  font-size: 16px;
  border: none;
  cursor: pointer;
  padding-top: 8px;
  width: 80px;
}

.dropbtn:hover {
  border: #ff5e14;
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

.dropdown:hover{
  border-top: #ff5e14;
}

.dropdown:hover .dropdown-content {
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
  height: 200px;
  z-index: 2;
  margin: 10px 50px;
  background-color: #f9f9f9;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}

ul {
  list-style: none;
  display: flex;
  flex-wrap: wrap;
  margin: 0 auto;
  padding: 0;
  justify-content: center;
  color: black;
  max-width: 100%;
}

li {
  width: 330px;
  margin: 10px;
  display: flex;
  flex-wrap: wrap;
  margin: 10px;
  justify-content: center;
}

.bar p {
  font-size: 22px;
  text-align: left;
}

#number {
  font-size: 34px;
  font-weight: 700;
}

.below {
  height: 400px;
}
</style>
