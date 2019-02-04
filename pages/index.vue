<template>
  <section>
    <div class="d-flex justify-content-center m-3">
    <h1>Tablero</h1>
    </div>
    <div class="container">
      <div class="row">
        <!-- <div class="col-sm">
          <h3>Ejemplo de rutas Con Vuex</h3>
        </div>
        <div class="col-sm">
          <h2>JOJO</h2>
        </div> -->

         <!-- <b-row>
           <b-col v-for="i in 8" :key="i">
              <div v-for="j in 8" :key="`${i}${j}`">{{`${i}${j}`}}</div>
           </b-col>
        </b-row>

        <div class="tablero ">
          <div class="celda" v-for="i in 8*8" :key="i">{{i}}</div>
        </div> -->

         <table id="tablero">
      <tr>
        <td>&#9820;</td>
        <td>&#9822;</td>
        <td>&#9821;</td>
        <td>&#9819;</td>
        <td>&#9818;</td>
        <td>&#9821;</td>
        <td>&#9822;</td>
        <td>&#9820;</td>
      </tr>
      <tr>
        <td>&#9823;</td>
        <td>&#9823;</td>
        <td>&#9823;</td>
        <td>&#9823;</td>
        <td>&#9823;</td>
        <td>&#9823;</td>
        <td>&#9823;</td>
        <td>&#9823;</td>
      </tr>
      <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
      </tr>
      <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
      </tr>
      <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
      </tr>
      <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
      </tr>
      <tr>
        <td>&#9823;</td>
        <td>&#9823;</td>
        <td>&#9823;</td>
        <td>&#9823;</td>
        <td>&#9823;</td>
        <td>&#9823;</td>
        <td>&#9823;</td>
        <td>&#9823;</td>
      </tr>
      <tr>
        <td>&#9820;</td>
        <td>&#9822;</td>
        <td>&#9821;</td>
        <td>&#9819;</td>
        <td>&#9818;</td>
        <td>&#9821;</td>
        <td>&#9822;</td>
        <td>&#9820;</td>
      </tr>
    </table>
      </div>
  </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'
 console.log('URL', process.env.NODE_ENV);

export default {
  layout: 'header',
  components: {
    Logo
  },
  data(){
    return {
      matriz: [['hola','adios'],['hola1', 'adios1']],
      matriz1: new Array(2),
    }
  },
  created() {
    this.matriz1[0] = new Array(8);
    this.matriz1[1] = new Array(8);

  }

}
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
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

.tablero{
  display: flex;
  flex-wrap: wrap;
}

.celda{
  flex-basis: calc(100%/8);

}
/* .celda:nth-child(3n+1){
  background-color: red;

}
.celda:nth-child(2n){
  background-color: yellow;

} */
/* .celda:nth-child(even){
  background-color: red;
  grid-row: 1 / 2;
  grid-column: 2/3;

}
.celda:nth-child(odd){
  background-color: yellow;

} */

#tablero{
  background: url(http://jesuscastillo.esy.es/DisenoInterfacesWeb/Tema4/imagenes/madera.jpeg);
  box-shadow: 0 10px 10px -6px rgba(0, 0, 0, .6);
  border-radius: 3px;
  border-collapse: collapse;
  width: 400px;
  height: 400px;
  margin: auto;
}

 td{
  color: #222;
  font-size: 36px;
  text-shadow: 1px 1px 1px rgba(255, 255, 255, 0.6);;
  width: 50px;
  height: 50px;
}

#tablero tr:nth-child(odd) td:nth-child(even),
#tablero tr:nth-child(even) td:nth-child(odd){
  background: rgba(0, 0, 0, 0.5);
}

#tablero tr:nth-child(n+7) td{
  color: #fff;
  text-shadow: 1px 1px 1px rgba(0,0,0,0.6);
}
</style>
