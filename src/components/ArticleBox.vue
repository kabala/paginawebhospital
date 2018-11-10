<template>
  <div class="article">
    <a>
      <img src="../imagenes/lavanguardia.jpg" /> <br />
      <div class="hover">
        <h3>Especialidades</h3>
        <p>
          La clinica cuenta con especialidades de
          ortopedia,cardiologia,endocrinologia
        </p>
      </div>
    </a>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.article {
  position: relative;
  overflow: hidden;
  cursor: pointer;

  a {
    position: relative;
    overflow: hidden;
    display: block;
  }

  &::hover {
    .hover {
      bottom: 0;
    }
  }

  img {
    position: relative;
    width: 100%;
    height: auto;
  }

  .hover {
    position: absolute;
    bottom: -50px;
    background-color: cyan;
    transition: all 0.3s ease-in-out;
  }
}
</style>
