<template>
  <nav>
    <router-link to="/">BLOG</router-link>
    <router-link to="/about">SHOP</router-link>
    <router-link to="#">FOOTERS</router-link>
    <div id="imagen">
      <img src="../src/assets/logo.png" alt="">
    </div>
    <router-link to="#">CART</router-link>
    <router-link to="#">CHECKOUT</router-link>
    <router-link to="/contacto">CONTACT</router-link>
    <div id="cart">
      <i class="fa-solid fa-cart-shopping"></i>
      <p>550€</p>
  </div>
  </nav>
  <footer id="footer">
    <div id="terminos">
      <ul>
        <li>Disclaimer</li> |
        <li>Terms and Conditions</li> |
        <li>Privacy Policy</li>
      </ul>
    </div>
    <div id="logo_blanco">
      <img src="../src/assets/logo_blanco.png" alt="">
    </div>

    <div id="patrocinadores">
      <div>
        <p>Amazon</p>
      </div>
      <div>
        <p>Discorver</p>
      </div>
      <div>
        <p>MasterCard</p>
      </div>
      <div>
        <p>Paypal</p>
      </div>
    </div>

    <img src="" alt="">
  </footer>
  <router-view/>
</template>

<style lang="sass">

*
  padding: 0
  margin: 0
  box-sizing: border-box
  font-family: 'Lato', sans-serif

  #footer
    position: absolute
    bottom: 0
    height: 15vh
    width: 100%
    display: flex
    justify-content: space-around
    align-items: center
    background-color: black
    color: white
    #patrocinadores
      height: 100% 
      width: 38%
      display: flex
      justify-content: space-around
      align-items: center
      div 
        height: 40%
        width: 100px
        background-color: white
        display: flex
        justify-content: center
        align-items: center

        p
          color: black
          font-weight: bold

    #logo_blanco
      height: 100%
      width:250px

      img 
        height: 97.5% 
        width: 90% 
    #terminos
      height: 60%
      width: 500px
      display: flex
      justify-content: center
      align-items: center

      ul 
        display: flex
        justify-content: space-around
        align-items: center
        height: 100%
        width: 100%

        li 
          list-style: none
nav
  height: 17vh
  border: 1px solid
  display: flex
  justify-content: space-around
  align-items: center
  background-color: #FCFCFC
  width: 100%
  #cart
    border: 1px solid
    height: 100%
    width: 100px
    display: flex
    justify-content: center
    align-items: center
    margin-right: -59px
    background-color: black
    flex-direction: column
    cursor: pointer
    margin-right: -17px

    p 
      color: white
    
    i 
      font-size: 30px
      color: white
      margin-bottom: 10px

  a 
    text-decoration: none
    color: black
    font-weight: bold
    margin-left: 100px 
  #imagen
    height: 100%
    img 
      height: 90%
      margin-top: 9px
      margin-left: 30px
  



//   a {
//     font-weight: bold;
//     color: #2c3e50;

//     &.router-link-exact-active {
//       color: #42b983;
//     }
//   }
// }

</style>
