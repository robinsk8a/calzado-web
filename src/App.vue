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
          <img src="" alt="" class="card__img">
          <div class="card__content">
            <div class="c-content__likes">
              <p>6</p>
              <img src="./components/img/longos01.jpg" alt="">
            </div>
            <div class="c-content__text">
              <h2>Some shoes</h2>
              <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas est aperiam odit hic, dicta modi harum facere omnis nostrum corrupti ut cumque, ea quia dolore!</p>
            </div>
            <div class="c-content__customer">
              <div class="customer-sizes">
                <h3>Disponibilidad de tallas</h3>
                <ul class="sizes">
                  <li>38</li>
                  <li>39</li>
                  <li>40</li>
                </ul>
              </div>
              <button>Haz tu pedido aquí</button>
            </div>
          </div>
        </div>
      </div>
    </div>

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
.hero-img::after {
  background: linear-gradient(to left, aliceblue, transparent);
  z-index: 8;
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

}
.display__img{

}
.prod-card{

}
.card__wrap{

}
.card__img{

}
.card__content{

}
.c-content__likes{

}
.c-content__text{

}
.c-content__customer{

}
.customer-sizes{

}
.sizes{

}
</style>