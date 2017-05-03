# androidnote

4.0后，新建android工程，会自动生成drawable,drawalbe-ldpi,drawable-mdpi,drawable-hdpi,drawable-xhdpi,drawable-xxhdpi六个文件夹，
除drawable外，其他5个文件夹对应四种级别的density：120dip（low），160dip（medium）,240dip（high），320dip（xhigh），480dip（drawable-xxhdpi）。
目前主流做法都是把图片文件放在drawable-hdpi文件夹内，和图片相关的xml文件(如按钮xml，用以在按钮点击时显示不同的背景图片效果)放在drawable文件夹内。


比如在一个低分辨率的手机上，Android就会选择ldpi文件夹下的图片，但是如果没有在ldpi的文件夹下找见相关的资源文件，Android系统会首先从hdpi文件夹中选择文件，
然后对图片资源进行缩放处理，显示在屏幕上；如果hdpi文件夹下也没有的话，会在默认的drawable文件夹中寻找。



就目前来说，mipmap文件夹只是用来放启动图标的，AndroidStudio新建项目的ic_launcher.png都是默认放在mipmap文件夹下的。



ldpi：240x320
mdpi：320x480
hdpi：480x800、480x854
xhdpi：至少960*720
xxhdpi：1280×720