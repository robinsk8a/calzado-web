<script setup>
import "./assets/main.css";
</script>

<template>
  <header class="header">
    <div class="header-wrapper">
      <div class="branding">
        <img src="./components/img/Isologo001.jpg" alt="">
        <div class="brand">
          <h3 >Origen</h3>
          <p>BY LONGOS</p>
        </div>
      </div>
      <nav class="nav">
        <li>Mayoristas</li>
        <li>Constacto</li>
      </nav> 
    </div>
  </header>
  <section class="hero">
    <img src="./components/img/longos02.jpg" alt="" class="hero-img">
    <div class="hero-section">
      <h1 class="h-title">Calzado Longos</h1>
      <p class="h-text">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Voluptatibus eaque earum laboriosam quidem, similique odit!</p>
      <button class="h-c2a">Comprar en Linea</button>
    </div>
  </section>
  <section class="store-section">
    <div class="products">
      <div class="prod-display">
        <div class="display__wrap">
          <img src="./components/img/longos01.jpg" alt="" class="display__img">
        </div>
      </div>
      <div class="prod-card">
        <div class="card__wrap">
          <img src="./components/img/longos01.jpg" alt="" class="card__img">
          <div class="card__content">

            <div class="c-content__likes">
              <p>6</p>
              <i class="fa-regular fa-heart"></i>
            </div>
            <div class="c-content__text">
              <h2 class="card__header">Some shoes</h2>
              <p class="card__description">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas est aperiam odit hic, dicta modi harum facere omnis nostrum corrupti ut cumque, ea quia dolore!</p>
            </div>
            <div class="c-content__customer">
              <div class="customer-sizes">
                <h4>Disponibilidad de tallas</h4>
                <ul class="customer__sizes">
                  <li>38</li>
                  <li>39</li>
                  <li>40</li>
                </ul>
              </div>
              <button class="c-content__button">
                Haz tu pedido aquí
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
    <footer class="footer">
      <div id="copyright" align="center"><small>&copy; 2024 - origenbylongos.com</small></div>
      <ul class="footer-list">
        <li>Outlet y Descuentos</li>
        <li>Comprar en Pereira</li>
        <li>Pedidos por mayor</li>
        <li>Comprar en línea</li>
        <li>Novedades</li>
        <li>Contacto</li>
      </ul>
    </footer>
  </section>
</template>

<style>
h1 , h2, h3 {
  font-family: var(--sans);
}
p {
  font-family: var(--serif);
}
.header {
  height: 4rem;
  width: 100%;
  color: var(--white-origen);
  text-transform: uppercase;
  font-size: 90%;
  margin-block: auto;
  background-color: rgba(0, 0, 0, 0.60);
  
}
.header-wrapper {
  height: 100%;
  max-width: var(--max-width) ;
  margin-inline: auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.branding{
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.8rem;  
}
.branding img {
  height: 2.8rem;
  border-radius: 50%;
}
.branding p {
  font-size: 50%;
  text-align: center;
}
.branding li {
  
  
}
.brand{

}
.nav{
  display: flex;
  align-items: center;
  gap: 1.4rem;
  font-weight: 600;
  font-family: var(--sans);
}
.hero{
  max-width: var(--max-width) ;
  height: calc(80svh - 4rem);
  display: flex;
  margin-inline: auto;
  margin-block: 10svh;
  background: rgb(228, 230, 231);
  border-radius: 2rem;
  overflow: hidden;
  box-shadow: 0 0.4rem 2rem 0.1rem rgba(0, 0, 0, 0.3);
}
.hero-img{
  height: 110%;
  mask-image: linear-gradient(to left, transparent 10%, black 50%);
  mask-mode: alpha;
  width: 45%;
  object-fit: cover;
}

.hero-section{
  max-width: 45rem;
  display: flex;
  flex-direction: column;
  padding: 10svh 2rem;
  height: 100%;
  width: 100%;
  flex: 1;
  margin-inline: auto;
}
.h-title{
  color: var(--red-origen);
  margin-bottom: 4svh;
  font-size: 2.4rem;
}
.h-text{
  padding-left: 1rem;
}
.h-c2a{
  margin-top: auto;
  margin-inline: auto;
  margin-bottom: 2rem;
  background-color: var(--red-origen);
  padding: 0.8rem 4rem;
  font-size: 2rem;
  border-radius: 1.4rem;
  color: aliceblue;
  box-shadow: 0 0.1rem 0.5rem 0rem rgba(0, 0, 0, 0.6);
  
}
.store-section{
  
}
.products{

}
.prod-display{

}
.display__wrap{
  width: 100%;
  background-color: rgba(0, 0, 0, 0.4);
  padding-inline: calc((100% - var(--max-width)) / 2);
  display: flex;
  justify-content: space-between;
}
.display__img{
  height: 20svh;
  padding: 2rem;
  background-color: rgba(240, 248, 255, 0.6);
}
.prod-card {
  background: rgba(240, 248, 255, 0.473);
  border-block: solid 0.5rem rgba(255, 166, 0, 0.9);
  width: 100%;
  height: 70svh;
  display: flex;
  justify-content: center;
  align-items: center;
}
.card__wrap{
  max-width: var(--max-width);
  height: 80%;
  margin: auto;
  background-color: var(--white-origen);
  border-radius: 2rem;
  overflow: hidden;
  display: flex;
  gap: 2rem;
  margin: auto;
}
.card__img{
  height: 100%;
  max-width: 45%;
  object-fit: cover;
}
.card__content{
  display: flex;
  flex-direction: column;
  position: relative;
  padding: 2.5rem 1rem;
}
.c-content__likes{
  display: flex;
  align-items: center;
  gap: 0.6rem;
  position: absolute;
  top: 1.4rem;
  right: 3rem;
  font-family: var(--sans);
  font-weight: 800;
}
.c-content__text{
  
}
.card__header {
  margin-bottom: 2rem;
}
.card__description{
  padding-left: 1rem;
}
.c-content__customer{
display: flex;
justify-content: space-around;
padding-inline: 1rem;
margin-top: auto;
}
.customer-sizes{
 display: flex;
 flex-direction: column;
 gap: 0.4rem;
 color: rgb(131, 130, 130);
 font-size: 80%;
}
.customer__sizes{
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
}
.c-content__button {
  background: var(--orange-origen);
  padding: 0.2rem 1rem;
  border-radius: 1rem;
  font-size: 70%;
  font-weight: 600;
}
.footer {
  background-color: rgb(104, 103, 103);
  display: flex;
  align-items: flex-start;
  justify-content: space-around;
  padding-inline: calc((100% - var(--max-width)) / 2);
  padding-block: 2rem;
  color: var(--white-origen);
}
.copyright {
}
.footer-list {
  padding-inline: 1rem;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 0.4rem;
  border-left: solid 0.2rem ;
}
</style>