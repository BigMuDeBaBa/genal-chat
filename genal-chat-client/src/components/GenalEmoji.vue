<template>
  <a-popover title="Emoji">
    <template slot="content">
      <div class='emoji-content'>
        <div>
          <span @click='addEmoji("😃")'>😃</span>
          <span @click='addEmoji("😁")'>😁</span>
          <span @click='addEmoji("😂")'>😂</span>
          <span @click='addEmoji("😄")'>😄</span>
          <span @click='addEmoji("😅")'>😅</span>
          <span @click='addEmoji("😆")'>😆</span>
          <span @click='addEmoji("😇")'>😇</span>
          <span @click='addEmoji("😈")'>😈</span>
          <span @click='addEmoji("😉")'>😉</span>
        </div>
        <div>
          <span @click='addEmoji("😊")'>😊</span>
          <span @click='addEmoji("😋")'>😋</span>
          <span @click='addEmoji("😌")'>😌</span>
          <span @click='addEmoji("😍")'>😍</span>
          <span @click='addEmoji("😎")'>😎</span>
          <span @click='addEmoji("😏")'>😏</span>
          <span @click='addEmoji("😐")'>😐</span>
          <span @click='addEmoji("😒")'>😒</span>
          <span @click='addEmoji("😓")'>😓</span>
        </div>
        <div>
          <span @click='addEmoji("😔")'>😔</span>
          <span @click='addEmoji("😕")'>😕</span>
          <span @click='addEmoji("😖")'>😖</span>
          <span @click='addEmoji("😗")'>😗</span>
          <span @click='addEmoji("😘")'>😘</span>
          <span @click='addEmoji("😙")'>😙</span>
          <span @click='addEmoji("😚")'>😚</span>
          <span @click='addEmoji("😜")'>😜</span>
          <span @click='addEmoji("😝")'>😝</span>
        </div>
        <div>
          <span @click='addEmoji("😞")'>😞</span>
          <span @click='addEmoji("😟")'>😟</span>
          <span @click='addEmoji("😠")'>😠</span>
          <span @click='addEmoji("😡")'>😡</span>
          <span @click='addEmoji("😢")'>😢</span>
          <span @click='addEmoji("😣")'>😣</span>
          <span @click='addEmoji("😤")'>😤</span>
          <span @click='addEmoji("😥")'>😥</span>
          <span @click='addEmoji("😦")'>😦</span>
        </div>
        <div>
          <span @click='addEmoji("😨")'>😨</span>
          <span @click='addEmoji("😩")'>😩</span>
          <span @click='addEmoji("😪")'>😪</span>
          <span @click='addEmoji("😫")'>😫</span>
          <span @click='addEmoji("😬")'>😬</span>
          <span @click='addEmoji("😭")'>😭</span>
          <span @click='addEmoji("😮")'>😮</span>
          <span @click='addEmoji("😯")'>😯</span>
          <span @click='addEmoji("😰")'>😰</span>
        </div>
        <div>
          <span @click='addEmoji("😲")'>😲</span>
          <span @click='addEmoji("😳")'>😳</span>
          <span @click='addEmoji("😴")'>😴</span>
          <span @click='addEmoji("😵")'>😵</span>
          <span @click='addEmoji("🧐")'>🧐</span>
          <span @click='addEmoji("😷")'>😷</span>
          <span @click='addEmoji("🙁")'>🙁</span>
          <span @click='addEmoji("🙂")'>🙂</span>
          <span @click='addEmoji("🙃")'>🙃</span>
        </div>
        <div>
          <span @click='addEmoji("🤐")'>🤐</span>
          <span @click='addEmoji("🤑")'>🤑</span>
          <span @click='addEmoji("🤒")'>🤒</span>
          <span @click='addEmoji("🤓")'>🤓</span>
          <span @click='addEmoji("🤔")'>🤔</span>
          <span @click='addEmoji("🤕")'>🤕</span>
          <span @click='addEmoji("🤠")'>🤠</span>
          <span @click='addEmoji("🤡")'>🤡</span>
          <span @click='addEmoji("🤢")'>🤢</span>
        </div>
        <div>
          <span @click='addEmoji("🤤")'>🤤</span>
          <span @click='addEmoji("🤥")'>🤥</span>
          <span @click='addEmoji("🤧")'>🤧</span>
          <span @click='addEmoji("🤨")'>🤨</span>
          <span @click='addEmoji("🤩")'>🤩</span>
          <span @click='addEmoji("🤪")'>🤪</span>
          <span @click='addEmoji("🤫")'>🤫</span>
          <span @click='addEmoji("🤬")'>🤬</span>
          <span @click='addEmoji("🤭")'>🤭</span>
        </div>
      </div>

    </template>
    <div trigger="click" class='genal-emoji'>
      😃
    </div>
  </a-popover>
</template>

<script lang="ts">
import { Component, Vue, Prop, Watch } from 'vue-property-decorator';


@Component
export default class GenalMessage extends Vue {
  addEmoji(emoji: string) {
    this.$emit('addEmoji', emoji)
  }
}
</script>
<style lang="scss" scoped>
.genal-emoji {
  height: 40px;
  width: 45px;
  position: absolute;
  cursor: pointer;
  left: 0px;
  top: 0px;
  z-index: 999;
  line-height: 40px;
  transition: .2s all linear;
  &:hover {
    background-color: rgb(135, 206, 235, .2);
  }
}
.emoji-content {
  color:#000;
  font-size:20px;
  span {
    cursor: pointer;
  }
}
</style>
