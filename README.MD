# 本开源项目主要解决了即时通讯中的speex音频格式文件直接在H5中播放的问题

### 直接让Speex格式的音频文件在H5页面中通过 audio标签播放

### 对于频率小于22khz的数据，我们需要复制一份，模拟成22khz，因为H5只支持大于22khz的数据，但是这种情况我们一般不会遇到

### 使用<script>标签引入源码

### 如果你想要在页面中通过写死的形式 静态播放 speex文件 引入后源码在全局顶部调用函数  initAudio()  

### 如果你的<audio>标签中  src属性是动态的，那么请你每次修改src属性前调用函数initAudio()，否则不可以播放speex格式的音频文件

### speex格式音频文件，后缀可能是ogg的，但是任然可以播放

### 本项目不支持任何模块化  禁止在框架中通过 import或者require导入  

### MVVM框架和原生的JS使用方法都是通过script引入，全局调用initAudio函数

### 只能通过script引入，谢谢！ 

# English 

# This open source project addresses the issue of speex audio files being played directly into H5 in instant messaging
### Direct Speex audio files to the audio tag on H5 pages
### For data with frequency less than 22khz, we need to copy it and simulate it as 22khz, because H5 only supports data larger than 22khz, but we will not encounter this kind of situation
### Use <script> tag to introduce source code
### If you want to play the speex file statically on the page by writing it out, call the function initAudio() at the top of the global table
### If the SRC attribute in your <audio> tag is dynamic, call the function initAudio() every time you change the SRC attribute, otherwise you cannot play speex audio files
### speex format audio file, suffix may be ogg, but still playable
### This project does not support any modularity that prohibits imports or require imports from the framework
### Both the MVVM framework and native JS use methods are introduced through script and call initAudio function globally
### Can only be introduced through script, thanks!



