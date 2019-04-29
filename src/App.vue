<template>
  <div id="app">


    <h2> {{msg}}</h2>
    <br>
    <a>
      {{obj.name}}
    </a>
    <br>
    <a>
      <span v-for="item in list">
        {{item}}
        <div v-text="msg">


        </div>
      </span>
    </a>

    <br>
    <ul>
      <li v-for="item in newsList">
        {{item.cate}}
        <ol>
          <li v-for="news in item.list">
            {{news.title}}
          </li>

        </ol>
      </li>

    </ul>

    <div v-bind:title="title">
绑定属性title

      <!--去除v-bind 绑定动态属性-->
      <br>
    </div>

    <div v-html="html">


    </div>
  </div>


<!--

<template>
  <section>
    <mu-tabs value="导航栏" class="tab">
      <mu-tab icon="adb" iconClass="iconClass" title="shsmart" titleClass="tab-title" value="shsmart" href="/index">
      </mu-tab>
      <mu-tab title="首页" value="homePage" href="/index">
      </mu-tab>
      <mu-tab title="技术博文" href="/">
      </mu-tab>
      <mu-tab title="资源链接" value="资源链接" href="/">
      </mu-tab>
      <mu-tab title="关于我" titleClass="aboutMe" value="about-me" href="/" :disabled="true">
      </mu-tab>
      <mu-tab title="留言板" href="/">
      </mu-tab>
    </mu-tabs>
    <mu-row :gutter="true" class="body">
      <mu-col width="20" tablet="20" desktop="20">
        &nbsp;
      </mu-col>
      <mu-col width="60" tablet="60" desktop="60">
        <mu-card>
          <mu-card-media title="This is me!">
            <img src="./static/img_default.JPG" height="200px" />
          </mu-card-media>
          <mu-card-title title="项目简介" titleClass="title" subTitle="作者" subTitleClass="subTile" class="main" />
          <mu-card-text>
            正文
          </mu-card-text>
        </mu-card>
      </mu-col>
      <mu-col width="20" tablet="20" desktop="20">
        &nbsp;
      </mu-col>
    </mu-row>
  </section>
</template>

-->

</template>

<script>
export default {
  name: 'app',
  data () {/*业务逻辑里面定义的数据*/
    return {
      msg: 'Welcome to Your Vue.js App',
      obj:{/*传入对象*/
        name:"richy's blog"
      },
      list:['hello','我是','richy'],
      newsList:[/*嵌套数组*/
        {
          "cate":"国内新闻",
          "list":[
            {'title':'中国歌剧'},
            {'title':'中国篮球'}
          ]
        },
        {
          "cate":"国际新闻",
          "list":[
            {'title':'国际歌剧'},
            {'title':'国际篮球'}
          ]
        }
      ],
      title:"绑定title",
      html:"绑定html"
    }
  }
}
</script>

<style lang="scss">
</style>
