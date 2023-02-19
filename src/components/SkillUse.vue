<template>
  <div class="hello">
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
    <h3>매그넘 펀치 캔슬</h3>
    <p>캔슬 전, 키세팅부터 알아봅시다.</p>
    <p>
      <strong>더 킹</strong>은 <strong class="strRed">S</strong>에 할당합니다.
      <br />
      <strong>매그넘 펀치</strong>는 <strong class="strRed">E</strong>에
      할당합니다.
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
</template>

<script>
export default {
  name: "SkillUse",
  props: {
    msg: String,
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
  margin: 10px 5px 0;
}
</style>
