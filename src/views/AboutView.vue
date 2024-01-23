<template>
  
  <section>
    <div v-for="mueble in muebles" :key="mueble" id="contenedor">
      <div class="imagen">
        <img :src="mueble.imagen" alt="">
      </div>

      <div class="informacion">
        <div class="texto">
          <p>{{mueble.name}}</p>
          <p>{{mueble.precio}}</p>
        </div>
        <div class="boton">
            <router-link :to="{ name: 'detalles', params: { id: mueble.id } }">Detalles</router-link>
        </div>

      </div>

    </div>
  </section>
</template>

<script>
import { muebles } from "/muebles.js";
console.log(muebles);

export default {
  name: 'CompraView',
  data(){
    return{
      muebles: muebles
    }
  }
}
</script>

<style lang="sass">
*
  padding: 0
  margin: 0
  box-sizing: border-box

  section
    height: 68vh
    display: flex
    justify-content: space-around
    align-items: center 

    #contenedor
      height: 70% 
      width: 300px
      display: flex
      flex-direction: column
      border-radius: 30px
      box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25)

      .informacion
        display: flex
        justify-content: center
        align-items: center
        flex-direction: row
        width: 100%
        height: 100% 
        .texto
          display: flex
          flex-direction: column
          justify-content: space-around
          height: 100% 
          width: 70%
          align-items: flex-start
          text-align: start

          p 
            margin-left: 15px
            color: #97572B
            font-size: 18px

        .boton
          width: 40% 
          height: 100% 
          display: flex
          justify-content: center
          align-items: flex-end
          a
            margin-bottom: 30px
            padding: .6rem
            background-color: black
            color: white
            width: 90% 
            border-radius: 20px
            text-decoration: none
            text-align: center
        

      .imagen
        height: 70% 
        width: 100%
        border-border-top-left-radius: 30px
        border-border-top-right-radius: 30px
        img 
          height: 100% 
          width: 100%
          border-top-left-radius: 30px
          border-top-right-radius: 30px
          

</style>
