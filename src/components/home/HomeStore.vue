<script setup>
const props = defineProps({
  imageSrc: {
    type: String,
    required: true
  },
  title: {
    type: String,
    required: true
  },
  description: {
    type: String,
    required: true
  }
});
</script>

<template>
  <section class="store-section">
  <div class="products">
      <div class="prod-display">
      <div class="display__wrap">
          <img :src="imageSrc" alt="Card Image" class="display__img">
      </div>
      </div>
      <div class="prod-card">
      <div class="card__wrap">
          <img :src="imageSrc" alt="Card Image" class="card__img">
          <div class="card__content">

          <div class="c-content__likes">
              <p>6</p>
              <i class="fa-regular fa-heart"></i>
          </div>
          <div class="c-content__text">
              <h2 class="card__header">{{ title }}</h2>
              <p class="card__description">{{ description }}</p>
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
  </section>

</template>