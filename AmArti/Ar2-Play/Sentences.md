# 好玩的

## 毒鸡汤
- badsoup
- [点击重新加载刷新](/#!AmArti/Ar2-Play/Sentences.md#) （会失效，还是浏览器手动刷新吧，或者按快捷键F5）

<!-- Body -->
<p id="badsoup">有人一笑就很好看，你是一看就挺好笑。</p>

<!-- Footer -->

<script>
  var xhr = new XMLHttpRequest();
  xhr.open('get', 'https://www.7ed.net/soup/api');
  xhr.onreadystatechange = function () {
    if (xhr.readyState === 4) {
      var data = JSON.parse(xhr.responseText);
      var badsoup = document.getElementById('badsoup');
      badsoup.innerText = data.badsoup;
    }
  }
  xhr.send();
</script>

## …