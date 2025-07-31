<script>
  export default {
    data() {
      return {
        questions: {
          0: {
            qNum: 0,
            hint: "この門をくぐる者は一切の希望を捨てよ",
            answer: ""
          },
          1:{
            qNum: 1,
            hint: "2ch発祥、初めて書き込みをする前にまずはしばらく場の様子をよく見学するよう促す言葉（6文字）",
            answer: "半年ROMれ"
          },
          2: {
            qNum: 2,
            hint: "乳首や陰核を敏感にしたり肥大させるために、人為的に吸引する器具（7文字）",
            answer: "ニップルポンプ"
          },
          3: {
            qNum: 3,
            hint: "催淫ガスや触手、スライムなどの罠で冒険者を翻弄する迷宮（11文字）",
            answer: "エロトラップダンジョン"
          },
          4: {
            qNum: 4,
            hint: "確実に精子を子宮に送り込むため、女性の脚を持ち上げたまま体重をかけて腰を打ち付ける体位の俗称（6文字）",
            answer: "種付けプレス"
          },
          5: {
            qNum: 5,
            hint: "がるまにで販売中、「マッスルサロンへようこそ!」「アサギ先輩、幸せになろうよ」などの濃厚な性描写と激重感情に定評のある作品を制作しているサークルの名前（5文字）",
            answer: "愛沢精肉店"
          },
          6: {
            qNum: 6,
            hint: "おつかれさまでした。引越し先のアカウントはこちらです。",
            answer: "アドレス"
          }
        }
        ,
        answer: "",
        count:0
      }
    },
    methods: {
      onClickEmit() {
        this.$emit('emit-event', this.questions);
        this.count += 1;
      }
    }
  }
</script>

<template>
  <div id="emit-area">
    <div v-if="count == 0">
      <button @click="onClickEmit">進む</button>
    </div>
    <div v-else>
      <label>Answer:<input type="text" v-model="answer"></label>
      <button @click="onClickEmit">回答</button>
    </div>
  </div>
</template>

<style>
</style>
