<script>
  import Form from './components/Form.vue'

  export default {
    components: {
      Form: Form
    },
    data() {
      return {
        result1: '',
      }
    },
    methods: {
      receive(data1) {
        //data1,data2は子コンポーネントから受け取った値
        this.result1 = data1[1];
      }
    }
  };
</script>

<template>
  <header>
    <div>
    </div>
    <div class="wrapper">
      <p>Result Area</p>
      <p>Result Text:{{result1.hint}}</p>
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
