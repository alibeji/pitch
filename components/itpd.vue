<template>
  <div
    class="itpd-wrapper"
    :class="{
      'second-slide': passingData == 2,
      'third-slide': passingData == 3,
      'fourth-slide': passingData == 4,
      'fith-slide': passingData == 5,
    }"
  >
    <svg
      width="216"
      height="72"
      viewBox="0 0 216 72"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <g id="it">
        <path id="Vector" d="M0 71.6V0H13.9V71.6H0Z" fill="#0497AF" />
        <path
          id="Vector_2"
          d="M82.3 12.2H59.5V71.6H45.7V12.2H22.8V0H82.4V12.2H82.3Z"
          fill="#0497AF"
        />
      </g>
      <g id="product">
        <path
          id="Vector_3"
          d="M91.2 71.6V0H121.5C124.8 0 127.8 0.7 130.6 2.1C133.4 3.5 135.8 5.3 137.8 7.5C139.8 9.8 141.4 12.3 142.5 15.2C143.6 18.1 144.2 20.9 144.2 23.8C144.2 26.8 143.7 29.8 142.6 32.6C141.5 35.5 140 38 138.1 40.2C136.2 42.4 133.8 44.2 131 45.5C128.2 46.8 125.2 47.5 121.9 47.5H105V71.5H91.2V71.6ZM105.1 35.4H121.2C123.8 35.4 125.9 34.4 127.6 32.3C129.3 30.2 130.2 27.4 130.2 23.8C130.2 22 129.9 20.4 129.4 18.9C128.9 17.5 128.2 16.2 127.3 15.2C126.4 14.2 125.4 13.4 124.2 12.9C123 12.4 121.8 12.1 120.6 12.1H105.1V35.4Z"
          fill="#B79E0E"
        />
      </g>
      <g id="design">
        <path
          id="Vector_4"
          d="M154 71.6V0H180C185.8 0 191 0.9 195.4 2.8C199.8 4.7 203.5 7.2 206.4 10.5C209.4 13.7 211.6 17.5 213.1 21.8C214.6 26.1 215.3 30.8 215.3 35.7C215.3 41.1 214.5 46.1 212.8 50.5C211.2 54.9 208.8 58.7 205.7 61.8C202.6 64.9 198.9 67.3 194.6 69.1C190.3 70.8 185.4 71.7 180 71.7H154V71.6ZM201.2 35.7C201.2 32.3 200.7 29.1 199.8 26.2C198.9 23.3 197.5 20.8 195.7 18.7C193.9 16.6 191.7 15 189 13.9C186.3 12.8 183.3 12.2 180 12.2H167.9V59.4H180C183.4 59.4 186.5 58.8 189.1 57.6C191.8 56.4 194 54.7 195.8 52.6C197.6 50.5 198.9 48 199.9 45.1C200.8 42.2 201.2 39 201.2 35.7Z"
          fill="#FC9232"
        />
      </g>
    </svg>
  </div>
</template>
<script>
export default {
  props: { passingData: Number },
}
</script>
<style scoped>
.itpd-wrapper {
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: center;
  position: absolute;
  height: fit-content;
  top: 52vh;
  right: 0rem;
  transition: ease all 1s;
}
.itpd-wrapper svg {
  width: 180px;
  transition: ease all 1s;
}
.itpd-wrapper svg #it {
  opacity: 1;
  transition: ease all 1s;
}
.itpd-wrapper svg #product {
  opacity: 1;
  transition: ease all 1s;
}
.itpd-wrapper svg #design {
  opacity: 1;
  transition: ease all 1s;
}
.itpd-wrapper.second-slide {
  top: 1rem;
  right: 1rem;
  width: 200px;
}
.itpd-wrapper.second-slide svg #product {
  opacity: 0.2;
  transition: ease all 1s;
}
.itpd-wrapper.second-slide svg #design {
  opacity: 0.2;
  transition: ease all 1s;
}
.itpd-wrapper.third-slide {
  top: 1rem;
  right: 1rem;
  width: 200px;
}
.itpd-wrapper.third-slide svg #it {
  opacity: 0.2;
  transition: ease all 1s;
}
.itpd-wrapper.third-slide svg #design {
  opacity: 0.2;
  transition: ease all 1s;
}
.itpd-wrapper.fourth-slide {
  top: 1rem;
  right: 1rem;
  width: 200px;
}
.itpd-wrapper.fourth-slide svg #product {
  opacity: 0.2;
  transition: ease all 1s;
}
.itpd-wrapper.fourth-slide svg #it {
  opacity: 0.2;
  transition: ease all 1s;
}
.itpd-wrapper.fith-slide {
  top: 1rem;
  right: 1rem;
  width: 200px;
}
</style>
