<template>
  <div class="hello">
    <img :src="img[0]" />
    <div class="one">
      <div class="title">
        <div class="mark">
          <div class="num">ONE</div>
          <div class="jiao"></div>
        </div>
        <div class="title_text">{{ title_text[0] }}</div>
      </div>
      <div class="title_bottom">
        <div class="new">{{ str }}</div>
        <div class="title_bottom_text">
          {{ text[0] }}
        </div>
      </div>
      <div class="img">
        <img :src="img[1]" />
      </div>
      <div class="btn">{{ btntext[0] }}</div>
    </div>
    <div class="m"></div>
    <div class="two">
      <div class="title">
        <div class="mark">
          <div class="num">TWO</div>
          <div class="jiao"></div>
        </div>
        <div class="title_text">{{ title_text[1] }}</div>
      </div>
      <div class="title_bottom">
        <div class="text">{{ mtext }}</div>
        <div class="title_bottom_conten">
          <div class="new">{{ str }}</div>
          <div class="title_bottom_text">
            {{ text[1] }}
          </div>
        </div>
        <div class="title_bottom_conten">
          <div class="new">{{ str }}</div>
          <div class="title_bottom_text">
            {{ text[2] }}
          </div>
        </div>
        <div class="title_bottom_conten">
          <div class="new">{{ str }}</div>
          <div class="title_bottom_text">
            {{ text[3] }}
          </div>
        </div>
      </div>
      <div class="btn">{{ btntext[1] }}</div>
    </div>
    <div class="n"></div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      img: [require("../assets/top.png"), require("../assets/one.png")],
      str: "NEW",
      mtext: "学习生活中遇到烦心事?快来这里和小伙伴们一起吐槽",
      text: [
        "可以创建私密学习房，和好友学习不再被人打扰",
        "频道内有主题，方便你找到组织",
        "对讲人数无上限，一起吐槽一起high！",
        "频道内直接组学习局遇到合拍的人别放走！",
      ],
      title_text: ["连线学习", "树洞对讲机"],
      btntext: ["试试新的连线学习", "频道high聊中，快去看看>"],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import url("../css/base.css");
.hello {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  img {
    width: 50vh;
  }
  .one {
    width: 38.5vh;
    height: 41.3vh;
    border: 0.5vh solid #000;
    border-radius: 4vh;
    margin: 10vh 0 0;
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    .title_bottom {
      position: absolute;
      display: flex;
      margin: 4vh 0;
      top: -1vh;
      .title_bottom_text {
        font-size: 2vh;
        text-align: left;
      }
    }
    .img {
      margin: 11vh 0;
      img {
        width: 30vh;
      }
    }
  }
  .m {
    width: 16vh;
    height: 1vh;
    position: absolute;
    bottom: -2.7vh;
    background-color: #ffeec0;
  }
  .two {
    width: 38.5vh;
    height: 41.3vh;
    border: 0.5vh solid #000;
    border-radius: 4vh;
    margin: 10vh 0 5vh;
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    .title_bottom {
      position: absolute;
      display: flex;
      flex-direction: column;
      align-items: center;
      margin: 4vh 0;
      top: -1vh;
      .title_bottom_conten {
        display: flex;
        margin: 0.7vh 0;
        width: 38vh;
        .title_bottom_text {
          font-size: 2vh;
          text-align: left;
          width: 30vh;
        }
      }
    }
    .text {
      width: 29.2vh;
      margin: 1.5vh 0 3vh;
      font-size: 2vh;
      text-align: left;
    }
  }
  .n {
    width: 16vh;
    height: 1vh;
    position: absolute;
    bottom: -54.6vh;
    background-color: #ffeec0;
  }
}
</style>
