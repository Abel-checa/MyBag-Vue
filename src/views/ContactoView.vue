<template>
    <section>
        <div id="contacto">
            <h1>CONTACTO</h1>
        </div>
        <div id="inputs">
            <div id="nombre_apellido">
                <input type="text" placeholder="Nombre">
                <input type="text" placeholder="Apellido">
            </div>
            <input type="text" placeholder="Correo Electronico">
            <input type="text" placeholder="Telfono">
            <textarea name="" id="mensage" cols="51" rows="10" placeholder="Escribe un mensage si deseas decirnos algo ..."></textarea>
        </div>
    </section>
</template>

<script>
export default {
    name: 'ContactoView'
}
</script>

<style lang="sass">
*
    padding: 0
    margin: 0
    box-sizing: border-box

    section
        height: 68vh
        width: 100% 
        display: flex
        flex-direction: row
        #contacto
            height: 100% 
            width: 50% 
            display: flex
            justify-content: center
            align-items: center
            h1 
                font-size: 70px

        #inputs
            height: 100% 
            width: 50% 
            display: flex
            flex-direction: column
            justify-content: center
            align-items: flex-start

            input 
                padding: .6rem
                border-radius: 20px
                outline: none
                border: 2px solid #97572B
                width: 52%
                margin-bottom: 30px
                margin-top: -15px
            #mensage
                border-radius: 20px 
                padding: .6rem
                border: 2px solid  #97572B


            #nombre_apellido
                width: 400px
                display: flex
                flex-direction: row
                justify-content: space-between
                align-items: center
                margin-bottom: 20px

                input 
                    padding: .6rem
                    border-radius: 20px
                    outline: none
                    border: 2px solid #97572B
                    margin-right: 10px

               
                    
                

                

</style>