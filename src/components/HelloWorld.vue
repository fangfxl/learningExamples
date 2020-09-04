<template>
    <div id="index">
      <ul>
        <li v-for="(item, index) of imgArr" :key="index"> <img :src="item" alt="图片描述"></li>
      </ul>
      <div class="upload">
        <input type="file" >
      </div>
    </div>
</template>

<script>
import Viewer from 'viewerjs';
import 'viewerjs/dist/viewer.css';
export default {
  name: 'HelloWorld',
  data () {
    return {
     imgArr:[
       'https://ss1.bdstatic.com/70cFuXSh_Q1YnxGkpoWK1HF6hhy/it/u=2785097329,1326408874&fm=26&gp=0.jpg',
       'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1599127857085&di=b1279ffff5ad94528206d1f418a03750&imgtype=0&src=http%3A%2F%2Fdpic.tiankong.com%2F2f%2Fhm%2FQJ6348448923.jpg%3Fx-oss-process%3Dstyle%2Fshow',
       'https://ss1.bdstatic.com/70cFuXSh_Q1YnxGkpoWK1HF6hhy/it/u=2785097329,1326408874&fm=26&gp=0.jpg'
     ],
    }
  },
  mounted() {
    const ViewerDom = document.getElementById('index');
    const viewer = new Viewer(ViewerDom, {
    // 'zIndex': 9999,
    // 'inline': true,
    // 'button': true,
    // 'navbar': true,
    // 'title': true, 
    // 'toolbar': true, 
    // 'tooltip': true, 
    // 'movable': true, 
    // 'zoomable': true, 
    // 'rotatable': true, 
    // 'scalable': true, 
    // 'transition': true, 
    // 'fullscreen': true, 
    // 'keyboard': true, 
    // 'url': 'data-source'
    })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
*{
padding:0;
margin: 0;
}
ul {
display: flex;
flex-wrap: wrap;
}
ul li{
width:265px;
height: 180px;
list-style: none;
border: 2px solid #CCC;
border-radius: 3px;
padding: 1px;
margin: 10px;
cursor: pointer;
}
ul li img{
width: 100%;
height: 100%;
}
</style>
