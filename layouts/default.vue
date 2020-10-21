<template>
  <div>
    <Nuxt />
  </div>
</template>


<script>
// // 禁止右键
// document.oncontextmenu=new Function("event.returnValue=false;");
// document.onselectstart=new Function("event.returnValue=false;");

// // 禁止选中文本
// var omitformtags=["input", "textarea", "select"];
// omitformtagsomitformtags=omitformtags.join("|");
// function disableselect(e){
// if (omitformtags.indexOf(e.target.tagName.toLowerCase())==-1){
// return false;
// }
// }
// function reEnable(){
// return true;
// }
// if (typeof document.onselectstart!="undefined"){
// document.onselectstart=new Function ("return false");
// }else{
// document.onmousedown=disableselect;
// document.onmouseup=reEnable;
// }

</script>
<style>
html {
  font-family:
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}



.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>
