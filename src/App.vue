<script setup>
import "./assets/main.css";
import Hero  from "@/components/home/Hero.vue";
import HomeStore from "@/components/home/HomeStore.vue";
import { ref , onMounted } from "vue";

const productsData = ref(null);

onMounted(async () => {
  try {
    const response = await fetch('@/data/products.json');
    productsData.value = await response.json();
  } catch (error) {
    console.error('Error fetching JSON data:', error);
  }
});

const header = ref(null);

const handleScroll = () => {
  const scrollPosition = window.scrollY;
  console.log(scrollPosition)
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

</script>

<template>
  <header class="header" ref="header">
    <div class="header-wrapper">
      <div class="branding">
        <img src="@/assets/img/Isologo001.jpg" alt="">
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

<!-- Hero Section -->
  <Hero />

<!-- Main store section -->
  <HomeStore :products="productsData" />

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
</template>

<style>
h1 , h2, h3 {
  font-family: var(--sans);
}
p {
  font-family: var(--serif);
}
.header {
  height: var(--header-height);
  width: 100%;
  color: var(--white-origen);
  text-transform: uppercase;
  font-size: 90%;
  margin-block: auto;
  background-color: rgba(0, 0, 0, 0.60);
  position: sticky;
  top: 0;
  z-index: 99;
  scroll-snap-align: start;
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
.footer {
  background-color: rgb(104, 103, 103);
  display: flex;
  align-items: flex-start;
  justify-content: space-around;
  padding-inline: calc((100% - var(--max-width)) / 2);
  padding-block: 2rem;
  color: var(--white-origen);
  scroll-snap-align: end;
}
.copyright {
}
.footer-list {
  padding-inline: 1rem;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  flex-wrap: wrap;
  row-gap: 0.4rem;
  column-gap: 2rem;
  border-left: solid 0.2rem ;
  height: 6rem;
}
</style>./components/Hero.vue./components/home/Hero.vue
