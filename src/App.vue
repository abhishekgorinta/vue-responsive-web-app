<template>
  <navbar/>
  <Carousel/>
  <Users/>
  <Form/>
  <Footer/>
</template>
<script>
import Carousel from './components/carousel.vue';
import Footer from './components/footer.vue';
import Form from './components/form.vue';
import navbar from './components/navbar.vue';
import Users from './components/users.vue';

export default{
  components:{navbar,Carousel,Users,Form,Footer}
}
</script>