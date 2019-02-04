<template>
<section class="container">
  <div class="row">
    <div class="col-10">
  <h1 class="text-center m-2">Apunte su jugada</h1>
   <ul class="tarjeta ">
    <li v-for="i in 12" :key="i">
      <a href="#">
        <h2>Title #{{i}}</h2>
        <p>Text Content #{{i}}</p>
      </a>
    </li>
   </ul>
   </div>
   </div>
 </section>
</template>
<script>
export default {
  layout: 'header'
}
</script>

<style scoped>
template{
  font-family:arial,sans-serif;
  font-size:100%;
  margin:1em;
  background:#666;
  color:#fff;
}

h2,p{
  font-size:100%;
  font-weight:normal;
}
.tarjeta,li{
  list-style:none;
}
.tarjeta{
  overflow:hidden;
  padding:3em;
}
.tarjeta li a{
  text-decoration:none;
  color:#000;
  background:#ffc;
  display:block;
  height:10em;
  width:10em;
  padding:1em;
  -moz-box-shadow:5px 5px 7px rgba(33,33,33,1);
  -webkit-box-shadow: 5px 5px 7px rgba(33,33,33,.7);
  box-shadow: 5px 5px 7px rgba(33,33,33,.7);
  -moz-transition:-moz-transform .15s linear;
  -o-transition:-o-transform .15s linear;
  -webkit-transition:-webkit-transform .15s linear;
}
.tarjeta li{
  margin:1em;
  float:left;
}
.tarjeta li h2{
  font-size:100%;
  font-weight:bold;
  padding-bottom:10px;
}
.tarjeta li p{
  font-family:"Reenie Beanie",arial,sans-serif;
  font-size:100%;
}
.tarjeta li a{
  -webkit-transform: rotate(-6deg);
  -o-transform: rotate(-6deg);
  -moz-transform:rotate(-6deg);
}
.tarjeta li:nth-child(even) a{
  -o-transform:rotate(4deg);
  -webkit-transform:rotate(4deg);
  -moz-transform:rotate(4deg);
  position:relative;
  top:5px;
  background:#cfc;
}
.tarjeta li:nth-child(3n) a{
  -o-transform:rotate(-3deg);
  -webkit-transform:rotate(-3deg);
  -moz-transform:rotate(-3deg);
  position:relative;
  top:-5px;
  background:#ccf;
}
.tarjeta li:nth-child(5n) a{
  -o-transform:rotate(5deg);
  -webkit-transform:rotate(5deg);
  -moz-transform:rotate(5deg);
  position:relative;
  top:-10px;
}
.tarjeta li a:hover,ul li a:focus{
  box-shadow:10px 10px 7px rgba(0,0,0,.7);
  -moz-box-shadow:10px 10px 7px rgba(0,0,0,.7);
  -webkit-box-shadow: 10px 10px 7px rgba(0,0,0,.7);
  -webkit-transform: scale(1.25);
  -moz-transform: scale(1.25);
  -o-transform: scale(1.25);
  position:relative;
  z-index:5;
}
ol{text-align:center;}
ol li{display:inline;padding-right:1em;}
ol li a{color:#fff;}
</style>
