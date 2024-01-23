<template>
  <div class="home">
    <div id="contenedor">
      <div id="first_entry">
        <div class="imagen">

        </div>

        <div class="texto">
          <h3>Nuestra Tienda</h3>
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Deleniti aut, est mollitia consectetur fugit necessitatibus ea officia, quaerat laudantium, deserunt aliquam dignissimos soluta nisi tempore nemo facilis perspiciatis culpa quis?</p>
          <div class="boton">
          <button @click="ir_compra">Comprar</button>
        </div>
        </div>
        
      </div>

      <div id="second_entry">
        <div class="imagen"></div>
        <div class="texto" id="second_text">
           <h3>Contactanos</h3>
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Deleniti aut, est mollitia consectetur fugit necessitatibus ea officia, quaerat laudantium, deserunt aliquam dignissimos soluta nisi tempore nemo facilis perspiciatis culpa quis?</p>
          <div class="boton">
            <button @click="ir_contacto">Contactar</button>
          </div>
        </div>
        
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'HomeView',
  methods: {
    ir_compra(){
      this.$router.push({name: 'about'})
    },
    ir_contacto(){
      this.$router.push({name: 'contacto'})
    }
  }
}
</script>

<style scoped lang="sass">
*
  padding: 0
  margin: 0
  box-sizing: border-box
  font-family: 'Inknut Antiqua', serif

  .home
    height: 68vh
    display: flex
    justify-content: center
    align-items: center 
    #contenedor 
      height: 90% 
      width: 80% 
      display: flex
      justify-content: center
      align-items: center
      flex-direction: column
      

      #first_entry
        height: 50% 
        width: 70% 
        display: flex
        justify-content: center
        align-items: center
        margin-bottom: 10px
        margin: 0 20px
        .boton
          width: 100%
          height: 70px
          display: flex
          justify-content: end
          align-items: center 
          button 
            width: 100px
            background-color: white
            border: 3px solid #97572B
            color: #97572B
            cursor: pointer
            transition: .4s
            &:hover
              background-color: #97572B
              color: white

        
      #second_entry
        height: 48% 
        width: 70% 
        display: flex
        flex-direction: row-reverse
        margin-right: 170px
        #second_text
          display: flex
          flex-direction: column
          align-items: flex-end
          justify-content: start
          align-items: flex-start
          .boton
            width: 100%
            height: 70px
            display: flex
            justify-content: end
            align-items: center
            button
              margin-right: 10px
              width: 100px 
              background-color: white
              border: 3px solid #97572B
              color: #97572B
              cursor: pointer
              transition: .4s
              &:hover
                background-color: #97572B
                color: white

      .imagen
          height: 100% 
          width: 40% 
          background: url('https://img.freepik.com/fotos-premium/fondo-muebles-modernos_469760-19704.jpg')
          background-size: cover

      .texto
        height: 100% 
        width: 40% 
        display: flex
        flex-direction: column
        justify-content: start
        align-items: flex-start

        h3 
          font-size: 15px
          margin-left: 5px

        p 
          font-size: 12px
          margin-left: 5px
          width: 98% 
        // h3, p 
        //   margin: 20px


</style>