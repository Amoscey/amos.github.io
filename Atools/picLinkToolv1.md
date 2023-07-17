#### 不行
[picLinkToolv1.md](https://amosc.top/#!Atools/picLinkToolv1.md)
#### 可以用的

- [网页-html-](https://amosc.top/Atools/picLinkTool1.html)
    - https://amosc.top/Atools/picLinkTool1.html


#### 预览界面(无法运行)
<!DOCTYPE html>
<html>
<head>
  <title>图床链接输出</title>
  <script>
    function generateOutput() {
      var links = document.getElementById("links").value.split("\n");
      var labels = document.getElementById("labels").value.split("\n");
      var output = "";
      
      for (var i = 0; i < links.length; i++) {
        var link = links[i].trim();
        if (link !== "") {
          output += "![](" + link + ")";
          
          if (labels.length > i && labels[i].trim() !== "") {
            output += " - " + labels[i].trim();
          }
          
          output += "\n";
        }
      }
      
      document.getElementById("output").textContent = output;
    }
  </script>
</head>
<body>
  <h5>图床链接生成</h5>
  <p>请输入图床链接：</p>
  <textarea id="links" rows="5" cols="50" placeholder="链接1&#10;链接2&#10;链接3&#10;..."></textarea>
  
  <p>请输入链接对应的标签：</p>
  <textarea id="labels" rows="5" cols="50" placeholder="链接1对应标签&#10;链接2对应标签&#10;链接3对应标签&#10;..."></textarea>
  
  <button onclick="generateOutput()">生成输出</button>
  
  <h5>输出结果：</h5>
  <pre id="output"></pre>
</body>

</html>