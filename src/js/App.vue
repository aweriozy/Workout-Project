<template>
  <div class="wrapper">
    <div class="container">
      <router-view> </router-view>
    </div>
  </div>
</template>

<script></script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");

$mainColor: #000000;
$additionColor: #25ab75;
$textColor: #fff;

::selection {
  background-color: $additionColor;
}

* {
  margin: 0;
  padding: 0;
}

body {
  font-family: "Poppins", sans-serif;
  font-weight: 400;
  background-color: $mainColor;
  color: $textColor;
  font-size: 1em;
}

.wrapper {
  overflow: hidden;
}

a {
  text-decoration: none;
  color: #ababab;
  transition: all 600ms ease;

  &:hover {
    color: #e5e5e5;
  }
}

li {
  list-style: none;
}

.container {
  @media (min-width: 1500px) {
    width: 1300px;
    margin: 0 auto;
  }
  @media (max-width: 1500px) and (min-width: 900px) {
    width: 80%;
    margin: 0 10%;
  }
  @media (max-width: 900px) {
    width: 90%;
    margin: 0 5%;
  }
}
</style>
