<template>
  <div class="hello">
    <h1>Hi There,</h1>
    <h1>I am <span>Azzam Alkhaldi</span> </h1>
    <p>
      Hello, I'm <span>Azzam</span>. My relationship with programing started at a young age, 
      and has become my life-long love. 
      On this website, 
      you'll discover some of my most website i created.
    </p>
    
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello {
  max-width: 500px;

}
.hello p {
  font-size: 20px;
}
.hello span {
  color: #42b983;
}
.hello p span {
  font-size: 26px;
  font-weight: bold;
}
a {
  color: #42b983;
}

@media screen and (max-width: 500px) {
  .hello p {
    max-width: 490px;
  }
  
}

</style>
