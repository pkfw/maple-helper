<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col">
        <h1>{{ msg }}</h1>
        <p>아래는 시간 측정 가이드입니다.</p>
        <h3>시작 전, 꼭 알고있어야 할 점</h3>
        <p>아래는 KMS 1.2.372 패치 이후 적용사항 입니다.</p>
        <pre>
          [리볼빙 캐논]
          매그넘 펀치, 더블 팡 사용 시 리볼빙 캐논을 직접 사용하는 기능이 삭제되고, 자동으로 발동되게 됩니다.
        </pre>
        <p>
          해당 패치 이후 더 이상 <strong>매그넘 펀치 캔슬</strong>, 일명
          <strong>맥캔</strong>에 매크로 설정이 따로 필요 없어졌습니다.
        </p>
        <h3>맥캔</h3>
        <p>캔슬 전, 키세팅부터 알아봅시다.</p>
        <p>
          <strong>더 킹</strong>은 <strong class="strRed">S</strong>에 할당합니다.
          <br />
          <strong>매그넘 펀치</strong>는 <strong class="strRed">E</strong>에 할당합니다.
          <br />
          <strong>더블 팡</strong>은 <strong class="strRed">R</strong>에 할당합니다.
          <br />
          <strong>점프</strong>는 <strong class="strRed">F</strong>에 할당합니다.
          <br />
        </p>
        <img
          class="skill-icon"
          src="@/assets/skill/image/icon/더킹.png"
          alt="더 킹"
        />
        <img
          class="skill-icon"
          src="@/assets/skill/image/icon/매그넘_펀치.png"
          alt="매그넘 펀치"
        />
        <img
          class="skill-icon"
          src="@/assets/skill/image/icon/더블_팡.png"
          alt="더블 팡"
        />
        <img
          class="skill-icon"
          src="@/assets/skill/image/icon/점프_F.png"
          alt="점프"
        /> 
        <p>이제 사용해봅시다.</p>
      </div>
      <div class="col">
        <div class="skill-box">{{ keyPress }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SkillUse",
  props: {
    msg: String,
  },
  data() {
    return {
      key: "",
      keyPress: "키보드를 입력하세요."
    }
  },
  methods:{
    onKeydown( event ) {
      // 키이벤트 전처리
      console.log(event.key);
      this.key = event.key;
      this.keyPressDown();
    },
    keyPressDown(key) {
      if(this.key == "s" || this.key == "e" || this.key == "r" || this.key == "f") {       
        this.keyPress = this.key;
      } else {
        this.keyPress = "잘못된 키"
      }
      this.keyPress += " 를 누르셨습니다."
    },
    keyPreprocessing() {
      if(this.key == "S" || this.key == "ㄴ") {
        this.key = "s";
      } else if(this.key == "E" || this.key == "ㄷ") {
        this.key = "e";
      } else if(this.key == "R" || this.key == "ㄱ") {
        this.key = "r";
      } else if(this.key == "F" || this.key == "ㄹ") {
        this.key = "f";
      }
    }
  },
  mounted() {
    document.addEventListener( "keydown", this.onKeydown );
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
strong {
  color: #42b983;
}
.strRed {
  color: orange;
}
.skill-icon {
  width: 60px;
  height: 60px;
  margin: 10px 5px;
}
.skill-box {
  border: solid 2px gray;
  border-radius: 10px;
  width: 100%;
  height: 300px;
}
</style>
