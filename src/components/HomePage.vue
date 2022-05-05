<template>
  <div class="home-box">
      <div class="input-box">
          <div class="mini-box">
              <p>Filtrar Por</p>
              <input type="text" placeholder="Escolha uma Opção">
          </div>
          <div class="mini-box">
              <p>Pesquisar Por</p>
              <input type="text" placeholder="Escolha uma Opção">
          </div>
          <div class="mini-box">
              <button>PESQUISAR</button>
          </div>
      </div>
      <div class="tags">
          <div class="tag" v-for="prod in prods" :key="prod.flag">
            <img v-bind:src="prod.flags.svg" v-bind:alt="prod.flag">            
          </div>
      </div>
  </div>
</template>

<script>
export default {
    name: "HomePage",
    data() {
        return {
            prods: []
        }
    },created() {
        fetch("https://restcountries.com/v3.1/all")
        .then(async res => {
            this.prods = await res.json()
            this.prods = this.prods.slice(0,12)
            })
        .catch(err => console.log(err))
    }
}
</script>

<style scoped>
    .home-box{
        width: 75%;
        margin: 3.5rem auto 2rem;
    }
    .input-box {
        text-align: left;
        display: flex;
        justify-content: space-between;
    }
    .mini-box {
        width: 30%;
    }
    .mini-box button {
        margin-top: .5rem;
        cursor: pointer;
        color: white;
        width: 8rem;
        height: 1.8rem;
        border: 1px solid rgb(112, 3, 107);
        border-radius: 10px;
        background-color: rgb(112, 3, 107);
    }
    .mini-box button:active {
        color: rgb(112, 3, 107);
        background-color: white;        
    }
    .tags {
        margin-top: 1rem;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-evenly;
    }
    .tag {        
        margin: .3rem;
        width: 23%;
        height: 9rem;
        box-shadow: 0px 3px 5px 2px rgba(0,0,0,0.40);
    }
    .tag img{
        width: 100%;
        height: 100%;
    }
</style>