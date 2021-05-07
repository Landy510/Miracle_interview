<template>
  <div id="app">
    <Navbar class="sticky-top" />
    <main class="flex-grow-1">
      <div class="container-fluid">
        <div class="row">
          <div class="col-sm-6 col-md-4 col-lg-3 mb-4" v-for="(item, index) in vedio" :key="index">
            <a class="card border-0 h-100" style=" text-decoration: none;">
              <!--<img :src="item.imageUrl" class="card-img-top" alt="...">-->
              <div :style="{ backgroundImage: 'url(' + item.imageUrl + ')' }" class="card-img-top card-img bg-cover"></div>
              <div class="card-body d-flex p-0 py-1">
                <div>
                  <div class="user-icon d-flex justify-content-center align-items-center" :style="{'background-color': item.bgColor}"> S </div>
                </div>
                <p class="card-text text-dark">{{ item.describe }}</p>
              </div>
            </a>
          </div>
        </div>
      </div>
    </main>
    <Footer class="footer" />
  </div>
</template>

<script>
import Navbar from './components/Navbar'
import Footer from './components/Footer'
export default {
  name: 'App',
  data () {
    return {
      vedio: [
        {
          imageUrl: 'https://i.postimg.cc/kM6ZnZSb/1.jpg',
          describe: '名嘴黃暐瀚媽媽出門遭撞 肇事者才酒駕剛交保? 台灣酒駕法是否要修改?｜竟有酸民出征留言讓人直搖頭',
          bgColor: 'red'
        },
        {
          imageUrl: 'https://i.postimg.cc/Bb9CZhWT/2.jpg',
          describe: 'Smile ~ Lofi hip hop mix ~ focus music',
          bgColor: 'purple'
        },
        {
          imageUrl: 'https://i.postimg.cc/63dvctSZ/3.jpg',
          describe: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Culpa officiis corrupti voluptate earum iure.',
          bgColor: 'green'
        },
        {
          imageUrl: 'https://i.postimg.cc/90CqNs5n/4.jpg',
          describe: '5:30 PM LOOK AT THE CITY ~Lofi hip hop mix~ beats to relax/study to ~ focus music',
          bgColor: 'red'
        },
        {
          imageUrl: 'https://i.postimg.cc/Sx3Ypnb8/5.jpg',
          describe: 'Kris Wu 吴亦凡 - 破晓 ( Dawn) MV',
          bgColor: 'yellow'
        },
        {
          imageUrl: 'https://i.postimg.cc/L59nVfjd/6.jpg',
          describe: 'The sunset is beautiful ~ Lofi hip hop ~ [ Jazzhop / chil beats / relax/study ] ~ focus music',
          bgColor: 'red'
        },
        {
          imageUrl: 'https://i.postimg.cc/28358Cwx/7.jpg',
          describe: 'Daily routine ~Lofi hip hop mix~ beats to relax/study to ~ focus music',
          bgColor: 'green'
        },
        {
          imageUrl: 'https://i.postimg.cc/sxMRygrQ/8.jpg',
          describe: 'Japanese City Pop Mixtape Vol.18 - BAYSIDE CITY',
          bgColor: 'red'
        },
        {
          imageUrl: 'https://i.postimg.cc/xTbS485B/9.jpg',
          describe: '【2020】抖音上最火的15首BGM神曲',
          bgColor: 'black'
        }
      ]
    }
  },
  components: {
    Navbar,
    Footer
  }
}
</script>

<style lang="scss">
@import "./assets/all";
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  height: 100vh;
  display: flex;
  flex-direction: column;
}
.footer {
  position: sticky;
  bottom: 0;
}
.card:hover {
  cursor: pointer;
  box-shadow: 7px 5px rgba(0, 0, 0, 0.5);
  transition: all .5s;
}
.user-icon {
 height:40px;
 width:40px;
 background-color: purple;
 border-radius: 50%;
 margin-right: 5px;
 color: white;
}
.card-text {
  font-weight: 600;
}
.card-img {
  height: 200px;
}
</style>
