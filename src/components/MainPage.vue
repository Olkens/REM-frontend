<template>
<Header />
<section id="offer-list">
<ul>
    <li>
    <div class="offer-box">
    <img class="offer-img" src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/43/White_square_50%25_transparency.svg/1024px-White_square_50%25_transparency.svg.png" />
    <h1>Offer</h1>
    <p>This is sample offer box</p>
    <button>See more</button>
</div>
    </li>

    <li>
    <div class="offer-box">
        <img class="offer-img" src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/43/White_square_50%25_transparency.svg/1024px-White_square_50%25_transparency.svg.png" />
    <h1>Offer</h1>
    <p>This is sample offer box</p>
    <button>See more</button>
</div>
    </li>
</ul>

</section>
</template>

<script>
import Header from './layout/Header.vue';

export default {
  components: {
    Header
  },
}
</script>

<style scoped>
body { 
    margin-left: auto;
}
h1 { 
    line-height: 0.5;
}
li { 
    margin-bottom: 20px;
}
ul { 
    list-style-type: none;
}

.offer-box { 
    border: 1px solid;
    width: fit-content;
}
.offer-img{
    height: 170px;
    width: 800px;
    margin-bottom: 5px;
}
</style>


