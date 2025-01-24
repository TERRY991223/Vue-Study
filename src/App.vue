<template>
<h1>영화 정보</h1>
<div v-for="(movie, i) in data" :key="i">
  <figure>
    <img :src="`${movie.imgUrl}`" alt="">
  </figure>
  <h3 class="bg-yellow" :style="textRed">{{movie.title}}</h3>
  <p>개봉 : {{ movie.year }}</p>
  <p>장르 : {{ movie.category }}</p>
  <button 
  @click="increseLike(i)">좋아요
</button>
  <span>{{ movie.like }}</span>
</div>
<!-- 반복문 -->
 <p v-for="(item, i) in foods" :key="i">{{ item }}</p>

</template>

<script>
export default {
  name:'App',
  data() {
    return {
    data: [
      {
        title: "극한 직업",
        year: 2023,
        category: "액션, 판타지, 어드벤처",
        like:0,
        imgUrl: "./assets/image1.webp",
      },
      {
        title: "퍼펙트맨",
        year: 2022,
        category: "액션, 코미디",
        like:0,
        imgUrl: "./assets/image2.webp",

      },
      {
        title: "노량",
        year: 2023,
        category: "액션, 드라마",
        like:0,
        imgUrl: "./assets/image3.webp",

      },
      ]
    }
  },
  methods:{
    increseLike(i) {
      this.data[i].like += 1;
    }
  }
}
</script>

<style>
.bg-yellow {
  background-color: yellow;
}

</style>
