<script setup>
const props = defineProps({
  products: {
    type: Array,
    required: true
  }
});
</script>

<template>
  <section class="store-section">
    <div class="products">
      <div class="prod-display">
        <div class="display__wrap">
          <img v-for="product in products" :src="product.photo" alt="Card Image" class="display__img">
        </div>
      </div>
      <!-- Card -->
      <div class="card-container">
        <div v-for="product in products" class="prod-card">
          <div  class="card__wrap">
            <img :src="product.photo" alt="Card Image" class="card__img">
            <div class="card__content">
  
              <div class="c-content__likes">
                <p>6</p>
                <i class="fa-regular fa-heart"></i>
              </div>
              <div class="c-content__text">
                <h2 class="card__header">{{ product.title }}</h2>
                <p class="card__description">{{ product.description }}</p>
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
    </div>
  </section>
</template>

<style scoped>
.store-section{
}
.products{

}
.prod-display{
  height: var(--prod-display);
  position: sticky;
  top: var(--header-height);
  
}
.display__wrap{
  width: 100%;
  background-color: rgba(0, 0, 0, 0.4);
  padding-inline: calc((100% - var(--max-width)) / 2);
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}
.display__img{
  height: var(--prod-display);
  aspect-ratio: 1/1;
  object-fit: cover;
  padding: calc(0.15 * var(--prod-display));
  background-color: rgba(240, 248, 255, 0.6);
}

/* Card */

.card-container {
  height: calc(100svh - var(--prod-display) - var(--header-height));
  overflow-y: auto;
  scroll-snap-align: end;
}

.prod-card {
  height: 100%;
  background: rgba(240, 248, 255, 0.473);
  border-block: solid 0.5rem rgba(255, 166, 0, 0.9);
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  row-gap: 10rem;
}
.card__wrap{
  scroll-snap-align: end;
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
  color: rgb(83, 86, 88);
}
</style>