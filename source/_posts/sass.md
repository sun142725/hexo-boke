---
title: sass
date: 2018-01-12 16:56:37
tags: css
author: 孙继红
---
## Sass简介
Sass 是一种css预处理器,CSS 预处理器定义了一种新的语言，其基本思想是，用一种专门的编程语言，为 CSS 增加了一些编程的特性，将 CSS 作为目标生成文件，然后开发者就只要使用这种语言进行编码工作。

除了sass还有一些其他常见的预处理语言

* LESS
* Stylus
Sass 有时候也被称为 SCSS,两者之间不同之处有以下两点：

文件扩展名不同，Sass 是以“.sass”后缀为扩展名，而 SCSS 是以“.scss”后缀为扩展名
语法书写方式不同，Sass 是以严格的缩进式语法规则来书写，不带大括号({})和分号(;)，而 SCSS 的语法书写和我们的 CSS 语法书写方式非常类似。
来看一个示例：

/* Sass 语法 */
$font-stack: Helvetica, sans-serif
$primary-color: #333
body
  font: 100% $font-stack
  color: $primary-color
/* Scss 语法 */
$font-stack: Helvetica, sans-serif;
$primary-color: #333;
body {
  font: 100% $font-stack;
  color: $primary-color;
}
编译出来的 CSS

body {
  font: 100% Helvetica, sans-serif;
  color: #333;
}
scss文件中可以完全像写正常的css那样去写.

2. sass安装
npm install -g node-sass
node-sass -w xxx.scss xxx.css --output-style expanded
node-sass 参数:

-w, --watch                Watch a directory or file
-r, --recursive            Recursively watch directories or files
-o, --output               Output directory
-x, --omit-source-map-url  Omit source map URL comment from output
-i, --indented-syntax      Treat data from stdin as sass code (versus scss)
-q, --quiet                Suppress log output except on error
-v, --version              Prints version info
--output-style             CSS output style (nested | expanded | compact | compressed)
--indent-type              Indent type for output CSS (space | tab)
--indent-width             Indent width; number of spaces or tabs (maximum value: 10)
--linefeed                 Linefeed style (cr | crlf | lf | lfcr)
--source-comments          Include debug info in output
--source-map               Emit source map
--source-map-contents      Embed include contents in map
--source-map-embed         Embed sourceMappingUrl as data URI
--source-map-root          Base path, will be emitted in source-map as is
--include-path             Path to look for imported files
--follow                   Follow symlinked directories
--precision                The amount of precision allowed in decimal numbers
--importer                 Path to .js file containing custom importer
--functions                Path to .js file containing custom functions
--help                     Print usage info
3. Sass的基本特性
变量
$brand-primary : darken(#428bca, 6.5%) !default;
$btn-primary-color : #fff !default;
$btn-primary-bg : $brand-primary !default;
$btn-primary-border : darken($btn-primary-bg, 5%) !default;
.btn-primary {
   background-color: $btn-primary-bg;
   color: $btn-primary-color;
   border: 1px solid $btn-primary-border;
}
$baseLineHeight: 2;
$baseLineHeight: 1.5 !default;
body{
    line-height: $baseLineHeight;
}
/* 局部变量 */
$color: orange !default;
.block {
  color: $color;
}
em {
  $color: red;
  a {
    color: $color;
  }
}
span {
  color: $color;
}
嵌套
nav {
  a {
    color: red;
    header & {
      color:green;
    }
  }
}

.box {
  border: {
   top: 1px solid red;
   bottom: 1px solid green;
  }
}

.clearfix{
  &:before,
  &:after {
    content:"";
    display: table;
  }
  &:after {
    clear:both;
    overflow: hidden;
  }
}
不要无节制嵌套,一切都根据实际情况判断

混合宏

@mixin border-radius{
  -webkit-border-radius: 5px;
  border-radius: 5px;
}
button{
  @include border-radius;
}
@mixin border-radius($radius:5px){
  -webkit-border-radius: $radius;
  border-radius: $radius;
}
.nav{
  @include border-radius;
}
.box{
  @include border-radius(3px);
}
@mixin center($width,$height){
  width: $width;
  height: $height;
  position: absolute;
  top: 50%;
  left: 50%;
  margin-top: -($height) / 2;
  margin-left: -($width) / 2;
}
.box-center {
  @include center(500px,300px);
}
@mixin box-shadow($shadows...){
  @if length($shadows) >= 1 {
    -webkit-box-shadow: $shadows;
    box-shadow: $shadows;
  } @else {
    $shadows: 0 0 2px rgba(#000,.25);
    -webkit-box-shadow: $shadow;
    box-shadow: $shadow;
  }
}
.box {
  @include box-shadow(0 0 1px rgba(#000,.5),0 0 2px rgba(#000,.2));
}
混合宏会生成冗余代码

扩展/继承
.btn {
  border: 1px solid #ccc;
  padding: 6px 10px;
  font-size: 14px;
}

.btn-primary {
  background-color: #f36;
  color: #fff;
  @extend .btn;
}

.btn-second {
  background-color: orange;
  color: #fff;
  @extend .btn;
}
不会生成冗余代码

占位符
%mt5 {
  margin-top: 5px;
}
%pt5{
  padding-top: 5px;
}
.btn {
  @extend %mt5;
  @extend %pt5;
}
mt5 和 pt5 并不会生成最终代码

插值#{}
允许在#{}内部解析变量

$properties: (margin, padding);
@mixin set-value($side, $value) {
  @each $prop in $properties {
    #{$prop}-#{$side}: $value;
  }
}
.login-box {
  @include set-value(top, 14px);
}
注释
类似 CSS 的注释方式，使用 ”/* ”开头，结属使用 ”*/ ”
类似 JavaScript 的注释方式，使用“//”
两者区别，前者会在编译出来的 CSS 显示，后者在编译出来的 CSS 中不会显示

数据类型
Sass 和 JavaScript 语言类似，也具有自己的数据类型，在 Sass 中包含以下几种数据类型：

数字: 如，1、 2、 13、 10px；
字符串：有引号字符串或无引号字符串，如，”foo” ‘bar’ baz；
颜色：如，blue, #04a3f9, rgba(255,0,0,0.5);
布尔型：如，true, false；
空值：如，null；
值列表：用空格或者逗号分开，如，1.5em 1em 0 2em , Helvetica, Arial, sans-serif
运算
.box {
  width: 20px + 8in;
}
$full-width: 960px;
$sidebar-width: 200px;
.content {
  width: $full-width -  $sidebar-width;
}
.box {
  width: 10px * 2;
}
.box {
  width: (100px / 2);
}
p {
  font: 10px/8px;             // 纯 CSS，不是除法运算
  $width: 1000px;
  width: $width/2;            // 使用了变量，是除法运算
  width: round(1.5)/2;        // 使用了函数，是除法运算
  height: (500px/2);          // 使用了圆括号，是除法运算
  margin-left: 5px + 8px/2px; // 使用了加（+）号，是除法运算
}
.box {
  width: ((220px + 720px) - 11 * 20 ) / 12 ;
}
p {
  color: #010203 + #040506;
  background-color: #010203 * 2;
}

$content: "Hello" + "" + "Sass!";
.box:before {
  content: " #{$content} ";
}
4. Sass高级特性
@if
@mixin blockOrHidden($boolean:true) {
  @if $boolean {
    display: block;
  }
  @else {
    display: none;
  }
}
.block {
  @include blockOrHidden;
}
.hidden{
  @include blockOrHidden(false);
}
@for
@for $i from <start> through <end>
@for $i from <start> to <end>
@for $i from 1 through 3 {
  .item-#{$i} { width: 2em * $i; }
}
@for $i from 1 to 3 {
  .item-#{$i} { width: 2em * $i; }
}
$grid-prefix: span !default;
$grid-width: 60px !default;
$grid-gutter: 20px !default;

%grid {
  float: left;
  margin-left: $grid-gutter / 2;
  margin-right: $grid-gutter / 2;
}
@for $i from 1 through 12 {
  .#{$grid-prefix}#{$i}{
    width: $grid-width * $i + $grid-gutter * ($i - 1);
    @extend %grid;
  }
}
@each
$list: adam john wynn mason kuroir; //$list 就是一个列表
@mixin author-images {
    @each $author in $list {
        .photo-#{$author} {
            background: url("/images/avatars/#{$author}.png") no-repeat;
        }
    }
}
.author-bio {
    @include author-images;
}
5. Sass中的函数
@function double($n) {
  @return $n * 2;
}
#sidebar {
  width: double(5px);
}
全部的内置函数

字符串函数
unquote
quote
To-upper-case
To-lower-case
percentage
.footer{
  width : percentage(.2)
}
round
ceil
floor
abs
min
max
random
列表函数

length 取列表数据的长度
nth (10px 20px 30px, 1)
join join(10px 20px, 30px 40px)
append append(10px 20px ,30px)
zip zip(1px 2px 3px,solid dashed dotted,green blue red)
index index(1px solid red, solid)
type-of type-of(100)
unit 取单位
unitless 判断一个值是否带有单位
comparable 判断两个数是否可以进行加减合并
if(true,1px,2px)
Maps 函数
map-get
map-has-key
map-keys
map-values
map-merge
map-remove
keywords
$map: (
  $key1: value1,
  $key2: value2,
  $key3: value3
)

$map: (
  key1: value1,
  key2: (
    key-1: value-1,
    key-2: value-2,
  ),
key3: value3
);

$theme-color: (
  default: (
      bgcolor: #fff,
      text-color: #444,
      link-color: #39f
  ),
  primary:(
      bgcolor: #000,
      text-color:#fff,
      link-color: #93f
  ),
  negative: (
      bgcolor: #f36,
      text-color: #fefefe,
      link-color: #d4e
  )
);

/* map-get */
$social-colors: (
  dribble: #ea4c89,
  facebook: #3b5998,
  github: #171515,
  google: #db4437,
  twitter: #55acee
);
.btn-dribble{
  color: map-get($social-colors,facebook);
}
/* 没有值不会报错 */
.btn-weibo{
  font-size: 12px;
  color: map-get($social-colors,weibo);
}

/* map中的容错函数 */
@function colors($color){
  @if not map-has-key($social-colors,$color){
      @warn "No color found for `#{$color}` in $social-colors map. Property omitted.";
  }
  @return map-get($social-colors,$color);
}
.btn-dribble {
  color: colors(dribble);
}
/* each 遍历 map */
@each $name in map-keys($social-colors){
  .btn-#{$name}{
      color: colors($name);
  }
}
@for $i from 1 through length(map-keys($social-colors)){
  .btn-#{nth(map-keys($social-colors),$i)} {
    color: colors(nth(map-keys($social-colors),$i));
  }
}

map-values($social-colors)
/*得到所有的值*/
$color: (
  text: #f36,
  link: #f63,
  border: #ddd,
  backround: #fff
);
$typo:(
  font-size: 12px,
  line-height: 1.6
);
$newcolor = map-merge($color, $typo);
/* 得到新值 */
$map:map-remove($social-colors,dribble);
颜色函数
rgb
rgba
red
green
blue
mix 混合两种颜色 第三个参数为第一种颜色的比例 mix(blue,red,20%)

lighten lighten(red, 20%);
darken darken(red,30%);

saturate 改变颜色的饱和度 参数单位为百分比 saturate(blue,20%)
desaturate

adjust-hue 通过调整色相 adjust-hue(blue,30deg)

grayscale 直接让饱和度为0 grayscale(blue);
alpha 获取透明度
opacity 获取透明度
rgba
opacify 增加透明度
fade-in 增加透明度
transparentize 减少透明度
fade-out 减少透明度
<ul class="swatches red">
  <li></li>
  ...
  <li></li>
</ul>
<ul class="swatches orange">
  <li></li>
  …
  <li></li>
</ul>
<ul class="swatches yellow">
  <li></li>
  …
  <li></li>
</ul>
<ul class="swatches green">
  <li></li>
  …
  <li></li>
</ul>
<ul class="swatches blue">
  <li></li>
  …
  <li></li>
</ul>
<ul class="swatches purple">
  <li></li>
  …
  <li></li>
</ul>
$redBase: #DC143C;
$orangeBase: saturate(lighten(adjust_hue($redBase, 39), 5), 7);//#f37a16
$yellowBase: saturate(lighten(adjust_hue($redBase, 64), 6), 13);//#fbdc14
$greenBase: desaturate(darken(adjust_hue($redBase, 102), 2), 11);//#73c620
$blueBase: saturate(darken(adjust_hue($redBase, 201), 2), 1);//#12b7d4
$purpleBase: saturate(darken(adjust_hue($redBase, 296), 2), 1);//#a012d4
$blackBase: #777;
$bgc: #fff;

//定义颜色变暗的 mixin
@mixin swatchesDarken($color) {
  @for $i from 1 through 10 {
    $x:$i+11;
    li:nth-child(#{$x}) {
      $n:$i*5;
      $bgc:darken($color,$n); //颜色变暗
      background-color: $bgc;
      &:hover:before { //hover状态显示颜色编号
        content: "#{$bgc}";
        color: lighten($bgc,40);
        font-family: verdana;
        font-size: 8px;
        padding: 2px;
      }
    }
  }
}
//定义颜色变亮的 mixin
@mixin swatchesLighten($color) {
  @for $i from 1 through 10 {
    $x:11-$i;
    li:nth-child(#{$x}) {
      $n:$i*5;
      $bgc:lighten($color,$n);
      background-color: $bgc;
      &:hover:before {
        content: "#{$bgc}";
        color: darken($bgc,40);
        font-family: verdana;
        font-size: 8px;
        padding: 2px;
      }
    }
  }
}

.swatches li {
  width: 4.7619047619%;
  float: left;
  height: 60px;
  list-style: none outside none;
}

ul.red {
  @include swatchesLighten($redBase);
  @include swatchesDarken($redBase);
  li:nth-child(11) {
    background-color: $redBase;
  }
}

ul.orange {
  @include swatchesLighten($orangeBase);
  @include swatchesDarken($orangeBase);
  li:nth-child(11) {
    background-color: $orangeBase;
  }
}

ul.yellow {
  @include swatchesLighten($yellowBase);
  @include swatchesDarken($yellowBase);
  li:nth-child(11) {
    background-color: $yellowBase;
  }
}

ul.green {
  @include swatchesLighten($greenBase);
  @include swatchesDarken($greenBase);
  li:nth-child(11) {
    background-color: $greenBase;
  }
}

ul.blue {
  @include swatchesLighten($blueBase);
  @include swatchesDarken($blueBase);
  li:nth-child(11) {
    background-color: $blueBase;
  }
}

ul.purple {
  @include swatchesLighten($purpleBase);
  @include swatchesDarken($purpleBase);
  li:nth-child(11) {
    background-color: $purpleBase;
  }
}

ul.black {
  @include swatchesLighten($blackBase);
  @include swatchesDarken($blackBase);
  li:nth-child(11) {
    background-color: $blackBase;
  }
}
6. Sass的@规则
@import

@media

.sidebar {
  width: 300px;
  @media screen and (orientation: landscape) {
    width: 500px;
  }
}
@media screen {
  .sidebar {
    @media (orientation: landscape) {
      width: 500px;
    }
  }
}

$media: screen;
$feature: -webkit-min-device-pixel-ratio;
$value: 1.5;

@media #{$media} and ($feature: $value) {
  .sidebar {
    width: 500px;
  }
}
@extend

@at-root

@debug

@warn

@error

@content

$small : 750px;
@mixin  onsmall {
  @media  only screen and (max-width: $small){
    @content;
  }
}

.navbar-content{
  max-width:980px;
  @include onsmall {
    min-width:320px;
  }
}
@mixin useRem($size){
  $device-list : 320px, 375px , 414px;
  html{
    @each $device in $device-list{
      @media screen and (min-width: $device){
        font-size: 100px * ($device/$size);
      }
    }
  }
}
@include useRem(750px);