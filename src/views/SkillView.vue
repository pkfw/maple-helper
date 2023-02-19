<template>
  <div class="skill">
    <SkillUse msg="블래스터 캔슬 연습" />
  </div>
</template>

<script>
// @ is an alias to /src
import SkillUse from "@/components/SkillUse.vue";

export default {
  name: "SkillView",
  components: {
    SkillUse,
  },
};
</script>
