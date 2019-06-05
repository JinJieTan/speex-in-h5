# 本开源项目主要解决了即时通讯中的speex音频格式文件直接在H5中播放的问题

* 本项目必须运行在服务器环境下 不能是本地打开index.html文件方式使用（因为用到了websocket通讯）

* 直接让Speex格式的音频文件在H5页面中通过 audio标签播放

* 对于频率小于22khz的数据，我们需要复制一份，模拟成22khz，因为H5只支持大于22khz的数据，但是这种情况我们一般不会遇到

* 使用<script>标签引入源码

* 如果你的使用方式是直接在页面中 <audio src="./test.ogg">，那么请你在引入源码，立即在全局JS代码顶部调用函数  initAudio()  

* 如果你的使用方式是动态添加audio标签，或者动态修改audio标签的src属性，那么请你每次修改src属性后调用函数initAudio()，否则是不可以播放speex格式的音频文件的

* speex格式音频文件，后缀可能是ogg的，但是任然可以播放（speex只是一个开源免费压缩协议）

* 本项目不支持任何模块化  禁止在框架中通过 import或者require导入 ，因为源码中涉及8进制的代码，严格模式下是不可以使用八进制的

* MVVM框架和原生的JS使用方法都是通过script引入，全局调用initAudio函数

* 只能通过script引入，谢谢！ 
* This open source project addresses the issue of speex audio files being played directly into H5 in instant messaging
* this project must be run in the server environment and cannot be used locally to open the index.html file (because websocket communication is used).
* direct Speex audio files to the audio tag on the H5 page
* for data with frequency less than 22khz, we need to copy it and simulate it as 22khz, because H5 only supports data larger than 22khz, but we don't usually encounter this kind of situation
* use <script> tag to introduce source code
* if you use <audio SRC ="./test.ogg"> directly in the page, then call initAudio() immediately at the top of the global JS code when you bring in the source code
* if you are dynamically adding audio tags or dynamically changing the SRC property of audio tags, call initAudio() every time you change the SRC property. Otherwise, speex audio files cannot be played
* speex format audio files, suffix may be ogg, but can still be played (speex is only an open source free compression agreement)
* this project does not support any modularity that prohibits imports or require imports in the framework, because the source code involves octal code that cannot be octal in strict mode
* both MVVM framework and native JS use methods are introduced through script, and initAudio function is called globally
* can only be introduced through script, thanks!
