<template>
 <div>
  <p>{{title}}</p>
  <!-- v-model を使ってinput_msgにinputタグで入力した値を都度反映する -->
  <SelectBox @selected="handleSelect"></SelectBox>
  <p>モデル名: {{ selectedValue }}</p>
  <p><input v-model="input_msg">
  <button @click="sendMessage">送信</button></p>
  <!-- 子コンポーネントのmessageに反映した値をを設定して呼び出す -->
  <hello-child :message="input_msg2"/>
 </div>
</template>
 
<script>
// 子コーポネントをインポートしてみよう！
import SelectBox from './SelectBox.vue';
import HelloChild from './HelloChild';

export default {
  data: function () {
    return {
      title: 'はろー！わーるど！',
      selectedValue: null,
      input_msg2: ''
    }
  },
  methods: {
      handleSelect(value) {
        this.selectedValue = value;
      },
      sendMessage() {
        // ここで実際にバックエンドにテキストを送信する処理を行う
        // 以下はサンプルとして、送信した内容をそのままレスポンスとして表示する
        this.input_msg2 = '送信された内容: ' + this.input_msg;
      },
    },
  components: {
    // 子コーポネントを追加してみよう！
    SelectBox,
    HelloChild
  }
}
</script>