<template>
  <v-container>
    <v-layout text-center wrap>
      <v-flex xs12>
        <h1 class="contentsTitle" ml10>About</h1>
      </v-flex>
      <v-layout xs12 wrap justify-center>
        <v-flex xs12 md6>
          <v-img
            :src="require('../assets/myprofileImage.jpg')"
            class="my-3 myImage"
            contain
            height="300"
          ></v-img>
        </v-flex>
        <v-flex xs12 md6 wrap>
          <v-flex xs12>
            <h2 class="name text-md-left">Yuma Shimizu : 清水 悠真</h2>
          </v-flex>
          <v-flex xs12>
            <h2 class="name text-md-left">東京理科大学 在学中</h2>
          </v-flex>
          <v-flex flex xs10 offset-xs1 offset-md0>
            <p class="subtitle-1 text-md-left aboutDesc">
              都内で学生をやりながら、webエンジニアとかデザイナーとかやってます。
              フリーランスも過去にやっていました。最近では企業でアプリケーション開発を行ったり、python等のプログラミング言語を教えたりしています。matcherなどで就職活動のアドバイザーも稀に行っています。2018年の冬ごろに日本IBMからITスペシャリストとして内定をいただき、来年度(2020年4月)からお勤めさせていただきます。
            </p>
          </v-flex>
        </v-flex>
      </v-layout>

      <v-flex mb-5 xs12>
        <h1 class="contentsTitle">Vision</h1>

        <v-layout justify-center wrap>
          <v-flex xs12>
            <h2 class="subname">人の心を動かす"Design"を追求する</h2>
          </v-flex>
          <v-flex xs10 md6>
            <p
              class="subtitle-1"
            >これは私がWebフロントエンドの知識もない頃、IllustratorやPhotoshopなどのデザインツールのみで仕事をしていた頃から常に意識していたことです。人の心を動かして、初めてデザインに意味を持ち、そして価値が付く、私はそう考えます。</p>
          </v-flex>
        </v-layout>
      </v-flex>

      <v-flex xs12 mb-5>
        <h1 class="contentsTitle">Skill</h1>
        <v-layout class="skillUp" wrap>
          <v-flex xs12 md6>
            <h2 class="skillTitle">Design</h2>
            <v-img
              :src="require('../assets/v-design.png')"
              class="my-3 myImage"
              contain
              height="250"
              mb-5
            ></v-img>
            <p class="subtitle-1">
              Adobe Photoshop / Adobe Illustrator
              /
              <br />Adobe XD / Sketch
            </p>
          </v-flex>
          <v-flex xs12 md6>
            <h2 class="skillTitle">Web Design</h2>
            <v-img
              :src="require('../assets/v-webdesign.png')"
              class="my-3 myImage"
              contain
              height="250"
              mb-5
            ></v-img>
            <p class="subtitle-1">
              HTML / CSS / javascript/ Wordpress / JQuery /
              <br />react.js / vue.js / etc..
            </p>
          </v-flex>
        </v-layout>

        <v-layout wrap>
          <v-flex xs12 md6>
            <h2 class="skillTitle">App Develop</h2>
            <v-img
              :src="require('../assets/v-apps.png')"
              class="my-3 myImage"
              contain
              height="250"
              mb-5
            ></v-img>
            <p class="subtitle-1">Vue.js / react.js / JavaSpringBoot / Git</p>
          </v-flex>
          <v-flex xs12 md6 justify-center>
            <h2 class="skillTitle">Education</h2>
            <v-img
              :src="require('../assets/v-education.png')"
              class="my-3 myImage"
              contain
              height="250"
              mb-5
            ></v-img>
            <p class="subtitle-1">HTML / CSS / javascript / python / Java</p>
          </v-flex>
        </v-layout>
      </v-flex>

      <v-flex xs12 md8 mb-5>
        <h1 class="contentsTitle">Works</h1>
        <v-flex offset-md5>
          <v-carousel cycle>
            <v-carousel-item
              v-for="(item,i) in items"
              :key="i"
              :src="item.src"
              reverse-transition="fade-transition"
              transition="fade-transition"
            ></v-carousel-item>
          </v-carousel>
        </v-flex>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          src: "img/slideImg1.jpg"
        },
        {
          src: "img/slideImg2.jpg"
        },
        {
          src: "img/slideImg3.jpg"
        },
        {
          src: "img/slideImg4.jpg"
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
h1,
h2,
h3,
h4,
p,
a {
  color: #41b883;
}
.skillTitle {
  font-size: 3rem;
  font-family: Copperplate, "Copperplate Gothic Light", fantasy;
}
.contentsTitle {
  font-size: 5rem;
  margin-left: 4rem;
  margin-bottom: 15rem;
  margin-top: 15rem;
  font-family: Copperplate, "Copperplate Gothic Light", fantasy;
  border-bottom: 1px solid #41b883;
  width: 25% !important;
  line-height: 60px;
}
.name {
  font-family: Quicksand, 游ゴシック体, "Yu Gothic", YuGothic,
    "ヒラギノ角ゴシック Pro", "Hiragino Kaku Gothic Pro", メイリオ, Meiryo,
    Osaka, "ＭＳ Ｐゴシック", "MS PGothic", sans-serif;
}
.name::first-letter {
  font-size: 3rem;
}
.subname {
  font-size: 3rem;
  font-family: Quicksand, 游ゴシック体, "Yu Gothic", YuGothic,
    "ヒラギノ角ゴシック Pro", "Hiragino Kaku Gothic Pro", メイリオ, Meiryo,
    Osaka, "ＭＳ Ｐゴシック", "MS PGothic", sans-serif;
}
.subname::first-letter {
  font-size: 5rem;
}
.aboutDesc {
  margin: 0 auto !important;
}

@media (min-width: 960px) {
  .skillUp {
    margin-bottom: 8rem;
  }
  .aboutDesc {
    margin: !important;
  }
}
</style>