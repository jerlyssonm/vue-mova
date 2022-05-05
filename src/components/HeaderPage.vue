<template>
  <header>
      <div class="head-box">
          <img class="logo" src="../assets/mova.svg" alt="logo mova">
          <button>
              <img src="../assets/left.png" alt="logo left">
              Voltar
          </button>
      </div>
  </header>
</template>

<script>
export default {
    name: "HeaderPage"

}
</script>

<style scoped>
    .head-box {
        margin: 0 auto;
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 90%;
        padding-top: 12px;
    }
    .logo {
        width: 5rem;
    }
    header {
        height: 5rem;
        width: 100vw;
        box-shadow: 0px 8px 5px -2px rgba(0,0,0,0.54);
    }
    button {
        border: 1px solid rgb(112, 3, 107);
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        width: 5rem;
        height: 1.5rem;
        cursor: pointer;
    }
    button img {
        width: 1rem;
    }
</style>