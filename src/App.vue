<script>
  import Form from './components/Form.vue'

  export default {
    components: {
      Form: Form
    },
    data() {
      return {
        result1: '',
        recieved:'この門をくぐる者は一切の希望を捨てよ',
        count:0
      }
    },
    methods: {
      receive(data1) {
        //data1,data2は子コンポーネントから受け取った値
        this.count += 1;
        this.result1 = data1[this.count];
        this.recieved = this.result1.hint;
      }
    }
  };
</script>

<template>
  <header>
    <div>
    </div>
    <div class="wrapper">
      <p>{{recieved}}</p>
      <Form @emit-event="receive"></Form>
    </div>
  </header>

</template>

<style>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
