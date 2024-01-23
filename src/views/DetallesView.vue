<template>
    <section>
        <div id="contenedor">   
            <div id="imagen">
                <img :src="mueble.imagen" alt="">
            </div>
            <div id="descripcion">
                <div id="cabecera_texto">
                    <h2>Detalles</h2>
                    <p>Este Mueble esta hecho de Madera Australiana, ademas de que viene incorporado un sistema de reclinado, recubierto de cuero y acolchado en la zona de los gluteos para una experiencia mas comoda.</p>
                </div>

                <div id="informacion">
                    <h2>{{mueble.name}}</h2>
                    <p>{{mueble.descripcion}}</p>

                </div>

                <div id="compra">
                    <p>{{mueble.precio}}</p>
                    <button @click="volver_inicio">Comprar</button>
                </div>
            </div>

        </div>
    </section>
</template>

<script>
import { muebles } from '/muebles.js'

export default {
    data(){
        return {
            muebles: muebles,
            mueble: ""
        }
    },
    methods: {
        mostrar(){
            const muebleFound = this.muebles.find(mueble => mueble.id == this.$route.params.id)
            this.mueble = muebleFound

        },
        volver_inicio(){
            this.$router.push({name: 'home'})
        }
    },
    mounted(){
        this.mostrar()
    }
}
</script>

<style scoped  lang="sass">
*
    padding: 0
    margin: 0
    box-sizing: border-box

    section
        height: 68vh
        width: 100%
        display: flex
        justify-content: center
        align-items: center
        flex-direction: row

        #contenedor
            height: 90%
            width: 70% 
            display: flex
            justify-content: center
            align-items: center
            flex-direction: row
            box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25)
            border-radius: 30px

            #imagen
                height: 100% 
                width: 40% 
                border-top-left-radius: 30px
                border-bottom-left-radius: 30px
                img 
                    height: 100% 
                    width: 100% 
                    border-top-left-radius: 30px
                    border-bottom-left-radius: 30px
            #descripcion
                width: 60%
                display: flex
                flex-direction: column
                justify-content: space-around
                align-items: center
                

                #cabecera_texto
                    height: 230px
                    display: flex
                    flex-direction: column
                    align-items: start
                    width: 100%
                    justify-content: space-evenly
                    p 
                        width: 80% 
                        margin-left: 20px
                        letter-spacing: 2px

                    h2 
                        font-size: 35px
                        color: #97572B
                        font-weight: bold
                        margin-left: 20px

                #informacion
                    height: 230px
                    width: 100% 
                    display: flex
                    flex-direction: column
                    align-items: start
                    justify-content: space-evenly
                    margin-top: -40px
                    
                    p 
                        width: 80% 
                        margin-left: 20px
                        letter-spacing: 2.5px

                    h2 
                        font-size: 30px
                        text-align: center
                        margin-left: 20px
                        color: #97572B
                        font-weight: bold

                #compra
                    height: 100px
                    width: 100% 
                    display: flex
                    flex-direction: row
                    justify-content: space-around
                    align-items: center

                    p 
                        font-size: 30px


                    button
                        padding: .7rem
                        width: 150px
                        border: none
                        background-color: white
                        border: 3px solid #97572B
                        font-size: 17px
                        color: #97572B
                        cursor: pointer
                        transition: .4s
                        &:hover
                            background-color: #97572B
                            color: white







</style>