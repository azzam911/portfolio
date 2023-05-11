<template>
  <div class="home">
    <HelloWorld/>
    <img class="logo" alt="my-logo" src="../assets/logo.png">
  </div>
  <div class="contact-us">
      <h2>Contact Me:</h2>
        <ul>
            <li>
              <a href="mailto:azzam.h.alkhaldi@gmai.com">Email</a>
            </li>
            <li>
              <a href="https://twitter.com/cyber_az1?s=09" target="_blank">Twitter</a>
            </li>
            <li>
              <a href="https://github.com/azzam911" target="_blank">GitHub</a>
            </li>
        </ul>
    </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  }
}
</script>

<style>
.home {
  display: flex;
  justify-content: space-around;
  align-items: center;
  text-align: left;
}
.home h1 {
  font-weight: bolder;
  margin: 30px 0;
}
.home .logo {
  animation: rotateImg 20s infinite linear;
}

@keyframes rotateImg {
  0%   {transform: rotate(0deg);}
  100% {transform: rotate(360deg);}
}

.contact-us {
    text-align: left;
    margin: 80px;
}
.contact-us ul {
  display: flex;
  gap: 40px;
  padding: 0 !important;
}

.contact-us ul li {
  background-color: #42b983;
  padding: 10px 20px;
  border-radius: 10px;
  cursor: pointer;
  font-size: 20px;
  margin: 20px 0;
  transition: .4s;
}

.contact-us ul li:hover {
  transform: scale(1.1);
}
.contact-us ul li a {
  color: #fff;
  text-decoration: none;
}
.contact-us ul li a:hover {
  color: #fff !important;
}
@media screen and (max-width: 800px) {
  .home {
    flex-direction: column;
    text-align: center;
    gap: 40px;
  }
  .contact-us {
    text-align: center;
  }
  .contact-us ul {
    display: inline-block;
    text-align: center;
    margin: auto;
    gap: 10px;
  }
}
</style>