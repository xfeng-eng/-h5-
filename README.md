由HTML+CSS简单实现，使用简单，直接将图片放入指定路径，修改图片名称后打开html文件即可。

**效果在线查看**：云服务器已过期，在线地址失效，可在文件夹【各效果简单截图】中查看简单截图效果

**公网访问**：若想实现公网访问，将前端文件移动公网服务器，搭配nginx即可实现

**食用教程**：（每个文件夹内有具体教程，此为正方体旋转效果教程，其它效果大差不差，注意图片数量及命名即可）

1. 使用电脑解压文件到任意目录后，打开解压后的文件，挑选11张照片放入images文件夹

2. 修改照片名称
   注意必须打开显示文件扩展名，百度教程：https://jingyan.baidu.com/article/d7130635d3e45f52fdf475bf.html
   背景照片重命名为：background.jpg

   小正方体6张照片分别命名为：
   01.jpg
   02.jpg
   03.jpg
   04.jpg
   05.jpg
   06.jpg
   大正方体6张照片分别命名为：
   1.jpg
   2.jpg
   3.jpg
   4.jpg
   5.jpg
   6.jpg

3. 直接双击index.html文件就可以看到效果，如果部分照片效果不佳可以去网页版美图秀秀修改照片尺寸
   注意：

   > [!CAUTION]
   >
   > 1. 图片尺寸需要修改 （解决展示不全的情况）
   >    首先01-06编号命名的图片尺寸是100x100px的大小的，1-6编号是400x400px，如果效果想展示最佳，100x100px的图片是以头部特写的照片最好，因为01-06是立体照片内部小正方体的照片，1-6编号是外部正方体的照片。
   > 2. 图片的方向需要修改（解决头朝下的问题）
   >    部分照片会出现头是倒着的情况，将它旋转180度。

4. BGM添加或删除

   如果需要BGM请右键单击index.html文件->打开方式->选择记事本打开
   然后在</body>和</html>之间复制粘贴下面代码，并打开music文件夹，放入下载的音乐文件命名为music.mp3

   ```html
   <audio id="vd" autoplay="autoplay" controls="controls"   loop="loop" preload="auto"
   
               src="music/music.mp3">
   
           你的浏览器版本太低，不支持audio标签
   
   </audio>
   
   <script type="text/javascript">
       window.onload = function(){
                setInterval("toggleSound()",100);
           }
   
       function toggleSound() {
                   var music = document.getElementById("vd");//获取ID  
                       
                   if (music.paused) { //判读是否播放  
                       music.paused=false;
                       music.play(); //没有就播放 
                   }    
           }
   </script>
   ```

   

5.修改网页标题，右键单击index.html文件->打开方式->选择记事本打开,找到<title>这里的文字可修改</title> ，将中间的文字修改并保存即可
