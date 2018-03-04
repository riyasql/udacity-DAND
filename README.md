<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />
<title>Bike_Share_Analysis (Showcase)</title><script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>

<style type="text/css">
    /*!
*
* Twitter Bootstrap
*
*/
/*!
 * Bootstrap v3.3.7 (http://getbootstrap.com)
 * Copyright 2011-2016 Twitter, Inc.
 * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
 */
/*! normalize.css v3.0.3 | MIT License | github.com/necolas/normalize.css */
html {
  font-family: sans-serif;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}
body {
  margin: 0;
}
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
menu,
nav,
section,
summary {
  display: block;
}
audio,
canvas,
progress,
video {
  display: inline-block;
  vertical-align: baseline;
}
audio:not([controls]) {
  display: none;
  height: 0;
}
[hidden],
template {
  display: none;
}
a {
  background-color: transparent;
}
a:active,
a:hover {
  outline: 0;
}
abbr[title] {
  border-bottom: 1px dotted;
}
b,
strong {
  font-weight: bold;
}
dfn {
  font-style: italic;
}
h1 {
  font-size: 2em;
  margin: 0.67em 0;
}
mark {
  background: #ff0;
  color: #000;
}
small {
  font-size: 80%;
}
sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}
sup {
  top: -0.5em;
}
sub {
  bottom: -0.25em;
}
img {
  border: 0;
}
svg:not(:root) {
  overflow: hidden;
}
figure {
  margin: 1em 40px;
}
hr {
  box-sizing: content-box;
  height: 0;
}
pre {
  overflow: auto;
}
code,
kbd,
pre,
samp {
  font-family: monospace, monospace;
  font-size: 1em;
}
button,
input,
optgroup,
select,
textarea {
  color: inherit;
  font: inherit;
  margin: 0;
}
button {
  overflow: visible;
}
button,
select {
  text-transform: none;
}
button,
html input[type="button"],
input[type="reset"],
input[type="submit"] {
  -webkit-appearance: button;
  cursor: pointer;
}
button[disabled],
html input[disabled] {
  cursor: default;
}
button::-moz-focus-inner,
input::-moz-focus-inner {
  border: 0;
  padding: 0;
}
input {
  line-height: normal;
}
input[type="checkbox"],
input[type="radio"] {
  box-sizing: border-box;
  padding: 0;
}
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: textfield;
  box-sizing: content-box;
}
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}
fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: 0.35em 0.625em 0.75em;
}
legend {
  border: 0;
  padding: 0;
}
textarea {
  overflow: auto;
}
optgroup {
  font-weight: bold;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
td,
th {
  padding: 0;
}
/*! Source: https://github.com/h5bp/html5-boilerplate/blob/master/src/css/main.css */
@media print {
  *,
  *:before,
  *:after {
    background: transparent !important;
    color: #000 !important;
    box-shadow: none !important;
    text-shadow: none !important;
  }
  a,
  a:visited {
    text-decoration: underline;
  }
  a[href]:after {
    content: " (" attr(href) ")";
  }
  abbr[title]:after {
    content: " (" attr(title) ")";
  }
  a[href^="#"]:after,
  a[href^="javascript:"]:after {
    content: "";
  }
  pre,
  blockquote {
    border: 1px solid #999;
    page-break-inside: avoid;
  }
  thead {
    display: table-header-group;
  }
  tr,
  img {
    page-break-inside: avoid;
  }
  img {
    max-width: 100% !important;
  }
  p,
  h2,
  h3 {
    orphans: 3;
    widows: 3;
  }
  h2,
  h3 {
    page-break-after: avoid;
  }
  .navbar {
    display: none;
  }
  .btn > .caret,
  .dropup > .btn > .caret {
    border-top-color: #000 !important;
  }
  .label {
    border: 1px solid #000;
  }
  .table {
    border-collapse: collapse !important;
  }
  .table td,
  .table th {
    background-color: #fff !important;
  }
  .table-bordered th,
  .table-bordered td {
    border: 1px solid #ddd !important;
  }
}
@font-face {
  font-family: 'Glyphicons Halflings';
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot');
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot?#iefix') format('embedded-opentype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff2') format('woff2'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff') format('woff'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.ttf') format('truetype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.svg#glyphicons_halflingsregular') format('svg');
}
.glyphicon {
  position: relative;
  top: 1px;
  display: inline-block;
  font-family: 'Glyphicons Halflings';
  font-style: normal;
  font-weight: normal;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.glyphicon-asterisk:before {
  content: "\002a";
}
.glyphicon-plus:before {
  content: "\002b";
}
.glyphicon-euro:before,
.glyphicon-eur:before {
  content: "\20ac";
}
.glyphicon-minus:before {
  content: "\2212";
}
.glyphicon-cloud:before {
  content: "\2601";
}
.glyphicon-envelope:before {
  content: "\2709";
}
.glyphicon-pencil:before {
  content: "\270f";
}
.glyphicon-glass:before {
  content: "\e001";
}
.glyphicon-music:before {
  content: "\e002";
}
.glyphicon-search:before {
  content: "\e003";
}
.glyphicon-heart:before {
  content: "\e005";
}
.glyphicon-star:before {
  content: "\e006";
}
.glyphicon-star-empty:before {
  content: "\e007";
}
.glyphicon-user:before {
  content: "\e008";
}
.glyphicon-film:before {
  content: "\e009";
}
.glyphicon-th-large:before {
  content: "\e010";
}
.glyphicon-th:before {
  content: "\e011";
}
.glyphicon-th-list:before {
  content: "\e012";
}
.glyphicon-ok:before {
  content: "\e013";
}
.glyphicon-remove:before {
  content: "\e014";
}
.glyphicon-zoom-in:before {
  content: "\e015";
}
.glyphicon-zoom-out:before {
  content: "\e016";
}
.glyphicon-off:before {
  content: "\e017";
}
.glyphicon-signal:before {
  content: "\e018";
}
.glyphicon-cog:before {
  content: "\e019";
}
.glyphicon-trash:before {
  content: "\e020";
}
.glyphicon-home:before {
  content: "\e021";
}
.glyphicon-file:before {
  content: "\e022";
}
.glyphicon-time:before {
  content: "\e023";
}
.glyphicon-road:before {
  content: "\e024";
}
.glyphicon-download-alt:before {
  content: "\e025";
}
.glyphicon-download:before {
  content: "\e026";
}
.glyphicon-upload:before {
  content: "\e027";
}
.glyphicon-inbox:before {
  content: "\e028";
}
.glyphicon-play-circle:before {
  content: "\e029";
}
.glyphicon-repeat:before {
  content: "\e030";
}
.glyphicon-refresh:before {
  content: "\e031";
}
.glyphicon-list-alt:before {
  content: "\e032";
}
.glyphicon-lock:before {
  content: "\e033";
}
.glyphicon-flag:before {
  content: "\e034";
}
.glyphicon-headphones:before {
  content: "\e035";
}
.glyphicon-volume-off:before {
  content: "\e036";
}
.glyphicon-volume-down:before {
  content: "\e037";
}
.glyphicon-volume-up:before {
  content: "\e038";
}
.glyphicon-qrcode:before {
  content: "\e039";
}
.glyphicon-barcode:before {
  content: "\e040";
}
.glyphicon-tag:before {
  content: "\e041";
}
.glyphicon-tags:before {
  content: "\e042";
}
.glyphicon-book:before {
  content: "\e043";
}
.glyphicon-bookmark:before {
  content: "\e044";
}
.glyphicon-print:before {
  content: "\e045";
}
.glyphicon-camera:before {
  content: "\e046";
}
.glyphicon-font:before {
  content: "\e047";
}
.glyphicon-bold:before {
  content: "\e048";
}
.glyphicon-italic:before {
  content: "\e049";
}
.glyphicon-text-height:before {
  content: "\e050";
}
.glyphicon-text-width:before {
  content: "\e051";
}
.glyphicon-align-left:before {
  content: "\e052";
}
.glyphicon-align-center:before {
  content: "\e053";
}
.glyphicon-align-right:before {
  content: "\e054";
}
.glyphicon-align-justify:before {
  content: "\e055";
}
.glyphicon-list:before {
  content: "\e056";
}
.glyphicon-indent-left:before {
  content: "\e057";
}
.glyphicon-indent-right:before {
  content: "\e058";
}
.glyphicon-facetime-video:before {
  content: "\e059";
}
.glyphicon-picture:before {
  content: "\e060";
}
.glyphicon-map-marker:before {
  content: "\e062";
}
.glyphicon-adjust:before {
  content: "\e063";
}
.glyphicon-tint:before {
  content: "\e064";
}
.glyphicon-edit:before {
  content: "\e065";
}
.glyphicon-share:before {
  content: "\e066";
}
.glyphicon-check:before {
  content: "\e067";
}
.glyphicon-move:before {
  content: "\e068";
}
.glyphicon-step-backward:before {
  content: "\e069";
}
.glyphicon-fast-backward:before {
  content: "\e070";
}
.glyphicon-backward:before {
  content: "\e071";
}
.glyphicon-play:before {
  content: "\e072";
}
.glyphicon-pause:before {
  content: "\e073";
}
.glyphicon-stop:before {
  content: "\e074";
}
.glyphicon-forward:before {
  content: "\e075";
}
.glyphicon-fast-forward:before {
  content: "\e076";
}
.glyphicon-step-forward:before {
  content: "\e077";
}
.glyphicon-eject:before {
  content: "\e078";
}
.glyphicon-chevron-left:before {
  content: "\e079";
}
.glyphicon-chevron-right:before {
  content: "\e080";
}
.glyphicon-plus-sign:before {
  content: "\e081";
}
.glyphicon-minus-sign:before {
  content: "\e082";
}
.glyphicon-remove-sign:before {
  content: "\e083";
}
.glyphicon-ok-sign:before {
  content: "\e084";
}
.glyphicon-question-sign:before {
  content: "\e085";
}
.glyphicon-info-sign:before {
  content: "\e086";
}
.glyphicon-screenshot:before {
  content: "\e087";
}
.glyphicon-remove-circle:before {
  content: "\e088";
}
.glyphicon-ok-circle:before {
  content: "\e089";
}
.glyphicon-ban-circle:before {
  content: "\e090";
}
.glyphicon-arrow-left:before {
  content: "\e091";
}
.glyphicon-arrow-right:before {
  content: "\e092";
}
.glyphicon-arrow-up:before {
  content: "\e093";
}
.glyphicon-arrow-down:before {
  content: "\e094";
}
.glyphicon-share-alt:before {
  content: "\e095";
}
.glyphicon-resize-full:before {
  content: "\e096";
}
.glyphicon-resize-small:before {
  content: "\e097";
}
.glyphicon-exclamation-sign:before {
  content: "\e101";
}
.glyphicon-gift:before {
  content: "\e102";
}
.glyphicon-leaf:before {
  content: "\e103";
}
.glyphicon-fire:before {
  content: "\e104";
}
.glyphicon-eye-open:before {
  content: "\e105";
}
.glyphicon-eye-close:before {
  content: "\e106";
}
.glyphicon-warning-sign:before {
  content: "\e107";
}
.glyphicon-plane:before {
  content: "\e108";
}
.glyphicon-calendar:before {
  content: "\e109";
}
.glyphicon-random:before {
  content: "\e110";
}
.glyphicon-comment:before {
  content: "\e111";
}
.glyphicon-magnet:before {
  content: "\e112";
}
.glyphicon-chevron-up:before {
  content: "\e113";
}
.glyphicon-chevron-down:before {
  content: "\e114";
}
.glyphicon-retweet:before {
  content: "\e115";
}
.glyphicon-shopping-cart:before {
  content: "\e116";
}
.glyphicon-folder-close:before {
  content: "\e117";
}
.glyphicon-folder-open:before {
  content: "\e118";
}
.glyphicon-resize-vertical:before {
  content: "\e119";
}
.glyphicon-resize-horizontal:before {
  content: "\e120";
}
.glyphicon-hdd:before {
  content: "\e121";
}
.glyphicon-bullhorn:before {
  content: "\e122";
}
.glyphicon-bell:before {
  content: "\e123";
}
.glyphicon-certificate:before {
  content: "\e124";
}
.glyphicon-thumbs-up:before {
  content: "\e125";
}
.glyphicon-thumbs-down:before {
  content: "\e126";
}
.glyphicon-hand-right:before {
  content: "\e127";
}
.glyphicon-hand-left:before {
  content: "\e128";
}
.glyphicon-hand-up:before {
  content: "\e129";
}
.glyphicon-hand-down:before {
  content: "\e130";
}
.glyphicon-circle-arrow-right:before {
  content: "\e131";
}
.glyphicon-circle-arrow-left:before {
  content: "\e132";
}
.glyphicon-circle-arrow-up:before {
  content: "\e133";
}
.glyphicon-circle-arrow-down:before {
  content: "\e134";
}
.glyphicon-globe:before {
  content: "\e135";
}
.glyphicon-wrench:before {
  content: "\e136";
}
.glyphicon-tasks:before {
  content: "\e137";
}
.glyphicon-filter:before {
  content: "\e138";
}
.glyphicon-briefcase:before {
  content: "\e139";
}
.glyphicon-fullscreen:before {
  content: "\e140";
}
.glyphicon-dashboard:before {
  content: "\e141";
}
.glyphicon-paperclip:before {
  content: "\e142";
}
.glyphicon-heart-empty:before {
  content: "\e143";
}
.glyphicon-link:before {
  content: "\e144";
}
.glyphicon-phone:before {
  content: "\e145";
}
.glyphicon-pushpin:before {
  content: "\e146";
}
.glyphicon-usd:before {
  content: "\e148";
}
.glyphicon-gbp:before {
  content: "\e149";
}
.glyphicon-sort:before {
  content: "\e150";
}
.glyphicon-sort-by-alphabet:before {
  content: "\e151";
}
.glyphicon-sort-by-alphabet-alt:before {
  content: "\e152";
}
.glyphicon-sort-by-order:before {
  content: "\e153";
}
.glyphicon-sort-by-order-alt:before {
  content: "\e154";
}
.glyphicon-sort-by-attributes:before {
  content: "\e155";
}
.glyphicon-sort-by-attributes-alt:before {
  content: "\e156";
}
.glyphicon-unchecked:before {
  content: "\e157";
}
.glyphicon-expand:before {
  content: "\e158";
}
.glyphicon-collapse-down:before {
  content: "\e159";
}
.glyphicon-collapse-up:before {
  content: "\e160";
}
.glyphicon-log-in:before {
  content: "\e161";
}
.glyphicon-flash:before {
  content: "\e162";
}
.glyphicon-log-out:before {
  content: "\e163";
}
.glyphicon-new-window:before {
  content: "\e164";
}
.glyphicon-record:before {
  content: "\e165";
}
.glyphicon-save:before {
  content: "\e166";
}
.glyphicon-open:before {
  content: "\e167";
}
.glyphicon-saved:before {
  content: "\e168";
}
.glyphicon-import:before {
  content: "\e169";
}
.glyphicon-export:before {
  content: "\e170";
}
.glyphicon-send:before {
  content: "\e171";
}
.glyphicon-floppy-disk:before {
  content: "\e172";
}
.glyphicon-floppy-saved:before {
  content: "\e173";
}
.glyphicon-floppy-remove:before {
  content: "\e174";
}
.glyphicon-floppy-save:before {
  content: "\e175";
}
.glyphicon-floppy-open:before {
  content: "\e176";
}
.glyphicon-credit-card:before {
  content: "\e177";
}
.glyphicon-transfer:before {
  content: "\e178";
}
.glyphicon-cutlery:before {
  content: "\e179";
}
.glyphicon-header:before {
  content: "\e180";
}
.glyphicon-compressed:before {
  content: "\e181";
}
.glyphicon-earphone:before {
  content: "\e182";
}
.glyphicon-phone-alt:before {
  content: "\e183";
}
.glyphicon-tower:before {
  content: "\e184";
}
.glyphicon-stats:before {
  content: "\e185";
}
.glyphicon-sd-video:before {
  content: "\e186";
}
.glyphicon-hd-video:before {
  content: "\e187";
}
.glyphicon-subtitles:before {
  content: "\e188";
}
.glyphicon-sound-stereo:before {
  content: "\e189";
}
.glyphicon-sound-dolby:before {
  content: "\e190";
}
.glyphicon-sound-5-1:before {
  content: "\e191";
}
.glyphicon-sound-6-1:before {
  content: "\e192";
}
.glyphicon-sound-7-1:before {
  content: "\e193";
}
.glyphicon-copyright-mark:before {
  content: "\e194";
}
.glyphicon-registration-mark:before {
  content: "\e195";
}
.glyphicon-cloud-download:before {
  content: "\e197";
}
.glyphicon-cloud-upload:before {
  content: "\e198";
}
.glyphicon-tree-conifer:before {
  content: "\e199";
}
.glyphicon-tree-deciduous:before {
  content: "\e200";
}
.glyphicon-cd:before {
  content: "\e201";
}
.glyphicon-save-file:before {
  content: "\e202";
}
.glyphicon-open-file:before {
  content: "\e203";
}
.glyphicon-level-up:before {
  content: "\e204";
}
.glyphicon-copy:before {
  content: "\e205";
}
.glyphicon-paste:before {
  content: "\e206";
}
.glyphicon-alert:before {
  content: "\e209";
}
.glyphicon-equalizer:before {
  content: "\e210";
}
.glyphicon-king:before {
  content: "\e211";
}
.glyphicon-queen:before {
  content: "\e212";
}
.glyphicon-pawn:before {
  content: "\e213";
}
.glyphicon-bishop:before {
  content: "\e214";
}
.glyphicon-knight:before {
  content: "\e215";
}
.glyphicon-baby-formula:before {
  content: "\e216";
}
.glyphicon-tent:before {
  content: "\26fa";
}
.glyphicon-blackboard:before {
  content: "\e218";
}
.glyphicon-bed:before {
  content: "\e219";
}
.glyphicon-apple:before {
  content: "\f8ff";
}
.glyphicon-erase:before {
  content: "\e221";
}
.glyphicon-hourglass:before {
  content: "\231b";
}
.glyphicon-lamp:before {
  content: "\e223";
}
.glyphicon-duplicate:before {
  content: "\e224";
}
.glyphicon-piggy-bank:before {
  content: "\e225";
}
.glyphicon-scissors:before {
  content: "\e226";
}
.glyphicon-bitcoin:before {
  content: "\e227";
}
.glyphicon-btc:before {
  content: "\e227";
}
.glyphicon-xbt:before {
  content: "\e227";
}
.glyphicon-yen:before {
  content: "\00a5";
}
.glyphicon-jpy:before {
  content: "\00a5";
}
.glyphicon-ruble:before {
  content: "\20bd";
}
.glyphicon-rub:before {
  content: "\20bd";
}
.glyphicon-scale:before {
  content: "\e230";
}
.glyphicon-ice-lolly:before {
  content: "\e231";
}
.glyphicon-ice-lolly-tasted:before {
  content: "\e232";
}
.glyphicon-education:before {
  content: "\e233";
}
.glyphicon-option-horizontal:before {
  content: "\e234";
}
.glyphicon-option-vertical:before {
  content: "\e235";
}
.glyphicon-menu-hamburger:before {
  content: "\e236";
}
.glyphicon-modal-window:before {
  content: "\e237";
}
.glyphicon-oil:before {
  content: "\e238";
}
.glyphicon-grain:before {
  content: "\e239";
}
.glyphicon-sunglasses:before {
  content: "\e240";
}
.glyphicon-text-size:before {
  content: "\e241";
}
.glyphicon-text-color:before {
  content: "\e242";
}
.glyphicon-text-background:before {
  content: "\e243";
}
.glyphicon-object-align-top:before {
  content: "\e244";
}
.glyphicon-object-align-bottom:before {
  content: "\e245";
}
.glyphicon-object-align-horizontal:before {
  content: "\e246";
}
.glyphicon-object-align-left:before {
  content: "\e247";
}
.glyphicon-object-align-vertical:before {
  content: "\e248";
}
.glyphicon-object-align-right:before {
  content: "\e249";
}
.glyphicon-triangle-right:before {
  content: "\e250";
}
.glyphicon-triangle-left:before {
  content: "\e251";
}
.glyphicon-triangle-bottom:before {
  content: "\e252";
}
.glyphicon-triangle-top:before {
  content: "\e253";
}
.glyphicon-console:before {
  content: "\e254";
}
.glyphicon-superscript:before {
  content: "\e255";
}
.glyphicon-subscript:before {
  content: "\e256";
}
.glyphicon-menu-left:before {
  content: "\e257";
}
.glyphicon-menu-right:before {
  content: "\e258";
}
.glyphicon-menu-down:before {
  content: "\e259";
}
.glyphicon-menu-up:before {
  content: "\e260";
}
* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
*:before,
*:after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
html {
  font-size: 10px;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  line-height: 1.42857143;
  color: #000;
  background-color: #fff;
}
input,
button,
select,
textarea {
  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
}
a {
  color: #337ab7;
  text-decoration: none;
}
a:hover,
a:focus {
  color: #23527c;
  text-decoration: underline;
}
a:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
figure {
  margin: 0;
}
img {
  vertical-align: middle;
}
.img-responsive,
.thumbnail > img,
.thumbnail a > img,
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  display: block;
  max-width: 100%;
  height: auto;
}
.img-rounded {
  border-radius: 3px;
}
.img-thumbnail {
  padding: 4px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  display: inline-block;
  max-width: 100%;
  height: auto;
}
.img-circle {
  border-radius: 50%;
}
hr {
  margin-top: 18px;
  margin-bottom: 18px;
  border: 0;
  border-top: 1px solid #eeeeee;
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
[role="button"] {
  cursor: pointer;
}
h1,
h2,
h3,
h4,
h5,
h6,
.h1,
.h2,
.h3,
.h4,
.h5,
.h6 {
  font-family: inherit;
  font-weight: 500;
  line-height: 1.1;
  color: inherit;
}
h1 small,
h2 small,
h3 small,
h4 small,
h5 small,
h6 small,
.h1 small,
.h2 small,
.h3 small,
.h4 small,
.h5 small,
.h6 small,
h1 .small,
h2 .small,
h3 .small,
h4 .small,
h5 .small,
h6 .small,
.h1 .small,
.h2 .small,
.h3 .small,
.h4 .small,
.h5 .small,
.h6 .small {
  font-weight: normal;
  line-height: 1;
  color: #777777;
}
h1,
.h1,
h2,
.h2,
h3,
.h3 {
  margin-top: 18px;
  margin-bottom: 9px;
}
h1 small,
.h1 small,
h2 small,
.h2 small,
h3 small,
.h3 small,
h1 .small,
.h1 .small,
h2 .small,
.h2 .small,
h3 .small,
.h3 .small {
  font-size: 65%;
}
h4,
.h4,
h5,
.h5,
h6,
.h6 {
  margin-top: 9px;
  margin-bottom: 9px;
}
h4 small,
.h4 small,
h5 small,
.h5 small,
h6 small,
.h6 small,
h4 .small,
.h4 .small,
h5 .small,
.h5 .small,
h6 .small,
.h6 .small {
  font-size: 75%;
}
h1,
.h1 {
  font-size: 33px;
}
h2,
.h2 {
  font-size: 27px;
}
h3,
.h3 {
  font-size: 23px;
}
h4,
.h4 {
  font-size: 17px;
}
h5,
.h5 {
  font-size: 13px;
}
h6,
.h6 {
  font-size: 12px;
}
p {
  margin: 0 0 9px;
}
.lead {
  margin-bottom: 18px;
  font-size: 14px;
  font-weight: 300;
  line-height: 1.4;
}
@media (min-width: 768px) {
  .lead {
    font-size: 19.5px;
  }
}
small,
.small {
  font-size: 92%;
}
mark,
.mark {
  background-color: #fcf8e3;
  padding: .2em;
}
.text-left {
  text-align: left;
}
.text-right {
  text-align: right;
}
.text-center {
  text-align: center;
}
.text-justify {
  text-align: justify;
}
.text-nowrap {
  white-space: nowrap;
}
.text-lowercase {
  text-transform: lowercase;
}
.text-uppercase {
  text-transform: uppercase;
}
.text-capitalize {
  text-transform: capitalize;
}
.text-muted {
  color: #777777;
}
.text-primary {
  color: #337ab7;
}
a.text-primary:hover,
a.text-primary:focus {
  color: #286090;
}
.text-success {
  color: #3c763d;
}
a.text-success:hover,
a.text-success:focus {
  color: #2b542c;
}
.text-info {
  color: #31708f;
}
a.text-info:hover,
a.text-info:focus {
  color: #245269;
}
.text-warning {
  color: #8a6d3b;
}
a.text-warning:hover,
a.text-warning:focus {
  color: #66512c;
}
.text-danger {
  color: #a94442;
}
a.text-danger:hover,
a.text-danger:focus {
  color: #843534;
}
.bg-primary {
  color: #fff;
  background-color: #337ab7;
}
a.bg-primary:hover,
a.bg-primary:focus {
  background-color: #286090;
}
.bg-success {
  background-color: #dff0d8;
}
a.bg-success:hover,
a.bg-success:focus {
  background-color: #c1e2b3;
}
.bg-info {
  background-color: #d9edf7;
}
a.bg-info:hover,
a.bg-info:focus {
  background-color: #afd9ee;
}
.bg-warning {
  background-color: #fcf8e3;
}
a.bg-warning:hover,
a.bg-warning:focus {
  background-color: #f7ecb5;
}
.bg-danger {
  background-color: #f2dede;
}
a.bg-danger:hover,
a.bg-danger:focus {
  background-color: #e4b9b9;
}
.page-header {
  padding-bottom: 8px;
  margin: 36px 0 18px;
  border-bottom: 1px solid #eeeeee;
}
ul,
ol {
  margin-top: 0;
  margin-bottom: 9px;
}
ul ul,
ol ul,
ul ol,
ol ol {
  margin-bottom: 0;
}
.list-unstyled {
  padding-left: 0;
  list-style: none;
}
.list-inline {
  padding-left: 0;
  list-style: none;
  margin-left: -5px;
}
.list-inline > li {
  display: inline-block;
  padding-left: 5px;
  padding-right: 5px;
}
dl {
  margin-top: 0;
  margin-bottom: 18px;
}
dt,
dd {
  line-height: 1.42857143;
}
dt {
  font-weight: bold;
}
dd {
  margin-left: 0;
}
@media (min-width: 541px) {
  .dl-horizontal dt {
    float: left;
    width: 160px;
    clear: left;
    text-align: right;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .dl-horizontal dd {
    margin-left: 180px;
  }
}
abbr[title],
abbr[data-original-title] {
  cursor: help;
  border-bottom: 1px dotted #777777;
}
.initialism {
  font-size: 90%;
  text-transform: uppercase;
}
blockquote {
  padding: 9px 18px;
  margin: 0 0 18px;
  font-size: inherit;
  border-left: 5px solid #eeeeee;
}
blockquote p:last-child,
blockquote ul:last-child,
blockquote ol:last-child {
  margin-bottom: 0;
}
blockquote footer,
blockquote small,
blockquote .small {
  display: block;
  font-size: 80%;
  line-height: 1.42857143;
  color: #777777;
}
blockquote footer:before,
blockquote small:before,
blockquote .small:before {
  content: '\2014 \00A0';
}
.blockquote-reverse,
blockquote.pull-right {
  padding-right: 15px;
  padding-left: 0;
  border-right: 5px solid #eeeeee;
  border-left: 0;
  text-align: right;
}
.blockquote-reverse footer:before,
blockquote.pull-right footer:before,
.blockquote-reverse small:before,
blockquote.pull-right small:before,
.blockquote-reverse .small:before,
blockquote.pull-right .small:before {
  content: '';
}
.blockquote-reverse footer:after,
blockquote.pull-right footer:after,
.blockquote-reverse small:after,
blockquote.pull-right small:after,
.blockquote-reverse .small:after,
blockquote.pull-right .small:after {
  content: '\00A0 \2014';
}
address {
  margin-bottom: 18px;
  font-style: normal;
  line-height: 1.42857143;
}
code,
kbd,
pre,
samp {
  font-family: monospace;
}
code {
  padding: 2px 4px;
  font-size: 90%;
  color: #c7254e;
  background-color: #f9f2f4;
  border-radius: 2px;
}
kbd {
  padding: 2px 4px;
  font-size: 90%;
  color: #888;
  background-color: transparent;
  border-radius: 1px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
}
kbd kbd {
  padding: 0;
  font-size: 100%;
  font-weight: bold;
  box-shadow: none;
}
pre {
  display: block;
  padding: 8.5px;
  margin: 0 0 9px;
  font-size: 12px;
  line-height: 1.42857143;
  word-break: break-all;
  word-wrap: break-word;
  color: #333333;
  background-color: #f5f5f5;
  border: 1px solid #ccc;
  border-radius: 2px;
}
pre code {
  padding: 0;
  font-size: inherit;
  color: inherit;
  white-space: pre-wrap;
  background-color: transparent;
  border-radius: 0;
}
.pre-scrollable {
  max-height: 340px;
  overflow-y: scroll;
}
.container {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
@media (min-width: 768px) {
  .container {
    width: 768px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 940px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1140px;
  }
}
.container-fluid {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
.row {
  margin-left: 0px;
  margin-right: 0px;
}
.col-xs-1, .col-sm-1, .col-md-1, .col-lg-1, .col-xs-2, .col-sm-2, .col-md-2, .col-lg-2, .col-xs-3, .col-sm-3, .col-md-3, .col-lg-3, .col-xs-4, .col-sm-4, .col-md-4, .col-lg-4, .col-xs-5, .col-sm-5, .col-md-5, .col-lg-5, .col-xs-6, .col-sm-6, .col-md-6, .col-lg-6, .col-xs-7, .col-sm-7, .col-md-7, .col-lg-7, .col-xs-8, .col-sm-8, .col-md-8, .col-lg-8, .col-xs-9, .col-sm-9, .col-md-9, .col-lg-9, .col-xs-10, .col-sm-10, .col-md-10, .col-lg-10, .col-xs-11, .col-sm-11, .col-md-11, .col-lg-11, .col-xs-12, .col-sm-12, .col-md-12, .col-lg-12 {
  position: relative;
  min-height: 1px;
  padding-left: 0px;
  padding-right: 0px;
}
.col-xs-1, .col-xs-2, .col-xs-3, .col-xs-4, .col-xs-5, .col-xs-6, .col-xs-7, .col-xs-8, .col-xs-9, .col-xs-10, .col-xs-11, .col-xs-12 {
  float: left;
}
.col-xs-12 {
  width: 100%;
}
.col-xs-11 {
  width: 91.66666667%;
}
.col-xs-10 {
  width: 83.33333333%;
}
.col-xs-9 {
  width: 75%;
}
.col-xs-8 {
  width: 66.66666667%;
}
.col-xs-7 {
  width: 58.33333333%;
}
.col-xs-6 {
  width: 50%;
}
.col-xs-5 {
  width: 41.66666667%;
}
.col-xs-4 {
  width: 33.33333333%;
}
.col-xs-3 {
  width: 25%;
}
.col-xs-2 {
  width: 16.66666667%;
}
.col-xs-1 {
  width: 8.33333333%;
}
.col-xs-pull-12 {
  right: 100%;
}
.col-xs-pull-11 {
  right: 91.66666667%;
}
.col-xs-pull-10 {
  right: 83.33333333%;
}
.col-xs-pull-9 {
  right: 75%;
}
.col-xs-pull-8 {
  right: 66.66666667%;
}
.col-xs-pull-7 {
  right: 58.33333333%;
}
.col-xs-pull-6 {
  right: 50%;
}
.col-xs-pull-5 {
  right: 41.66666667%;
}
.col-xs-pull-4 {
  right: 33.33333333%;
}
.col-xs-pull-3 {
  right: 25%;
}
.col-xs-pull-2 {
  right: 16.66666667%;
}
.col-xs-pull-1 {
  right: 8.33333333%;
}
.col-xs-pull-0 {
  right: auto;
}
.col-xs-push-12 {
  left: 100%;
}
.col-xs-push-11 {
  left: 91.66666667%;
}
.col-xs-push-10 {
  left: 83.33333333%;
}
.col-xs-push-9 {
  left: 75%;
}
.col-xs-push-8 {
  left: 66.66666667%;
}
.col-xs-push-7 {
  left: 58.33333333%;
}
.col-xs-push-6 {
  left: 50%;
}
.col-xs-push-5 {
  left: 41.66666667%;
}
.col-xs-push-4 {
  left: 33.33333333%;
}
.col-xs-push-3 {
  left: 25%;
}
.col-xs-push-2 {
  left: 16.66666667%;
}
.col-xs-push-1 {
  left: 8.33333333%;
}
.col-xs-push-0 {
  left: auto;
}
.col-xs-offset-12 {
  margin-left: 100%;
}
.col-xs-offset-11 {
  margin-left: 91.66666667%;
}
.col-xs-offset-10 {
  margin-left: 83.33333333%;
}
.col-xs-offset-9 {
  margin-left: 75%;
}
.col-xs-offset-8 {
  margin-left: 66.66666667%;
}
.col-xs-offset-7 {
  margin-left: 58.33333333%;
}
.col-xs-offset-6 {
  margin-left: 50%;
}
.col-xs-offset-5 {
  margin-left: 41.66666667%;
}
.col-xs-offset-4 {
  margin-left: 33.33333333%;
}
.col-xs-offset-3 {
  margin-left: 25%;
}
.col-xs-offset-2 {
  margin-left: 16.66666667%;
}
.col-xs-offset-1 {
  margin-left: 8.33333333%;
}
.col-xs-offset-0 {
  margin-left: 0%;
}
@media (min-width: 768px) {
  .col-sm-1, .col-sm-2, .col-sm-3, .col-sm-4, .col-sm-5, .col-sm-6, .col-sm-7, .col-sm-8, .col-sm-9, .col-sm-10, .col-sm-11, .col-sm-12 {
    float: left;
  }
  .col-sm-12 {
    width: 100%;
  }
  .col-sm-11 {
    width: 91.66666667%;
  }
  .col-sm-10 {
    width: 83.33333333%;
  }
  .col-sm-9 {
    width: 75%;
  }
  .col-sm-8 {
    width: 66.66666667%;
  }
  .col-sm-7 {
    width: 58.33333333%;
  }
  .col-sm-6 {
    width: 50%;
  }
  .col-sm-5 {
    width: 41.66666667%;
  }
  .col-sm-4 {
    width: 33.33333333%;
  }
  .col-sm-3 {
    width: 25%;
  }
  .col-sm-2 {
    width: 16.66666667%;
  }
  .col-sm-1 {
    width: 8.33333333%;
  }
  .col-sm-pull-12 {
    right: 100%;
  }
  .col-sm-pull-11 {
    right: 91.66666667%;
  }
  .col-sm-pull-10 {
    right: 83.33333333%;
  }
  .col-sm-pull-9 {
    right: 75%;
  }
  .col-sm-pull-8 {
    right: 66.66666667%;
  }
  .col-sm-pull-7 {
    right: 58.33333333%;
  }
  .col-sm-pull-6 {
    right: 50%;
  }
  .col-sm-pull-5 {
    right: 41.66666667%;
  }
  .col-sm-pull-4 {
    right: 33.33333333%;
  }
  .col-sm-pull-3 {
    right: 25%;
  }
  .col-sm-pull-2 {
    right: 16.66666667%;
  }
  .col-sm-pull-1 {
    right: 8.33333333%;
  }
  .col-sm-pull-0 {
    right: auto;
  }
  .col-sm-push-12 {
    left: 100%;
  }
  .col-sm-push-11 {
    left: 91.66666667%;
  }
  .col-sm-push-10 {
    left: 83.33333333%;
  }
  .col-sm-push-9 {
    left: 75%;
  }
  .col-sm-push-8 {
    left: 66.66666667%;
  }
  .col-sm-push-7 {
    left: 58.33333333%;
  }
  .col-sm-push-6 {
    left: 50%;
  }
  .col-sm-push-5 {
    left: 41.66666667%;
  }
  .col-sm-push-4 {
    left: 33.33333333%;
  }
  .col-sm-push-3 {
    left: 25%;
  }
  .col-sm-push-2 {
    left: 16.66666667%;
  }
  .col-sm-push-1 {
    left: 8.33333333%;
  }
  .col-sm-push-0 {
    left: auto;
  }
  .col-sm-offset-12 {
    margin-left: 100%;
  }
  .col-sm-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-sm-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-sm-offset-9 {
    margin-left: 75%;
  }
  .col-sm-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-sm-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-sm-offset-6 {
    margin-left: 50%;
  }
  .col-sm-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-sm-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-sm-offset-3 {
    margin-left: 25%;
  }
  .col-sm-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-sm-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-sm-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 992px) {
  .col-md-1, .col-md-2, .col-md-3, .col-md-4, .col-md-5, .col-md-6, .col-md-7, .col-md-8, .col-md-9, .col-md-10, .col-md-11, .col-md-12 {
    float: left;
  }
  .col-md-12 {
    width: 100%;
  }
  .col-md-11 {
    width: 91.66666667%;
  }
  .col-md-10 {
    width: 83.33333333%;
  }
  .col-md-9 {
    width: 75%;
  }
  .col-md-8 {
    width: 66.66666667%;
  }
  .col-md-7 {
    width: 58.33333333%;
  }
  .col-md-6 {
    width: 50%;
  }
  .col-md-5 {
    width: 41.66666667%;
  }
  .col-md-4 {
    width: 33.33333333%;
  }
  .col-md-3 {
    width: 25%;
  }
  .col-md-2 {
    width: 16.66666667%;
  }
  .col-md-1 {
    width: 8.33333333%;
  }
  .col-md-pull-12 {
    right: 100%;
  }
  .col-md-pull-11 {
    right: 91.66666667%;
  }
  .col-md-pull-10 {
    right: 83.33333333%;
  }
  .col-md-pull-9 {
    right: 75%;
  }
  .col-md-pull-8 {
    right: 66.66666667%;
  }
  .col-md-pull-7 {
    right: 58.33333333%;
  }
  .col-md-pull-6 {
    right: 50%;
  }
  .col-md-pull-5 {
    right: 41.66666667%;
  }
  .col-md-pull-4 {
    right: 33.33333333%;
  }
  .col-md-pull-3 {
    right: 25%;
  }
  .col-md-pull-2 {
    right: 16.66666667%;
  }
  .col-md-pull-1 {
    right: 8.33333333%;
  }
  .col-md-pull-0 {
    right: auto;
  }
  .col-md-push-12 {
    left: 100%;
  }
  .col-md-push-11 {
    left: 91.66666667%;
  }
  .col-md-push-10 {
    left: 83.33333333%;
  }
  .col-md-push-9 {
    left: 75%;
  }
  .col-md-push-8 {
    left: 66.66666667%;
  }
  .col-md-push-7 {
    left: 58.33333333%;
  }
  .col-md-push-6 {
    left: 50%;
  }
  .col-md-push-5 {
    left: 41.66666667%;
  }
  .col-md-push-4 {
    left: 33.33333333%;
  }
  .col-md-push-3 {
    left: 25%;
  }
  .col-md-push-2 {
    left: 16.66666667%;
  }
  .col-md-push-1 {
    left: 8.33333333%;
  }
  .col-md-push-0 {
    left: auto;
  }
  .col-md-offset-12 {
    margin-left: 100%;
  }
  .col-md-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-md-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-md-offset-9 {
    margin-left: 75%;
  }
  .col-md-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-md-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-md-offset-6 {
    margin-left: 50%;
  }
  .col-md-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-md-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-md-offset-3 {
    margin-left: 25%;
  }
  .col-md-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-md-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-md-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 1200px) {
  .col-lg-1, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6, .col-lg-7, .col-lg-8, .col-lg-9, .col-lg-10, .col-lg-11, .col-lg-12 {
    float: left;
  }
  .col-lg-12 {
    width: 100%;
  }
  .col-lg-11 {
    width: 91.66666667%;
  }
  .col-lg-10 {
    width: 83.33333333%;
  }
  .col-lg-9 {
    width: 75%;
  }
  .col-lg-8 {
    width: 66.66666667%;
  }
  .col-lg-7 {
    width: 58.33333333%;
  }
  .col-lg-6 {
    width: 50%;
  }
  .col-lg-5 {
    width: 41.66666667%;
  }
  .col-lg-4 {
    width: 33.33333333%;
  }
  .col-lg-3 {
    width: 25%;
  }
  .col-lg-2 {
    width: 16.66666667%;
  }
  .col-lg-1 {
    width: 8.33333333%;
  }
  .col-lg-pull-12 {
    right: 100%;
  }
  .col-lg-pull-11 {
    right: 91.66666667%;
  }
  .col-lg-pull-10 {
    right: 83.33333333%;
  }
  .col-lg-pull-9 {
    right: 75%;
  }
  .col-lg-pull-8 {
    right: 66.66666667%;
  }
  .col-lg-pull-7 {
    right: 58.33333333%;
  }
  .col-lg-pull-6 {
    right: 50%;
  }
  .col-lg-pull-5 {
    right: 41.66666667%;
  }
  .col-lg-pull-4 {
    right: 33.33333333%;
  }
  .col-lg-pull-3 {
    right: 25%;
  }
  .col-lg-pull-2 {
    right: 16.66666667%;
  }
  .col-lg-pull-1 {
    right: 8.33333333%;
  }
  .col-lg-pull-0 {
    right: auto;
  }
  .col-lg-push-12 {
    left: 100%;
  }
  .col-lg-push-11 {
    left: 91.66666667%;
  }
  .col-lg-push-10 {
    left: 83.33333333%;
  }
  .col-lg-push-9 {
    left: 75%;
  }
  .col-lg-push-8 {
    left: 66.66666667%;
  }
  .col-lg-push-7 {
    left: 58.33333333%;
  }
  .col-lg-push-6 {
    left: 50%;
  }
  .col-lg-push-5 {
    left: 41.66666667%;
  }
  .col-lg-push-4 {
    left: 33.33333333%;
  }
  .col-lg-push-3 {
    left: 25%;
  }
  .col-lg-push-2 {
    left: 16.66666667%;
  }
  .col-lg-push-1 {
    left: 8.33333333%;
  }
  .col-lg-push-0 {
    left: auto;
  }
  .col-lg-offset-12 {
    margin-left: 100%;
  }
  .col-lg-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-lg-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-lg-offset-9 {
    margin-left: 75%;
  }
  .col-lg-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-lg-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-lg-offset-6 {
    margin-left: 50%;
  }
  .col-lg-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-lg-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-lg-offset-3 {
    margin-left: 25%;
  }
  .col-lg-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-lg-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-lg-offset-0 {
    margin-left: 0%;
  }
}
table {
  background-color: transparent;
}
caption {
  padding-top: 8px;
  padding-bottom: 8px;
  color: #777777;
  text-align: left;
}
th {
  text-align: left;
}
.table {
  width: 100%;
  max-width: 100%;
  margin-bottom: 18px;
}
.table > thead > tr > th,
.table > tbody > tr > th,
.table > tfoot > tr > th,
.table > thead > tr > td,
.table > tbody > tr > td,
.table > tfoot > tr > td {
  padding: 8px;
  line-height: 1.42857143;
  vertical-align: top;
  border-top: 1px solid #ddd;
}
.table > thead > tr > th {
  vertical-align: bottom;
  border-bottom: 2px solid #ddd;
}
.table > caption + thead > tr:first-child > th,
.table > colgroup + thead > tr:first-child > th,
.table > thead:first-child > tr:first-child > th,
.table > caption + thead > tr:first-child > td,
.table > colgroup + thead > tr:first-child > td,
.table > thead:first-child > tr:first-child > td {
  border-top: 0;
}
.table > tbody + tbody {
  border-top: 2px solid #ddd;
}
.table .table {
  background-color: #fff;
}
.table-condensed > thead > tr > th,
.table-condensed > tbody > tr > th,
.table-condensed > tfoot > tr > th,
.table-condensed > thead > tr > td,
.table-condensed > tbody > tr > td,
.table-condensed > tfoot > tr > td {
  padding: 5px;
}
.table-bordered {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > tbody > tr > th,
.table-bordered > tfoot > tr > th,
.table-bordered > thead > tr > td,
.table-bordered > tbody > tr > td,
.table-bordered > tfoot > tr > td {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > thead > tr > td {
  border-bottom-width: 2px;
}
.table-striped > tbody > tr:nth-of-type(odd) {
  background-color: #f9f9f9;
}
.table-hover > tbody > tr:hover {
  background-color: #f5f5f5;
}
table col[class*="col-"] {
  position: static;
  float: none;
  display: table-column;
}
table td[class*="col-"],
table th[class*="col-"] {
  position: static;
  float: none;
  display: table-cell;
}
.table > thead > tr > td.active,
.table > tbody > tr > td.active,
.table > tfoot > tr > td.active,
.table > thead > tr > th.active,
.table > tbody > tr > th.active,
.table > tfoot > tr > th.active,
.table > thead > tr.active > td,
.table > tbody > tr.active > td,
.table > tfoot > tr.active > td,
.table > thead > tr.active > th,
.table > tbody > tr.active > th,
.table > tfoot > tr.active > th {
  background-color: #f5f5f5;
}
.table-hover > tbody > tr > td.active:hover,
.table-hover > tbody > tr > th.active:hover,
.table-hover > tbody > tr.active:hover > td,
.table-hover > tbody > tr:hover > .active,
.table-hover > tbody > tr.active:hover > th {
  background-color: #e8e8e8;
}
.table > thead > tr > td.success,
.table > tbody > tr > td.success,
.table > tfoot > tr > td.success,
.table > thead > tr > th.success,
.table > tbody > tr > th.success,
.table > tfoot > tr > th.success,
.table > thead > tr.success > td,
.table > tbody > tr.success > td,
.table > tfoot > tr.success > td,
.table > thead > tr.success > th,
.table > tbody > tr.success > th,
.table > tfoot > tr.success > th {
  background-color: #dff0d8;
}
.table-hover > tbody > tr > td.success:hover,
.table-hover > tbody > tr > th.success:hover,
.table-hover > tbody > tr.success:hover > td,
.table-hover > tbody > tr:hover > .success,
.table-hover > tbody > tr.success:hover > th {
  background-color: #d0e9c6;
}
.table > thead > tr > td.info,
.table > tbody > tr > td.info,
.table > tfoot > tr > td.info,
.table > thead > tr > th.info,
.table > tbody > tr > th.info,
.table > tfoot > tr > th.info,
.table > thead > tr.info > td,
.table > tbody > tr.info > td,
.table > tfoot > tr.info > td,
.table > thead > tr.info > th,
.table > tbody > tr.info > th,
.table > tfoot > tr.info > th {
  background-color: #d9edf7;
}
.table-hover > tbody > tr > td.info:hover,
.table-hover > tbody > tr > th.info:hover,
.table-hover > tbody > tr.info:hover > td,
.table-hover > tbody > tr:hover > .info,
.table-hover > tbody > tr.info:hover > th {
  background-color: #c4e3f3;
}
.table > thead > tr > td.warning,
.table > tbody > tr > td.warning,
.table > tfoot > tr > td.warning,
.table > thead > tr > th.warning,
.table > tbody > tr > th.warning,
.table > tfoot > tr > th.warning,
.table > thead > tr.warning > td,
.table > tbody > tr.warning > td,
.table > tfoot > tr.warning > td,
.table > thead > tr.warning > th,
.table > tbody > tr.warning > th,
.table > tfoot > tr.warning > th {
  background-color: #fcf8e3;
}
.table-hover > tbody > tr > td.warning:hover,
.table-hover > tbody > tr > th.warning:hover,
.table-hover > tbody > tr.warning:hover > td,
.table-hover > tbody > tr:hover > .warning,
.table-hover > tbody > tr.warning:hover > th {
  background-color: #faf2cc;
}
.table > thead > tr > td.danger,
.table > tbody > tr > td.danger,
.table > tfoot > tr > td.danger,
.table > thead > tr > th.danger,
.table > tbody > tr > th.danger,
.table > tfoot > tr > th.danger,
.table > thead > tr.danger > td,
.table > tbody > tr.danger > td,
.table > tfoot > tr.danger > td,
.table > thead > tr.danger > th,
.table > tbody > tr.danger > th,
.table > tfoot > tr.danger > th {
  background-color: #f2dede;
}
.table-hover > tbody > tr > td.danger:hover,
.table-hover > tbody > tr > th.danger:hover,
.table-hover > tbody > tr.danger:hover > td,
.table-hover > tbody > tr:hover > .danger,
.table-hover > tbody > tr.danger:hover > th {
  background-color: #ebcccc;
}
.table-responsive {
  overflow-x: auto;
  min-height: 0.01%;
}
@media screen and (max-width: 767px) {
  .table-responsive {
    width: 100%;
    margin-bottom: 13.5px;
    overflow-y: hidden;
    -ms-overflow-style: -ms-autohiding-scrollbar;
    border: 1px solid #ddd;
  }
  .table-responsive > .table {
    margin-bottom: 0;
  }
  .table-responsive > .table > thead > tr > th,
  .table-responsive > .table > tbody > tr > th,
  .table-responsive > .table > tfoot > tr > th,
  .table-responsive > .table > thead > tr > td,
  .table-responsive > .table > tbody > tr > td,
  .table-responsive > .table > tfoot > tr > td {
    white-space: nowrap;
  }
  .table-responsive > .table-bordered {
    border: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:first-child,
  .table-responsive > .table-bordered > tbody > tr > th:first-child,
  .table-responsive > .table-bordered > tfoot > tr > th:first-child,
  .table-responsive > .table-bordered > thead > tr > td:first-child,
  .table-responsive > .table-bordered > tbody > tr > td:first-child,
  .table-responsive > .table-bordered > tfoot > tr > td:first-child {
    border-left: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:last-child,
  .table-responsive > .table-bordered > tbody > tr > th:last-child,
  .table-responsive > .table-bordered > tfoot > tr > th:last-child,
  .table-responsive > .table-bordered > thead > tr > td:last-child,
  .table-responsive > .table-bordered > tbody > tr > td:last-child,
  .table-responsive > .table-bordered > tfoot > tr > td:last-child {
    border-right: 0;
  }
  .table-responsive > .table-bordered > tbody > tr:last-child > th,
  .table-responsive > .table-bordered > tfoot > tr:last-child > th,
  .table-responsive > .table-bordered > tbody > tr:last-child > td,
  .table-responsive > .table-bordered > tfoot > tr:last-child > td {
    border-bottom: 0;
  }
}
fieldset {
  padding: 0;
  margin: 0;
  border: 0;
  min-width: 0;
}
legend {
  display: block;
  width: 100%;
  padding: 0;
  margin-bottom: 18px;
  font-size: 19.5px;
  line-height: inherit;
  color: #333333;
  border: 0;
  border-bottom: 1px solid #e5e5e5;
}
label {
  display: inline-block;
  max-width: 100%;
  margin-bottom: 5px;
  font-weight: bold;
}
input[type="search"] {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
input[type="radio"],
input[type="checkbox"] {
  margin: 4px 0 0;
  margin-top: 1px \9;
  line-height: normal;
}
input[type="file"] {
  display: block;
}
input[type="range"] {
  display: block;
  width: 100%;
}
select[multiple],
select[size] {
  height: auto;
}
input[type="file"]:focus,
input[type="radio"]:focus,
input[type="checkbox"]:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
output {
  display: block;
  padding-top: 7px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
}
.form-control {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
}
.form-control:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.form-control::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.form-control:-ms-input-placeholder {
  color: #999;
}
.form-control::-webkit-input-placeholder {
  color: #999;
}
.form-control::-ms-expand {
  border: 0;
  background-color: transparent;
}
.form-control[disabled],
.form-control[readonly],
fieldset[disabled] .form-control {
  background-color: #eeeeee;
  opacity: 1;
}
.form-control[disabled],
fieldset[disabled] .form-control {
  cursor: not-allowed;
}
textarea.form-control {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: none;
}
@media screen and (-webkit-min-device-pixel-ratio: 0) {
  input[type="date"].form-control,
  input[type="time"].form-control,
  input[type="datetime-local"].form-control,
  input[type="month"].form-control {
    line-height: 32px;
  }
  input[type="date"].input-sm,
  input[type="time"].input-sm,
  input[type="datetime-local"].input-sm,
  input[type="month"].input-sm,
  .input-group-sm input[type="date"],
  .input-group-sm input[type="time"],
  .input-group-sm input[type="datetime-local"],
  .input-group-sm input[type="month"] {
    line-height: 30px;
  }
  input[type="date"].input-lg,
  input[type="time"].input-lg,
  input[type="datetime-local"].input-lg,
  input[type="month"].input-lg,
  .input-group-lg input[type="date"],
  .input-group-lg input[type="time"],
  .input-group-lg input[type="datetime-local"],
  .input-group-lg input[type="month"] {
    line-height: 45px;
  }
}
.form-group {
  margin-bottom: 15px;
}
.radio,
.checkbox {
  position: relative;
  display: block;
  margin-top: 10px;
  margin-bottom: 10px;
}
.radio label,
.checkbox label {
  min-height: 18px;
  padding-left: 20px;
  margin-bottom: 0;
  font-weight: normal;
  cursor: pointer;
}
.radio input[type="radio"],
.radio-inline input[type="radio"],
.checkbox input[type="checkbox"],
.checkbox-inline input[type="checkbox"] {
  position: absolute;
  margin-left: -20px;
  margin-top: 4px \9;
}
.radio + .radio,
.checkbox + .checkbox {
  margin-top: -5px;
}
.radio-inline,
.checkbox-inline {
  position: relative;
  display: inline-block;
  padding-left: 20px;
  margin-bottom: 0;
  vertical-align: middle;
  font-weight: normal;
  cursor: pointer;
}
.radio-inline + .radio-inline,
.checkbox-inline + .checkbox-inline {
  margin-top: 0;
  margin-left: 10px;
}
input[type="radio"][disabled],
input[type="checkbox"][disabled],
input[type="radio"].disabled,
input[type="checkbox"].disabled,
fieldset[disabled] input[type="radio"],
fieldset[disabled] input[type="checkbox"] {
  cursor: not-allowed;
}
.radio-inline.disabled,
.checkbox-inline.disabled,
fieldset[disabled] .radio-inline,
fieldset[disabled] .checkbox-inline {
  cursor: not-allowed;
}
.radio.disabled label,
.checkbox.disabled label,
fieldset[disabled] .radio label,
fieldset[disabled] .checkbox label {
  cursor: not-allowed;
}
.form-control-static {
  padding-top: 7px;
  padding-bottom: 7px;
  margin-bottom: 0;
  min-height: 31px;
}
.form-control-static.input-lg,
.form-control-static.input-sm {
  padding-left: 0;
  padding-right: 0;
}
.input-sm {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-sm {
  height: 30px;
  line-height: 30px;
}
textarea.input-sm,
select[multiple].input-sm {
  height: auto;
}
.form-group-sm .form-control {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.form-group-sm select.form-control {
  height: 30px;
  line-height: 30px;
}
.form-group-sm textarea.form-control,
.form-group-sm select[multiple].form-control {
  height: auto;
}
.form-group-sm .form-control-static {
  height: 30px;
  min-height: 30px;
  padding: 6px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.input-lg {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-lg {
  height: 45px;
  line-height: 45px;
}
textarea.input-lg,
select[multiple].input-lg {
  height: auto;
}
.form-group-lg .form-control {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.form-group-lg select.form-control {
  height: 45px;
  line-height: 45px;
}
.form-group-lg textarea.form-control,
.form-group-lg select[multiple].form-control {
  height: auto;
}
.form-group-lg .form-control-static {
  height: 45px;
  min-height: 35px;
  padding: 11px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.has-feedback {
  position: relative;
}
.has-feedback .form-control {
  padding-right: 40px;
}
.form-control-feedback {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 2;
  display: block;
  width: 32px;
  height: 32px;
  line-height: 32px;
  text-align: center;
  pointer-events: none;
}
.input-lg + .form-control-feedback,
.input-group-lg + .form-control-feedback,
.form-group-lg .form-control + .form-control-feedback {
  width: 45px;
  height: 45px;
  line-height: 45px;
}
.input-sm + .form-control-feedback,
.input-group-sm + .form-control-feedback,
.form-group-sm .form-control + .form-control-feedback {
  width: 30px;
  height: 30px;
  line-height: 30px;
}
.has-success .help-block,
.has-success .control-label,
.has-success .radio,
.has-success .checkbox,
.has-success .radio-inline,
.has-success .checkbox-inline,
.has-success.radio label,
.has-success.checkbox label,
.has-success.radio-inline label,
.has-success.checkbox-inline label {
  color: #3c763d;
}
.has-success .form-control {
  border-color: #3c763d;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-success .form-control:focus {
  border-color: #2b542c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
}
.has-success .input-group-addon {
  color: #3c763d;
  border-color: #3c763d;
  background-color: #dff0d8;
}
.has-success .form-control-feedback {
  color: #3c763d;
}
.has-warning .help-block,
.has-warning .control-label,
.has-warning .radio,
.has-warning .checkbox,
.has-warning .radio-inline,
.has-warning .checkbox-inline,
.has-warning.radio label,
.has-warning.checkbox label,
.has-warning.radio-inline label,
.has-warning.checkbox-inline label {
  color: #8a6d3b;
}
.has-warning .form-control {
  border-color: #8a6d3b;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-warning .form-control:focus {
  border-color: #66512c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
}
.has-warning .input-group-addon {
  color: #8a6d3b;
  border-color: #8a6d3b;
  background-color: #fcf8e3;
}
.has-warning .form-control-feedback {
  color: #8a6d3b;
}
.has-error .help-block,
.has-error .control-label,
.has-error .radio,
.has-error .checkbox,
.has-error .radio-inline,
.has-error .checkbox-inline,
.has-error.radio label,
.has-error.checkbox label,
.has-error.radio-inline label,
.has-error.checkbox-inline label {
  color: #a94442;
}
.has-error .form-control {
  border-color: #a94442;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-error .form-control:focus {
  border-color: #843534;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
}
.has-error .input-group-addon {
  color: #a94442;
  border-color: #a94442;
  background-color: #f2dede;
}
.has-error .form-control-feedback {
  color: #a94442;
}
.has-feedback label ~ .form-control-feedback {
  top: 23px;
}
.has-feedback label.sr-only ~ .form-control-feedback {
  top: 0;
}
.help-block {
  display: block;
  margin-top: 5px;
  margin-bottom: 10px;
  color: #404040;
}
@media (min-width: 768px) {
  .form-inline .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .form-inline .form-control-static {
    display: inline-block;
  }
  .form-inline .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .form-inline .input-group .input-group-addon,
  .form-inline .input-group .input-group-btn,
  .form-inline .input-group .form-control {
    width: auto;
  }
  .form-inline .input-group > .form-control {
    width: 100%;
  }
  .form-inline .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio,
  .form-inline .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio label,
  .form-inline .checkbox label {
    padding-left: 0;
  }
  .form-inline .radio input[type="radio"],
  .form-inline .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .form-inline .has-feedback .form-control-feedback {
    top: 0;
  }
}
.form-horizontal .radio,
.form-horizontal .checkbox,
.form-horizontal .radio-inline,
.form-horizontal .checkbox-inline {
  margin-top: 0;
  margin-bottom: 0;
  padding-top: 7px;
}
.form-horizontal .radio,
.form-horizontal .checkbox {
  min-height: 25px;
}
.form-horizontal .form-group {
  margin-left: 0px;
  margin-right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .control-label {
    text-align: right;
    margin-bottom: 0;
    padding-top: 7px;
  }
}
.form-horizontal .has-feedback .form-control-feedback {
  right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .form-group-lg .control-label {
    padding-top: 11px;
    font-size: 17px;
  }
}
@media (min-width: 768px) {
  .form-horizontal .form-group-sm .control-label {
    padding-top: 6px;
    font-size: 12px;
  }
}
.btn {
  display: inline-block;
  margin-bottom: 0;
  font-weight: normal;
  text-align: center;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  background-image: none;
  border: 1px solid transparent;
  white-space: nowrap;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  border-radius: 2px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.btn:focus,
.btn:active:focus,
.btn.active:focus,
.btn.focus,
.btn:active.focus,
.btn.active.focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
.btn:hover,
.btn:focus,
.btn.focus {
  color: #333;
  text-decoration: none;
}
.btn:active,
.btn.active {
  outline: 0;
  background-image: none;
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn.disabled,
.btn[disabled],
fieldset[disabled] .btn {
  cursor: not-allowed;
  opacity: 0.65;
  filter: alpha(opacity=65);
  -webkit-box-shadow: none;
  box-shadow: none;
}
a.btn.disabled,
fieldset[disabled] a.btn {
  pointer-events: none;
}
.btn-default {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.btn-default:focus,
.btn-default.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.btn-default:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active:hover,
.btn-default.active:hover,
.open > .dropdown-toggle.btn-default:hover,
.btn-default:active:focus,
.btn-default.active:focus,
.open > .dropdown-toggle.btn-default:focus,
.btn-default:active.focus,
.btn-default.active.focus,
.open > .dropdown-toggle.btn-default.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  background-image: none;
}
.btn-default.disabled:hover,
.btn-default[disabled]:hover,
fieldset[disabled] .btn-default:hover,
.btn-default.disabled:focus,
.btn-default[disabled]:focus,
fieldset[disabled] .btn-default:focus,
.btn-default.disabled.focus,
.btn-default[disabled].focus,
fieldset[disabled] .btn-default.focus {
  background-color: #fff;
  border-color: #ccc;
}
.btn-default .badge {
  color: #fff;
  background-color: #333;
}
.btn-primary {
  color: #fff;
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary:focus,
.btn-primary.focus {
  color: #fff;
  background-color: #286090;
  border-color: #122b40;
}
.btn-primary:hover {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active:hover,
.btn-primary.active:hover,
.open > .dropdown-toggle.btn-primary:hover,
.btn-primary:active:focus,
.btn-primary.active:focus,
.open > .dropdown-toggle.btn-primary:focus,
.btn-primary:active.focus,
.btn-primary.active.focus,
.open > .dropdown-toggle.btn-primary.focus {
  color: #fff;
  background-color: #204d74;
  border-color: #122b40;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  background-image: none;
}
.btn-primary.disabled:hover,
.btn-primary[disabled]:hover,
fieldset[disabled] .btn-primary:hover,
.btn-primary.disabled:focus,
.btn-primary[disabled]:focus,
fieldset[disabled] .btn-primary:focus,
.btn-primary.disabled.focus,
.btn-primary[disabled].focus,
fieldset[disabled] .btn-primary.focus {
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary .badge {
  color: #337ab7;
  background-color: #fff;
}
.btn-success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success:focus,
.btn-success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.btn-success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active:hover,
.btn-success.active:hover,
.open > .dropdown-toggle.btn-success:hover,
.btn-success:active:focus,
.btn-success.active:focus,
.open > .dropdown-toggle.btn-success:focus,
.btn-success:active.focus,
.btn-success.active.focus,
.open > .dropdown-toggle.btn-success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  background-image: none;
}
.btn-success.disabled:hover,
.btn-success[disabled]:hover,
fieldset[disabled] .btn-success:hover,
.btn-success.disabled:focus,
.btn-success[disabled]:focus,
fieldset[disabled] .btn-success:focus,
.btn-success.disabled.focus,
.btn-success[disabled].focus,
fieldset[disabled] .btn-success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.btn-info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info:focus,
.btn-info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.btn-info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active:hover,
.btn-info.active:hover,
.open > .dropdown-toggle.btn-info:hover,
.btn-info:active:focus,
.btn-info.active:focus,
.open > .dropdown-toggle.btn-info:focus,
.btn-info:active.focus,
.btn-info.active.focus,
.open > .dropdown-toggle.btn-info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  background-image: none;
}
.btn-info.disabled:hover,
.btn-info[disabled]:hover,
fieldset[disabled] .btn-info:hover,
.btn-info.disabled:focus,
.btn-info[disabled]:focus,
fieldset[disabled] .btn-info:focus,
.btn-info.disabled.focus,
.btn-info[disabled].focus,
fieldset[disabled] .btn-info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.btn-warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning:focus,
.btn-warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.btn-warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active:hover,
.btn-warning.active:hover,
.open > .dropdown-toggle.btn-warning:hover,
.btn-warning:active:focus,
.btn-warning.active:focus,
.open > .dropdown-toggle.btn-warning:focus,
.btn-warning:active.focus,
.btn-warning.active.focus,
.open > .dropdown-toggle.btn-warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  background-image: none;
}
.btn-warning.disabled:hover,
.btn-warning[disabled]:hover,
fieldset[disabled] .btn-warning:hover,
.btn-warning.disabled:focus,
.btn-warning[disabled]:focus,
fieldset[disabled] .btn-warning:focus,
.btn-warning.disabled.focus,
.btn-warning[disabled].focus,
fieldset[disabled] .btn-warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.btn-danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger:focus,
.btn-danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.btn-danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active:hover,
.btn-danger.active:hover,
.open > .dropdown-toggle.btn-danger:hover,
.btn-danger:active:focus,
.btn-danger.active:focus,
.open > .dropdown-toggle.btn-danger:focus,
.btn-danger:active.focus,
.btn-danger.active.focus,
.open > .dropdown-toggle.btn-danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  background-image: none;
}
.btn-danger.disabled:hover,
.btn-danger[disabled]:hover,
fieldset[disabled] .btn-danger:hover,
.btn-danger.disabled:focus,
.btn-danger[disabled]:focus,
fieldset[disabled] .btn-danger:focus,
.btn-danger.disabled.focus,
.btn-danger[disabled].focus,
fieldset[disabled] .btn-danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger .badge {
  color: #d9534f;
  background-color: #fff;
}
.btn-link {
  color: #337ab7;
  font-weight: normal;
  border-radius: 0;
}
.btn-link,
.btn-link:active,
.btn-link.active,
.btn-link[disabled],
fieldset[disabled] .btn-link {
  background-color: transparent;
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn-link,
.btn-link:hover,
.btn-link:focus,
.btn-link:active {
  border-color: transparent;
}
.btn-link:hover,
.btn-link:focus {
  color: #23527c;
  text-decoration: underline;
  background-color: transparent;
}
.btn-link[disabled]:hover,
fieldset[disabled] .btn-link:hover,
.btn-link[disabled]:focus,
fieldset[disabled] .btn-link:focus {
  color: #777777;
  text-decoration: none;
}
.btn-lg,
.btn-group-lg > .btn {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.btn-sm,
.btn-group-sm > .btn {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-xs,
.btn-group-xs > .btn {
  padding: 1px 5px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-block {
  display: block;
  width: 100%;
}
.btn-block + .btn-block {
  margin-top: 5px;
}
input[type="submit"].btn-block,
input[type="reset"].btn-block,
input[type="button"].btn-block {
  width: 100%;
}
.fade {
  opacity: 0;
  -webkit-transition: opacity 0.15s linear;
  -o-transition: opacity 0.15s linear;
  transition: opacity 0.15s linear;
}
.fade.in {
  opacity: 1;
}
.collapse {
  display: none;
}
.collapse.in {
  display: block;
}
tr.collapse.in {
  display: table-row;
}
tbody.collapse.in {
  display: table-row-group;
}
.collapsing {
  position: relative;
  height: 0;
  overflow: hidden;
  -webkit-transition-property: height, visibility;
  transition-property: height, visibility;
  -webkit-transition-duration: 0.35s;
  transition-duration: 0.35s;
  -webkit-transition-timing-function: ease;
  transition-timing-function: ease;
}
.caret {
  display: inline-block;
  width: 0;
  height: 0;
  margin-left: 2px;
  vertical-align: middle;
  border-top: 4px dashed;
  border-top: 4px solid \9;
  border-right: 4px solid transparent;
  border-left: 4px solid transparent;
}
.dropup,
.dropdown {
  position: relative;
}
.dropdown-toggle:focus {
  outline: 0;
}
.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 1000;
  display: none;
  float: left;
  min-width: 160px;
  padding: 5px 0;
  margin: 2px 0 0;
  list-style: none;
  font-size: 13px;
  text-align: left;
  background-color: #fff;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.15);
  border-radius: 2px;
  -webkit-box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  background-clip: padding-box;
}
.dropdown-menu.pull-right {
  right: 0;
  left: auto;
}
.dropdown-menu .divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.dropdown-menu > li > a {
  display: block;
  padding: 3px 20px;
  clear: both;
  font-weight: normal;
  line-height: 1.42857143;
  color: #333333;
  white-space: nowrap;
}
.dropdown-menu > li > a:hover,
.dropdown-menu > li > a:focus {
  text-decoration: none;
  color: #262626;
  background-color: #f5f5f5;
}
.dropdown-menu > .active > a,
.dropdown-menu > .active > a:hover,
.dropdown-menu > .active > a:focus {
  color: #fff;
  text-decoration: none;
  outline: 0;
  background-color: #337ab7;
}
.dropdown-menu > .disabled > a,
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  color: #777777;
}
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  text-decoration: none;
  background-color: transparent;
  background-image: none;
  filter: progid:DXImageTransform.Microsoft.gradient(enabled = false);
  cursor: not-allowed;
}
.open > .dropdown-menu {
  display: block;
}
.open > a {
  outline: 0;
}
.dropdown-menu-right {
  left: auto;
  right: 0;
}
.dropdown-menu-left {
  left: 0;
  right: auto;
}
.dropdown-header {
  display: block;
  padding: 3px 20px;
  font-size: 12px;
  line-height: 1.42857143;
  color: #777777;
  white-space: nowrap;
}
.dropdown-backdrop {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  z-index: 990;
}
.pull-right > .dropdown-menu {
  right: 0;
  left: auto;
}
.dropup .caret,
.navbar-fixed-bottom .dropdown .caret {
  border-top: 0;
  border-bottom: 4px dashed;
  border-bottom: 4px solid \9;
  content: "";
}
.dropup .dropdown-menu,
.navbar-fixed-bottom .dropdown .dropdown-menu {
  top: auto;
  bottom: 100%;
  margin-bottom: 2px;
}
@media (min-width: 541px) {
  .navbar-right .dropdown-menu {
    left: auto;
    right: 0;
  }
  .navbar-right .dropdown-menu-left {
    left: 0;
    right: auto;
  }
}
.btn-group,
.btn-group-vertical {
  position: relative;
  display: inline-block;
  vertical-align: middle;
}
.btn-group > .btn,
.btn-group-vertical > .btn {
  position: relative;
  float: left;
}
.btn-group > .btn:hover,
.btn-group-vertical > .btn:hover,
.btn-group > .btn:focus,
.btn-group-vertical > .btn:focus,
.btn-group > .btn:active,
.btn-group-vertical > .btn:active,
.btn-group > .btn.active,
.btn-group-vertical > .btn.active {
  z-index: 2;
}
.btn-group .btn + .btn,
.btn-group .btn + .btn-group,
.btn-group .btn-group + .btn,
.btn-group .btn-group + .btn-group {
  margin-left: -1px;
}
.btn-toolbar {
  margin-left: -5px;
}
.btn-toolbar .btn,
.btn-toolbar .btn-group,
.btn-toolbar .input-group {
  float: left;
}
.btn-toolbar > .btn,
.btn-toolbar > .btn-group,
.btn-toolbar > .input-group {
  margin-left: 5px;
}
.btn-group > .btn:not(:first-child):not(:last-child):not(.dropdown-toggle) {
  border-radius: 0;
}
.btn-group > .btn:first-child {
  margin-left: 0;
}
.btn-group > .btn:first-child:not(:last-child):not(.dropdown-toggle) {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn:last-child:not(:first-child),
.btn-group > .dropdown-toggle:not(:first-child) {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group > .btn-group {
  float: left;
}
.btn-group > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group .dropdown-toggle:active,
.btn-group.open .dropdown-toggle {
  outline: 0;
}
.btn-group > .btn + .dropdown-toggle {
  padding-left: 8px;
  padding-right: 8px;
}
.btn-group > .btn-lg + .dropdown-toggle {
  padding-left: 12px;
  padding-right: 12px;
}
.btn-group.open .dropdown-toggle {
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn-group.open .dropdown-toggle.btn-link {
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn .caret {
  margin-left: 0;
}
.btn-lg .caret {
  border-width: 5px 5px 0;
  border-bottom-width: 0;
}
.dropup .btn-lg .caret {
  border-width: 0 5px 5px;
}
.btn-group-vertical > .btn,
.btn-group-vertical > .btn-group,
.btn-group-vertical > .btn-group > .btn {
  display: block;
  float: none;
  width: 100%;
  max-width: 100%;
}
.btn-group-vertical > .btn-group > .btn {
  float: none;
}
.btn-group-vertical > .btn + .btn,
.btn-group-vertical > .btn + .btn-group,
.btn-group-vertical > .btn-group + .btn,
.btn-group-vertical > .btn-group + .btn-group {
  margin-top: -1px;
  margin-left: 0;
}
.btn-group-vertical > .btn:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.btn-group-vertical > .btn:first-child:not(:last-child) {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn:last-child:not(:first-child) {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
.btn-group-vertical > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.btn-group-justified {
  display: table;
  width: 100%;
  table-layout: fixed;
  border-collapse: separate;
}
.btn-group-justified > .btn,
.btn-group-justified > .btn-group {
  float: none;
  display: table-cell;
  width: 1%;
}
.btn-group-justified > .btn-group .btn {
  width: 100%;
}
.btn-group-justified > .btn-group .dropdown-menu {
  left: auto;
}
[data-toggle="buttons"] > .btn input[type="radio"],
[data-toggle="buttons"] > .btn-group > .btn input[type="radio"],
[data-toggle="buttons"] > .btn input[type="checkbox"],
[data-toggle="buttons"] > .btn-group > .btn input[type="checkbox"] {
  position: absolute;
  clip: rect(0, 0, 0, 0);
  pointer-events: none;
}
.input-group {
  position: relative;
  display: table;
  border-collapse: separate;
}
.input-group[class*="col-"] {
  float: none;
  padding-left: 0;
  padding-right: 0;
}
.input-group .form-control {
  position: relative;
  z-index: 2;
  float: left;
  width: 100%;
  margin-bottom: 0;
}
.input-group .form-control:focus {
  z-index: 3;
}
.input-group-lg > .form-control,
.input-group-lg > .input-group-addon,
.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-group-lg > .form-control,
select.input-group-lg > .input-group-addon,
select.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  line-height: 45px;
}
textarea.input-group-lg > .form-control,
textarea.input-group-lg > .input-group-addon,
textarea.input-group-lg > .input-group-btn > .btn,
select[multiple].input-group-lg > .form-control,
select[multiple].input-group-lg > .input-group-addon,
select[multiple].input-group-lg > .input-group-btn > .btn {
  height: auto;
}
.input-group-sm > .form-control,
.input-group-sm > .input-group-addon,
.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-group-sm > .form-control,
select.input-group-sm > .input-group-addon,
select.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  line-height: 30px;
}
textarea.input-group-sm > .form-control,
textarea.input-group-sm > .input-group-addon,
textarea.input-group-sm > .input-group-btn > .btn,
select[multiple].input-group-sm > .form-control,
select[multiple].input-group-sm > .input-group-addon,
select[multiple].input-group-sm > .input-group-btn > .btn {
  height: auto;
}
.input-group-addon,
.input-group-btn,
.input-group .form-control {
  display: table-cell;
}
.input-group-addon:not(:first-child):not(:last-child),
.input-group-btn:not(:first-child):not(:last-child),
.input-group .form-control:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.input-group-addon,
.input-group-btn {
  width: 1%;
  white-space: nowrap;
  vertical-align: middle;
}
.input-group-addon {
  padding: 6px 12px;
  font-size: 13px;
  font-weight: normal;
  line-height: 1;
  color: #555555;
  text-align: center;
  background-color: #eeeeee;
  border: 1px solid #ccc;
  border-radius: 2px;
}
.input-group-addon.input-sm {
  padding: 5px 10px;
  font-size: 12px;
  border-radius: 1px;
}
.input-group-addon.input-lg {
  padding: 10px 16px;
  font-size: 17px;
  border-radius: 3px;
}
.input-group-addon input[type="radio"],
.input-group-addon input[type="checkbox"] {
  margin-top: 0;
}
.input-group .form-control:first-child,
.input-group-addon:first-child,
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group > .btn,
.input-group-btn:first-child > .dropdown-toggle,
.input-group-btn:last-child > .btn:not(:last-child):not(.dropdown-toggle),
.input-group-btn:last-child > .btn-group:not(:last-child) > .btn {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.input-group-addon:first-child {
  border-right: 0;
}
.input-group .form-control:last-child,
.input-group-addon:last-child,
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group > .btn,
.input-group-btn:last-child > .dropdown-toggle,
.input-group-btn:first-child > .btn:not(:first-child),
.input-group-btn:first-child > .btn-group:not(:first-child) > .btn {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.input-group-addon:last-child {
  border-left: 0;
}
.input-group-btn {
  position: relative;
  font-size: 0;
  white-space: nowrap;
}
.input-group-btn > .btn {
  position: relative;
}
.input-group-btn > .btn + .btn {
  margin-left: -1px;
}
.input-group-btn > .btn:hover,
.input-group-btn > .btn:focus,
.input-group-btn > .btn:active {
  z-index: 2;
}
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group {
  margin-right: -1px;
}
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group {
  z-index: 2;
  margin-left: -1px;
}
.nav {
  margin-bottom: 0;
  padding-left: 0;
  list-style: none;
}
.nav > li {
  position: relative;
  display: block;
}
.nav > li > a {
  position: relative;
  display: block;
  padding: 10px 15px;
}
.nav > li > a:hover,
.nav > li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.nav > li.disabled > a {
  color: #777777;
}
.nav > li.disabled > a:hover,
.nav > li.disabled > a:focus {
  color: #777777;
  text-decoration: none;
  background-color: transparent;
  cursor: not-allowed;
}
.nav .open > a,
.nav .open > a:hover,
.nav .open > a:focus {
  background-color: #eeeeee;
  border-color: #337ab7;
}
.nav .nav-divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.nav > li > a > img {
  max-width: none;
}
.nav-tabs {
  border-bottom: 1px solid #ddd;
}
.nav-tabs > li {
  float: left;
  margin-bottom: -1px;
}
.nav-tabs > li > a {
  margin-right: 2px;
  line-height: 1.42857143;
  border: 1px solid transparent;
  border-radius: 2px 2px 0 0;
}
.nav-tabs > li > a:hover {
  border-color: #eeeeee #eeeeee #ddd;
}
.nav-tabs > li.active > a,
.nav-tabs > li.active > a:hover,
.nav-tabs > li.active > a:focus {
  color: #555555;
  background-color: #fff;
  border: 1px solid #ddd;
  border-bottom-color: transparent;
  cursor: default;
}
.nav-tabs.nav-justified {
  width: 100%;
  border-bottom: 0;
}
.nav-tabs.nav-justified > li {
  float: none;
}
.nav-tabs.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-tabs.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-tabs.nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs.nav-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs.nav-justified > .active > a,
.nav-tabs.nav-justified > .active > a:hover,
.nav-tabs.nav-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs.nav-justified > .active > a,
  .nav-tabs.nav-justified > .active > a:hover,
  .nav-tabs.nav-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.nav-pills > li {
  float: left;
}
.nav-pills > li > a {
  border-radius: 2px;
}
.nav-pills > li + li {
  margin-left: 2px;
}
.nav-pills > li.active > a,
.nav-pills > li.active > a:hover,
.nav-pills > li.active > a:focus {
  color: #fff;
  background-color: #337ab7;
}
.nav-stacked > li {
  float: none;
}
.nav-stacked > li + li {
  margin-top: 2px;
  margin-left: 0;
}
.nav-justified {
  width: 100%;
}
.nav-justified > li {
  float: none;
}
.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs-justified {
  border-bottom: 0;
}
.nav-tabs-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs-justified > .active > a,
.nav-tabs-justified > .active > a:hover,
.nav-tabs-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs-justified > .active > a,
  .nav-tabs-justified > .active > a:hover,
  .nav-tabs-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.tab-content > .tab-pane {
  display: none;
}
.tab-content > .active {
  display: block;
}
.nav-tabs .dropdown-menu {
  margin-top: -1px;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar {
  position: relative;
  min-height: 30px;
  margin-bottom: 18px;
  border: 1px solid transparent;
}
@media (min-width: 541px) {
  .navbar {
    border-radius: 2px;
  }
}
@media (min-width: 541px) {
  .navbar-header {
    float: left;
  }
}
.navbar-collapse {
  overflow-x: visible;
  padding-right: 0px;
  padding-left: 0px;
  border-top: 1px solid transparent;
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
  -webkit-overflow-scrolling: touch;
}
.navbar-collapse.in {
  overflow-y: auto;
}
@media (min-width: 541px) {
  .navbar-collapse {
    width: auto;
    border-top: 0;
    box-shadow: none;
  }
  .navbar-collapse.collapse {
    display: block !important;
    height: auto !important;
    padding-bottom: 0;
    overflow: visible !important;
  }
  .navbar-collapse.in {
    overflow-y: visible;
  }
  .navbar-fixed-top .navbar-collapse,
  .navbar-static-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    padding-left: 0;
    padding-right: 0;
  }
}
.navbar-fixed-top .navbar-collapse,
.navbar-fixed-bottom .navbar-collapse {
  max-height: 340px;
}
@media (max-device-width: 540px) and (orientation: landscape) {
  .navbar-fixed-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    max-height: 200px;
  }
}
.container > .navbar-header,
.container-fluid > .navbar-header,
.container > .navbar-collapse,
.container-fluid > .navbar-collapse {
  margin-right: 0px;
  margin-left: 0px;
}
@media (min-width: 541px) {
  .container > .navbar-header,
  .container-fluid > .navbar-header,
  .container > .navbar-collapse,
  .container-fluid > .navbar-collapse {
    margin-right: 0;
    margin-left: 0;
  }
}
.navbar-static-top {
  z-index: 1000;
  border-width: 0 0 1px;
}
@media (min-width: 541px) {
  .navbar-static-top {
    border-radius: 0;
  }
}
.navbar-fixed-top,
.navbar-fixed-bottom {
  position: fixed;
  right: 0;
  left: 0;
  z-index: 1030;
}
@media (min-width: 541px) {
  .navbar-fixed-top,
  .navbar-fixed-bottom {
    border-radius: 0;
  }
}
.navbar-fixed-top {
  top: 0;
  border-width: 0 0 1px;
}
.navbar-fixed-bottom {
  bottom: 0;
  margin-bottom: 0;
  border-width: 1px 0 0;
}
.navbar-brand {
  float: left;
  padding: 6px 0px;
  font-size: 17px;
  line-height: 18px;
  height: 30px;
}
.navbar-brand:hover,
.navbar-brand:focus {
  text-decoration: none;
}
.navbar-brand > img {
  display: block;
}
@media (min-width: 541px) {
  .navbar > .container .navbar-brand,
  .navbar > .container-fluid .navbar-brand {
    margin-left: 0px;
  }
}
.navbar-toggle {
  position: relative;
  float: right;
  margin-right: 0px;
  padding: 9px 10px;
  margin-top: -2px;
  margin-bottom: -2px;
  background-color: transparent;
  background-image: none;
  border: 1px solid transparent;
  border-radius: 2px;
}
.navbar-toggle:focus {
  outline: 0;
}
.navbar-toggle .icon-bar {
  display: block;
  width: 22px;
  height: 2px;
  border-radius: 1px;
}
.navbar-toggle .icon-bar + .icon-bar {
  margin-top: 4px;
}
@media (min-width: 541px) {
  .navbar-toggle {
    display: none;
  }
}
.navbar-nav {
  margin: 3px 0px;
}
.navbar-nav > li > a {
  padding-top: 10px;
  padding-bottom: 10px;
  line-height: 18px;
}
@media (max-width: 540px) {
  .navbar-nav .open .dropdown-menu {
    position: static;
    float: none;
    width: auto;
    margin-top: 0;
    background-color: transparent;
    border: 0;
    box-shadow: none;
  }
  .navbar-nav .open .dropdown-menu > li > a,
  .navbar-nav .open .dropdown-menu .dropdown-header {
    padding: 5px 15px 5px 25px;
  }
  .navbar-nav .open .dropdown-menu > li > a {
    line-height: 18px;
  }
  .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-nav .open .dropdown-menu > li > a:focus {
    background-image: none;
  }
}
@media (min-width: 541px) {
  .navbar-nav {
    float: left;
    margin: 0;
  }
  .navbar-nav > li {
    float: left;
  }
  .navbar-nav > li > a {
    padding-top: 6px;
    padding-bottom: 6px;
  }
}
.navbar-form {
  margin-left: 0px;
  margin-right: 0px;
  padding: 10px 0px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
  -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  margin-top: -1px;
  margin-bottom: -1px;
}
@media (min-width: 768px) {
  .navbar-form .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .navbar-form .form-control-static {
    display: inline-block;
  }
  .navbar-form .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .navbar-form .input-group .input-group-addon,
  .navbar-form .input-group .input-group-btn,
  .navbar-form .input-group .form-control {
    width: auto;
  }
  .navbar-form .input-group > .form-control {
    width: 100%;
  }
  .navbar-form .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio,
  .navbar-form .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio label,
  .navbar-form .checkbox label {
    padding-left: 0;
  }
  .navbar-form .radio input[type="radio"],
  .navbar-form .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .navbar-form .has-feedback .form-control-feedback {
    top: 0;
  }
}
@media (max-width: 540px) {
  .navbar-form .form-group {
    margin-bottom: 5px;
  }
  .navbar-form .form-group:last-child {
    margin-bottom: 0;
  }
}
@media (min-width: 541px) {
  .navbar-form {
    width: auto;
    border: 0;
    margin-left: 0;
    margin-right: 0;
    padding-top: 0;
    padding-bottom: 0;
    -webkit-box-shadow: none;
    box-shadow: none;
  }
}
.navbar-nav > li > .dropdown-menu {
  margin-top: 0;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar-fixed-bottom .navbar-nav > li > .dropdown-menu {
  margin-bottom: 0;
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.navbar-btn {
  margin-top: -1px;
  margin-bottom: -1px;
}
.navbar-btn.btn-sm {
  margin-top: 0px;
  margin-bottom: 0px;
}
.navbar-btn.btn-xs {
  margin-top: 4px;
  margin-bottom: 4px;
}
.navbar-text {
  margin-top: 6px;
  margin-bottom: 6px;
}
@media (min-width: 541px) {
  .navbar-text {
    float: left;
    margin-left: 0px;
    margin-right: 0px;
  }
}
@media (min-width: 541px) {
  .navbar-left {
    float: left !important;
    float: left;
  }
  .navbar-right {
    float: right !important;
    float: right;
    margin-right: 0px;
  }
  .navbar-right ~ .navbar-right {
    margin-right: 0;
  }
}
.navbar-default {
  background-color: #f8f8f8;
  border-color: #e7e7e7;
}
.navbar-default .navbar-brand {
  color: #777;
}
.navbar-default .navbar-brand:hover,
.navbar-default .navbar-brand:focus {
  color: #5e5e5e;
  background-color: transparent;
}
.navbar-default .navbar-text {
  color: #777;
}
.navbar-default .navbar-nav > li > a {
  color: #777;
}
.navbar-default .navbar-nav > li > a:hover,
.navbar-default .navbar-nav > li > a:focus {
  color: #333;
  background-color: transparent;
}
.navbar-default .navbar-nav > .active > a,
.navbar-default .navbar-nav > .active > a:hover,
.navbar-default .navbar-nav > .active > a:focus {
  color: #555;
  background-color: #e7e7e7;
}
.navbar-default .navbar-nav > .disabled > a,
.navbar-default .navbar-nav > .disabled > a:hover,
.navbar-default .navbar-nav > .disabled > a:focus {
  color: #ccc;
  background-color: transparent;
}
.navbar-default .navbar-toggle {
  border-color: #ddd;
}
.navbar-default .navbar-toggle:hover,
.navbar-default .navbar-toggle:focus {
  background-color: #ddd;
}
.navbar-default .navbar-toggle .icon-bar {
  background-color: #888;
}
.navbar-default .navbar-collapse,
.navbar-default .navbar-form {
  border-color: #e7e7e7;
}
.navbar-default .navbar-nav > .open > a,
.navbar-default .navbar-nav > .open > a:hover,
.navbar-default .navbar-nav > .open > a:focus {
  background-color: #e7e7e7;
  color: #555;
}
@media (max-width: 540px) {
  .navbar-default .navbar-nav .open .dropdown-menu > li > a {
    color: #777;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #333;
    background-color: transparent;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #555;
    background-color: #e7e7e7;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #ccc;
    background-color: transparent;
  }
}
.navbar-default .navbar-link {
  color: #777;
}
.navbar-default .navbar-link:hover {
  color: #333;
}
.navbar-default .btn-link {
  color: #777;
}
.navbar-default .btn-link:hover,
.navbar-default .btn-link:focus {
  color: #333;
}
.navbar-default .btn-link[disabled]:hover,
fieldset[disabled] .navbar-default .btn-link:hover,
.navbar-default .btn-link[disabled]:focus,
fieldset[disabled] .navbar-default .btn-link:focus {
  color: #ccc;
}
.navbar-inverse {
  background-color: #222;
  border-color: #080808;
}
.navbar-inverse .navbar-brand {
  color: #9d9d9d;
}
.navbar-inverse .navbar-brand:hover,
.navbar-inverse .navbar-brand:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-text {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a:hover,
.navbar-inverse .navbar-nav > li > a:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-nav > .active > a,
.navbar-inverse .navbar-nav > .active > a:hover,
.navbar-inverse .navbar-nav > .active > a:focus {
  color: #fff;
  background-color: #080808;
}
.navbar-inverse .navbar-nav > .disabled > a,
.navbar-inverse .navbar-nav > .disabled > a:hover,
.navbar-inverse .navbar-nav > .disabled > a:focus {
  color: #444;
  background-color: transparent;
}
.navbar-inverse .navbar-toggle {
  border-color: #333;
}
.navbar-inverse .navbar-toggle:hover,
.navbar-inverse .navbar-toggle:focus {
  background-color: #333;
}
.navbar-inverse .navbar-toggle .icon-bar {
  background-color: #fff;
}
.navbar-inverse .navbar-collapse,
.navbar-inverse .navbar-form {
  border-color: #101010;
}
.navbar-inverse .navbar-nav > .open > a,
.navbar-inverse .navbar-nav > .open > a:hover,
.navbar-inverse .navbar-nav > .open > a:focus {
  background-color: #080808;
  color: #fff;
}
@media (max-width: 540px) {
  .navbar-inverse .navbar-nav .open .dropdown-menu > .dropdown-header {
    border-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu .divider {
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a {
    color: #9d9d9d;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #fff;
    background-color: transparent;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #fff;
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #444;
    background-color: transparent;
  }
}
.navbar-inverse .navbar-link {
  color: #9d9d9d;
}
.navbar-inverse .navbar-link:hover {
  color: #fff;
}
.navbar-inverse .btn-link {
  color: #9d9d9d;
}
.navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link:focus {
  color: #fff;
}
.navbar-inverse .btn-link[disabled]:hover,
fieldset[disabled] .navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link[disabled]:focus,
fieldset[disabled] .navbar-inverse .btn-link:focus {
  color: #444;
}
.breadcrumb {
  padding: 8px 15px;
  margin-bottom: 18px;
  list-style: none;
  background-color: #f5f5f5;
  border-radius: 2px;
}
.breadcrumb > li {
  display: inline-block;
}
.breadcrumb > li + li:before {
  content: "/\00a0";
  padding: 0 5px;
  color: #5e5e5e;
}
.breadcrumb > .active {
  color: #777777;
}
.pagination {
  display: inline-block;
  padding-left: 0;
  margin: 18px 0;
  border-radius: 2px;
}
.pagination > li {
  display: inline;
}
.pagination > li > a,
.pagination > li > span {
  position: relative;
  float: left;
  padding: 6px 12px;
  line-height: 1.42857143;
  text-decoration: none;
  color: #337ab7;
  background-color: #fff;
  border: 1px solid #ddd;
  margin-left: -1px;
}
.pagination > li:first-child > a,
.pagination > li:first-child > span {
  margin-left: 0;
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.pagination > li:last-child > a,
.pagination > li:last-child > span {
  border-bottom-right-radius: 2px;
  border-top-right-radius: 2px;
}
.pagination > li > a:hover,
.pagination > li > span:hover,
.pagination > li > a:focus,
.pagination > li > span:focus {
  z-index: 2;
  color: #23527c;
  background-color: #eeeeee;
  border-color: #ddd;
}
.pagination > .active > a,
.pagination > .active > span,
.pagination > .active > a:hover,
.pagination > .active > span:hover,
.pagination > .active > a:focus,
.pagination > .active > span:focus {
  z-index: 3;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
  cursor: default;
}
.pagination > .disabled > span,
.pagination > .disabled > span:hover,
.pagination > .disabled > span:focus,
.pagination > .disabled > a,
.pagination > .disabled > a:hover,
.pagination > .disabled > a:focus {
  color: #777777;
  background-color: #fff;
  border-color: #ddd;
  cursor: not-allowed;
}
.pagination-lg > li > a,
.pagination-lg > li > span {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.pagination-lg > li:first-child > a,
.pagination-lg > li:first-child > span {
  border-bottom-left-radius: 3px;
  border-top-left-radius: 3px;
}
.pagination-lg > li:last-child > a,
.pagination-lg > li:last-child > span {
  border-bottom-right-radius: 3px;
  border-top-right-radius: 3px;
}
.pagination-sm > li > a,
.pagination-sm > li > span {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.pagination-sm > li:first-child > a,
.pagination-sm > li:first-child > span {
  border-bottom-left-radius: 1px;
  border-top-left-radius: 1px;
}
.pagination-sm > li:last-child > a,
.pagination-sm > li:last-child > span {
  border-bottom-right-radius: 1px;
  border-top-right-radius: 1px;
}
.pager {
  padding-left: 0;
  margin: 18px 0;
  list-style: none;
  text-align: center;
}
.pager li {
  display: inline;
}
.pager li > a,
.pager li > span {
  display: inline-block;
  padding: 5px 14px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 15px;
}
.pager li > a:hover,
.pager li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.pager .next > a,
.pager .next > span {
  float: right;
}
.pager .previous > a,
.pager .previous > span {
  float: left;
}
.pager .disabled > a,
.pager .disabled > a:hover,
.pager .disabled > a:focus,
.pager .disabled > span {
  color: #777777;
  background-color: #fff;
  cursor: not-allowed;
}
.label {
  display: inline;
  padding: .2em .6em .3em;
  font-size: 75%;
  font-weight: bold;
  line-height: 1;
  color: #fff;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: .25em;
}
a.label:hover,
a.label:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.label:empty {
  display: none;
}
.btn .label {
  position: relative;
  top: -1px;
}
.label-default {
  background-color: #777777;
}
.label-default[href]:hover,
.label-default[href]:focus {
  background-color: #5e5e5e;
}
.label-primary {
  background-color: #337ab7;
}
.label-primary[href]:hover,
.label-primary[href]:focus {
  background-color: #286090;
}
.label-success {
  background-color: #5cb85c;
}
.label-success[href]:hover,
.label-success[href]:focus {
  background-color: #449d44;
}
.label-info {
  background-color: #5bc0de;
}
.label-info[href]:hover,
.label-info[href]:focus {
  background-color: #31b0d5;
}
.label-warning {
  background-color: #f0ad4e;
}
.label-warning[href]:hover,
.label-warning[href]:focus {
  background-color: #ec971f;
}
.label-danger {
  background-color: #d9534f;
}
.label-danger[href]:hover,
.label-danger[href]:focus {
  background-color: #c9302c;
}
.badge {
  display: inline-block;
  min-width: 10px;
  padding: 3px 7px;
  font-size: 12px;
  font-weight: bold;
  color: #fff;
  line-height: 1;
  vertical-align: middle;
  white-space: nowrap;
  text-align: center;
  background-color: #777777;
  border-radius: 10px;
}
.badge:empty {
  display: none;
}
.btn .badge {
  position: relative;
  top: -1px;
}
.btn-xs .badge,
.btn-group-xs > .btn .badge {
  top: 0;
  padding: 1px 5px;
}
a.badge:hover,
a.badge:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.list-group-item.active > .badge,
.nav-pills > .active > a > .badge {
  color: #337ab7;
  background-color: #fff;
}
.list-group-item > .badge {
  float: right;
}
.list-group-item > .badge + .badge {
  margin-right: 5px;
}
.nav-pills > li > a > .badge {
  margin-left: 3px;
}
.jumbotron {
  padding-top: 30px;
  padding-bottom: 30px;
  margin-bottom: 30px;
  color: inherit;
  background-color: #eeeeee;
}
.jumbotron h1,
.jumbotron .h1 {
  color: inherit;
}
.jumbotron p {
  margin-bottom: 15px;
  font-size: 20px;
  font-weight: 200;
}
.jumbotron > hr {
  border-top-color: #d5d5d5;
}
.container .jumbotron,
.container-fluid .jumbotron {
  border-radius: 3px;
  padding-left: 0px;
  padding-right: 0px;
}
.jumbotron .container {
  max-width: 100%;
}
@media screen and (min-width: 768px) {
  .jumbotron {
    padding-top: 48px;
    padding-bottom: 48px;
  }
  .container .jumbotron,
  .container-fluid .jumbotron {
    padding-left: 60px;
    padding-right: 60px;
  }
  .jumbotron h1,
  .jumbotron .h1 {
    font-size: 59px;
  }
}
.thumbnail {
  display: block;
  padding: 4px;
  margin-bottom: 18px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: border 0.2s ease-in-out;
  -o-transition: border 0.2s ease-in-out;
  transition: border 0.2s ease-in-out;
}
.thumbnail > img,
.thumbnail a > img {
  margin-left: auto;
  margin-right: auto;
}
a.thumbnail:hover,
a.thumbnail:focus,
a.thumbnail.active {
  border-color: #337ab7;
}
.thumbnail .caption {
  padding: 9px;
  color: #000;
}
.alert {
  padding: 15px;
  margin-bottom: 18px;
  border: 1px solid transparent;
  border-radius: 2px;
}
.alert h4 {
  margin-top: 0;
  color: inherit;
}
.alert .alert-link {
  font-weight: bold;
}
.alert > p,
.alert > ul {
  margin-bottom: 0;
}
.alert > p + p {
  margin-top: 5px;
}
.alert-dismissable,
.alert-dismissible {
  padding-right: 35px;
}
.alert-dismissable .close,
.alert-dismissible .close {
  position: relative;
  top: -2px;
  right: -21px;
  color: inherit;
}
.alert-success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #3c763d;
}
.alert-success hr {
  border-top-color: #c9e2b3;
}
.alert-success .alert-link {
  color: #2b542c;
}
.alert-info {
  background-color: #d9edf7;
  border-color: #bce8f1;
  color: #31708f;
}
.alert-info hr {
  border-top-color: #a6e1ec;
}
.alert-info .alert-link {
  color: #245269;
}
.alert-warning {
  background-color: #fcf8e3;
  border-color: #faebcc;
  color: #8a6d3b;
}
.alert-warning hr {
  border-top-color: #f7e1b5;
}
.alert-warning .alert-link {
  color: #66512c;
}
.alert-danger {
  background-color: #f2dede;
  border-color: #ebccd1;
  color: #a94442;
}
.alert-danger hr {
  border-top-color: #e4b9c0;
}
.alert-danger .alert-link {
  color: #843534;
}
@-webkit-keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
@keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
.progress {
  overflow: hidden;
  height: 18px;
  margin-bottom: 18px;
  background-color: #f5f5f5;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
}
.progress-bar {
  float: left;
  width: 0%;
  height: 100%;
  font-size: 12px;
  line-height: 18px;
  color: #fff;
  text-align: center;
  background-color: #337ab7;
  -webkit-box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  -webkit-transition: width 0.6s ease;
  -o-transition: width 0.6s ease;
  transition: width 0.6s ease;
}
.progress-striped .progress-bar,
.progress-bar-striped {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-size: 40px 40px;
}
.progress.active .progress-bar,
.progress-bar.active {
  -webkit-animation: progress-bar-stripes 2s linear infinite;
  -o-animation: progress-bar-stripes 2s linear infinite;
  animation: progress-bar-stripes 2s linear infinite;
}
.progress-bar-success {
  background-color: #5cb85c;
}
.progress-striped .progress-bar-success {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-info {
  background-color: #5bc0de;
}
.progress-striped .progress-bar-info {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-warning {
  background-color: #f0ad4e;
}
.progress-striped .progress-bar-warning {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-danger {
  background-color: #d9534f;
}
.progress-striped .progress-bar-danger {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.media {
  margin-top: 15px;
}
.media:first-child {
  margin-top: 0;
}
.media,
.media-body {
  zoom: 1;
  overflow: hidden;
}
.media-body {
  width: 10000px;
}
.media-object {
  display: block;
}
.media-object.img-thumbnail {
  max-width: none;
}
.media-right,
.media > .pull-right {
  padding-left: 10px;
}
.media-left,
.media > .pull-left {
  padding-right: 10px;
}
.media-left,
.media-right,
.media-body {
  display: table-cell;
  vertical-align: top;
}
.media-middle {
  vertical-align: middle;
}
.media-bottom {
  vertical-align: bottom;
}
.media-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.media-list {
  padding-left: 0;
  list-style: none;
}
.list-group {
  margin-bottom: 20px;
  padding-left: 0;
}
.list-group-item {
  position: relative;
  display: block;
  padding: 10px 15px;
  margin-bottom: -1px;
  background-color: #fff;
  border: 1px solid #ddd;
}
.list-group-item:first-child {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
}
.list-group-item:last-child {
  margin-bottom: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
a.list-group-item,
button.list-group-item {
  color: #555;
}
a.list-group-item .list-group-item-heading,
button.list-group-item .list-group-item-heading {
  color: #333;
}
a.list-group-item:hover,
button.list-group-item:hover,
a.list-group-item:focus,
button.list-group-item:focus {
  text-decoration: none;
  color: #555;
  background-color: #f5f5f5;
}
button.list-group-item {
  width: 100%;
  text-align: left;
}
.list-group-item.disabled,
.list-group-item.disabled:hover,
.list-group-item.disabled:focus {
  background-color: #eeeeee;
  color: #777777;
  cursor: not-allowed;
}
.list-group-item.disabled .list-group-item-heading,
.list-group-item.disabled:hover .list-group-item-heading,
.list-group-item.disabled:focus .list-group-item-heading {
  color: inherit;
}
.list-group-item.disabled .list-group-item-text,
.list-group-item.disabled:hover .list-group-item-text,
.list-group-item.disabled:focus .list-group-item-text {
  color: #777777;
}
.list-group-item.active,
.list-group-item.active:hover,
.list-group-item.active:focus {
  z-index: 2;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.list-group-item.active .list-group-item-heading,
.list-group-item.active:hover .list-group-item-heading,
.list-group-item.active:focus .list-group-item-heading,
.list-group-item.active .list-group-item-heading > small,
.list-group-item.active:hover .list-group-item-heading > small,
.list-group-item.active:focus .list-group-item-heading > small,
.list-group-item.active .list-group-item-heading > .small,
.list-group-item.active:hover .list-group-item-heading > .small,
.list-group-item.active:focus .list-group-item-heading > .small {
  color: inherit;
}
.list-group-item.active .list-group-item-text,
.list-group-item.active:hover .list-group-item-text,
.list-group-item.active:focus .list-group-item-text {
  color: #c7ddef;
}
.list-group-item-success {
  color: #3c763d;
  background-color: #dff0d8;
}
a.list-group-item-success,
button.list-group-item-success {
  color: #3c763d;
}
a.list-group-item-success .list-group-item-heading,
button.list-group-item-success .list-group-item-heading {
  color: inherit;
}
a.list-group-item-success:hover,
button.list-group-item-success:hover,
a.list-group-item-success:focus,
button.list-group-item-success:focus {
  color: #3c763d;
  background-color: #d0e9c6;
}
a.list-group-item-success.active,
button.list-group-item-success.active,
a.list-group-item-success.active:hover,
button.list-group-item-success.active:hover,
a.list-group-item-success.active:focus,
button.list-group-item-success.active:focus {
  color: #fff;
  background-color: #3c763d;
  border-color: #3c763d;
}
.list-group-item-info {
  color: #31708f;
  background-color: #d9edf7;
}
a.list-group-item-info,
button.list-group-item-info {
  color: #31708f;
}
a.list-group-item-info .list-group-item-heading,
button.list-group-item-info .list-group-item-heading {
  color: inherit;
}
a.list-group-item-info:hover,
button.list-group-item-info:hover,
a.list-group-item-info:focus,
button.list-group-item-info:focus {
  color: #31708f;
  background-color: #c4e3f3;
}
a.list-group-item-info.active,
button.list-group-item-info.active,
a.list-group-item-info.active:hover,
button.list-group-item-info.active:hover,
a.list-group-item-info.active:focus,
button.list-group-item-info.active:focus {
  color: #fff;
  background-color: #31708f;
  border-color: #31708f;
}
.list-group-item-warning {
  color: #8a6d3b;
  background-color: #fcf8e3;
}
a.list-group-item-warning,
button.list-group-item-warning {
  color: #8a6d3b;
}
a.list-group-item-warning .list-group-item-heading,
button.list-group-item-warning .list-group-item-heading {
  color: inherit;
}
a.list-group-item-warning:hover,
button.list-group-item-warning:hover,
a.list-group-item-warning:focus,
button.list-group-item-warning:focus {
  color: #8a6d3b;
  background-color: #faf2cc;
}
a.list-group-item-warning.active,
button.list-group-item-warning.active,
a.list-group-item-warning.active:hover,
button.list-group-item-warning.active:hover,
a.list-group-item-warning.active:focus,
button.list-group-item-warning.active:focus {
  color: #fff;
  background-color: #8a6d3b;
  border-color: #8a6d3b;
}
.list-group-item-danger {
  color: #a94442;
  background-color: #f2dede;
}
a.list-group-item-danger,
button.list-group-item-danger {
  color: #a94442;
}
a.list-group-item-danger .list-group-item-heading,
button.list-group-item-danger .list-group-item-heading {
  color: inherit;
}
a.list-group-item-danger:hover,
button.list-group-item-danger:hover,
a.list-group-item-danger:focus,
button.list-group-item-danger:focus {
  color: #a94442;
  background-color: #ebcccc;
}
a.list-group-item-danger.active,
button.list-group-item-danger.active,
a.list-group-item-danger.active:hover,
button.list-group-item-danger.active:hover,
a.list-group-item-danger.active:focus,
button.list-group-item-danger.active:focus {
  color: #fff;
  background-color: #a94442;
  border-color: #a94442;
}
.list-group-item-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.list-group-item-text {
  margin-bottom: 0;
  line-height: 1.3;
}
.panel {
  margin-bottom: 18px;
  background-color: #fff;
  border: 1px solid transparent;
  border-radius: 2px;
  -webkit-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
}
.panel-body {
  padding: 15px;
}
.panel-heading {
  padding: 10px 15px;
  border-bottom: 1px solid transparent;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel-heading > .dropdown .dropdown-toggle {
  color: inherit;
}
.panel-title {
  margin-top: 0;
  margin-bottom: 0;
  font-size: 15px;
  color: inherit;
}
.panel-title > a,
.panel-title > small,
.panel-title > .small,
.panel-title > small > a,
.panel-title > .small > a {
  color: inherit;
}
.panel-footer {
  padding: 10px 15px;
  background-color: #f5f5f5;
  border-top: 1px solid #ddd;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .list-group,
.panel > .panel-collapse > .list-group {
  margin-bottom: 0;
}
.panel > .list-group .list-group-item,
.panel > .panel-collapse > .list-group .list-group-item {
  border-width: 1px 0;
  border-radius: 0;
}
.panel > .list-group:first-child .list-group-item:first-child,
.panel > .panel-collapse > .list-group:first-child .list-group-item:first-child {
  border-top: 0;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .list-group:last-child .list-group-item:last-child,
.panel > .panel-collapse > .list-group:last-child .list-group-item:last-child {
  border-bottom: 0;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .panel-heading + .panel-collapse > .list-group .list-group-item:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.panel-heading + .list-group .list-group-item:first-child {
  border-top-width: 0;
}
.list-group + .panel-footer {
  border-top-width: 0;
}
.panel > .table,
.panel > .table-responsive > .table,
.panel > .panel-collapse > .table {
  margin-bottom: 0;
}
.panel > .table caption,
.panel > .table-responsive > .table caption,
.panel > .panel-collapse > .table caption {
  padding-left: 15px;
  padding-right: 15px;
}
.panel > .table:first-child,
.panel > .table-responsive:first-child > .table:first-child {
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child {
  border-top-left-radius: 1px;
  border-top-right-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:first-child {
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:last-child {
  border-top-right-radius: 1px;
}
.panel > .table:last-child,
.panel > .table-responsive:last-child > .table:last-child {
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child {
  border-bottom-left-radius: 1px;
  border-bottom-right-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:first-child {
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:last-child {
  border-bottom-right-radius: 1px;
}
.panel > .panel-body + .table,
.panel > .panel-body + .table-responsive,
.panel > .table + .panel-body,
.panel > .table-responsive + .panel-body {
  border-top: 1px solid #ddd;
}
.panel > .table > tbody:first-child > tr:first-child th,
.panel > .table > tbody:first-child > tr:first-child td {
  border-top: 0;
}
.panel > .table-bordered,
.panel > .table-responsive > .table-bordered {
  border: 0;
}
.panel > .table-bordered > thead > tr > th:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:first-child,
.panel > .table-bordered > tbody > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:first-child,
.panel > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-bordered > thead > tr > td:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:first-child,
.panel > .table-bordered > tbody > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:first-child,
.panel > .table-bordered > tfoot > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:first-child {
  border-left: 0;
}
.panel > .table-bordered > thead > tr > th:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:last-child,
.panel > .table-bordered > tbody > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:last-child,
.panel > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-bordered > thead > tr > td:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:last-child,
.panel > .table-bordered > tbody > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:last-child,
.panel > .table-bordered > tfoot > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:last-child {
  border-right: 0;
}
.panel > .table-bordered > thead > tr:first-child > td,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > td,
.panel > .table-bordered > tbody > tr:first-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > td,
.panel > .table-bordered > thead > tr:first-child > th,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > th,
.panel > .table-bordered > tbody > tr:first-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > th {
  border-bottom: 0;
}
.panel > .table-bordered > tbody > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > td,
.panel > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-bordered > tbody > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > th,
.panel > .table-bordered > tfoot > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > th {
  border-bottom: 0;
}
.panel > .table-responsive {
  border: 0;
  margin-bottom: 0;
}
.panel-group {
  margin-bottom: 18px;
}
.panel-group .panel {
  margin-bottom: 0;
  border-radius: 2px;
}
.panel-group .panel + .panel {
  margin-top: 5px;
}
.panel-group .panel-heading {
  border-bottom: 0;
}
.panel-group .panel-heading + .panel-collapse > .panel-body,
.panel-group .panel-heading + .panel-collapse > .list-group {
  border-top: 1px solid #ddd;
}
.panel-group .panel-footer {
  border-top: 0;
}
.panel-group .panel-footer + .panel-collapse .panel-body {
  border-bottom: 1px solid #ddd;
}
.panel-default {
  border-color: #ddd;
}
.panel-default > .panel-heading {
  color: #333333;
  background-color: #f5f5f5;
  border-color: #ddd;
}
.panel-default > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ddd;
}
.panel-default > .panel-heading .badge {
  color: #f5f5f5;
  background-color: #333333;
}
.panel-default > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ddd;
}
.panel-primary {
  border-color: #337ab7;
}
.panel-primary > .panel-heading {
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.panel-primary > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #337ab7;
}
.panel-primary > .panel-heading .badge {
  color: #337ab7;
  background-color: #fff;
}
.panel-primary > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #337ab7;
}
.panel-success {
  border-color: #d6e9c6;
}
.panel-success > .panel-heading {
  color: #3c763d;
  background-color: #dff0d8;
  border-color: #d6e9c6;
}
.panel-success > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #d6e9c6;
}
.panel-success > .panel-heading .badge {
  color: #dff0d8;
  background-color: #3c763d;
}
.panel-success > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #d6e9c6;
}
.panel-info {
  border-color: #bce8f1;
}
.panel-info > .panel-heading {
  color: #31708f;
  background-color: #d9edf7;
  border-color: #bce8f1;
}
.panel-info > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #bce8f1;
}
.panel-info > .panel-heading .badge {
  color: #d9edf7;
  background-color: #31708f;
}
.panel-info > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #bce8f1;
}
.panel-warning {
  border-color: #faebcc;
}
.panel-warning > .panel-heading {
  color: #8a6d3b;
  background-color: #fcf8e3;
  border-color: #faebcc;
}
.panel-warning > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #faebcc;
}
.panel-warning > .panel-heading .badge {
  color: #fcf8e3;
  background-color: #8a6d3b;
}
.panel-warning > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #faebcc;
}
.panel-danger {
  border-color: #ebccd1;
}
.panel-danger > .panel-heading {
  color: #a94442;
  background-color: #f2dede;
  border-color: #ebccd1;
}
.panel-danger > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ebccd1;
}
.panel-danger > .panel-heading .badge {
  color: #f2dede;
  background-color: #a94442;
}
.panel-danger > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ebccd1;
}
.embed-responsive {
  position: relative;
  display: block;
  height: 0;
  padding: 0;
  overflow: hidden;
}
.embed-responsive .embed-responsive-item,
.embed-responsive iframe,
.embed-responsive embed,
.embed-responsive object,
.embed-responsive video {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  height: 100%;
  width: 100%;
  border: 0;
}
.embed-responsive-16by9 {
  padding-bottom: 56.25%;
}
.embed-responsive-4by3 {
  padding-bottom: 75%;
}
.well {
  min-height: 20px;
  padding: 19px;
  margin-bottom: 20px;
  background-color: #f5f5f5;
  border: 1px solid #e3e3e3;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
}
.well blockquote {
  border-color: #ddd;
  border-color: rgba(0, 0, 0, 0.15);
}
.well-lg {
  padding: 24px;
  border-radius: 3px;
}
.well-sm {
  padding: 9px;
  border-radius: 1px;
}
.close {
  float: right;
  font-size: 19.5px;
  font-weight: bold;
  line-height: 1;
  color: #000;
  text-shadow: 0 1px 0 #fff;
  opacity: 0.2;
  filter: alpha(opacity=20);
}
.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
  opacity: 0.5;
  filter: alpha(opacity=50);
}
button.close {
  padding: 0;
  cursor: pointer;
  background: transparent;
  border: 0;
  -webkit-appearance: none;
}
.modal-open {
  overflow: hidden;
}
.modal {
  display: none;
  overflow: hidden;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1050;
  -webkit-overflow-scrolling: touch;
  outline: 0;
}
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, -25%);
  -ms-transform: translate(0, -25%);
  -o-transform: translate(0, -25%);
  transform: translate(0, -25%);
  -webkit-transition: -webkit-transform 0.3s ease-out;
  -moz-transition: -moz-transform 0.3s ease-out;
  -o-transition: -o-transform 0.3s ease-out;
  transition: transform 0.3s ease-out;
}
.modal.in .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
.modal-open .modal {
  overflow-x: hidden;
  overflow-y: auto;
}
.modal-dialog {
  position: relative;
  width: auto;
  margin: 10px;
}
.modal-content {
  position: relative;
  background-color: #fff;
  border: 1px solid #999;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  background-clip: padding-box;
  outline: 0;
}
.modal-backdrop {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1040;
  background-color: #000;
}
.modal-backdrop.fade {
  opacity: 0;
  filter: alpha(opacity=0);
}
.modal-backdrop.in {
  opacity: 0.5;
  filter: alpha(opacity=50);
}
.modal-header {
  padding: 15px;
  border-bottom: 1px solid #e5e5e5;
}
.modal-header .close {
  margin-top: -2px;
}
.modal-title {
  margin: 0;
  line-height: 1.42857143;
}
.modal-body {
  position: relative;
  padding: 15px;
}
.modal-footer {
  padding: 15px;
  text-align: right;
  border-top: 1px solid #e5e5e5;
}
.modal-footer .btn + .btn {
  margin-left: 5px;
  margin-bottom: 0;
}
.modal-footer .btn-group .btn + .btn {
  margin-left: -1px;
}
.modal-footer .btn-block + .btn-block {
  margin-left: 0;
}
.modal-scrollbar-measure {
  position: absolute;
  top: -9999px;
  width: 50px;
  height: 50px;
  overflow: scroll;
}
@media (min-width: 768px) {
  .modal-dialog {
    width: 600px;
    margin: 30px auto;
  }
  .modal-content {
    -webkit-box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
  }
  .modal-sm {
    width: 300px;
  }
}
@media (min-width: 992px) {
  .modal-lg {
    width: 900px;
  }
}
.tooltip {
  position: absolute;
  z-index: 1070;
  display: block;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 12px;
  opacity: 0;
  filter: alpha(opacity=0);
}
.tooltip.in {
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.tooltip.top {
  margin-top: -3px;
  padding: 5px 0;
}
.tooltip.right {
  margin-left: 3px;
  padding: 0 5px;
}
.tooltip.bottom {
  margin-top: 3px;
  padding: 5px 0;
}
.tooltip.left {
  margin-left: -3px;
  padding: 0 5px;
}
.tooltip-inner {
  max-width: 200px;
  padding: 3px 8px;
  color: #fff;
  text-align: center;
  background-color: #000;
  border-radius: 2px;
}
.tooltip-arrow {
  position: absolute;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.tooltip.top .tooltip-arrow {
  bottom: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-left .tooltip-arrow {
  bottom: 0;
  right: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-right .tooltip-arrow {
  bottom: 0;
  left: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.right .tooltip-arrow {
  top: 50%;
  left: 0;
  margin-top: -5px;
  border-width: 5px 5px 5px 0;
  border-right-color: #000;
}
.tooltip.left .tooltip-arrow {
  top: 50%;
  right: 0;
  margin-top: -5px;
  border-width: 5px 0 5px 5px;
  border-left-color: #000;
}
.tooltip.bottom .tooltip-arrow {
  top: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-left .tooltip-arrow {
  top: 0;
  right: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-right .tooltip-arrow {
  top: 0;
  left: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.popover {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1060;
  display: none;
  max-width: 276px;
  padding: 1px;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 13px;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}
.popover.top {
  margin-top: -10px;
}
.popover.right {
  margin-left: 10px;
}
.popover.bottom {
  margin-top: 10px;
}
.popover.left {
  margin-left: -10px;
}
.popover-title {
  margin: 0;
  padding: 8px 14px;
  font-size: 13px;
  background-color: #f7f7f7;
  border-bottom: 1px solid #ebebeb;
  border-radius: 2px 2px 0 0;
}
.popover-content {
  padding: 9px 14px;
}
.popover > .arrow,
.popover > .arrow:after {
  position: absolute;
  display: block;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.popover > .arrow {
  border-width: 11px;
}
.popover > .arrow:after {
  border-width: 10px;
  content: "";
}
.popover.top > .arrow {
  left: 50%;
  margin-left: -11px;
  border-bottom-width: 0;
  border-top-color: #999999;
  border-top-color: rgba(0, 0, 0, 0.25);
  bottom: -11px;
}
.popover.top > .arrow:after {
  content: " ";
  bottom: 1px;
  margin-left: -10px;
  border-bottom-width: 0;
  border-top-color: #fff;
}
.popover.right > .arrow {
  top: 50%;
  left: -11px;
  margin-top: -11px;
  border-left-width: 0;
  border-right-color: #999999;
  border-right-color: rgba(0, 0, 0, 0.25);
}
.popover.right > .arrow:after {
  content: " ";
  left: 1px;
  bottom: -10px;
  border-left-width: 0;
  border-right-color: #fff;
}
.popover.bottom > .arrow {
  left: 50%;
  margin-left: -11px;
  border-top-width: 0;
  border-bottom-color: #999999;
  border-bottom-color: rgba(0, 0, 0, 0.25);
  top: -11px;
}
.popover.bottom > .arrow:after {
  content: " ";
  top: 1px;
  margin-left: -10px;
  border-top-width: 0;
  border-bottom-color: #fff;
}
.popover.left > .arrow {
  top: 50%;
  right: -11px;
  margin-top: -11px;
  border-right-width: 0;
  border-left-color: #999999;
  border-left-color: rgba(0, 0, 0, 0.25);
}
.popover.left > .arrow:after {
  content: " ";
  right: 1px;
  border-right-width: 0;
  border-left-color: #fff;
  bottom: -10px;
}
.carousel {
  position: relative;
}
.carousel-inner {
  position: relative;
  overflow: hidden;
  width: 100%;
}
.carousel-inner > .item {
  display: none;
  position: relative;
  -webkit-transition: 0.6s ease-in-out left;
  -o-transition: 0.6s ease-in-out left;
  transition: 0.6s ease-in-out left;
}
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  line-height: 1;
}
@media all and (transform-3d), (-webkit-transform-3d) {
  .carousel-inner > .item {
    -webkit-transition: -webkit-transform 0.6s ease-in-out;
    -moz-transition: -moz-transform 0.6s ease-in-out;
    -o-transition: -o-transform 0.6s ease-in-out;
    transition: transform 0.6s ease-in-out;
    -webkit-backface-visibility: hidden;
    -moz-backface-visibility: hidden;
    backface-visibility: hidden;
    -webkit-perspective: 1000px;
    -moz-perspective: 1000px;
    perspective: 1000px;
  }
  .carousel-inner > .item.next,
  .carousel-inner > .item.active.right {
    -webkit-transform: translate3d(100%, 0, 0);
    transform: translate3d(100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.prev,
  .carousel-inner > .item.active.left {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.next.left,
  .carousel-inner > .item.prev.right,
  .carousel-inner > .item.active {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    left: 0;
  }
}
.carousel-inner > .active,
.carousel-inner > .next,
.carousel-inner > .prev {
  display: block;
}
.carousel-inner > .active {
  left: 0;
}
.carousel-inner > .next,
.carousel-inner > .prev {
  position: absolute;
  top: 0;
  width: 100%;
}
.carousel-inner > .next {
  left: 100%;
}
.carousel-inner > .prev {
  left: -100%;
}
.carousel-inner > .next.left,
.carousel-inner > .prev.right {
  left: 0;
}
.carousel-inner > .active.left {
  left: -100%;
}
.carousel-inner > .active.right {
  left: 100%;
}
.carousel-control {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  width: 15%;
  opacity: 0.5;
  filter: alpha(opacity=50);
  font-size: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
  background-color: rgba(0, 0, 0, 0);
}
.carousel-control.left {
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#80000000', endColorstr='#00000000', GradientType=1);
}
.carousel-control.right {
  left: auto;
  right: 0;
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#00000000', endColorstr='#80000000', GradientType=1);
}
.carousel-control:hover,
.carousel-control:focus {
  outline: 0;
  color: #fff;
  text-decoration: none;
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.carousel-control .icon-prev,
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-left,
.carousel-control .glyphicon-chevron-right {
  position: absolute;
  top: 50%;
  margin-top: -10px;
  z-index: 5;
  display: inline-block;
}
.carousel-control .icon-prev,
.carousel-control .glyphicon-chevron-left {
  left: 50%;
  margin-left: -10px;
}
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-right {
  right: 50%;
  margin-right: -10px;
}
.carousel-control .icon-prev,
.carousel-control .icon-next {
  width: 20px;
  height: 20px;
  line-height: 1;
  font-family: serif;
}
.carousel-control .icon-prev:before {
  content: '\2039';
}
.carousel-control .icon-next:before {
  content: '\203a';
}
.carousel-indicators {
  position: absolute;
  bottom: 10px;
  left: 50%;
  z-index: 15;
  width: 60%;
  margin-left: -30%;
  padding-left: 0;
  list-style: none;
  text-align: center;
}
.carousel-indicators li {
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 1px;
  text-indent: -999px;
  border: 1px solid #fff;
  border-radius: 10px;
  cursor: pointer;
  background-color: #000 \9;
  background-color: rgba(0, 0, 0, 0);
}
.carousel-indicators .active {
  margin: 0;
  width: 12px;
  height: 12px;
  background-color: #fff;
}
.carousel-caption {
  position: absolute;
  left: 15%;
  right: 15%;
  bottom: 20px;
  z-index: 10;
  padding-top: 20px;
  padding-bottom: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
}
.carousel-caption .btn {
  text-shadow: none;
}
@media screen and (min-width: 768px) {
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-prev,
  .carousel-control .icon-next {
    width: 30px;
    height: 30px;
    margin-top: -10px;
    font-size: 30px;
  }
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .icon-prev {
    margin-left: -10px;
  }
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-next {
    margin-right: -10px;
  }
  .carousel-caption {
    left: 20%;
    right: 20%;
    padding-bottom: 30px;
  }
  .carousel-indicators {
    bottom: 20px;
  }
}
.clearfix:before,
.clearfix:after,
.dl-horizontal dd:before,
.dl-horizontal dd:after,
.container:before,
.container:after,
.container-fluid:before,
.container-fluid:after,
.row:before,
.row:after,
.form-horizontal .form-group:before,
.form-horizontal .form-group:after,
.btn-toolbar:before,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:before,
.btn-group-vertical > .btn-group:after,
.nav:before,
.nav:after,
.navbar:before,
.navbar:after,
.navbar-header:before,
.navbar-header:after,
.navbar-collapse:before,
.navbar-collapse:after,
.pager:before,
.pager:after,
.panel-body:before,
.panel-body:after,
.modal-header:before,
.modal-header:after,
.modal-footer:before,
.modal-footer:after,
.item_buttons:before,
.item_buttons:after {
  content: " ";
  display: table;
}
.clearfix:after,
.dl-horizontal dd:after,
.container:after,
.container-fluid:after,
.row:after,
.form-horizontal .form-group:after,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:after,
.nav:after,
.navbar:after,
.navbar-header:after,
.navbar-collapse:after,
.pager:after,
.panel-body:after,
.modal-header:after,
.modal-footer:after,
.item_buttons:after {
  clear: both;
}
.center-block {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.pull-right {
  float: right !important;
}
.pull-left {
  float: left !important;
}
.hide {
  display: none !important;
}
.show {
  display: block !important;
}
.invisible {
  visibility: hidden;
}
.text-hide {
  font: 0/0 a;
  color: transparent;
  text-shadow: none;
  background-color: transparent;
  border: 0;
}
.hidden {
  display: none !important;
}
.affix {
  position: fixed;
}
@-ms-viewport {
  width: device-width;
}
.visible-xs,
.visible-sm,
.visible-md,
.visible-lg {
  display: none !important;
}
.visible-xs-block,
.visible-xs-inline,
.visible-xs-inline-block,
.visible-sm-block,
.visible-sm-inline,
.visible-sm-inline-block,
.visible-md-block,
.visible-md-inline,
.visible-md-inline-block,
.visible-lg-block,
.visible-lg-inline,
.visible-lg-inline-block {
  display: none !important;
}
@media (max-width: 767px) {
  .visible-xs {
    display: block !important;
  }
  table.visible-xs {
    display: table !important;
  }
  tr.visible-xs {
    display: table-row !important;
  }
  th.visible-xs,
  td.visible-xs {
    display: table-cell !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-block {
    display: block !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline {
    display: inline !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm {
    display: block !important;
  }
  table.visible-sm {
    display: table !important;
  }
  tr.visible-sm {
    display: table-row !important;
  }
  th.visible-sm,
  td.visible-sm {
    display: table-cell !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-block {
    display: block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline {
    display: inline !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md {
    display: block !important;
  }
  table.visible-md {
    display: table !important;
  }
  tr.visible-md {
    display: table-row !important;
  }
  th.visible-md,
  td.visible-md {
    display: table-cell !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-block {
    display: block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline {
    display: inline !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg {
    display: block !important;
  }
  table.visible-lg {
    display: table !important;
  }
  tr.visible-lg {
    display: table-row !important;
  }
  th.visible-lg,
  td.visible-lg {
    display: table-cell !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-block {
    display: block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline {
    display: inline !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline-block {
    display: inline-block !important;
  }
}
@media (max-width: 767px) {
  .hidden-xs {
    display: none !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .hidden-sm {
    display: none !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .hidden-md {
    display: none !important;
  }
}
@media (min-width: 1200px) {
  .hidden-lg {
    display: none !important;
  }
}
.visible-print {
  display: none !important;
}
@media print {
  .visible-print {
    display: block !important;
  }
  table.visible-print {
    display: table !important;
  }
  tr.visible-print {
    display: table-row !important;
  }
  th.visible-print,
  td.visible-print {
    display: table-cell !important;
  }
}
.visible-print-block {
  display: none !important;
}
@media print {
  .visible-print-block {
    display: block !important;
  }
}
.visible-print-inline {
  display: none !important;
}
@media print {
  .visible-print-inline {
    display: inline !important;
  }
}
.visible-print-inline-block {
  display: none !important;
}
@media print {
  .visible-print-inline-block {
    display: inline-block !important;
  }
}
@media print {
  .hidden-print {
    display: none !important;
  }
}
/*!
*
* Font Awesome
*
*/
/*!
 *  Font Awesome 4.2.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */
/* FONT PATH
 * -------------------------- */
@font-face {
  font-family: 'FontAwesome';
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.2.0');
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.2.0') format('embedded-opentype'), url('../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.2.0') format('woff'), url('../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.2.0') format('truetype'), url('../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.2.0#fontawesomeregular') format('svg');
  font-weight: normal;
  font-style: normal;
}
.fa {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
/* makes the font 33% larger relative to the icon container */
.fa-lg {
  font-size: 1.33333333em;
  line-height: 0.75em;
  vertical-align: -15%;
}
.fa-2x {
  font-size: 2em;
}
.fa-3x {
  font-size: 3em;
}
.fa-4x {
  font-size: 4em;
}
.fa-5x {
  font-size: 5em;
}
.fa-fw {
  width: 1.28571429em;
  text-align: center;
}
.fa-ul {
  padding-left: 0;
  margin-left: 2.14285714em;
  list-style-type: none;
}
.fa-ul > li {
  position: relative;
}
.fa-li {
  position: absolute;
  left: -2.14285714em;
  width: 2.14285714em;
  top: 0.14285714em;
  text-align: center;
}
.fa-li.fa-lg {
  left: -1.85714286em;
}
.fa-border {
  padding: .2em .25em .15em;
  border: solid 0.08em #eee;
  border-radius: .1em;
}
.pull-right {
  float: right;
}
.pull-left {
  float: left;
}
.fa.pull-left {
  margin-right: .3em;
}
.fa.pull-right {
  margin-left: .3em;
}
.fa-spin {
  -webkit-animation: fa-spin 2s infinite linear;
  animation: fa-spin 2s infinite linear;
}
@-webkit-keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
@keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
.fa-rotate-90 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=1);
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
}
.fa-rotate-180 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2);
  -webkit-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  transform: rotate(180deg);
}
.fa-rotate-270 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=3);
  -webkit-transform: rotate(270deg);
  -ms-transform: rotate(270deg);
  transform: rotate(270deg);
}
.fa-flip-horizontal {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1);
  -webkit-transform: scale(-1, 1);
  -ms-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
.fa-flip-vertical {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1);
  -webkit-transform: scale(1, -1);
  -ms-transform: scale(1, -1);
  transform: scale(1, -1);
}
:root .fa-rotate-90,
:root .fa-rotate-180,
:root .fa-rotate-270,
:root .fa-flip-horizontal,
:root .fa-flip-vertical {
  filter: none;
}
.fa-stack {
  position: relative;
  display: inline-block;
  width: 2em;
  height: 2em;
  line-height: 2em;
  vertical-align: middle;
}
.fa-stack-1x,
.fa-stack-2x {
  position: absolute;
  left: 0;
  width: 100%;
  text-align: center;
}
.fa-stack-1x {
  line-height: inherit;
}
.fa-stack-2x {
  font-size: 2em;
}
.fa-inverse {
  color: #fff;
}
/* Font Awesome uses the Unicode Private Use Area (PUA) to ensure screen
   readers do not read off random characters that represent icons */
.fa-glass:before {
  content: "\f000";
}
.fa-music:before {
  content: "\f001";
}
.fa-search:before {
  content: "\f002";
}
.fa-envelope-o:before {
  content: "\f003";
}
.fa-heart:before {
  content: "\f004";
}
.fa-star:before {
  content: "\f005";
}
.fa-star-o:before {
  content: "\f006";
}
.fa-user:before {
  content: "\f007";
}
.fa-film:before {
  content: "\f008";
}
.fa-th-large:before {
  content: "\f009";
}
.fa-th:before {
  content: "\f00a";
}
.fa-th-list:before {
  content: "\f00b";
}
.fa-check:before {
  content: "\f00c";
}
.fa-remove:before,
.fa-close:before,
.fa-times:before {
  content: "\f00d";
}
.fa-search-plus:before {
  content: "\f00e";
}
.fa-search-minus:before {
  content: "\f010";
}
.fa-power-off:before {
  content: "\f011";
}
.fa-signal:before {
  content: "\f012";
}
.fa-gear:before,
.fa-cog:before {
  content: "\f013";
}
.fa-trash-o:before {
  content: "\f014";
}
.fa-home:before {
  content: "\f015";
}
.fa-file-o:before {
  content: "\f016";
}
.fa-clock-o:before {
  content: "\f017";
}
.fa-road:before {
  content: "\f018";
}
.fa-download:before {
  content: "\f019";
}
.fa-arrow-circle-o-down:before {
  content: "\f01a";
}
.fa-arrow-circle-o-up:before {
  content: "\f01b";
}
.fa-inbox:before {
  content: "\f01c";
}
.fa-play-circle-o:before {
  content: "\f01d";
}
.fa-rotate-right:before,
.fa-repeat:before {
  content: "\f01e";
}
.fa-refresh:before {
  content: "\f021";
}
.fa-list-alt:before {
  content: "\f022";
}
.fa-lock:before {
  content: "\f023";
}
.fa-flag:before {
  content: "\f024";
}
.fa-headphones:before {
  content: "\f025";
}
.fa-volume-off:before {
  content: "\f026";
}
.fa-volume-down:before {
  content: "\f027";
}
.fa-volume-up:before {
  content: "\f028";
}
.fa-qrcode:before {
  content: "\f029";
}
.fa-barcode:before {
  content: "\f02a";
}
.fa-tag:before {
  content: "\f02b";
}
.fa-tags:before {
  content: "\f02c";
}
.fa-book:before {
  content: "\f02d";
}
.fa-bookmark:before {
  content: "\f02e";
}
.fa-print:before {
  content: "\f02f";
}
.fa-camera:before {
  content: "\f030";
}
.fa-font:before {
  content: "\f031";
}
.fa-bold:before {
  content: "\f032";
}
.fa-italic:before {
  content: "\f033";
}
.fa-text-height:before {
  content: "\f034";
}
.fa-text-width:before {
  content: "\f035";
}
.fa-align-left:before {
  content: "\f036";
}
.fa-align-center:before {
  content: "\f037";
}
.fa-align-right:before {
  content: "\f038";
}
.fa-align-justify:before {
  content: "\f039";
}
.fa-list:before {
  content: "\f03a";
}
.fa-dedent:before,
.fa-outdent:before {
  content: "\f03b";
}
.fa-indent:before {
  content: "\f03c";
}
.fa-video-camera:before {
  content: "\f03d";
}
.fa-photo:before,
.fa-image:before,
.fa-picture-o:before {
  content: "\f03e";
}
.fa-pencil:before {
  content: "\f040";
}
.fa-map-marker:before {
  content: "\f041";
}
.fa-adjust:before {
  content: "\f042";
}
.fa-tint:before {
  content: "\f043";
}
.fa-edit:before,
.fa-pencil-square-o:before {
  content: "\f044";
}
.fa-share-square-o:before {
  content: "\f045";
}
.fa-check-square-o:before {
  content: "\f046";
}
.fa-arrows:before {
  content: "\f047";
}
.fa-step-backward:before {
  content: "\f048";
}
.fa-fast-backward:before {
  content: "\f049";
}
.fa-backward:before {
  content: "\f04a";
}
.fa-play:before {
  content: "\f04b";
}
.fa-pause:before {
  content: "\f04c";
}
.fa-stop:before {
  content: "\f04d";
}
.fa-forward:before {
  content: "\f04e";
}
.fa-fast-forward:before {
  content: "\f050";
}
.fa-step-forward:before {
  content: "\f051";
}
.fa-eject:before {
  content: "\f052";
}
.fa-chevron-left:before {
  content: "\f053";
}
.fa-chevron-right:before {
  content: "\f054";
}
.fa-plus-circle:before {
  content: "\f055";
}
.fa-minus-circle:before {
  content: "\f056";
}
.fa-times-circle:before {
  content: "\f057";
}
.fa-check-circle:before {
  content: "\f058";
}
.fa-question-circle:before {
  content: "\f059";
}
.fa-info-circle:before {
  content: "\f05a";
}
.fa-crosshairs:before {
  content: "\f05b";
}
.fa-times-circle-o:before {
  content: "\f05c";
}
.fa-check-circle-o:before {
  content: "\f05d";
}
.fa-ban:before {
  content: "\f05e";
}
.fa-arrow-left:before {
  content: "\f060";
}
.fa-arrow-right:before {
  content: "\f061";
}
.fa-arrow-up:before {
  content: "\f062";
}
.fa-arrow-down:before {
  content: "\f063";
}
.fa-mail-forward:before,
.fa-share:before {
  content: "\f064";
}
.fa-expand:before {
  content: "\f065";
}
.fa-compress:before {
  content: "\f066";
}
.fa-plus:before {
  content: "\f067";
}
.fa-minus:before {
  content: "\f068";
}
.fa-asterisk:before {
  content: "\f069";
}
.fa-exclamation-circle:before {
  content: "\f06a";
}
.fa-gift:before {
  content: "\f06b";
}
.fa-leaf:before {
  content: "\f06c";
}
.fa-fire:before {
  content: "\f06d";
}
.fa-eye:before {
  content: "\f06e";
}
.fa-eye-slash:before {
  content: "\f070";
}
.fa-warning:before,
.fa-exclamation-triangle:before {
  content: "\f071";
}
.fa-plane:before {
  content: "\f072";
}
.fa-calendar:before {
  content: "\f073";
}
.fa-random:before {
  content: "\f074";
}
.fa-comment:before {
  content: "\f075";
}
.fa-magnet:before {
  content: "\f076";
}
.fa-chevron-up:before {
  content: "\f077";
}
.fa-chevron-down:before {
  content: "\f078";
}
.fa-retweet:before {
  content: "\f079";
}
.fa-shopping-cart:before {
  content: "\f07a";
}
.fa-folder:before {
  content: "\f07b";
}
.fa-folder-open:before {
  content: "\f07c";
}
.fa-arrows-v:before {
  content: "\f07d";
}
.fa-arrows-h:before {
  content: "\f07e";
}
.fa-bar-chart-o:before,
.fa-bar-chart:before {
  content: "\f080";
}
.fa-twitter-square:before {
  content: "\f081";
}
.fa-facebook-square:before {
  content: "\f082";
}
.fa-camera-retro:before {
  content: "\f083";
}
.fa-key:before {
  content: "\f084";
}
.fa-gears:before,
.fa-cogs:before {
  content: "\f085";
}
.fa-comments:before {
  content: "\f086";
}
.fa-thumbs-o-up:before {
  content: "\f087";
}
.fa-thumbs-o-down:before {
  content: "\f088";
}
.fa-star-half:before {
  content: "\f089";
}
.fa-heart-o:before {
  content: "\f08a";
}
.fa-sign-out:before {
  content: "\f08b";
}
.fa-linkedin-square:before {
  content: "\f08c";
}
.fa-thumb-tack:before {
  content: "\f08d";
}
.fa-external-link:before {
  content: "\f08e";
}
.fa-sign-in:before {
  content: "\f090";
}
.fa-trophy:before {
  content: "\f091";
}
.fa-github-square:before {
  content: "\f092";
}
.fa-upload:before {
  content: "\f093";
}
.fa-lemon-o:before {
  content: "\f094";
}
.fa-phone:before {
  content: "\f095";
}
.fa-square-o:before {
  content: "\f096";
}
.fa-bookmark-o:before {
  content: "\f097";
}
.fa-phone-square:before {
  content: "\f098";
}
.fa-twitter:before {
  content: "\f099";
}
.fa-facebook:before {
  content: "\f09a";
}
.fa-github:before {
  content: "\f09b";
}
.fa-unlock:before {
  content: "\f09c";
}
.fa-credit-card:before {
  content: "\f09d";
}
.fa-rss:before {
  content: "\f09e";
}
.fa-hdd-o:before {
  content: "\f0a0";
}
.fa-bullhorn:before {
  content: "\f0a1";
}
.fa-bell:before {
  content: "\f0f3";
}
.fa-certificate:before {
  content: "\f0a3";
}
.fa-hand-o-right:before {
  content: "\f0a4";
}
.fa-hand-o-left:before {
  content: "\f0a5";
}
.fa-hand-o-up:before {
  content: "\f0a6";
}
.fa-hand-o-down:before {
  content: "\f0a7";
}
.fa-arrow-circle-left:before {
  content: "\f0a8";
}
.fa-arrow-circle-right:before {
  content: "\f0a9";
}
.fa-arrow-circle-up:before {
  content: "\f0aa";
}
.fa-arrow-circle-down:before {
  content: "\f0ab";
}
.fa-globe:before {
  content: "\f0ac";
}
.fa-wrench:before {
  content: "\f0ad";
}
.fa-tasks:before {
  content: "\f0ae";
}
.fa-filter:before {
  content: "\f0b0";
}
.fa-briefcase:before {
  content: "\f0b1";
}
.fa-arrows-alt:before {
  content: "\f0b2";
}
.fa-group:before,
.fa-users:before {
  content: "\f0c0";
}
.fa-chain:before,
.fa-link:before {
  content: "\f0c1";
}
.fa-cloud:before {
  content: "\f0c2";
}
.fa-flask:before {
  content: "\f0c3";
}
.fa-cut:before,
.fa-scissors:before {
  content: "\f0c4";
}
.fa-copy:before,
.fa-files-o:before {
  content: "\f0c5";
}
.fa-paperclip:before {
  content: "\f0c6";
}
.fa-save:before,
.fa-floppy-o:before {
  content: "\f0c7";
}
.fa-square:before {
  content: "\f0c8";
}
.fa-navicon:before,
.fa-reorder:before,
.fa-bars:before {
  content: "\f0c9";
}
.fa-list-ul:before {
  content: "\f0ca";
}
.fa-list-ol:before {
  content: "\f0cb";
}
.fa-strikethrough:before {
  content: "\f0cc";
}
.fa-underline:before {
  content: "\f0cd";
}
.fa-table:before {
  content: "\f0ce";
}
.fa-magic:before {
  content: "\f0d0";
}
.fa-truck:before {
  content: "\f0d1";
}
.fa-pinterest:before {
  content: "\f0d2";
}
.fa-pinterest-square:before {
  content: "\f0d3";
}
.fa-google-plus-square:before {
  content: "\f0d4";
}
.fa-google-plus:before {
  content: "\f0d5";
}
.fa-money:before {
  content: "\f0d6";
}
.fa-caret-down:before {
  content: "\f0d7";
}
.fa-caret-up:before {
  content: "\f0d8";
}
.fa-caret-left:before {
  content: "\f0d9";
}
.fa-caret-right:before {
  content: "\f0da";
}
.fa-columns:before {
  content: "\f0db";
}
.fa-unsorted:before,
.fa-sort:before {
  content: "\f0dc";
}
.fa-sort-down:before,
.fa-sort-desc:before {
  content: "\f0dd";
}
.fa-sort-up:before,
.fa-sort-asc:before {
  content: "\f0de";
}
.fa-envelope:before {
  content: "\f0e0";
}
.fa-linkedin:before {
  content: "\f0e1";
}
.fa-rotate-left:before,
.fa-undo:before {
  content: "\f0e2";
}
.fa-legal:before,
.fa-gavel:before {
  content: "\f0e3";
}
.fa-dashboard:before,
.fa-tachometer:before {
  content: "\f0e4";
}
.fa-comment-o:before {
  content: "\f0e5";
}
.fa-comments-o:before {
  content: "\f0e6";
}
.fa-flash:before,
.fa-bolt:before {
  content: "\f0e7";
}
.fa-sitemap:before {
  content: "\f0e8";
}
.fa-umbrella:before {
  content: "\f0e9";
}
.fa-paste:before,
.fa-clipboard:before {
  content: "\f0ea";
}
.fa-lightbulb-o:before {
  content: "\f0eb";
}
.fa-exchange:before {
  content: "\f0ec";
}
.fa-cloud-download:before {
  content: "\f0ed";
}
.fa-cloud-upload:before {
  content: "\f0ee";
}
.fa-user-md:before {
  content: "\f0f0";
}
.fa-stethoscope:before {
  content: "\f0f1";
}
.fa-suitcase:before {
  content: "\f0f2";
}
.fa-bell-o:before {
  content: "\f0a2";
}
.fa-coffee:before {
  content: "\f0f4";
}
.fa-cutlery:before {
  content: "\f0f5";
}
.fa-file-text-o:before {
  content: "\f0f6";
}
.fa-building-o:before {
  content: "\f0f7";
}
.fa-hospital-o:before {
  content: "\f0f8";
}
.fa-ambulance:before {
  content: "\f0f9";
}
.fa-medkit:before {
  content: "\f0fa";
}
.fa-fighter-jet:before {
  content: "\f0fb";
}
.fa-beer:before {
  content: "\f0fc";
}
.fa-h-square:before {
  content: "\f0fd";
}
.fa-plus-square:before {
  content: "\f0fe";
}
.fa-angle-double-left:before {
  content: "\f100";
}
.fa-angle-double-right:before {
  content: "\f101";
}
.fa-angle-double-up:before {
  content: "\f102";
}
.fa-angle-double-down:before {
  content: "\f103";
}
.fa-angle-left:before {
  content: "\f104";
}
.fa-angle-right:before {
  content: "\f105";
}
.fa-angle-up:before {
  content: "\f106";
}
.fa-angle-down:before {
  content: "\f107";
}
.fa-desktop:before {
  content: "\f108";
}
.fa-laptop:before {
  content: "\f109";
}
.fa-tablet:before {
  content: "\f10a";
}
.fa-mobile-phone:before,
.fa-mobile:before {
  content: "\f10b";
}
.fa-circle-o:before {
  content: "\f10c";
}
.fa-quote-left:before {
  content: "\f10d";
}
.fa-quote-right:before {
  content: "\f10e";
}
.fa-spinner:before {
  content: "\f110";
}
.fa-circle:before {
  content: "\f111";
}
.fa-mail-reply:before,
.fa-reply:before {
  content: "\f112";
}
.fa-github-alt:before {
  content: "\f113";
}
.fa-folder-o:before {
  content: "\f114";
}
.fa-folder-open-o:before {
  content: "\f115";
}
.fa-smile-o:before {
  content: "\f118";
}
.fa-frown-o:before {
  content: "\f119";
}
.fa-meh-o:before {
  content: "\f11a";
}
.fa-gamepad:before {
  content: "\f11b";
}
.fa-keyboard-o:before {
  content: "\f11c";
}
.fa-flag-o:before {
  content: "\f11d";
}
.fa-flag-checkered:before {
  content: "\f11e";
}
.fa-terminal:before {
  content: "\f120";
}
.fa-code:before {
  content: "\f121";
}
.fa-mail-reply-all:before,
.fa-reply-all:before {
  content: "\f122";
}
.fa-star-half-empty:before,
.fa-star-half-full:before,
.fa-star-half-o:before {
  content: "\f123";
}
.fa-location-arrow:before {
  content: "\f124";
}
.fa-crop:before {
  content: "\f125";
}
.fa-code-fork:before {
  content: "\f126";
}
.fa-unlink:before,
.fa-chain-broken:before {
  content: "\f127";
}
.fa-question:before {
  content: "\f128";
}
.fa-info:before {
  content: "\f129";
}
.fa-exclamation:before {
  content: "\f12a";
}
.fa-superscript:before {
  content: "\f12b";
}
.fa-subscript:before {
  content: "\f12c";
}
.fa-eraser:before {
  content: "\f12d";
}
.fa-puzzle-piece:before {
  content: "\f12e";
}
.fa-microphone:before {
  content: "\f130";
}
.fa-microphone-slash:before {
  content: "\f131";
}
.fa-shield:before {
  content: "\f132";
}
.fa-calendar-o:before {
  content: "\f133";
}
.fa-fire-extinguisher:before {
  content: "\f134";
}
.fa-rocket:before {
  content: "\f135";
}
.fa-maxcdn:before {
  content: "\f136";
}
.fa-chevron-circle-left:before {
  content: "\f137";
}
.fa-chevron-circle-right:before {
  content: "\f138";
}
.fa-chevron-circle-up:before {
  content: "\f139";
}
.fa-chevron-circle-down:before {
  content: "\f13a";
}
.fa-html5:before {
  content: "\f13b";
}
.fa-css3:before {
  content: "\f13c";
}
.fa-anchor:before {
  content: "\f13d";
}
.fa-unlock-alt:before {
  content: "\f13e";
}
.fa-bullseye:before {
  content: "\f140";
}
.fa-ellipsis-h:before {
  content: "\f141";
}
.fa-ellipsis-v:before {
  content: "\f142";
}
.fa-rss-square:before {
  content: "\f143";
}
.fa-play-circle:before {
  content: "\f144";
}
.fa-ticket:before {
  content: "\f145";
}
.fa-minus-square:before {
  content: "\f146";
}
.fa-minus-square-o:before {
  content: "\f147";
}
.fa-level-up:before {
  content: "\f148";
}
.fa-level-down:before {
  content: "\f149";
}
.fa-check-square:before {
  content: "\f14a";
}
.fa-pencil-square:before {
  content: "\f14b";
}
.fa-external-link-square:before {
  content: "\f14c";
}
.fa-share-square:before {
  content: "\f14d";
}
.fa-compass:before {
  content: "\f14e";
}
.fa-toggle-down:before,
.fa-caret-square-o-down:before {
  content: "\f150";
}
.fa-toggle-up:before,
.fa-caret-square-o-up:before {
  content: "\f151";
}
.fa-toggle-right:before,
.fa-caret-square-o-right:before {
  content: "\f152";
}
.fa-euro:before,
.fa-eur:before {
  content: "\f153";
}
.fa-gbp:before {
  content: "\f154";
}
.fa-dollar:before,
.fa-usd:before {
  content: "\f155";
}
.fa-rupee:before,
.fa-inr:before {
  content: "\f156";
}
.fa-cny:before,
.fa-rmb:before,
.fa-yen:before,
.fa-jpy:before {
  content: "\f157";
}
.fa-ruble:before,
.fa-rouble:before,
.fa-rub:before {
  content: "\f158";
}
.fa-won:before,
.fa-krw:before {
  content: "\f159";
}
.fa-bitcoin:before,
.fa-btc:before {
  content: "\f15a";
}
.fa-file:before {
  content: "\f15b";
}
.fa-file-text:before {
  content: "\f15c";
}
.fa-sort-alpha-asc:before {
  content: "\f15d";
}
.fa-sort-alpha-desc:before {
  content: "\f15e";
}
.fa-sort-amount-asc:before {
  content: "\f160";
}
.fa-sort-amount-desc:before {
  content: "\f161";
}
.fa-sort-numeric-asc:before {
  content: "\f162";
}
.fa-sort-numeric-desc:before {
  content: "\f163";
}
.fa-thumbs-up:before {
  content: "\f164";
}
.fa-thumbs-down:before {
  content: "\f165";
}
.fa-youtube-square:before {
  content: "\f166";
}
.fa-youtube:before {
  content: "\f167";
}
.fa-xing:before {
  content: "\f168";
}
.fa-xing-square:before {
  content: "\f169";
}
.fa-youtube-play:before {
  content: "\f16a";
}
.fa-dropbox:before {
  content: "\f16b";
}
.fa-stack-overflow:before {
  content: "\f16c";
}
.fa-instagram:before {
  content: "\f16d";
}
.fa-flickr:before {
  content: "\f16e";
}
.fa-adn:before {
  content: "\f170";
}
.fa-bitbucket:before {
  content: "\f171";
}
.fa-bitbucket-square:before {
  content: "\f172";
}
.fa-tumblr:before {
  content: "\f173";
}
.fa-tumblr-square:before {
  content: "\f174";
}
.fa-long-arrow-down:before {
  content: "\f175";
}
.fa-long-arrow-up:before {
  content: "\f176";
}
.fa-long-arrow-left:before {
  content: "\f177";
}
.fa-long-arrow-right:before {
  content: "\f178";
}
.fa-apple:before {
  content: "\f179";
}
.fa-windows:before {
  content: "\f17a";
}
.fa-android:before {
  content: "\f17b";
}
.fa-linux:before {
  content: "\f17c";
}
.fa-dribbble:before {
  content: "\f17d";
}
.fa-skype:before {
  content: "\f17e";
}
.fa-foursquare:before {
  content: "\f180";
}
.fa-trello:before {
  content: "\f181";
}
.fa-female:before {
  content: "\f182";
}
.fa-male:before {
  content: "\f183";
}
.fa-gittip:before {
  content: "\f184";
}
.fa-sun-o:before {
  content: "\f185";
}
.fa-moon-o:before {
  content: "\f186";
}
.fa-archive:before {
  content: "\f187";
}
.fa-bug:before {
  content: "\f188";
}
.fa-vk:before {
  content: "\f189";
}
.fa-weibo:before {
  content: "\f18a";
}
.fa-renren:before {
  content: "\f18b";
}
.fa-pagelines:before {
  content: "\f18c";
}
.fa-stack-exchange:before {
  content: "\f18d";
}
.fa-arrow-circle-o-right:before {
  content: "\f18e";
}
.fa-arrow-circle-o-left:before {
  content: "\f190";
}
.fa-toggle-left:before,
.fa-caret-square-o-left:before {
  content: "\f191";
}
.fa-dot-circle-o:before {
  content: "\f192";
}
.fa-wheelchair:before {
  content: "\f193";
}
.fa-vimeo-square:before {
  content: "\f194";
}
.fa-turkish-lira:before,
.fa-try:before {
  content: "\f195";
}
.fa-plus-square-o:before {
  content: "\f196";
}
.fa-space-shuttle:before {
  content: "\f197";
}
.fa-slack:before {
  content: "\f198";
}
.fa-envelope-square:before {
  content: "\f199";
}
.fa-wordpress:before {
  content: "\f19a";
}
.fa-openid:before {
  content: "\f19b";
}
.fa-institution:before,
.fa-bank:before,
.fa-university:before {
  content: "\f19c";
}
.fa-mortar-board:before,
.fa-graduation-cap:before {
  content: "\f19d";
}
.fa-yahoo:before {
  content: "\f19e";
}
.fa-google:before {
  content: "\f1a0";
}
.fa-reddit:before {
  content: "\f1a1";
}
.fa-reddit-square:before {
  content: "\f1a2";
}
.fa-stumbleupon-circle:before {
  content: "\f1a3";
}
.fa-stumbleupon:before {
  content: "\f1a4";
}
.fa-delicious:before {
  content: "\f1a5";
}
.fa-digg:before {
  content: "\f1a6";
}
.fa-pied-piper:before {
  content: "\f1a7";
}
.fa-pied-piper-alt:before {
  content: "\f1a8";
}
.fa-drupal:before {
  content: "\f1a9";
}
.fa-joomla:before {
  content: "\f1aa";
}
.fa-language:before {
  content: "\f1ab";
}
.fa-fax:before {
  content: "\f1ac";
}
.fa-building:before {
  content: "\f1ad";
}
.fa-child:before {
  content: "\f1ae";
}
.fa-paw:before {
  content: "\f1b0";
}
.fa-spoon:before {
  content: "\f1b1";
}
.fa-cube:before {
  content: "\f1b2";
}
.fa-cubes:before {
  content: "\f1b3";
}
.fa-behance:before {
  content: "\f1b4";
}
.fa-behance-square:before {
  content: "\f1b5";
}
.fa-steam:before {
  content: "\f1b6";
}
.fa-steam-square:before {
  content: "\f1b7";
}
.fa-recycle:before {
  content: "\f1b8";
}
.fa-automobile:before,
.fa-car:before {
  content: "\f1b9";
}
.fa-cab:before,
.fa-taxi:before {
  content: "\f1ba";
}
.fa-tree:before {
  content: "\f1bb";
}
.fa-spotify:before {
  content: "\f1bc";
}
.fa-deviantart:before {
  content: "\f1bd";
}
.fa-soundcloud:before {
  content: "\f1be";
}
.fa-database:before {
  content: "\f1c0";
}
.fa-file-pdf-o:before {
  content: "\f1c1";
}
.fa-file-word-o:before {
  content: "\f1c2";
}
.fa-file-excel-o:before {
  content: "\f1c3";
}
.fa-file-powerpoint-o:before {
  content: "\f1c4";
}
.fa-file-photo-o:before,
.fa-file-picture-o:before,
.fa-file-image-o:before {
  content: "\f1c5";
}
.fa-file-zip-o:before,
.fa-file-archive-o:before {
  content: "\f1c6";
}
.fa-file-sound-o:before,
.fa-file-audio-o:before {
  content: "\f1c7";
}
.fa-file-movie-o:before,
.fa-file-video-o:before {
  content: "\f1c8";
}
.fa-file-code-o:before {
  content: "\f1c9";
}
.fa-vine:before {
  content: "\f1ca";
}
.fa-codepen:before {
  content: "\f1cb";
}
.fa-jsfiddle:before {
  content: "\f1cc";
}
.fa-life-bouy:before,
.fa-life-buoy:before,
.fa-life-saver:before,
.fa-support:before,
.fa-life-ring:before {
  content: "\f1cd";
}
.fa-circle-o-notch:before {
  content: "\f1ce";
}
.fa-ra:before,
.fa-rebel:before {
  content: "\f1d0";
}
.fa-ge:before,
.fa-empire:before {
  content: "\f1d1";
}
.fa-git-square:before {
  content: "\f1d2";
}
.fa-git:before {
  content: "\f1d3";
}
.fa-hacker-news:before {
  content: "\f1d4";
}
.fa-tencent-weibo:before {
  content: "\f1d5";
}
.fa-qq:before {
  content: "\f1d6";
}
.fa-wechat:before,
.fa-weixin:before {
  content: "\f1d7";
}
.fa-send:before,
.fa-paper-plane:before {
  content: "\f1d8";
}
.fa-send-o:before,
.fa-paper-plane-o:before {
  content: "\f1d9";
}
.fa-history:before {
  content: "\f1da";
}
.fa-circle-thin:before {
  content: "\f1db";
}
.fa-header:before {
  content: "\f1dc";
}
.fa-paragraph:before {
  content: "\f1dd";
}
.fa-sliders:before {
  content: "\f1de";
}
.fa-share-alt:before {
  content: "\f1e0";
}
.fa-share-alt-square:before {
  content: "\f1e1";
}
.fa-bomb:before {
  content: "\f1e2";
}
.fa-soccer-ball-o:before,
.fa-futbol-o:before {
  content: "\f1e3";
}
.fa-tty:before {
  content: "\f1e4";
}
.fa-binoculars:before {
  content: "\f1e5";
}
.fa-plug:before {
  content: "\f1e6";
}
.fa-slideshare:before {
  content: "\f1e7";
}
.fa-twitch:before {
  content: "\f1e8";
}
.fa-yelp:before {
  content: "\f1e9";
}
.fa-newspaper-o:before {
  content: "\f1ea";
}
.fa-wifi:before {
  content: "\f1eb";
}
.fa-calculator:before {
  content: "\f1ec";
}
.fa-paypal:before {
  content: "\f1ed";
}
.fa-google-wallet:before {
  content: "\f1ee";
}
.fa-cc-visa:before {
  content: "\f1f0";
}
.fa-cc-mastercard:before {
  content: "\f1f1";
}
.fa-cc-discover:before {
  content: "\f1f2";
}
.fa-cc-amex:before {
  content: "\f1f3";
}
.fa-cc-paypal:before {
  content: "\f1f4";
}
.fa-cc-stripe:before {
  content: "\f1f5";
}
.fa-bell-slash:before {
  content: "\f1f6";
}
.fa-bell-slash-o:before {
  content: "\f1f7";
}
.fa-trash:before {
  content: "\f1f8";
}
.fa-copyright:before {
  content: "\f1f9";
}
.fa-at:before {
  content: "\f1fa";
}
.fa-eyedropper:before {
  content: "\f1fb";
}
.fa-paint-brush:before {
  content: "\f1fc";
}
.fa-birthday-cake:before {
  content: "\f1fd";
}
.fa-area-chart:before {
  content: "\f1fe";
}
.fa-pie-chart:before {
  content: "\f200";
}
.fa-line-chart:before {
  content: "\f201";
}
.fa-lastfm:before {
  content: "\f202";
}
.fa-lastfm-square:before {
  content: "\f203";
}
.fa-toggle-off:before {
  content: "\f204";
}
.fa-toggle-on:before {
  content: "\f205";
}
.fa-bicycle:before {
  content: "\f206";
}
.fa-bus:before {
  content: "\f207";
}
.fa-ioxhost:before {
  content: "\f208";
}
.fa-angellist:before {
  content: "\f209";
}
.fa-cc:before {
  content: "\f20a";
}
.fa-shekel:before,
.fa-sheqel:before,
.fa-ils:before {
  content: "\f20b";
}
.fa-meanpath:before {
  content: "\f20c";
}
/*!
*
* IPython base
*
*/
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
code {
  color: #000;
}
pre {
  font-size: inherit;
  line-height: inherit;
}
label {
  font-weight: normal;
}
/* Make the page background atleast 100% the height of the view port */
/* Make the page itself atleast 70% the height of the view port */
.border-box-sizing {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.corner-all {
  border-radius: 2px;
}
.no-padding {
  padding: 0px;
}
/* Flexible box model classes */
/* Taken from Alex Russell http://infrequently.org/2009/08/css-3-progress/ */
/* This file is a compatability layer.  It allows the usage of flexible box 
model layouts accross multiple browsers, including older browsers.  The newest,
universal implementation of the flexible box model is used when available (see
`Modern browsers` comments below).  Browsers that are known to implement this 
new spec completely include:
    Firefox 28.0+
    Chrome 29.0+
    Internet Explorer 11+ 
    Opera 17.0+
Browsers not listed, including Safari, are supported via the styling under the
`Old browsers` comments below.
*/
.hbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
.hbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.vbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
.vbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.hbox.reverse,
.vbox.reverse,
.reverse {
  /* Old browsers */
  -webkit-box-direction: reverse;
  -moz-box-direction: reverse;
  box-direction: reverse;
  /* Modern browsers */
  flex-direction: row-reverse;
}
.hbox.box-flex0,
.vbox.box-flex0,
.box-flex0 {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
  width: auto;
}
.hbox.box-flex1,
.vbox.box-flex1,
.box-flex1 {
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex,
.vbox.box-flex,
.box-flex {
  /* Old browsers */
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex2,
.vbox.box-flex2,
.box-flex2 {
  /* Old browsers */
  -webkit-box-flex: 2;
  -moz-box-flex: 2;
  box-flex: 2;
  /* Modern browsers */
  flex: 2;
}
.box-group1 {
  /*  Deprecated */
  -webkit-box-flex-group: 1;
  -moz-box-flex-group: 1;
  box-flex-group: 1;
}
.box-group2 {
  /* Deprecated */
  -webkit-box-flex-group: 2;
  -moz-box-flex-group: 2;
  box-flex-group: 2;
}
.hbox.start,
.vbox.start,
.start {
  /* Old browsers */
  -webkit-box-pack: start;
  -moz-box-pack: start;
  box-pack: start;
  /* Modern browsers */
  justify-content: flex-start;
}
.hbox.end,
.vbox.end,
.end {
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
}
.hbox.center,
.vbox.center,
.center {
  /* Old browsers */
  -webkit-box-pack: center;
  -moz-box-pack: center;
  box-pack: center;
  /* Modern browsers */
  justify-content: center;
}
.hbox.baseline,
.vbox.baseline,
.baseline {
  /* Old browsers */
  -webkit-box-pack: baseline;
  -moz-box-pack: baseline;
  box-pack: baseline;
  /* Modern browsers */
  justify-content: baseline;
}
.hbox.stretch,
.vbox.stretch,
.stretch {
  /* Old browsers */
  -webkit-box-pack: stretch;
  -moz-box-pack: stretch;
  box-pack: stretch;
  /* Modern browsers */
  justify-content: stretch;
}
.hbox.align-start,
.vbox.align-start,
.align-start {
  /* Old browsers */
  -webkit-box-align: start;
  -moz-box-align: start;
  box-align: start;
  /* Modern browsers */
  align-items: flex-start;
}
.hbox.align-end,
.vbox.align-end,
.align-end {
  /* Old browsers */
  -webkit-box-align: end;
  -moz-box-align: end;
  box-align: end;
  /* Modern browsers */
  align-items: flex-end;
}
.hbox.align-center,
.vbox.align-center,
.align-center {
  /* Old browsers */
  -webkit-box-align: center;
  -moz-box-align: center;
  box-align: center;
  /* Modern browsers */
  align-items: center;
}
.hbox.align-baseline,
.vbox.align-baseline,
.align-baseline {
  /* Old browsers */
  -webkit-box-align: baseline;
  -moz-box-align: baseline;
  box-align: baseline;
  /* Modern browsers */
  align-items: baseline;
}
.hbox.align-stretch,
.vbox.align-stretch,
.align-stretch {
  /* Old browsers */
  -webkit-box-align: stretch;
  -moz-box-align: stretch;
  box-align: stretch;
  /* Modern browsers */
  align-items: stretch;
}
div.error {
  margin: 2em;
  text-align: center;
}
div.error > h1 {
  font-size: 500%;
  line-height: normal;
}
div.error > p {
  font-size: 200%;
  line-height: normal;
}
div.traceback-wrapper {
  text-align: left;
  max-width: 800px;
  margin: auto;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
body {
  background-color: #fff;
  /* This makes sure that the body covers the entire window and needs to
       be in a different element than the display: box in wrapper below */
  position: absolute;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  overflow: visible;
}
body > #header {
  /* Initially hidden to prevent FLOUC */
  display: none;
  background-color: #fff;
  /* Display over codemirror */
  position: relative;
  z-index: 100;
}
body > #header #header-container {
  padding-bottom: 5px;
  padding-top: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
body > #header .header-bar {
  width: 100%;
  height: 1px;
  background: #e7e7e7;
  margin-bottom: -1px;
}
@media print {
  body > #header {
    display: none !important;
  }
}
#header-spacer {
  width: 100%;
  visibility: hidden;
}
@media print {
  #header-spacer {
    display: none;
  }
}
#ipython_notebook {
  padding-left: 0px;
  padding-top: 1px;
  padding-bottom: 1px;
}
@media (max-width: 991px) {
  #ipython_notebook {
    margin-left: 10px;
  }
}
[dir="rtl"] #ipython_notebook {
  float: right !important;
}
#noscript {
  width: auto;
  padding-top: 16px;
  padding-bottom: 16px;
  text-align: center;
  font-size: 22px;
  color: red;
  font-weight: bold;
}
#ipython_notebook img {
  height: 28px;
}
#site {
  width: 100%;
  display: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  overflow: auto;
}
@media print {
  #site {
    height: auto !important;
  }
}
/* Smaller buttons */
.ui-button .ui-button-text {
  padding: 0.2em 0.8em;
  font-size: 77%;
}
input.ui-button {
  padding: 0.3em 0.9em;
}
span#login_widget {
  float: right;
}
span#login_widget > .button,
#logout {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button:focus,
#logout:focus,
span#login_widget > .button.focus,
#logout.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
span#login_widget > .button:hover,
#logout:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active:hover,
#logout:active:hover,
span#login_widget > .button.active:hover,
#logout.active:hover,
.open > .dropdown-togglespan#login_widget > .button:hover,
.open > .dropdown-toggle#logout:hover,
span#login_widget > .button:active:focus,
#logout:active:focus,
span#login_widget > .button.active:focus,
#logout.active:focus,
.open > .dropdown-togglespan#login_widget > .button:focus,
.open > .dropdown-toggle#logout:focus,
span#login_widget > .button:active.focus,
#logout:active.focus,
span#login_widget > .button.active.focus,
#logout.active.focus,
.open > .dropdown-togglespan#login_widget > .button.focus,
.open > .dropdown-toggle#logout.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  background-image: none;
}
span#login_widget > .button.disabled:hover,
#logout.disabled:hover,
span#login_widget > .button[disabled]:hover,
#logout[disabled]:hover,
fieldset[disabled] span#login_widget > .button:hover,
fieldset[disabled] #logout:hover,
span#login_widget > .button.disabled:focus,
#logout.disabled:focus,
span#login_widget > .button[disabled]:focus,
#logout[disabled]:focus,
fieldset[disabled] span#login_widget > .button:focus,
fieldset[disabled] #logout:focus,
span#login_widget > .button.disabled.focus,
#logout.disabled.focus,
span#login_widget > .button[disabled].focus,
#logout[disabled].focus,
fieldset[disabled] span#login_widget > .button.focus,
fieldset[disabled] #logout.focus {
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button .badge,
#logout .badge {
  color: #fff;
  background-color: #333;
}
.nav-header {
  text-transform: none;
}
#header > span {
  margin-top: 10px;
}
.modal_stretch .modal-dialog {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  min-height: 80vh;
}
.modal_stretch .modal-dialog .modal-body {
  max-height: calc(100vh - 200px);
  overflow: auto;
  flex: 1;
}
@media (min-width: 768px) {
  .modal .modal-dialog {
    width: 700px;
  }
}
@media (min-width: 768px) {
  select.form-control {
    margin-left: 12px;
    margin-right: 12px;
  }
}
/*!
*
* IPython auth
*
*/
.center-nav {
  display: inline-block;
  margin-bottom: -4px;
}
/*!
*
* IPython tree view
*
*/
/* We need an invisible input field on top of the sentense*/
/* "Drag file onto the list ..." */
.alternate_upload {
  background-color: none;
  display: inline;
}
.alternate_upload.form {
  padding: 0;
  margin: 0;
}
.alternate_upload input.fileinput {
  text-align: center;
  vertical-align: middle;
  display: inline;
  opacity: 0;
  z-index: 2;
  width: 12ex;
  margin-right: -12ex;
}
.alternate_upload .btn-upload {
  height: 22px;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
[dir="rtl"] #tabs li {
  float: right;
}
ul#tabs {
  margin-bottom: 4px;
}
[dir="rtl"] ul#tabs {
  margin-right: 0px;
}
ul#tabs a {
  padding-top: 6px;
  padding-bottom: 4px;
}
ul.breadcrumb a:focus,
ul.breadcrumb a:hover {
  text-decoration: none;
}
ul.breadcrumb i.icon-home {
  font-size: 16px;
  margin-right: 4px;
}
ul.breadcrumb span {
  color: #5e5e5e;
}
.list_toolbar {
  padding: 4px 0 4px 0;
  vertical-align: middle;
}
.list_toolbar .tree-buttons {
  padding-top: 1px;
}
[dir="rtl"] .list_toolbar .tree-buttons {
  float: left !important;
}
[dir="rtl"] .list_toolbar .pull-right {
  padding-top: 1px;
  float: left !important;
}
[dir="rtl"] .list_toolbar .pull-left {
  float: right !important;
}
.dynamic-buttons {
  padding-top: 3px;
  display: inline-block;
}
.list_toolbar [class*="span"] {
  min-height: 24px;
}
.list_header {
  font-weight: bold;
  background-color: #EEE;
}
.list_placeholder {
  font-weight: bold;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
}
.list_container {
  margin-top: 4px;
  margin-bottom: 20px;
  border: 1px solid #ddd;
  border-radius: 2px;
}
.list_container > div {
  border-bottom: 1px solid #ddd;
}
.list_container > div:hover .list-item {
  background-color: red;
}
.list_container > div:last-child {
  border: none;
}
.list_item:hover .list_item {
  background-color: #ddd;
}
.list_item a {
  text-decoration: none;
}
.list_item:hover {
  background-color: #fafafa;
}
.list_header > div,
.list_item > div {
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
.list_header > div input,
.list_item > div input {
  margin-right: 7px;
  margin-left: 14px;
  vertical-align: baseline;
  line-height: 22px;
  position: relative;
  top: -1px;
}
.list_header > div .item_link,
.list_item > div .item_link {
  margin-left: -1px;
  vertical-align: baseline;
  line-height: 22px;
}
.new-file input[type=checkbox] {
  visibility: hidden;
}
.item_name {
  line-height: 22px;
  height: 24px;
}
.item_icon {
  font-size: 14px;
  color: #5e5e5e;
  margin-right: 7px;
  margin-left: 7px;
  line-height: 22px;
  vertical-align: baseline;
}
.item_buttons {
  line-height: 1em;
  margin-left: -5px;
}
.item_buttons .btn,
.item_buttons .btn-group,
.item_buttons .input-group {
  float: left;
}
.item_buttons > .btn,
.item_buttons > .btn-group,
.item_buttons > .input-group {
  margin-left: 5px;
}
.item_buttons .btn {
  min-width: 13ex;
}
.item_buttons .running-indicator {
  padding-top: 4px;
  color: #5cb85c;
}
.item_buttons .kernel-name {
  padding-top: 4px;
  color: #5bc0de;
  margin-right: 7px;
  float: left;
}
.toolbar_info {
  height: 24px;
  line-height: 24px;
}
.list_item input:not([type=checkbox]) {
  padding-top: 3px;
  padding-bottom: 3px;
  height: 22px;
  line-height: 14px;
  margin: 0px;
}
.highlight_text {
  color: blue;
}
#project_name {
  display: inline-block;
  padding-left: 7px;
  margin-left: -2px;
}
#project_name > .breadcrumb {
  padding: 0px;
  margin-bottom: 0px;
  background-color: transparent;
  font-weight: bold;
}
#tree-selector {
  padding-right: 0px;
}
[dir="rtl"] #tree-selector a {
  float: right;
}
#button-select-all {
  min-width: 50px;
}
#select-all {
  margin-left: 7px;
  margin-right: 2px;
}
.menu_icon {
  margin-right: 2px;
}
.tab-content .row {
  margin-left: 0px;
  margin-right: 0px;
}
.folder_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f114";
}
.folder_icon:before.pull-left {
  margin-right: .3em;
}
.folder_icon:before.pull-right {
  margin-left: .3em;
}
.notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
}
.notebook_icon:before.pull-left {
  margin-right: .3em;
}
.notebook_icon:before.pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
  color: #5cb85c;
}
.running_notebook_icon:before.pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.pull-right {
  margin-left: .3em;
}
.file_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f016";
  position: relative;
  top: -2px;
}
.file_icon:before.pull-left {
  margin-right: .3em;
}
.file_icon:before.pull-right {
  margin-left: .3em;
}
#notebook_toolbar .pull-right {
  padding-top: 0px;
  margin-right: -1px;
}
ul#new-menu {
  left: auto;
  right: 0;
}
[dir="rtl"] #new-menu {
  text-align: right;
}
.kernel-menu-icon {
  padding-right: 12px;
  width: 24px;
  content: "\f096";
}
.kernel-menu-icon:before {
  content: "\f096";
}
.kernel-menu-icon-current:before {
  content: "\f00c";
}
#tab_content {
  padding-top: 20px;
}
#running .panel-group .panel {
  margin-top: 3px;
  margin-bottom: 1em;
}
#running .panel-group .panel .panel-heading {
  background-color: #EEE;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
#running .panel-group .panel .panel-heading a:focus,
#running .panel-group .panel .panel-heading a:hover {
  text-decoration: none;
}
#running .panel-group .panel .panel-body {
  padding: 0px;
}
#running .panel-group .panel .panel-body .list_container {
  margin-top: 0px;
  margin-bottom: 0px;
  border: 0px;
  border-radius: 0px;
}
#running .panel-group .panel .panel-body .list_container .list_item {
  border-bottom: 1px solid #ddd;
}
#running .panel-group .panel .panel-body .list_container .list_item:last-child {
  border-bottom: 0px;
}
[dir="rtl"] #running .col-sm-8 {
  float: right !important;
}
.delete-button {
  display: none;
}
.duplicate-button {
  display: none;
}
.rename-button {
  display: none;
}
.shutdown-button {
  display: none;
}
.dynamic-instructions {
  display: inline-block;
  padding-top: 4px;
}
/*!
*
* IPython text editor webapp
*
*/
.selected-keymap i.fa {
  padding: 0px 5px;
}
.selected-keymap i.fa:before {
  content: "\f00c";
}
#mode-menu {
  overflow: auto;
  max-height: 20em;
}
.edit_app #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.edit_app #menubar .navbar {
  /* Use a negative 1 bottom margin, so the border overlaps the border of the
    header */
  margin-bottom: -1px;
}
.dirty-indicator {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator.pull-left {
  margin-right: .3em;
}
.dirty-indicator.pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-dirty.pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-clean.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f00c";
}
.dirty-indicator-clean:before.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.pull-right {
  margin-left: .3em;
}
#filename {
  font-size: 16pt;
  display: table;
  padding: 0px 5px;
}
#current-mode {
  padding-left: 5px;
  padding-right: 5px;
}
#texteditor-backdrop {
  padding-top: 20px;
  padding-bottom: 20px;
}
@media not print {
  #texteditor-backdrop {
    background-color: #EEE;
  }
}
@media print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container {
    padding: 0px;
    background-color: #fff;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI colors. */
.ansibold {
  font-weight: bold;
}
/* use dark versions for foreground, to improve visibility */
.ansiblack {
  color: black;
}
.ansired {
  color: darkred;
}
.ansigreen {
  color: darkgreen;
}
.ansiyellow {
  color: #c4a000;
}
.ansiblue {
  color: darkblue;
}
.ansipurple {
  color: darkviolet;
}
.ansicyan {
  color: steelblue;
}
.ansigray {
  color: gray;
}
/* and light for background, for the same reason */
.ansibgblack {
  background-color: black;
}
.ansibgred {
  background-color: red;
}
.ansibggreen {
  background-color: green;
}
.ansibgyellow {
  background-color: yellow;
}
.ansibgblue {
  background-color: blue;
}
.ansibgpurple {
  background-color: magenta;
}
.ansibgcyan {
  background-color: cyan;
}
.ansibggray {
  background-color: gray;
}
div.cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-radius: 2px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  border-width: 1px;
  border-style: solid;
  border-color: transparent;
  width: 100%;
  padding: 5px;
  /* This acts as a spacer between cells, that is outside the border */
  margin: 0px;
  outline: none;
  border-left-width: 1px;
  padding-left: 5px;
  background: linear-gradient(to right, transparent -40px, transparent 1px, transparent 1px, transparent 100%);
}
div.cell.jupyter-soft-selected {
  border-left-color: #90CAF9;
  border-left-color: #E3F2FD;
  border-left-width: 1px;
  padding-left: 5px;
  border-right-color: #E3F2FD;
  border-right-width: 1px;
  background: #E3F2FD;
}
@media print {
  div.cell.jupyter-soft-selected {
    border-color: transparent;
  }
}
div.cell.selected {
  border-color: #ababab;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 5px, transparent 5px, transparent 100%);
}
@media print {
  div.cell.selected {
    border-color: transparent;
  }
}
div.cell.selected.jupyter-soft-selected {
  border-left-width: 0;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 7px, #E3F2FD 7px, #E3F2FD 100%);
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #66BB6A -40px, #66BB6A 5px, transparent 5px, transparent 100%);
}
@media print {
  .edit_mode div.cell.selected {
    border-color: transparent;
  }
}
.prompt {
  /* This needs to be wide enough for 3 digit prompt numbers: In[100]: */
  min-width: 14ex;
  /* This padding is tuned to match the padding on the CodeMirror editor. */
  padding: 0.4em;
  margin: 0px;
  font-family: monospace;
  text-align: right;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
  /* Don't highlight prompt number selection */
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  /* Use default cursor */
  cursor: default;
}
@media (max-width: 540px) {
  .prompt {
    text-align: left;
  }
}
div.inner_cell {
  min-width: 0;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_area {
  border: 1px solid #cfcfcf;
  border-radius: 2px;
  background: #f7f7f7;
  line-height: 1.21429em;
}
/* This is needed so that empty prompt areas can collapse to zero height when there
   is no content in the output_subarea and the prompt. The main purpose of this is
   to make sure that empty JavaScript output_subareas have no height. */
div.prompt:empty {
  padding-top: 0;
  padding-bottom: 0;
}
div.unrecognized_cell {
  padding: 5px 5px 5px 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.unrecognized_cell .inner_cell {
  border-radius: 2px;
  padding: 5px;
  font-weight: bold;
  color: red;
  border: 1px solid #cfcfcf;
  background: #eaeaea;
}
div.unrecognized_cell .inner_cell a {
  color: inherit;
  text-decoration: none;
}
div.unrecognized_cell .inner_cell a:hover {
  color: inherit;
  text-decoration: none;
}
@media (max-width: 540px) {
  div.unrecognized_cell > div.prompt {
    display: none;
  }
}
div.code_cell {
  /* avoid page breaking on code cells when printing */
}
@media print {
  div.code_cell {
    page-break-inside: avoid;
  }
}
/* any special styling for code cells that are currently running goes here */
div.input {
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.input {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_prompt {
  color: #303F9F;
  border-top: 1px solid transparent;
}
div.input_area > div.highlight {
  margin: 0.4em;
  border: none;
  padding: 0px;
  background-color: transparent;
}
div.input_area > div.highlight > pre {
  margin: 0px;
  border: none;
  padding: 0px;
  background-color: transparent;
}
/* The following gets added to the <head> if it is detected that the user has a
 * monospace font with inconsistent normal/bold/italic height.  See
 * notebookmain.js.  Such fonts will have keywords vertically offset with
 * respect to the rest of the text.  The user should select a better font.
 * See: https://github.com/ipython/ipython/issues/1503
 *
 * .CodeMirror span {
 *      vertical-align: bottom;
 * }
 */
.CodeMirror {
  line-height: 1.21429em;
  /* Changed from 1em to our global default */
  font-size: 14px;
  height: auto;
  /* Changed to auto to autogrow */
  background: none;
  /* Changed from white to allow our bg to show through */
}
.CodeMirror-scroll {
  /*  The CodeMirror docs are a bit fuzzy on if overflow-y should be hidden or visible.*/
  /*  We have found that if it is visible, vertical scrollbars appear with font size changes.*/
  overflow-y: hidden;
  overflow-x: auto;
}
.CodeMirror-lines {
  /* In CM2, this used to be 0.4em, but in CM3 it went to 4px. We need the em value because */
  /* we have set a different line-height and want this to scale with that. */
  padding: 0.4em;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. We need the 0 value because of how we size */
  /* .CodeMirror-lines */
  padding: 0;
  border: 0;
  border-radius: 0;
}
/*
Original style from softwaremaniacs.org (c) Ivan Sagalaev <Maniac@SoftwareManiacs.Org>
Adapted from GitHub theme
*/
.highlight-base {
  color: #000;
}
.highlight-variable {
  color: #000;
}
.highlight-variable-2 {
  color: #1a1a1a;
}
.highlight-variable-3 {
  color: #333333;
}
.highlight-string {
  color: #BA2121;
}
.highlight-comment {
  color: #408080;
  font-style: italic;
}
.highlight-number {
  color: #080;
}
.highlight-atom {
  color: #88F;
}
.highlight-keyword {
  color: #008000;
  font-weight: bold;
}
.highlight-builtin {
  color: #008000;
}
.highlight-error {
  color: #f00;
}
.highlight-operator {
  color: #AA22FF;
  font-weight: bold;
}
.highlight-meta {
  color: #AA22FF;
}
/* previously not defined, copying from default codemirror */
.highlight-def {
  color: #00f;
}
.highlight-string-2 {
  color: #f50;
}
.highlight-qualifier {
  color: #555;
}
.highlight-bracket {
  color: #997;
}
.highlight-tag {
  color: #170;
}
.highlight-attribute {
  color: #00c;
}
.highlight-header {
  color: blue;
}
.highlight-quote {
  color: #090;
}
.highlight-link {
  color: #00c;
}
/* apply the same style to codemirror */
.cm-s-ipython span.cm-keyword {
  color: #008000;
  font-weight: bold;
}
.cm-s-ipython span.cm-atom {
  color: #88F;
}
.cm-s-ipython span.cm-number {
  color: #080;
}
.cm-s-ipython span.cm-def {
  color: #00f;
}
.cm-s-ipython span.cm-variable {
  color: #000;
}
.cm-s-ipython span.cm-operator {
  color: #AA22FF;
  font-weight: bold;
}
.cm-s-ipython span.cm-variable-2 {
  color: #1a1a1a;
}
.cm-s-ipython span.cm-variable-3 {
  color: #333333;
}
.cm-s-ipython span.cm-comment {
  color: #408080;
  font-style: italic;
}
.cm-s-ipython span.cm-string {
  color: #BA2121;
}
.cm-s-ipython span.cm-string-2 {
  color: #f50;
}
.cm-s-ipython span.cm-meta {
  color: #AA22FF;
}
.cm-s-ipython span.cm-qualifier {
  color: #555;
}
.cm-s-ipython span.cm-builtin {
  color: #008000;
}
.cm-s-ipython span.cm-bracket {
  color: #997;
}
.cm-s-ipython span.cm-tag {
  color: #170;
}
.cm-s-ipython span.cm-attribute {
  color: #00c;
}
.cm-s-ipython span.cm-header {
  color: blue;
}
.cm-s-ipython span.cm-quote {
  color: #090;
}
.cm-s-ipython span.cm-link {
  color: #00c;
}
.cm-s-ipython span.cm-error {
  color: #f00;
}
.cm-s-ipython span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}
div.output_wrapper {
  /* this position must be relative to enable descendents to be absolute within it */
  position: relative;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  z-index: 1;
}
/* class for the output area when it should be height-limited */
div.output_scroll {
  /* ideally, this would be max-height, but FF barfs all over that */
  height: 24em;
  /* FF needs this *and the wrapper* to specify full width, or it will shrinkwrap */
  width: 100%;
  overflow: auto;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  display: block;
}
/* output div while it is collapsed */
div.output_collapsed {
  margin: 0px;
  padding: 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
div.out_prompt_overlay {
  height: 100%;
  padding: 0px 0.4em;
  position: absolute;
  border-radius: 2px;
}
div.out_prompt_overlay:hover {
  /* use inner shadow to get border that is computed the same on WebKit/FF */
  -webkit-box-shadow: inset 0 0 1px #000;
  box-shadow: inset 0 0 1px #000;
  background: rgba(240, 240, 240, 0.5);
}
div.output_prompt {
  color: #D84315;
}
/* This class is the outer container of all output sections. */
div.output_area {
  padding: 0px;
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.output_area .MathJax_Display {
  text-align: left !important;
}
div.output_area .rendered_html table {
  margin-left: 0;
  margin-right: 0;
}
div.output_area .rendered_html img {
  margin-left: 0;
  margin-right: 0;
}
div.output_area img,
div.output_area svg {
  max-width: 100%;
  height: auto;
}
div.output_area img.unconfined,
div.output_area svg.unconfined {
  max-width: none;
}
/* This is needed to protect the pre formating from global settings such
   as that of bootstrap */
.output {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.output_area {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
div.output_area pre {
  margin: 0;
  padding: 0;
  border: 0;
  vertical-align: baseline;
  color: black;
  background-color: transparent;
  border-radius: 0;
}
/* This class is for the output subarea inside the output_area and after
   the prompt div. */
div.output_subarea {
  overflow-x: auto;
  padding: 0.4em;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
  max-width: calc(100% - 14ex);
}
div.output_scroll div.output_subarea {
  overflow-x: visible;
}
/* The rest of the output_* classes are for special styling of the different
   output types */
/* all text output has this class: */
div.output_text {
  text-align: left;
  color: #000;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
}
/* stdout/stderr are 'text' as well as 'stream', but execute_result/error are *not* streams */
div.output_stderr {
  background: #fdd;
  /* very light red background for stderr */
}
div.output_latex {
  text-align: left;
}
/* Empty output_javascript divs should have no height */
div.output_javascript:empty {
  padding: 0;
}
.js-error {
  color: darkred;
}
/* raw_input styles */
div.raw_input_container {
  line-height: 1.21429em;
  padding-top: 5px;
}
pre.raw_input_prompt {
  /* nothing needed here. */
}
input.raw_input {
  font-family: monospace;
  font-size: inherit;
  color: inherit;
  width: auto;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
}
input.raw_input:focus {
  box-shadow: none;
}
p.p-space {
  margin-bottom: 10px;
}
div.output_unrecognized {
  padding: 5px;
  font-weight: bold;
  color: red;
}
div.output_unrecognized a {
  color: inherit;
  text-decoration: none;
}
div.output_unrecognized a:hover {
  color: inherit;
  text-decoration: none;
}
.rendered_html {
  color: #000;
  /* any extras will just be numbers: */
}
.rendered_html em {
  font-style: italic;
}
.rendered_html strong {
  font-weight: bold;
}
.rendered_html u {
  text-decoration: underline;
}
.rendered_html :link {
  text-decoration: underline;
}
.rendered_html :visited {
  text-decoration: underline;
}
.rendered_html h1 {
  font-size: 185.7%;
  margin: 1.08em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h2 {
  font-size: 157.1%;
  margin: 1.27em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h3 {
  font-size: 128.6%;
  margin: 1.55em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h4 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h5 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h6 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h1:first-child {
  margin-top: 0.538em;
}
.rendered_html h2:first-child {
  margin-top: 0.636em;
}
.rendered_html h3:first-child {
  margin-top: 0.777em;
}
.rendered_html h4:first-child {
  margin-top: 1em;
}
.rendered_html h5:first-child {
  margin-top: 1em;
}
.rendered_html h6:first-child {
  margin-top: 1em;
}
.rendered_html ul {
  list-style: disc;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ul ul {
  list-style: square;
  margin: 0em 2em;
}
.rendered_html ul ul ul {
  list-style: circle;
  margin: 0em 2em;
}
.rendered_html ol {
  list-style: decimal;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ol ol {
  list-style: upper-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol {
  list-style: lower-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol {
  list-style: lower-roman;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol ol {
  list-style: decimal;
  margin: 0em 2em;
}
.rendered_html * + ul {
  margin-top: 1em;
}
.rendered_html * + ol {
  margin-top: 1em;
}
.rendered_html hr {
  color: black;
  background-color: black;
}
.rendered_html pre {
  margin: 1em 2em;
}
.rendered_html pre,
.rendered_html code {
  border: 0;
  background-color: #fff;
  color: #000;
  font-size: 100%;
  padding: 0px;
}
.rendered_html blockquote {
  margin: 1em 2em;
}
.rendered_html table {
  margin-left: auto;
  margin-right: auto;
  border: 1px solid black;
  border-collapse: collapse;
}
.rendered_html tr,
.rendered_html th,
.rendered_html td {
  border: 1px solid black;
  border-collapse: collapse;
  margin: 1em 2em;
}
.rendered_html td,
.rendered_html th {
  text-align: left;
  vertical-align: middle;
  padding: 4px;
}
.rendered_html th {
  font-weight: bold;
}
.rendered_html * + table {
  margin-top: 1em;
}
.rendered_html p {
  text-align: left;
}
.rendered_html * + p {
  margin-top: 1em;
}
.rendered_html img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.rendered_html * + img {
  margin-top: 1em;
}
.rendered_html img,
.rendered_html svg {
  max-width: 100%;
  height: auto;
}
.rendered_html img.unconfined,
.rendered_html svg.unconfined {
  max-width: none;
}
div.text_cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.text_cell > div.prompt {
    display: none;
  }
}
div.text_cell_render {
  /*font-family: "Helvetica Neue", Arial, Helvetica, Geneva, sans-serif;*/
  outline: none;
  resize: none;
  width: inherit;
  border-style: none;
  padding: 0.5em 0.5em 0.5em 0.4em;
  color: #000;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
a.anchor-link:link {
  text-decoration: none;
  padding: 0px 20px;
  visibility: hidden;
}
h1:hover .anchor-link,
h2:hover .anchor-link,
h3:hover .anchor-link,
h4:hover .anchor-link,
h5:hover .anchor-link,
h6:hover .anchor-link {
  visibility: visible;
}
.text_cell.rendered .input_area {
  display: none;
}
.text_cell.rendered .rendered_html {
  overflow-x: auto;
  overflow-y: hidden;
}
.text_cell.unrendered .text_cell_render {
  display: none;
}
.cm-header-1,
.cm-header-2,
.cm-header-3,
.cm-header-4,
.cm-header-5,
.cm-header-6 {
  font-weight: bold;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
.cm-header-1 {
  font-size: 185.7%;
}
.cm-header-2 {
  font-size: 157.1%;
}
.cm-header-3 {
  font-size: 128.6%;
}
.cm-header-4 {
  font-size: 110%;
}
.cm-header-5 {
  font-size: 100%;
  font-style: italic;
}
.cm-header-6 {
  font-size: 100%;
  font-style: italic;
}
/*!
*
* IPython notebook webapp
*
*/
@media (max-width: 767px) {
  .notebook_app {
    padding-left: 0px;
    padding-right: 0px;
  }
}
#ipython-main-app {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook_panel {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook {
  font-size: 14px;
  line-height: 20px;
  overflow-y: hidden;
  overflow-x: auto;
  width: 100%;
  /* This spaces the page away from the edge of the notebook area */
  padding-top: 20px;
  margin: 0px;
  outline: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  min-height: 100%;
}
@media not print {
  #notebook-container {
    padding: 15px;
    background-color: #fff;
    min-height: 0;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
@media print {
  #notebook-container {
    width: 100%;
  }
}
div.ui-widget-content {
  border: 1px solid #ababab;
  outline: none;
}
pre.dialog {
  background-color: #f7f7f7;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding: 0.4em;
  padding-left: 2em;
}
p.dialog {
  padding: 0.2em;
}
/* Word-wrap output correctly.  This is the CSS3 spelling, though Firefox seems
   to not honor it correctly.  Webkit browsers (Chrome, rekonq, Safari) do.
 */
pre,
code,
kbd,
samp {
  white-space: pre-wrap;
}
#fonttest {
  font-family: monospace;
}
p {
  margin-bottom: 0;
}
.end_space {
  min-height: 100px;
  transition: height .2s ease;
}
.notebook_app > #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
@media not print {
  .notebook_app {
    background-color: #EEE;
  }
}
kbd {
  border-style: solid;
  border-width: 1px;
  box-shadow: none;
  margin: 2px;
  padding-left: 2px;
  padding-right: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
/* CSS for the cell toolbar */
.celltoolbar {
  border: thin solid #CFCFCF;
  border-bottom: none;
  background: #EEE;
  border-radius: 2px 2px 0px 0px;
  width: 100%;
  height: 29px;
  padding-right: 4px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
  display: -webkit-flex;
}
@media print {
  .celltoolbar {
    display: none;
  }
}
.ctb_hideshow {
  display: none;
  vertical-align: bottom;
}
/* ctb_show is added to the ctb_hideshow div to show the cell toolbar.
   Cell toolbars are only shown when the ctb_global_show class is also set.
*/
.ctb_global_show .ctb_show.ctb_hideshow {
  display: block;
}
.ctb_global_show .ctb_show + .input_area,
.ctb_global_show .ctb_show + div.text_cell_input,
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border-top-right-radius: 0px;
  border-top-left-radius: 0px;
}
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border: 1px solid #cfcfcf;
}
.celltoolbar {
  font-size: 87%;
  padding-top: 3px;
}
.celltoolbar select {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  width: inherit;
  font-size: inherit;
  height: 22px;
  padding: 0px;
  display: inline-block;
}
.celltoolbar select:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.celltoolbar select::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.celltoolbar select:-ms-input-placeholder {
  color: #999;
}
.celltoolbar select::-webkit-input-placeholder {
  color: #999;
}
.celltoolbar select::-ms-expand {
  border: 0;
  background-color: transparent;
}
.celltoolbar select[disabled],
.celltoolbar select[readonly],
fieldset[disabled] .celltoolbar select {
  background-color: #eeeeee;
  opacity: 1;
}
.celltoolbar select[disabled],
fieldset[disabled] .celltoolbar select {
  cursor: not-allowed;
}
textarea.celltoolbar select {
  height: auto;
}
select.celltoolbar select {
  height: 30px;
  line-height: 30px;
}
textarea.celltoolbar select,
select[multiple].celltoolbar select {
  height: auto;
}
.celltoolbar label {
  margin-left: 5px;
  margin-right: 5px;
}
.completions {
  position: absolute;
  z-index: 110;
  overflow: hidden;
  border: 1px solid #ababab;
  border-radius: 2px;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  line-height: 1;
}
.completions select {
  background: white;
  outline: none;
  border: none;
  padding: 0px;
  margin: 0px;
  overflow: auto;
  font-family: monospace;
  font-size: 110%;
  color: #000;
  width: auto;
}
.completions select option.context {
  color: #286090;
}
#kernel_logo_widget {
  float: right !important;
  float: right;
}
#kernel_logo_widget .current_kernel_logo {
  display: none;
  margin-top: -1px;
  margin-bottom: -1px;
  width: 32px;
  height: 32px;
}
#menubar {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  margin-top: 1px;
}
#menubar .navbar {
  border-top: 1px;
  border-radius: 0px 0px 2px 2px;
  margin-bottom: 0px;
}
#menubar .navbar-toggle {
  float: left;
  padding-top: 7px;
  padding-bottom: 7px;
  border: none;
}
#menubar .navbar-collapse {
  clear: left;
}
.nav-wrapper {
  border-bottom: 1px solid #e7e7e7;
}
i.menu-icon {
  padding-top: 4px;
}
ul#help_menu li a {
  overflow: hidden;
  padding-right: 2.2em;
}
ul#help_menu li a i {
  margin-right: -1.2em;
}
.dropdown-submenu {
  position: relative;
}
.dropdown-submenu > .dropdown-menu {
  top: 0;
  left: 100%;
  margin-top: -6px;
  margin-left: -1px;
}
.dropdown-submenu:hover > .dropdown-menu {
  display: block;
}
.dropdown-submenu > a:after {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: block;
  content: "\f0da";
  float: right;
  color: #333333;
  margin-top: 2px;
  margin-right: -10px;
}
.dropdown-submenu > a:after.pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.pull-right {
  margin-left: .3em;
}
.dropdown-submenu:hover > a:after {
  color: #262626;
}
.dropdown-submenu.pull-left {
  float: none;
}
.dropdown-submenu.pull-left > .dropdown-menu {
  left: -100%;
  margin-left: 10px;
}
#notification_area {
  float: right !important;
  float: right;
  z-index: 10;
}
.indicator_area {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
#kernel_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  border-left: 1px solid;
}
#kernel_indicator .kernel_indicator_name {
  padding-left: 5px;
  padding-right: 5px;
}
#modal_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
#readonly-indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  margin-top: 2px;
  margin-bottom: 0px;
  margin-left: 0px;
  margin-right: 0px;
  display: none;
}
.modal_indicator:before {
  width: 1.28571429em;
  text-align: center;
}
.edit_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f040";
}
.edit_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: ' ';
}
.command_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f10c";
}
.kernel_idle_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f111";
}
.kernel_busy_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f1e2";
}
.kernel_dead_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f127";
}
.kernel_disconnected_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.pull-right {
  margin-left: .3em;
}
.notification_widget {
  color: #777;
  z-index: 10;
  background: rgba(240, 240, 240, 0.5);
  margin-right: 4px;
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget:focus,
.notification_widget.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.notification_widget:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active:hover,
.notification_widget.active:hover,
.open > .dropdown-toggle.notification_widget:hover,
.notification_widget:active:focus,
.notification_widget.active:focus,
.open > .dropdown-toggle.notification_widget:focus,
.notification_widget:active.focus,
.notification_widget.active.focus,
.open > .dropdown-toggle.notification_widget.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  background-image: none;
}
.notification_widget.disabled:hover,
.notification_widget[disabled]:hover,
fieldset[disabled] .notification_widget:hover,
.notification_widget.disabled:focus,
.notification_widget[disabled]:focus,
fieldset[disabled] .notification_widget:focus,
.notification_widget.disabled.focus,
.notification_widget[disabled].focus,
fieldset[disabled] .notification_widget.focus {
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget .badge {
  color: #fff;
  background-color: #333;
}
.notification_widget.warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning:focus,
.notification_widget.warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.notification_widget.warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active:hover,
.notification_widget.warning.active:hover,
.open > .dropdown-toggle.notification_widget.warning:hover,
.notification_widget.warning:active:focus,
.notification_widget.warning.active:focus,
.open > .dropdown-toggle.notification_widget.warning:focus,
.notification_widget.warning:active.focus,
.notification_widget.warning.active.focus,
.open > .dropdown-toggle.notification_widget.warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  background-image: none;
}
.notification_widget.warning.disabled:hover,
.notification_widget.warning[disabled]:hover,
fieldset[disabled] .notification_widget.warning:hover,
.notification_widget.warning.disabled:focus,
.notification_widget.warning[disabled]:focus,
fieldset[disabled] .notification_widget.warning:focus,
.notification_widget.warning.disabled.focus,
.notification_widget.warning[disabled].focus,
fieldset[disabled] .notification_widget.warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.notification_widget.success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success:focus,
.notification_widget.success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.notification_widget.success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active:hover,
.notification_widget.success.active:hover,
.open > .dropdown-toggle.notification_widget.success:hover,
.notification_widget.success:active:focus,
.notification_widget.success.active:focus,
.open > .dropdown-toggle.notification_widget.success:focus,
.notification_widget.success:active.focus,
.notification_widget.success.active.focus,
.open > .dropdown-toggle.notification_widget.success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  background-image: none;
}
.notification_widget.success.disabled:hover,
.notification_widget.success[disabled]:hover,
fieldset[disabled] .notification_widget.success:hover,
.notification_widget.success.disabled:focus,
.notification_widget.success[disabled]:focus,
fieldset[disabled] .notification_widget.success:focus,
.notification_widget.success.disabled.focus,
.notification_widget.success[disabled].focus,
fieldset[disabled] .notification_widget.success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.notification_widget.info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info:focus,
.notification_widget.info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.notification_widget.info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active:hover,
.notification_widget.info.active:hover,
.open > .dropdown-toggle.notification_widget.info:hover,
.notification_widget.info:active:focus,
.notification_widget.info.active:focus,
.open > .dropdown-toggle.notification_widget.info:focus,
.notification_widget.info:active.focus,
.notification_widget.info.active.focus,
.open > .dropdown-toggle.notification_widget.info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  background-image: none;
}
.notification_widget.info.disabled:hover,
.notification_widget.info[disabled]:hover,
fieldset[disabled] .notification_widget.info:hover,
.notification_widget.info.disabled:focus,
.notification_widget.info[disabled]:focus,
fieldset[disabled] .notification_widget.info:focus,
.notification_widget.info.disabled.focus,
.notification_widget.info[disabled].focus,
fieldset[disabled] .notification_widget.info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.notification_widget.danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger:focus,
.notification_widget.danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.notification_widget.danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active:hover,
.notification_widget.danger.active:hover,
.open > .dropdown-toggle.notification_widget.danger:hover,
.notification_widget.danger:active:focus,
.notification_widget.danger.active:focus,
.open > .dropdown-toggle.notification_widget.danger:focus,
.notification_widget.danger:active.focus,
.notification_widget.danger.active.focus,
.open > .dropdown-toggle.notification_widget.danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  background-image: none;
}
.notification_widget.danger.disabled:hover,
.notification_widget.danger[disabled]:hover,
fieldset[disabled] .notification_widget.danger:hover,
.notification_widget.danger.disabled:focus,
.notification_widget.danger[disabled]:focus,
fieldset[disabled] .notification_widget.danger:focus,
.notification_widget.danger.disabled.focus,
.notification_widget.danger[disabled].focus,
fieldset[disabled] .notification_widget.danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger .badge {
  color: #d9534f;
  background-color: #fff;
}
div#pager {
  background-color: #fff;
  font-size: 14px;
  line-height: 20px;
  overflow: hidden;
  display: none;
  position: fixed;
  bottom: 0px;
  width: 100%;
  max-height: 50%;
  padding-top: 8px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  /* Display over codemirror */
  z-index: 100;
  /* Hack which prevents jquery ui resizable from changing top. */
  top: auto !important;
}
div#pager pre {
  line-height: 1.21429em;
  color: #000;
  background-color: #f7f7f7;
  padding: 0.4em;
}
div#pager #pager-button-area {
  position: absolute;
  top: 8px;
  right: 20px;
}
div#pager #pager-contents {
  position: relative;
  overflow: auto;
  width: 100%;
  height: 100%;
}
div#pager #pager-contents #pager-container {
  position: relative;
  padding: 15px 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
div#pager .ui-resizable-handle {
  top: 0px;
  height: 8px;
  background: #f7f7f7;
  border-top: 1px solid #cfcfcf;
  border-bottom: 1px solid #cfcfcf;
  /* This injects handle bars (a short, wide = symbol) for 
        the resize handle. */
}
div#pager .ui-resizable-handle::after {
  content: '';
  top: 2px;
  left: 50%;
  height: 3px;
  width: 30px;
  margin-left: -15px;
  position: absolute;
  border-top: 1px solid #cfcfcf;
}
.quickhelp {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  line-height: 1.8em;
}
.shortcut_key {
  display: inline-block;
  width: 21ex;
  text-align: right;
  font-family: monospace;
}
.shortcut_descr {
  display: inline-block;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
span.save_widget {
  margin-top: 6px;
}
span.save_widget span.filename {
  height: 1em;
  line-height: 1em;
  padding: 3px;
  margin-left: 16px;
  border: none;
  font-size: 146.5%;
  border-radius: 2px;
}
span.save_widget span.filename:hover {
  background-color: #e6e6e6;
}
span.checkpoint_status,
span.autosave_status {
  font-size: small;
}
@media (max-width: 767px) {
  span.save_widget {
    font-size: small;
  }
  span.checkpoint_status,
  span.autosave_status {
    display: none;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  span.checkpoint_status {
    display: none;
  }
  span.autosave_status {
    font-size: x-small;
  }
}
.toolbar {
  padding: 0px;
  margin-left: -5px;
  margin-top: 2px;
  margin-bottom: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.toolbar select,
.toolbar label {
  width: auto;
  vertical-align: middle;
  margin-right: 2px;
  margin-bottom: 0px;
  display: inline;
  font-size: 92%;
  margin-left: 0.3em;
  margin-right: 0.3em;
  padding: 0px;
  padding-top: 3px;
}
.toolbar .btn {
  padding: 2px 8px;
}
.toolbar .btn-group {
  margin-top: 0px;
  margin-left: 5px;
}
#maintoolbar {
  margin-bottom: -3px;
  margin-top: -8px;
  border: 0px;
  min-height: 27px;
  margin-left: 0px;
  padding-top: 11px;
  padding-bottom: 3px;
}
#maintoolbar .navbar-text {
  float: none;
  vertical-align: middle;
  text-align: right;
  margin-left: 5px;
  margin-right: 0px;
  margin-top: 0px;
}
.select-xs {
  height: 24px;
}
.pulse,
.dropdown-menu > li > a.pulse,
li.pulse > a.dropdown-toggle,
li.pulse.open > a.dropdown-toggle {
  background-color: #F37626;
  color: white;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
/** WARNING IF YOU ARE EDITTING THIS FILE, if this is a .css file, It has a lot
 * of chance of beeing generated from the ../less/[samename].less file, you can
 * try to get back the less file by reverting somme commit in history
 **/
/*
 * We'll try to get something pretty, so we
 * have some strange css to have the scroll bar on
 * the left with fix button on the top right of the tooltip
 */
@-moz-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-webkit-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-moz-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-webkit-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
/*properties of tooltip after "expand"*/
.bigtooltip {
  overflow: auto;
  height: 200px;
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
}
/*properties of tooltip before "expand"*/
.smalltooltip {
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
  text-overflow: ellipsis;
  overflow: hidden;
  height: 80px;
}
.tooltipbuttons {
  position: absolute;
  padding-right: 15px;
  top: 0px;
  right: 0px;
}
.tooltiptext {
  /*avoid the button to overlap on some docstring*/
  padding-right: 30px;
}
.ipython_tooltip {
  max-width: 700px;
  /*fade-in animation when inserted*/
  -webkit-animation: fadeOut 400ms;
  -moz-animation: fadeOut 400ms;
  animation: fadeOut 400ms;
  -webkit-animation: fadeIn 400ms;
  -moz-animation: fadeIn 400ms;
  animation: fadeIn 400ms;
  vertical-align: middle;
  background-color: #f7f7f7;
  overflow: visible;
  border: #ababab 1px solid;
  outline: none;
  padding: 3px;
  margin: 0px;
  padding-left: 7px;
  font-family: monospace;
  min-height: 50px;
  -moz-box-shadow: 0px 6px 10px -1px #adadad;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  border-radius: 2px;
  position: absolute;
  z-index: 1000;
}
.ipython_tooltip a {
  float: right;
}
.ipython_tooltip .tooltiptext pre {
  border: 0;
  border-radius: 0;
  font-size: 100%;
  background-color: #f7f7f7;
}
.pretooltiparrow {
  left: 0px;
  margin: 0px;
  top: -16px;
  width: 40px;
  height: 16px;
  overflow: hidden;
  position: absolute;
}
.pretooltiparrow:before {
  background-color: #f7f7f7;
  border: 1px #ababab solid;
  z-index: 11;
  content: "";
  position: absolute;
  left: 15px;
  top: 10px;
  width: 25px;
  height: 25px;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
}
ul.typeahead-list i {
  margin-left: -10px;
  width: 18px;
}
ul.typeahead-list {
  max-height: 80vh;
  overflow: auto;
}
ul.typeahead-list > li > a {
  /** Firefox bug **/
  /* see https://github.com/jupyter/notebook/issues/559 */
  white-space: normal;
}
.cmd-palette .modal-body {
  padding: 7px;
}
.cmd-palette form {
  background: white;
}
.cmd-palette input {
  outline: none;
}
.no-shortcut {
  display: none;
}
.command-shortcut:before {
  content: "(command)";
  padding-right: 3px;
  color: #777777;
}
.edit-shortcut:before {
  content: "(edit)";
  padding-right: 3px;
  color: #777777;
}
#find-and-replace #replace-preview .match,
#find-and-replace #replace-preview .insert {
  background-color: #BBDEFB;
  border-color: #90CAF9;
  border-style: solid;
  border-width: 1px;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .match {
  background-color: #FFCDD2;
  border-color: #EF9A9A;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .insert {
  background-color: #C8E6C9;
  border-color: #A5D6A7;
  border-radius: 0px;
}
#find-and-replace #replace-preview {
  max-height: 60vh;
  overflow: auto;
}
#find-and-replace #replace-preview pre {
  padding: 5px 10px;
}
.terminal-app {
  background: #EEE;
}
.terminal-app #header {
  background: #fff;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.terminal-app .terminal {
  width: 100%;
  float: left;
  font-family: monospace;
  color: white;
  background: black;
  padding: 0.4em;
  border-radius: 2px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
}
.terminal-app .terminal,
.terminal-app .terminal dummy-screen {
  line-height: 1em;
  font-size: 14px;
}
.terminal-app .terminal .xterm-rows {
  padding: 10px;
}
.terminal-app .terminal-cursor {
  color: black;
  background: white;
}
.terminal-app #terminado-container {
  margin-top: 20px;
}
/*# sourceMappingURL=style.min.css.map */
    </style>
<style type="text/css">
    .highlight .hll { background-color: #ffffcc }
.highlight  { background: #f8f8f8; }
.highlight .c { color: #408080; font-style: italic } /* Comment */
.highlight .err { border: 1px solid #FF0000 } /* Error */
.highlight .k { color: #008000; font-weight: bold } /* Keyword */
.highlight .o { color: #666666 } /* Operator */
.highlight .ch { color: #408080; font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: #408080; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #BC7A00 } /* Comment.Preproc */
.highlight .cpf { color: #408080; font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: #408080; font-style: italic } /* Comment.Single */
.highlight .cs { color: #408080; font-style: italic } /* Comment.Special */
.highlight .gd { color: #A00000 } /* Generic.Deleted */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #FF0000 } /* Generic.Error */
.highlight .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight .gi { color: #00A000 } /* Generic.Inserted */
.highlight .go { color: #888888 } /* Generic.Output */
.highlight .gp { color: #000080; font-weight: bold } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight .gt { color: #0044DD } /* Generic.Traceback */
.highlight .kc { color: #008000; font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: #008000; font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: #008000; font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: #008000 } /* Keyword.Pseudo */
.highlight .kr { color: #008000; font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #B00040 } /* Keyword.Type */
.highlight .m { color: #666666 } /* Literal.Number */
.highlight .s { color: #BA2121 } /* Literal.String */
.highlight .na { color: #7D9029 } /* Name.Attribute */
.highlight .nb { color: #008000 } /* Name.Builtin */
.highlight .nc { color: #0000FF; font-weight: bold } /* Name.Class */
.highlight .no { color: #880000 } /* Name.Constant */
.highlight .nd { color: #AA22FF } /* Name.Decorator */
.highlight .ni { color: #999999; font-weight: bold } /* Name.Entity */
.highlight .ne { color: #D2413A; font-weight: bold } /* Name.Exception */
.highlight .nf { color: #0000FF } /* Name.Function */
.highlight .nl { color: #A0A000 } /* Name.Label */
.highlight .nn { color: #0000FF; font-weight: bold } /* Name.Namespace */
.highlight .nt { color: #008000; font-weight: bold } /* Name.Tag */
.highlight .nv { color: #19177C } /* Name.Variable */
.highlight .ow { color: #AA22FF; font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mb { color: #666666 } /* Literal.Number.Bin */
.highlight .mf { color: #666666 } /* Literal.Number.Float */
.highlight .mh { color: #666666 } /* Literal.Number.Hex */
.highlight .mi { color: #666666 } /* Literal.Number.Integer */
.highlight .mo { color: #666666 } /* Literal.Number.Oct */
.highlight .sa { color: #BA2121 } /* Literal.String.Affix */
.highlight .sb { color: #BA2121 } /* Literal.String.Backtick */
.highlight .sc { color: #BA2121 } /* Literal.String.Char */
.highlight .dl { color: #BA2121 } /* Literal.String.Delimiter */
.highlight .sd { color: #BA2121; font-style: italic } /* Literal.String.Doc */
.highlight .s2 { color: #BA2121 } /* Literal.String.Double */
.highlight .se { color: #BB6622; font-weight: bold } /* Literal.String.Escape */
.highlight .sh { color: #BA2121 } /* Literal.String.Heredoc */
.highlight .si { color: #BB6688; font-weight: bold } /* Literal.String.Interpol */
.highlight .sx { color: #008000 } /* Literal.String.Other */
.highlight .sr { color: #BB6688 } /* Literal.String.Regex */
.highlight .s1 { color: #BA2121 } /* Literal.String.Single */
.highlight .ss { color: #19177C } /* Literal.String.Symbol */
.highlight .bp { color: #008000 } /* Name.Builtin.Pseudo */
.highlight .fm { color: #0000FF } /* Name.Function.Magic */
.highlight .vc { color: #19177C } /* Name.Variable.Class */
.highlight .vg { color: #19177C } /* Name.Variable.Global */
.highlight .vi { color: #19177C } /* Name.Variable.Instance */
.highlight .vm { color: #19177C } /* Name.Variable.Magic */
.highlight .il { color: #666666 } /* Literal.Number.Integer.Long */
    </style>
<style type="text/css">
    
/* Temporary definitions which will become obsolete with Notebook release 5.0 */
.ansi-black-fg { color: #3E424D; }
.ansi-black-bg { background-color: #3E424D; }
.ansi-black-intense-fg { color: #282C36; }
.ansi-black-intense-bg { background-color: #282C36; }
.ansi-red-fg { color: #E75C58; }
.ansi-red-bg { background-color: #E75C58; }
.ansi-red-intense-fg { color: #B22B31; }
.ansi-red-intense-bg { background-color: #B22B31; }
.ansi-green-fg { color: #00A250; }
.ansi-green-bg { background-color: #00A250; }
.ansi-green-intense-fg { color: #007427; }
.ansi-green-intense-bg { background-color: #007427; }
.ansi-yellow-fg { color: #DDB62B; }
.ansi-yellow-bg { background-color: #DDB62B; }
.ansi-yellow-intense-fg { color: #B27D12; }
.ansi-yellow-intense-bg { background-color: #B27D12; }
.ansi-blue-fg { color: #208FFB; }
.ansi-blue-bg { background-color: #208FFB; }
.ansi-blue-intense-fg { color: #0065CA; }
.ansi-blue-intense-bg { background-color: #0065CA; }
.ansi-magenta-fg { color: #D160C4; }
.ansi-magenta-bg { background-color: #D160C4; }
.ansi-magenta-intense-fg { color: #A03196; }
.ansi-magenta-intense-bg { background-color: #A03196; }
.ansi-cyan-fg { color: #60C6C8; }
.ansi-cyan-bg { background-color: #60C6C8; }
.ansi-cyan-intense-fg { color: #258F8F; }
.ansi-cyan-intense-bg { background-color: #258F8F; }
.ansi-white-fg { color: #C5C1B4; }
.ansi-white-bg { background-color: #C5C1B4; }
.ansi-white-intense-fg { color: #A1A6B2; }
.ansi-white-intense-bg { background-color: #A1A6B2; }
.ansi-bold { font-weight: bold; }
    </style>


<style type="text/css">
/* Overrides of notebook CSS for static HTML export */
body {
  overflow: visible;
  padding: 8px;
}
div#notebook {
  overflow: visible;
  border-top: none;
}@media print {
  div.cell {
    display: block;
    page-break-inside: avoid;
  } 
  div.output_wrapper { 
    display: block;
    page-break-inside: avoid; 
  }
  div.output { 
    display: block;
    page-break-inside: avoid; 
  }
}
</style>

<!-- Custom stylesheet, it must be in the same directory as the html file -->
<link rel="stylesheet" href="custom.css">

<!-- Loading mathjax macro -->
<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-AMS_HTML"></script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
            processEscapes: true,
            processEnvironments: true
        },
        // Center justify equations in code and markdown cells. Elsewhere
        // we use CSS to left justify single line equations in code cells.
        displayAlign: 'center',
        "HTML-CSS": {
            styles: {'.MathJax_Display': {"margin": 0}},
            linebreaks: { automatic: true }
        }
    });
    </script>
    <!-- End of mathjax configuration --></head>
<body>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="2016-US-Bike-Share-Activity-Snapshot">2016 US Bike Share Activity Snapshot<a class="anchor-link" href="#2016-US-Bike-Share-Activity-Snapshot">&#182;</a></h1><h2 id="Table-of-Contents">Table of Contents<a class="anchor-link" href="#Table-of-Contents">&#182;</a></h2><ul>
<li><a href="#intro">Introduction</a></li>
<li><a href="#pose_questions">Posing Questions</a></li>
<li><a href="#wrangling">Data Collection and Wrangling</a><ul>
<li><a href="#condensing">Condensing the Trip Data</a></li>
</ul>
</li>
<li><a href="#eda">Exploratory Data Analysis</a><ul>
<li><a href="#statistics">Statistics</a></li>
<li><a href="#visualizations">Visualizations</a></li>
</ul>
</li>
<li><a href="#eda_continued">Performing Your Own Analysis</a></li>
<li><a href="#conclusions">Conclusions</a></li>
</ul>
<p><a id='intro'></a></p>
<h2 id="Introduction">Introduction<a class="anchor-link" href="#Introduction">&#182;</a></h2><p>Over the past decade, bicycle-sharing systems have been growing in number and popularity in cities across the world. Bicycle-sharing systems allow users to rent bicycles for short trips, typically 30 minutes or less. Thanks to the rise in information technologies, it is easy for a user of the system to access a dock within the system to unlock or return bicycles. These technologies also provide a wealth of data that can be used to explore how these bike-sharing systems are used.</p>
<p>In this project, I will perform an exploratory analysis on data provided by <a href="https://www.motivateco.com/">Motivate</a>, a bike-share system provider for many major cities in the United States. You will compare the system usage between three large cities: New York City, Chicago, and Washington, DC. You will also see if there are any differences within each system for those users that are registered, regular users and those users that are short-term, casual users.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a id='pose_questions'></a></p>
<h2 id="Posing-Questions">Posing Questions<a class="anchor-link" href="#Posing-Questions">&#182;</a></h2><p><strong>Question 1</strong>: What are the most common docks that are used over time and are they near any prominent landmarks?
    How old is each user in the bike-share system?</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a id='wrangling'></a></p>
<h2 id="Data-Collection-and-Wrangling">Data Collection and Wrangling<a class="anchor-link" href="#Data-Collection-and-Wrangling">&#182;</a></h2><p>In this project, we will focus on the record of individual trips taken in 2016 from our selected cities: New York City, Chicago, and Washington, DC. Each of these cities has a page where we can freely download the trip data.:</p>
<ul>
<li>New York City (Citi Bike): <a href="https://www.citibikenyc.com/system-data">Link</a></li>
<li>Chicago (Divvy): <a href="https://www.divvybikes.com/system-data">Link</a></li>
<li>Washington, DC (Capital Bikeshare): <a href="https://www.capitalbikeshare.com/system-data">Link</a></li>
</ul>
<p>If you visit these pages, you will notice that each city has a different way of delivering its data. Chicago updates with new data twice a year, Washington DC is quarterly, and New York City is monthly.</p>
<p><strong>Question 2</strong>: However, there is still a lot of data for us to investigate, so it's a good idea to start off by looking at one entry from each of the cities we're going to analyze. I will run the first code cell below to load some packages and functions that I'll be using in your analysis. Then, complete the second code cell to print out the first trip recorded from each of the cities (the second line of each data file).</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[1]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">## import all necessary packages and functions.</span>
<span class="kn">import</span> <span class="nn">csv</span> <span class="c1"># read and write csv files</span>
<span class="kn">from</span> <span class="nn">datetime</span> <span class="k">import</span> <span class="n">datetime</span> <span class="c1"># operations to parse dates</span>
<span class="kn">from</span> <span class="nn">pprint</span> <span class="k">import</span> <span class="n">pprint</span> <span class="c1"># use to print data structures like dictionaries in</span>
                          <span class="c1"># a nicer way than the base print function.</span>
<span class="kn">import</span> <span class="nn">calendar</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[5]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">print_first_point</span><span class="p">(</span><span class="n">filename</span><span class="p">):</span>
    <span class="sd">&quot;&quot;&quot;</span>
<span class="sd">    This function prints and returns the first data point (second row) from</span>
<span class="sd">    a csv file that includes a header row.</span>
<span class="sd">    &quot;&quot;&quot;</span>
    <span class="c1"># print city name for reference</span>
    <span class="n">city</span> <span class="o">=</span> <span class="n">filename</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s1">&#39;-&#39;</span><span class="p">)[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s1">&#39;/&#39;</span><span class="p">)[</span><span class="o">-</span><span class="mi">1</span><span class="p">]</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;</span><span class="se">\n</span><span class="s1">City: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">city</span><span class="p">))</span>
    
    <span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">filename</span><span class="p">,</span> <span class="s1">&#39;r&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f_in</span><span class="p">:</span>
        <span class="c1">## TODO: Use the csv library to set up a DictReader object. ##</span>
        <span class="c1">## see https://docs.python.org/3/library/csv.html           ##</span>
        <span class="n">trip_reader</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">DictReader</span><span class="p">(</span><span class="n">f_in</span><span class="p">)</span>
        
        <span class="c1">## TODO: Use a function on the DictReader object to read the     ##</span>
        <span class="c1">## first trip from the data file and store it in a variable.     ##</span>
        <span class="c1">## see https://docs.python.org/3/library/csv.html#reader-objects ##</span>
        <span class="n">first_trip</span> <span class="o">=</span> <span class="nb">next</span><span class="p">(</span><span class="n">trip_reader</span><span class="p">)</span>
        
        <span class="c1">## TODO: Use the pprint library to print the first trip. ##</span>
        <span class="c1">## see https://docs.python.org/3/library/pprint.html     ##</span>
        <span class="n">pprint</span><span class="p">(</span><span class="n">first_trip</span><span class="p">)</span>
    <span class="c1"># output city name and first trip for later testing</span>
    <span class="k">return</span> <span class="p">(</span><span class="n">city</span><span class="p">,</span> <span class="n">first_trip</span><span class="p">)</span>

<span class="c1"># list of files for each city</span>
<span class="n">data_files</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;NYC-CitiBike-2016.csv&#39;</span><span class="p">,</span>
              <span class="s1">&#39;Chicago-Divvy-2016.csv&#39;</span><span class="p">,</span>
              <span class="s1">&#39;Washington-CapitalBikeshare-2016.csv&#39;</span><span class="p">,]</span>

<span class="c1"># print the first trip from each file, store in dictionary</span>
<span class="n">example_trips</span> <span class="o">=</span> <span class="p">{}</span>
<span class="k">for</span> <span class="n">data_file</span> <span class="ow">in</span> <span class="n">data_files</span><span class="p">:</span>
    <span class="n">city</span><span class="p">,</span> <span class="n">first_trip</span> <span class="o">=</span> <span class="n">print_first_point</span><span class="p">(</span><span class="n">data_file</span><span class="p">)</span>
    <span class="n">example_trips</span><span class="p">[</span><span class="n">city</span><span class="p">]</span> <span class="o">=</span> <span class="n">first_trip</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>
City: NYC
OrderedDict([(&#39;tripduration&#39;, &#39;839&#39;),
             (&#39;starttime&#39;, &#39;1/1/2016 00:09:55&#39;),
             (&#39;stoptime&#39;, &#39;1/1/2016 00:23:54&#39;),
             (&#39;start station id&#39;, &#39;532&#39;),
             (&#39;start station name&#39;, &#39;S 5 Pl &amp; S 4 St&#39;),
             (&#39;start station latitude&#39;, &#39;40.710451&#39;),
             (&#39;start station longitude&#39;, &#39;-73.960876&#39;),
             (&#39;end station id&#39;, &#39;401&#39;),
             (&#39;end station name&#39;, &#39;Allen St &amp; Rivington St&#39;),
             (&#39;end station latitude&#39;, &#39;40.72019576&#39;),
             (&#39;end station longitude&#39;, &#39;-73.98997825&#39;),
             (&#39;bikeid&#39;, &#39;17109&#39;),
             (&#39;usertype&#39;, &#39;Customer&#39;),
             (&#39;birth year&#39;, &#39;&#39;),
             (&#39;gender&#39;, &#39;0&#39;)])

City: Chicago
OrderedDict([(&#39;trip_id&#39;, &#39;9080545&#39;),
             (&#39;starttime&#39;, &#39;3/31/2016 23:30&#39;),
             (&#39;stoptime&#39;, &#39;3/31/2016 23:46&#39;),
             (&#39;bikeid&#39;, &#39;2295&#39;),
             (&#39;tripduration&#39;, &#39;926&#39;),
             (&#39;from_station_id&#39;, &#39;156&#39;),
             (&#39;from_station_name&#39;, &#39;Clark St &amp; Wellington Ave&#39;),
             (&#39;to_station_id&#39;, &#39;166&#39;),
             (&#39;to_station_name&#39;, &#39;Ashland Ave &amp; Wrightwood Ave&#39;),
             (&#39;usertype&#39;, &#39;Subscriber&#39;),
             (&#39;gender&#39;, &#39;Male&#39;),
             (&#39;birthyear&#39;, &#39;1990&#39;)])

City: Washington
OrderedDict([(&#39;Duration (ms)&#39;, &#39;427387&#39;),
             (&#39;Start date&#39;, &#39;3/31/2016 22:57&#39;),
             (&#39;End date&#39;, &#39;3/31/2016 23:04&#39;),
             (&#39;Start station number&#39;, &#39;31602&#39;),
             (&#39;Start station&#39;, &#39;Park Rd &amp; Holmead Pl NW&#39;),
             (&#39;End station number&#39;, &#39;31207&#39;),
             (&#39;End station&#39;, &#39;Georgia Ave and Fairmont St NW&#39;),
             (&#39;Bike number&#39;, &#39;W20842&#39;),
             (&#39;Member Type&#39;, &#39;Registered&#39;)])
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a id='condensing'></a></p>
<h3 id="Condensing-the-Trip-Data">Condensing the Trip Data<a class="anchor-link" href="#Condensing-the-Trip-Data">&#182;</a></h3><p>It should also be observable from the above printout that each city provides different information. Even where the information is the same, the column names and formats are sometimes different. To make things as simple as possible when we get to the actual exploration, we should trim and clean the data. Cleaning the data makes sure that the data formats across the cities are consistent, while trimming focuses only on the parts of the data we are most interested in to make the exploration easier to work with.</p>
<p>I will generate new data files with five values of interest for each trip: trip duration, starting month, starting hour, day of the week, and user type. Each of these may require additional wrangling depending on the city:</p>
<ul>
<li><strong>Duration</strong>: This has been given to us in seconds (New York, Chicago) or milliseconds (Washington). A more natural unit of analysis will be if all the trip durations are given in terms of minutes.</li>
<li><strong>Month</strong>, <strong>Hour</strong>, <strong>Day of Week</strong>: Ridership volume is likely to change based on the season, time of day, and whether it is a weekday or weekend. The New York City data includes the seconds in their timestamps, while Washington and Chicago do not. The <a href="https://docs.python.org/3/library/datetime.html"><code>datetime</code></a> package will be very useful here to make the needed conversions.</li>
<li><strong>User Type</strong>: It is possible that users who are subscribed to a bike-share system will have different patterns of use compared to users who only have temporary passes. Washington divides its users into two types: 'Registered' for users with annual, monthly, and other longer-term subscriptions, and 'Casual', for users with 24-hour, 3-day, and other short-term passes. The New York and Chicago data uses 'Subscriber' and 'Customer' for these groups, respectively. For consistency, I will convert the Washington labels to match the other two.</li>
</ul>
<p><strong>Question 3a</strong>: What are the times of trips in seconds? What are the types of users for each city?(make sure that all user names are the same throughout each city)</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[11]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">duration_in_mins</span><span class="p">(</span><span class="n">datum</span><span class="p">,</span> <span class="n">city</span><span class="p">):</span>
    <span class="sd">&quot;&quot;&quot;</span>
<span class="sd">    Takes as input a dictionary containing info about a single trip (datum) and</span>
<span class="sd">    its origin city (city) and returns the trip duration in units of minutes.</span>
<span class="sd">    </span>
<span class="sd">    Remember that Washington is in terms of milliseconds while Chicago and NYC</span>
<span class="sd">    are in terms of seconds. </span>
<span class="sd">    </span>
<span class="sd">    HINT: The csv module reads in all of the data as strings, including numeric</span>
<span class="sd">    values. You will need a function to convert the strings into an appropriate</span>
<span class="sd">    numeric type when making your transformations.</span>
<span class="sd">    see https://docs.python.org/3/library/functions.html</span>
<span class="sd">    &quot;&quot;&quot;</span>
    <span class="c1"># YOUR CODE HERE</span>
    <span class="k">if</span> <span class="n">city</span> <span class="o">==</span> <span class="s1">&#39;Washington&#39;</span><span class="p">:</span>
        <span class="n">seconds_object</span> <span class="o">=</span> <span class="nb">int</span><span class="p">(</span><span class="n">datum</span><span class="p">[</span><span class="s1">&#39;Duration (ms)&#39;</span><span class="p">])</span>
        <span class="n">duration</span> <span class="o">=</span> <span class="n">seconds_object</span> <span class="o">/</span> <span class="mi">60000</span>
    <span class="k">else</span><span class="p">:</span>
        <span class="n">seconds_object</span> <span class="o">=</span> <span class="nb">int</span><span class="p">(</span><span class="n">datum</span><span class="p">[</span><span class="s1">&#39;tripduration&#39;</span><span class="p">])</span>
        <span class="n">duration</span> <span class="o">=</span> <span class="n">seconds_object</span> <span class="o">/</span> <span class="mi">60</span>
    <span class="k">return</span> <span class="n">duration</span>
   


<span class="c1"># Some tests to check that your code works. There should be no output if all of</span>
<span class="c1"># the assertions pass. The `example_trips` dictionary was obtained from when</span>
<span class="c1"># I printed the first trip from each of the original data files.</span>
<span class="n">tests</span> <span class="o">=</span> <span class="p">{</span><span class="s1">&#39;NYC&#39;</span><span class="p">:</span> <span class="mf">13.9833</span><span class="p">,</span>
         <span class="s1">&#39;Chicago&#39;</span><span class="p">:</span> <span class="mf">15.4333</span><span class="p">,</span>
         <span class="s1">&#39;Washington&#39;</span><span class="p">:</span> <span class="mf">7.1231</span><span class="p">}</span>

<span class="k">for</span> <span class="n">city</span> <span class="ow">in</span> <span class="n">tests</span><span class="p">:</span>
    <span class="k">assert</span> <span class="nb">abs</span><span class="p">(</span><span class="n">duration_in_mins</span><span class="p">(</span><span class="n">example_trips</span><span class="p">[</span><span class="n">city</span><span class="p">],</span> <span class="n">city</span><span class="p">)</span> <span class="o">-</span> <span class="n">tests</span><span class="p">[</span><span class="n">city</span><span class="p">])</span> <span class="o">&lt;</span> <span class="o">.</span><span class="mi">001</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[12]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">time_of_trip</span><span class="p">(</span><span class="n">datum</span><span class="p">,</span> <span class="n">city</span><span class="p">):</span>
    <span class="sd">&quot;&quot;&quot;</span>
<span class="sd">    Takes as input a dictionary containing info about a single trip (datum) and</span>
<span class="sd">    its origin city (city) and returns the month, hour, and day of the week in</span>
<span class="sd">    which the trip was made.</span>
<span class="sd">    </span>
<span class="sd">    Remember that NYC includes seconds, while Washington and Chicago do not.</span>
<span class="sd">    &quot;&quot;&quot;</span>
        
        
    <span class="c1"># YOUR CODE HERE</span>
    <span class="k">if</span> <span class="n">city</span> <span class="o">==</span> <span class="s1">&#39;NYC&#39;</span><span class="p">:</span>
        <span class="n">datetime_object</span> <span class="o">=</span> <span class="n">datetime</span><span class="o">.</span><span class="n">strptime</span><span class="p">(</span><span class="n">datum</span><span class="p">[</span><span class="s1">&#39;starttime&#39;</span><span class="p">],</span> <span class="s1">&#39;%m/</span><span class="si">%d</span><span class="s1">/%Y %H:%M:%S&#39;</span><span class="p">)</span>
    <span class="k">elif</span> <span class="n">city</span> <span class="o">==</span> <span class="s1">&#39;Chicago&#39;</span><span class="p">:</span>
        <span class="n">datetime_object</span> <span class="o">=</span> <span class="n">datetime</span><span class="o">.</span><span class="n">strptime</span><span class="p">(</span><span class="n">datum</span><span class="p">[</span><span class="s1">&#39;starttime&#39;</span><span class="p">],</span> <span class="s1">&#39;%m/</span><span class="si">%d</span><span class="s1">/%Y %H:%M&#39;</span><span class="p">)</span>
    <span class="k">elif</span> <span class="n">city</span> <span class="o">==</span> <span class="s1">&#39;Washington&#39;</span><span class="p">:</span>
        <span class="n">datetime_object</span> <span class="o">=</span> <span class="n">datetime</span><span class="o">.</span><span class="n">strptime</span><span class="p">(</span><span class="n">datum</span><span class="p">[</span><span class="s1">&#39;Start date&#39;</span><span class="p">],</span> <span class="s1">&#39;%m/</span><span class="si">%d</span><span class="s1">/%Y %H:%M&#39;</span><span class="p">)</span>
    <span class="k">return</span> <span class="p">((</span><span class="n">datetime_object</span><span class="o">.</span><span class="n">month</span><span class="p">,</span> <span class="n">datetime_object</span><span class="o">.</span><span class="n">hour</span><span class="p">,</span> <span class="n">calendar</span><span class="o">.</span><span class="n">day_name</span><span class="p">[</span><span class="n">datetime_object</span><span class="o">.</span><span class="n">weekday</span><span class="p">()]))</span>


<span class="c1"># Some tests to check that your code works. There should be no output if all of</span>
<span class="c1"># the assertions pass. The `example_trips` dictionary was obtained from when</span>
<span class="c1"># you printed the first trip from each of the original data files.</span>
<span class="n">tests</span> <span class="o">=</span> <span class="p">{</span><span class="s1">&#39;NYC&#39;</span><span class="p">:</span> <span class="p">(</span><span class="mi">1</span><span class="p">,</span> <span class="mi">0</span><span class="p">,</span> <span class="s1">&#39;Friday&#39;</span><span class="p">),</span>
         <span class="s1">&#39;Chicago&#39;</span><span class="p">:</span> <span class="p">(</span><span class="mi">3</span><span class="p">,</span> <span class="mi">23</span><span class="p">,</span> <span class="s1">&#39;Thursday&#39;</span><span class="p">),</span>
         <span class="s1">&#39;Washington&#39;</span><span class="p">:</span> <span class="p">(</span><span class="mi">3</span><span class="p">,</span> <span class="mi">22</span><span class="p">,</span> <span class="s1">&#39;Thursday&#39;</span><span class="p">)}</span>
<span class="k">for</span> <span class="n">city</span> <span class="ow">in</span> <span class="n">tests</span><span class="p">:</span>
    <span class="k">assert</span> <span class="n">time_of_trip</span><span class="p">(</span><span class="n">example_trips</span><span class="p">[</span><span class="n">city</span><span class="p">],</span> <span class="n">city</span><span class="p">)</span> <span class="o">==</span> <span class="n">tests</span><span class="p">[</span><span class="n">city</span><span class="p">]</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[10]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">type_of_user</span><span class="p">(</span><span class="n">datum</span><span class="p">,</span> <span class="n">city</span><span class="p">):</span>
    <span class="sd">&quot;&quot;&quot;</span>
<span class="sd">    Takes as input a dictionary containing info about a single trip (datum) and</span>
<span class="sd">    its origin city (city) and returns the type of system user that made the</span>
<span class="sd">    trip.</span>
<span class="sd">    </span>
<span class="sd">    Remember that Washington has different category names compared to Chicago</span>
<span class="sd">    and NYC. </span>
<span class="sd">    &quot;&quot;&quot;</span>
    
    <span class="c1"># YOUR CODE HERE</span>
    <span class="k">if</span> <span class="n">city</span> <span class="ow">in</span> <span class="p">[</span><span class="s1">&#39;Chicago&#39;</span><span class="p">,</span> <span class="s1">&#39;NYC&#39;</span><span class="p">]:</span>
        <span class="k">return</span> <span class="n">datum</span><span class="p">[</span><span class="s1">&#39;usertype&#39;</span><span class="p">]</span>
    <span class="k">elif</span> <span class="n">city</span> <span class="o">==</span> <span class="s1">&#39;Washington&#39;</span><span class="p">:</span>
        <span class="k">if</span> <span class="n">datum</span><span class="p">[</span><span class="s1">&#39;Member Type&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Registered&#39;</span><span class="p">:</span> 
            <span class="n">user_type</span> <span class="o">=</span> <span class="s1">&#39;Subscriber&#39;</span>
        <span class="k">elif</span> <span class="n">datum</span><span class="p">[</span><span class="s1">&#39;Member Type&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Casual&#39;</span><span class="p">:</span>
            <span class="n">user_type</span> <span class="o">=</span> <span class="s1">&#39;Customer&#39;</span>
    <span class="k">return</span> <span class="n">user_type</span>


<span class="c1"># Some tests to check that your code works. There should be no output if all of</span>
<span class="c1"># the assertions pass.</span>
<span class="n">tests</span> <span class="o">=</span> <span class="p">{</span><span class="s1">&#39;NYC&#39;</span><span class="p">:</span> <span class="s1">&#39;Customer&#39;</span><span class="p">,</span>
         <span class="s1">&#39;Chicago&#39;</span><span class="p">:</span> <span class="s1">&#39;Subscriber&#39;</span><span class="p">,</span>
         <span class="s1">&#39;Washington&#39;</span><span class="p">:</span> <span class="s1">&#39;Subscriber&#39;</span><span class="p">}</span>
<span class="k">for</span> <span class="n">city</span> <span class="ow">in</span> <span class="n">tests</span><span class="p">:</span>
    <span class="k">assert</span> <span class="n">type_of_user</span><span class="p">(</span><span class="n">example_trips</span><span class="p">[</span><span class="n">city</span><span class="p">],</span> <span class="n">city</span><span class="p">)</span> <span class="o">==</span> <span class="n">tests</span><span class="p">[</span><span class="n">city</span><span class="p">]</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><strong>Question 3b</strong>: By using the helper functions above, create a condensed data file for each city that has only the data types we are looking for - duration of trip, type of user, and month, hour, day of week.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[13]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">condense_data</span><span class="p">(</span><span class="n">in_file</span><span class="p">,</span> <span class="n">out_file</span><span class="p">,</span> <span class="n">city</span><span class="p">):</span>
    <span class="sd">&quot;&quot;&quot;</span>
<span class="sd">    This function takes full data from the specified input file</span>
<span class="sd">    and writes the condensed data to a specified output file. The city</span>
<span class="sd">    argument determines how the input file will be parsed.</span>
<span class="sd">    </span>
<span class="sd">    HINT: See the cell below to see how the arguments are structured!</span>
<span class="sd">    &quot;&quot;&quot;</span>
    <span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">out_file</span><span class="p">,</span> <span class="s1">&#39;w&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f_out</span><span class="p">,</span> <span class="nb">open</span><span class="p">(</span><span class="n">in_file</span><span class="p">,</span> <span class="s1">&#39;r&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f_in</span><span class="p">:</span>
        <span class="c1"># set up csv DictWriter object - writer requires column names for the</span>
        <span class="c1"># first row as the &quot;fieldnames&quot; argument</span>
        <span class="n">out_colnames</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;duration&#39;</span><span class="p">,</span> <span class="s1">&#39;month&#39;</span><span class="p">,</span> <span class="s1">&#39;hour&#39;</span><span class="p">,</span> <span class="s1">&#39;day_of_week&#39;</span><span class="p">,</span> <span class="s1">&#39;user_type&#39;</span><span class="p">]</span>        
        <span class="n">trip_writer</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">DictWriter</span><span class="p">(</span><span class="n">f_out</span><span class="p">,</span> <span class="n">fieldnames</span> <span class="o">=</span> <span class="n">out_colnames</span><span class="p">)</span>
        <span class="n">trip_writer</span><span class="o">.</span><span class="n">writeheader</span><span class="p">()</span>
        
        <span class="c1">## TODO: set up csv DictReader object ##</span>
        <span class="n">trip_reader</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">DictReader</span><span class="p">(</span><span class="n">f_in</span><span class="p">)</span>

        <span class="c1"># collect data from and process each row</span>
        <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">trip_reader</span><span class="p">:</span>
            <span class="c1"># set up a dictionary to hold the values for the cleaned and trimmed</span>
            <span class="c1"># data point</span>

            <span class="n">new_point</span> <span class="o">=</span> <span class="p">{}</span>

            <span class="c1">## TODO: use the helper functions to get the cleaned data from  ##</span>
            <span class="c1">## the original data dictionaries.                              ##</span>
            <span class="c1">## Note that the keys for the new_point dictionary should match ##</span>
            <span class="c1">## the column names set in the DictWriter object above. ##</span>
            <span class="n">new_point</span><span class="p">[</span><span class="s1">&#39;duration&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">duration_in_mins</span><span class="p">(</span><span class="n">row</span><span class="p">,</span> <span class="n">city</span><span class="p">)</span>
            <span class="n">new_point</span><span class="p">[</span><span class="s1">&#39;month&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">time_of_trip</span><span class="p">(</span><span class="n">row</span><span class="p">,</span> <span class="n">city</span><span class="p">)</span>
            <span class="n">new_point</span><span class="p">[</span><span class="s1">&#39;hour&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">time_of_trip</span><span class="p">(</span><span class="n">row</span><span class="p">,</span> <span class="n">city</span><span class="p">)</span>
            <span class="n">new_point</span><span class="p">[</span><span class="s1">&#39;day_of_week&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">time_of_trip</span><span class="p">(</span><span class="n">row</span><span class="p">,</span> <span class="n">city</span><span class="p">)</span>
            <span class="n">new_point</span><span class="p">[</span><span class="s1">&#39;user_type&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">type_of_user</span><span class="p">(</span><span class="n">row</span><span class="p">,</span> <span class="n">city</span><span class="p">)</span>
            

            <span class="c1">## TODO: write the processed information to the output file.     ##</span>
            <span class="c1">## see https://docs.python.org/3/library/csv.html#writer-objects ##</span>
            <span class="n">trip_writer</span><span class="o">.</span><span class="n">writerow</span><span class="p">(</span><span class="n">new_point</span><span class="p">)</span>

            
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[50]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Run this cell to check your work</span>
<span class="n">city_info</span> <span class="o">=</span> <span class="p">{</span><span class="s1">&#39;Washington&#39;</span><span class="p">:</span> <span class="p">{</span><span class="s1">&#39;in_file&#39;</span><span class="p">:</span> <span class="s1">&#39;./data/Washington-CapitalBikeshare-2016.csv&#39;</span><span class="p">,</span>
                            <span class="s1">&#39;out_file&#39;</span><span class="p">:</span> <span class="s1">&#39;./data/Washington-2016-Summary.csv&#39;</span><span class="p">},</span>
             <span class="s1">&#39;Chicago&#39;</span><span class="p">:</span> <span class="p">{</span><span class="s1">&#39;in_file&#39;</span><span class="p">:</span> <span class="s1">&#39;./data/Chicago-Divvy-2016.csv&#39;</span><span class="p">,</span>
                         <span class="s1">&#39;out_file&#39;</span><span class="p">:</span> <span class="s1">&#39;./data/Chicago-2016-Summary.csv&#39;</span><span class="p">},</span>
             <span class="s1">&#39;NYC&#39;</span><span class="p">:</span> <span class="p">{</span><span class="s1">&#39;in_file&#39;</span><span class="p">:</span> <span class="s1">&#39;./data/NYC-CitiBike-2016.csv&#39;</span><span class="p">,</span>
                     <span class="s1">&#39;out_file&#39;</span><span class="p">:</span> <span class="s1">&#39;./data/NYC-2016-Summary.csv&#39;</span><span class="p">}}</span>

<span class="k">for</span> <span class="n">city</span><span class="p">,</span> <span class="n">filenames</span> <span class="ow">in</span> <span class="n">city_info</span><span class="o">.</span><span class="n">items</span><span class="p">():</span>
    <span class="n">condense_data</span><span class="p">(</span><span class="n">filenames</span><span class="p">[</span><span class="s1">&#39;in_file&#39;</span><span class="p">],</span> <span class="n">filenames</span><span class="p">[</span><span class="s1">&#39;out_file&#39;</span><span class="p">],</span> <span class="n">city</span><span class="p">)</span>
    <span class="n">print_first_point</span><span class="p">(</span><span class="n">filenames</span><span class="p">[</span><span class="s1">&#39;out_file&#39;</span><span class="p">])</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>
City: Washington
OrderedDict([(&#39;duration&#39;, &#39;7.123116666666666&#39;),
             (&#39;month&#39;, &#34;(3, 22, &#39;Thursday&#39;)&#34;),
             (&#39;hour&#39;, &#34;(3, 22, &#39;Thursday&#39;)&#34;),
             (&#39;day_of_week&#39;, &#34;(3, 22, &#39;Thursday&#39;)&#34;),
             (&#39;user_type&#39;, &#39;Subscriber&#39;)])

City: Chicago
OrderedDict([(&#39;duration&#39;, &#39;15.433333333333334&#39;),
             (&#39;month&#39;, &#34;(3, 23, &#39;Thursday&#39;)&#34;),
             (&#39;hour&#39;, &#34;(3, 23, &#39;Thursday&#39;)&#34;),
             (&#39;day_of_week&#39;, &#34;(3, 23, &#39;Thursday&#39;)&#34;),
             (&#39;user_type&#39;, &#39;Subscriber&#39;)])

City: NYC
OrderedDict([(&#39;duration&#39;, &#39;13.983333333333333&#39;),
             (&#39;month&#39;, &#34;(1, 0, &#39;Friday&#39;)&#34;),
             (&#39;hour&#39;, &#34;(1, 0, &#39;Friday&#39;)&#34;),
             (&#39;day_of_week&#39;, &#34;(1, 0, &#39;Friday&#39;)&#34;),
             (&#39;user_type&#39;, &#39;Customer&#39;)])
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a id='eda'></a></p>
<h2 id="Exploratory-Data-Analysis">Exploratory Data Analysis<a class="anchor-link" href="#Exploratory-Data-Analysis">&#182;</a></h2><p>Now that we have the data collected and wrangled, we're ready to start exploring the data. In this section I will write some code to compute descriptive statistics from the data. I will also create some histograms from 'matplotlib' for the data files.</p>
<p><a id='statistics'></a></p>
<h3 id="Statistics">Statistics<a class="anchor-link" href="#Statistics">&#182;</a></h3><p>First, let's compute some basic counts. The first cell below contains a function that uses the csv module to iterate through a provided data file, returning the number of trips made by subscribers and customers. The second cell runs this function on the example Bay Area data in the <code>/examples/</code> folder.</p>
<p><strong>Question 4a</strong>: Which city has the highest number of trips? Which city has the highest proportion of trips made by subscribers? Which city has the highest proportion of trips made by short-term customers?</p>
<p><strong>Answer</strong>: New York City has the highest number of trips. New York City has the highest total number of trips made by subscribers. Chicago has the highest proportion of trips made by short-term customers.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[14]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">number_of_trips</span><span class="p">(</span><span class="n">filename</span><span class="p">):</span>
    <span class="sd">&quot;&quot;&quot;</span>
<span class="sd">    This function reads in a file with trip data and reports the number of</span>
<span class="sd">    trips made by subscribers, customers, and total overall.</span>
<span class="sd">    &quot;&quot;&quot;</span>
    <span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">filename</span><span class="p">,</span> <span class="s1">&#39;r&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f_in</span><span class="p">:</span>
        <span class="c1"># set up csv reader object</span>
        <span class="n">reader</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">DictReader</span><span class="p">(</span><span class="n">f_in</span><span class="p">)</span>
        
        <span class="c1"># initialize count variables</span>
        <span class="n">n_subscribers</span> <span class="o">=</span> <span class="mi">0</span>
        <span class="n">n_customers</span> <span class="o">=</span> <span class="mi">0</span>
        
        <span class="c1"># tally up ride types</span>
        <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">reader</span><span class="p">:</span>
            <span class="k">if</span> <span class="n">row</span><span class="p">[</span><span class="s1">&#39;user_type&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Subscriber&#39;</span><span class="p">:</span>
                <span class="n">n_subscribers</span> <span class="o">+=</span> <span class="mi">1</span>
            <span class="k">else</span><span class="p">:</span>
                <span class="n">n_customers</span> <span class="o">+=</span> <span class="mi">1</span>
        
        <span class="c1"># compute total number of rides</span>
        <span class="n">n_total</span> <span class="o">=</span> <span class="n">n_subscribers</span> <span class="o">+</span> <span class="n">n_customers</span>
        
        <span class="c1"># return tallies as a tuple</span>
        <span class="k">return</span><span class="p">(</span><span class="n">n_subscribers</span><span class="p">,</span> <span class="n">n_customers</span><span class="p">,</span> <span class="n">n_total</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[16]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># I will run this cell for an example of what the output will look like on the city files.</span>
<span class="n">data_file</span> <span class="o">=</span> <span class="s1">&#39;BayArea-Y3-Summary.csv&#39;</span>
<span class="nb">print</span><span class="p">(</span><span class="n">number_of_trips</span><span class="p">(</span><span class="n">data_file</span><span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>(5666, 633, 6299)
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[19]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">city_files</span> <span class="o">=</span> <span class="p">[[</span><span class="s1">&#39;Washington&#39;</span><span class="p">,</span> <span class="s1">&#39;Registered&#39;</span><span class="p">,</span> <span class="s1">&#39;Washington-2016-Summary.csv&#39;</span><span class="p">],</span>
             <span class="p">[</span><span class="s1">&#39;Chicago&#39;</span><span class="p">,</span> <span class="s1">&#39;Subscriber&#39;</span><span class="p">,</span> <span class="s1">&#39;Chicago-2016-Summary.csv&#39;</span><span class="p">],</span>
             <span class="p">[</span><span class="s1">&#39;New York&#39;</span><span class="p">,</span> <span class="s1">&#39;Subscriber&#39;</span><span class="p">,</span> <span class="s1">&#39;NYC-2016-Summary.csv&#39;</span><span class="p">]]</span>
<span class="k">def</span> <span class="nf">number_of_trips_updated</span><span class="p">(</span><span class="n">filename</span><span class="p">,</span> <span class="n">user</span><span class="p">):</span>
    <span class="sd">&quot;&quot;&quot;</span>
<span class="sd">    This function reads in a file with trip data and reports the number of</span>
<span class="sd">    trips made by subscribers, customers, and total overall.</span>
<span class="sd">    &quot;&quot;&quot;</span>
        
    <span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">filename</span><span class="p">,</span> <span class="s1">&#39;r&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f_in</span><span class="p">:</span>
        <span class="c1"># set up csv reader object</span>
        <span class="n">reader</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">DictReader</span><span class="p">(</span><span class="n">f_in</span><span class="p">)</span>
        
        <span class="c1"># initialize count variables</span>
        <span class="n">n_subscribers</span> <span class="o">=</span> <span class="mi">0</span>
        <span class="n">n_customers</span> <span class="o">=</span> <span class="mi">0</span>
        
        <span class="c1"># tally up ride types</span>
        <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">reader</span><span class="p">:</span>
            <span class="k">if</span> <span class="n">row</span><span class="p">[</span><span class="s1">&#39;user_type&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Subscriber&#39;</span><span class="p">:</span>
                <span class="n">n_subscribers</span> <span class="o">+=</span> <span class="mi">1</span>
            <span class="k">else</span><span class="p">:</span>
                <span class="n">n_customers</span> <span class="o">+=</span> <span class="mi">1</span>
        
        <span class="c1"># compute total number of rides</span>
        <span class="n">n_total</span> <span class="o">=</span> <span class="n">n_subscribers</span> <span class="o">+</span> <span class="n">n_customers</span>
        
        <span class="c1"># compute the proportion of trips made by subscribers, rounded to 3 decimals</span>
        <span class="n">subscribers_proportion</span> <span class="o">=</span> <span class="nb">round</span><span class="p">(</span><span class="n">n_subscribers</span> <span class="o">/</span> <span class="n">n_total</span><span class="p">,</span> <span class="mi">3</span><span class="p">)</span>
        
        <span class="c1"># return tallies as a tuple</span>
        <span class="k">return</span><span class="p">(</span><span class="n">n_subscribers</span><span class="p">,</span> <span class="n">n_customers</span><span class="p">,</span> <span class="n">n_total</span><span class="p">,</span> <span class="n">subscribers_proportion</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[20]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">print</span><span class="p">(</span><span class="s1">&#39;The number of trips made by subscribers, customers, the total overall and </span><span class="se">\n</span><span class="s1">&#39;</span>
      <span class="s1">&#39;the proportion of trips made by the subscribers are:&#39;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;&quot;</span> <span class="p">)</span>

<span class="k">for</span> <span class="n">entry</span> <span class="ow">in</span> <span class="n">city_files</span><span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;For </span><span class="si">{}</span><span class="s1">: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">entry</span><span class="p">[</span><span class="mi">0</span><span class="p">],</span> <span class="n">number_of_trips_updated</span><span class="p">(</span><span class="n">entry</span><span class="p">[</span><span class="mi">2</span><span class="p">],</span> <span class="n">entry</span><span class="p">[</span><span class="mi">1</span><span class="p">])))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>The number of trips made by subscribers, customers, the total overall and 
the proportion of trips made by the subscribers are:

For Washington: (51753, 14573, 66326, 0.78)
For Chicago: (54982, 17149, 72131, 0.762)
For New York: (245896, 30902, 276798, 0.888)
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><strong>Question 4b</strong>: Bike-share systems are designed for riders to take short trips. Most of the time, users are allowed to take trips of 30 minutes or less with no additional charges, with overage charges made for trips of longer than that duration. What is the average trip length for each city? What proportion of rides made in each city are longer than 30 minutes?</p>
<p><strong>Answer</strong>: The average trip length for Washington, Chicago, and New York is 18.93 minutes, 16.56 minutes, and 15.81 minutes respectively. The proportion of rides that are longer than 30 minutes for Washington, Chicago, and New York City is 10.8%, 8.3%, and 7.3% respectively.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[21]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">## The csv module reads in all of the data as strings, including        ##</span>
<span class="c1">## numeric values. I will need a function to convert the strings        ##</span>
<span class="c1">## into an appropriate numeric type before aggregating the data.        ##</span>

<span class="n">city_files</span> <span class="o">=</span> <span class="p">[[</span><span class="s1">&#39;Washington&#39;</span><span class="p">,</span> <span class="s1">&#39;Registered&#39;</span><span class="p">,</span> <span class="s1">&#39;Washington-2016-Summary.csv&#39;</span><span class="p">],</span>
             <span class="p">[</span><span class="s1">&#39;Chicago&#39;</span><span class="p">,</span> <span class="s1">&#39;Subscriber&#39;</span><span class="p">,</span> <span class="s1">&#39;Chicago-2016-Summary.csv&#39;</span><span class="p">],</span>
             <span class="p">[</span><span class="s1">&#39;New York&#39;</span><span class="p">,</span> <span class="s1">&#39;Subscriber&#39;</span><span class="p">,</span> <span class="s1">&#39;NYC-2016-Summary.csv&#39;</span><span class="p">]]</span>
<span class="k">def</span> <span class="nf">average_duration</span><span class="p">(</span><span class="n">filename</span><span class="p">,</span> <span class="n">city</span><span class="p">):</span>
    <span class="sd">&quot;&quot;&quot;</span>
<span class="sd">    This function reads in a file with trip data and the corresponding city, </span>
<span class="sd">    and reports average duration </span>
<span class="sd">    and the percentage of trips that are longer than 30 minutes.</span>
<span class="sd">    &quot;&quot;&quot;</span>
        
    <span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">filename</span><span class="p">,</span> <span class="s1">&#39;r&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f_in</span><span class="p">:</span>
        <span class="c1"># set up csv reader object</span>
        <span class="n">reader</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">DictReader</span><span class="p">(</span><span class="n">f_in</span><span class="p">)</span>
        
        <span class="c1"># initialize count variables</span>
        <span class="n">tot_duration</span> <span class="o">=</span> <span class="mi">0</span>
        <span class="n">longer_trips</span> <span class="o">=</span> <span class="mi">0</span>
        
        <span class="c1"># get the sum of all trip durations and the number of trips loger than 30 minutes</span>
        <span class="c1"># round to 3 decimals</span>
        <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">reader</span><span class="p">:</span>
            <span class="n">tot_duration</span> <span class="o">=</span> <span class="n">tot_duration</span> <span class="o">+</span> <span class="nb">round</span><span class="p">(</span><span class="nb">float</span><span class="p">(</span><span class="n">row</span><span class="p">[</span><span class="s1">&#39;duration&#39;</span><span class="p">]),</span><span class="mi">3</span><span class="p">)</span>
            <span class="k">if</span> <span class="nb">float</span><span class="p">(</span><span class="n">row</span><span class="p">[</span><span class="s1">&#39;duration&#39;</span><span class="p">])</span> <span class="o">&gt;</span> <span class="mi">30</span><span class="p">:</span>
                <span class="n">longer_trips</span> <span class="o">=</span> <span class="n">longer_trips</span> <span class="o">+</span> <span class="mi">1</span>
        
        <span class="c1"># get the total number of rides, using a previously defined function</span>
        <span class="k">for</span> <span class="n">entry</span> <span class="ow">in</span> <span class="n">city_files</span><span class="p">:</span>
            <span class="k">if</span> <span class="n">city</span> <span class="o">==</span><span class="n">entry</span><span class="p">[</span><span class="mi">0</span><span class="p">]:</span> 
                <span class="n">n_total</span> <span class="o">=</span> <span class="n">number_of_trips_updated</span><span class="p">(</span><span class="n">filename</span><span class="p">,</span> <span class="n">entry</span><span class="p">[</span><span class="mi">1</span><span class="p">])[</span><span class="mi">2</span><span class="p">]</span>
        
        
        <span class="c1"># return the average duration and the proportion of trips loger than 30 minutes </span>
        <span class="k">return</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">tot_duration</span><span class="o">/</span><span class="n">n_total</span><span class="p">,</span> <span class="mi">3</span><span class="p">),</span> <span class="nb">round</span><span class="p">(</span><span class="n">longer_trips</span><span class="o">/</span><span class="n">n_total</span><span class="p">,</span> <span class="mi">3</span><span class="p">))</span>
    
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;The average trip length for each city, followed by </span><span class="se">\n</span><span class="s1">&#39;&#39;the proportion of rides made in each city that are longer than 30 minutes:&#39;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;&quot;</span><span class="p">)</span>

<span class="k">for</span> <span class="n">entry</span> <span class="ow">in</span> <span class="n">city_files</span><span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;For </span><span class="si">{}</span><span class="s1">: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">entry</span><span class="p">[</span><span class="mi">0</span><span class="p">],</span> <span class="n">average_duration</span><span class="p">(</span><span class="n">entry</span><span class="p">[</span><span class="mi">2</span><span class="p">],</span> <span class="n">entry</span><span class="p">[</span><span class="mi">0</span><span class="p">])))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>The average trip length for each city, followed by 
the proportion of rides made in each city that are longer than 30 minutes:

For Washington: (18.933, 0.108)
For Chicago: (16.564, 0.083)
For New York: (15.813, 0.073)
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><strong>Question 4c</strong>: I will dig deeper into the question of trip duration based on ridership. By choosing Chicago for example, which type of user takes longer rides on average: Subscribers or Customers?</p>
<p><strong>Answer</strong>: Customers take more trips than subscribers on average. Within Chicago, customers take on average twice as long as subscribers.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[22]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">## I will use this function to answer question 4c ##</span>

<span class="n">city_files</span> <span class="o">=</span> <span class="p">[[</span><span class="s1">&#39;Washington&#39;</span><span class="p">,</span> <span class="s1">&#39;Registered&#39;</span><span class="p">,</span> <span class="s1">&#39;Washington-2016-Summary.csv&#39;</span><span class="p">],</span>
             <span class="p">[</span><span class="s1">&#39;Chicago&#39;</span><span class="p">,</span> <span class="s1">&#39;Subscriber&#39;</span><span class="p">,</span> <span class="s1">&#39;Chicago-2016-Summary.csv&#39;</span><span class="p">],</span>
             <span class="p">[</span><span class="s1">&#39;New York&#39;</span><span class="p">,</span> <span class="s1">&#39;Subscriber&#39;</span><span class="p">,</span> <span class="s1">&#39;NYC-2016-Summary.csv&#39;</span><span class="p">]]</span>
<span class="k">def</span> <span class="nf">average_duration_split</span><span class="p">(</span><span class="n">city</span><span class="p">,</span> <span class="n">user</span><span class="p">,</span> <span class="n">filename</span><span class="p">):</span>
    <span class="sd">&quot;&quot;&quot;</span>
<span class="sd">    This function reads an entry in city_files and reports </span>
<span class="sd">    the average length for trips made by subscribers and</span>
<span class="sd">    the average trip length for trips made by short term customers.</span>
<span class="sd">    &quot;&quot;&quot;</span>
        
    <span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">filename</span><span class="p">,</span> <span class="s1">&#39;r&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f_in</span><span class="p">:</span>
        <span class="c1"># set up csv reader object</span>
        <span class="n">reader</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">DictReader</span><span class="p">(</span><span class="n">f_in</span><span class="p">)</span>
        
        <span class="c1"># initialize count variables</span>
        <span class="n">duration_subscriber</span> <span class="o">=</span> <span class="mi">0</span>
        <span class="n">duration_customer</span> <span class="o">=</span> <span class="mi">0</span>
        
        <span class="c1"># find totals for trips durations, by user type</span>
        <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">reader</span><span class="p">:</span>
            <span class="k">if</span> <span class="n">row</span><span class="p">[</span><span class="s1">&#39;user_type&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Subscriber&#39;</span><span class="p">:</span>
                <span class="n">duration_subscriber</span> <span class="o">=</span> <span class="n">duration_subscriber</span> <span class="o">+</span> <span class="nb">round</span><span class="p">(</span><span class="nb">float</span><span class="p">(</span><span class="n">row</span><span class="p">[</span><span class="s1">&#39;duration&#39;</span><span class="p">]),</span><span class="mi">3</span><span class="p">)</span>
            <span class="k">else</span><span class="p">:</span>
                <span class="n">duration_customer</span> <span class="o">=</span> <span class="n">duration_customer</span> <span class="o">+</span> <span class="nb">round</span><span class="p">(</span><span class="nb">float</span><span class="p">(</span><span class="n">row</span><span class="p">[</span><span class="s1">&#39;duration&#39;</span><span class="p">]),</span><span class="mi">3</span><span class="p">)</span>
        
        <span class="c1"># get total number of rides for each type of rider</span>
        <span class="k">for</span> <span class="n">entry</span> <span class="ow">in</span> <span class="n">city_files</span><span class="p">:</span>
            <span class="k">if</span> <span class="n">city</span> <span class="o">==</span> <span class="n">entry</span><span class="p">[</span><span class="mi">0</span><span class="p">]:</span> 
                <span class="n">n_subscribers</span> <span class="o">=</span> <span class="n">number_of_trips_updated</span><span class="p">(</span><span class="n">entry</span><span class="p">[</span><span class="mi">2</span><span class="p">],</span> <span class="n">entry</span><span class="p">[</span><span class="mi">1</span><span class="p">])[</span><span class="mi">0</span><span class="p">]</span>
                <span class="n">n_customers</span> <span class="o">=</span> <span class="n">number_of_trips_updated</span><span class="p">(</span><span class="n">entry</span><span class="p">[</span><span class="mi">2</span><span class="p">],</span> <span class="n">entry</span><span class="p">[</span><span class="mi">1</span><span class="p">])[</span><span class="mi">1</span><span class="p">]</span>
        
        <span class="c1"># return the averages as a tuple</span>
        <span class="k">return</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">duration_subscriber</span><span class="o">/</span><span class="n">n_subscribers</span><span class="p">,</span><span class="mi">3</span><span class="p">),</span> <span class="nb">round</span><span class="p">(</span><span class="n">duration_customer</span><span class="o">/</span><span class="n">n_customers</span><span class="p">,</span><span class="mi">3</span><span class="p">))</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[23]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">### print the information obtained from average_duration_split function for each city</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;The average trip length for each city, split by type of users,</span><span class="se">\n</span><span class="s1">&#39;</span>
      <span class="s1">&#39;for Subscribers and for short-term Customers:&#39;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;&quot;</span><span class="p">)</span>

<span class="k">for</span> <span class="n">entry</span> <span class="ow">in</span> <span class="n">city_files</span><span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;For </span><span class="si">{}</span><span class="s1">: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">entry</span><span class="p">[</span><span class="mi">0</span><span class="p">],</span> <span class="n">average_duration_split</span><span class="p">(</span><span class="n">entry</span><span class="p">[</span><span class="mi">0</span><span class="p">],</span> <span class="n">entry</span><span class="p">[</span><span class="mi">1</span><span class="p">],</span> <span class="n">entry</span><span class="p">[</span><span class="mi">2</span><span class="p">])))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>The average trip length for each city, split by type of users,
for Subscribers and for short-term Customers:

For Washington: (12.528, 41.678)
For Chicago: (12.067, 30.98)
For New York: (13.681, 32.776)
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a id='visualizations'></a></p>
<h3 id="Visualizations">Visualizations<a class="anchor-link" href="#Visualizations">&#182;</a></h3><p>The last set of values that I computed have pulled up an interesting result. While the mean trip time for Subscribers is well under 30 minutes, the mean trip time for Customers is actually <em>above</em> 30 minutes! It will be interesting for us to look at how the trip times are distributed. In order to do this, a new library will be introduced here, <code>matplotlib</code>.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[25]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># load library</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>

<span class="c1"># this is a &#39;magic word&#39; that allows for plots to be displayed</span>
<span class="c1"># inline with the notebook.</span>
<span class="o">%</span><span class="k">matplotlib</span> inline 

<span class="c1"># example histogram, data taken from bay area sample</span>
<span class="n">data</span> <span class="o">=</span> <span class="p">[</span> <span class="mf">7.65</span><span class="p">,</span>  <span class="mf">8.92</span><span class="p">,</span>  <span class="mf">7.42</span><span class="p">,</span>  <span class="mf">5.50</span><span class="p">,</span> <span class="mf">16.17</span><span class="p">,</span>  <span class="mf">4.20</span><span class="p">,</span>  <span class="mf">8.98</span><span class="p">,</span>  <span class="mf">9.62</span><span class="p">,</span> <span class="mf">11.48</span><span class="p">,</span> <span class="mf">14.33</span><span class="p">,</span>
        <span class="mf">19.02</span><span class="p">,</span> <span class="mf">21.53</span><span class="p">,</span>  <span class="mf">3.90</span><span class="p">,</span>  <span class="mf">7.97</span><span class="p">,</span>  <span class="mf">2.62</span><span class="p">,</span>  <span class="mf">2.67</span><span class="p">,</span>  <span class="mf">3.08</span><span class="p">,</span> <span class="mf">14.40</span><span class="p">,</span> <span class="mf">12.90</span><span class="p">,</span>  <span class="mf">7.83</span><span class="p">,</span>
        <span class="mf">25.12</span><span class="p">,</span>  <span class="mf">8.30</span><span class="p">,</span>  <span class="mf">4.93</span><span class="p">,</span> <span class="mf">12.43</span><span class="p">,</span> <span class="mf">10.60</span><span class="p">,</span>  <span class="mf">6.17</span><span class="p">,</span> <span class="mf">10.88</span><span class="p">,</span>  <span class="mf">4.78</span><span class="p">,</span> <span class="mf">15.15</span><span class="p">,</span>  <span class="mf">3.53</span><span class="p">,</span>
         <span class="mf">9.43</span><span class="p">,</span> <span class="mf">13.32</span><span class="p">,</span> <span class="mf">11.72</span><span class="p">,</span>  <span class="mf">9.85</span><span class="p">,</span>  <span class="mf">5.22</span><span class="p">,</span> <span class="mf">15.10</span><span class="p">,</span>  <span class="mf">3.95</span><span class="p">,</span>  <span class="mf">3.17</span><span class="p">,</span>  <span class="mf">8.78</span><span class="p">,</span>  <span class="mf">1.88</span><span class="p">,</span>
         <span class="mf">4.55</span><span class="p">,</span> <span class="mf">12.68</span><span class="p">,</span> <span class="mf">12.38</span><span class="p">,</span>  <span class="mf">9.78</span><span class="p">,</span>  <span class="mf">7.63</span><span class="p">,</span>  <span class="mf">6.45</span><span class="p">,</span> <span class="mf">17.38</span><span class="p">,</span> <span class="mf">11.90</span><span class="p">,</span> <span class="mf">11.52</span><span class="p">,</span>  <span class="mf">8.63</span><span class="p">,]</span>
<span class="n">plt</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">data</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Distribution of Trip Durations&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;Duration (m)&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
AABJRU5ErkJggg==
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>In the above cell, we collected fifty trip times in a list, and passed this list as the first argument to the <code>.hist()</code> function. This function performs the computations and creates plotting objects for generating a histogram, but the plot is actually not rendered until the <code>.show()</code> function is executed. The <code>.title()</code> and <code>.xlabel()</code> functions provide some labeling for plot context.</p>
<p>I will now use these functions to create a histogram of the trip times for the city I selected in question 4c.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[27]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">## I will collect all of the trip times as a list and then use ##</span>
<span class="c1">## pyplot functions to generate a histogram of trip times.     ##</span>

<span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">city_files</span><span class="p">[</span><span class="mi">1</span><span class="p">][</span><span class="mi">2</span><span class="p">],</span> <span class="s1">&#39;r&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f_in</span><span class="p">:</span>
    <span class="c1"># set up csv reader object</span>
    <span class="n">reader</span> <span class="o">=</span> <span class="nb">list</span><span class="p">(</span><span class="n">csv</span><span class="o">.</span><span class="n">DictReader</span><span class="p">(</span><span class="n">f_in</span><span class="p">))</span>
        
<span class="c1">### create an empty list for the data to be saved in</span>
<span class="n">times_list</span> <span class="o">=</span> <span class="p">[]</span>

<span class="c1">### save all the trip durations, as float numbers in a list</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="nb">len</span><span class="p">(</span><span class="n">reader</span><span class="p">)):</span>
    <span class="n">times_list</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="nb">float</span><span class="p">(</span><span class="n">reader</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;duration&#39;</span><span class="p">]))</span>
            
<span class="c1">### a naive histogram of the trip durations, all riders in Chicago </span>

<span class="n">plt</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">times_list</span><span class="p">)</span>

<span class="c1">### title and axes labelling</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;</span><span class="se">\n</span><span class="s1"> Distribution of Trip Durations - Chicago </span><span class="se">\n</span><span class="s1">&#39;</span><span class="p">,</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">16</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;Duration (mins)&#39;</span><span class="p">,</span> <span class="n">fontsize</span> <span class="o">=</span> <span class="mi">14</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;Number of Trips&#39;</span><span class="p">,</span> <span class="n">fontsize</span> <span class="o">=</span> <span class="mi">14</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
gg==
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>The plot consists of one extremely tall bar on the left, maybe a very short second bar, and a whole lot of empty space in the center and right. Take a look at the duration values on the x-axis. This suggests that there are some highly infrequent outliers in the data. Instead of reprocessing the data, I will use additional parameters with the <code>.hist()</code> function to limit the range of data that is plotted. Documentation for the function can be found <a href="https://matplotlib.org/devdocs/api/_as_gen/matplotlib.pyplot.hist.html#matplotlib.pyplot.hist">[here]</a>.</p>
<p><strong>Question 5</strong>: We will use the parameters of the <code>.hist()</code> function to plot the distribution of trip times for the Subscribers and Customers in Chicago. This time, we will add limits to the plots so that only trips of duration less than 75 minutes are plotted. As a bonus, we will set the plots up so that bars are in five-minute wide intervals. For each group, where is the peak of each distribution? How would you describe the shape of each distribution?</p>
<p><strong>Answer</strong>: Peak distribution of number of trips is at 1272 trips for Subscribers. These peak number of trips last between 5-10 minutes. For Customers, peak distribution of number of trips is 1432 and these trips last between 20-25 minutes. Both graphs are positively skewed.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[30]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">## This cell will take in the duration of each city and output a histogram of the duration of ##</span>
<span class="c1">## Subscribers and Customers in Chicago.                                                      ##</span>

<span class="k">def</span> <span class="nf">durations_list</span><span class="p">(</span><span class="n">entry</span><span class="p">):</span>
    <span class="c1"># set up csv reader object</span>
    <span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">entry</span><span class="p">[</span><span class="mi">2</span><span class="p">],</span> <span class="s1">&#39;r&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f_in</span><span class="p">:</span>
        <span class="n">reader</span> <span class="o">=</span> <span class="nb">list</span><span class="p">(</span><span class="n">csv</span><span class="o">.</span><span class="n">DictReader</span><span class="p">(</span><span class="n">f_in</span><span class="p">))</span>
        
        <span class="c1"># create empty lists for each rider type</span>
        <span class="n">total_riders</span> <span class="o">=</span> <span class="p">[]</span> 
        <span class="n">subscribers</span> <span class="o">=</span> <span class="p">[]</span> 
        <span class="n">customers</span> <span class="o">=</span> <span class="p">[]</span> 
        
        <span class="c1"># tally up all the duration times for each user type</span>
        <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="nb">len</span><span class="p">(</span><span class="n">reader</span><span class="p">)):</span>
            <span class="n">total_riders</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="nb">float</span><span class="p">(</span><span class="n">reader</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;duration&#39;</span><span class="p">]))</span>   
            <span class="k">if</span> <span class="n">reader</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;user_type&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="n">entry</span><span class="p">[</span><span class="mi">1</span><span class="p">]:</span>
                <span class="n">subscribers</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="nb">float</span><span class="p">(</span><span class="n">reader</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;duration&#39;</span><span class="p">]))</span>
            <span class="k">else</span><span class="p">:</span>
                <span class="n">customers</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="nb">float</span><span class="p">(</span><span class="n">reader</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="s1">&#39;duration&#39;</span><span class="p">]))</span>
        <span class="k">return</span><span class="p">(</span><span class="n">total_riders</span><span class="p">,</span> <span class="n">subscribers</span><span class="p">,</span> <span class="n">customers</span><span class="p">)</span>

<span class="c1"># set up city_files for the histogram</span>
<span class="n">city_files</span> <span class="o">=</span> <span class="p">[[</span><span class="s1">&#39;Washington&#39;</span><span class="p">,</span> <span class="s1">&#39;Registered&#39;</span><span class="p">,</span> <span class="s1">&#39;Washington-2016-Summary.csv&#39;</span><span class="p">],</span>
             <span class="p">[</span><span class="s1">&#39;Chicago&#39;</span><span class="p">,</span> <span class="s1">&#39;Subscriber&#39;</span><span class="p">,</span> <span class="s1">&#39;Chicago-2016-Summary.csv&#39;</span><span class="p">],</span>
             <span class="p">[</span><span class="s1">&#39;New York&#39;</span><span class="p">,</span> <span class="s1">&#39;Subscriber&#39;</span><span class="p">,</span> <span class="s1">&#39;NYC-2016-Summary.csv&#39;</span><span class="p">]]</span>   

<span class="c1"># run the function above for the city of chicago</span>
<span class="n">chicago_total</span> <span class="o">=</span> <span class="n">durations_list</span><span class="p">(</span><span class="n">city_files</span><span class="p">[</span><span class="mi">1</span><span class="p">])[</span><span class="mi">0</span><span class="p">]</span>
<span class="n">chicago_subscribers</span> <span class="o">=</span> <span class="n">durations_list</span><span class="p">(</span><span class="n">city_files</span><span class="p">[</span><span class="mi">1</span><span class="p">])[</span><span class="mi">1</span><span class="p">]</span>
<span class="n">chicago_customers</span> <span class="o">=</span> <span class="n">durations_list</span><span class="p">(</span><span class="n">city_files</span><span class="p">[</span><span class="mi">1</span><span class="p">])[</span><span class="mi">2</span><span class="p">]</span>   

<span class="c1"># run the necessary packages</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="o">%</span> <span class="n">matplotlib</span> <span class="n">inline</span>

<span class="c1"># set up histogram characteristics</span>
<span class="n">x_labels</span> <span class="o">=</span> <span class="p">[</span><span class="mi">0</span><span class="p">,</span><span class="mi">5</span><span class="p">,</span><span class="mi">10</span><span class="p">,</span><span class="mi">15</span><span class="p">,</span><span class="mi">20</span><span class="p">,</span><span class="mi">25</span><span class="p">,</span><span class="mi">30</span><span class="p">,</span><span class="mi">35</span><span class="p">,</span><span class="mi">40</span><span class="p">,</span><span class="mi">45</span><span class="p">,</span><span class="mi">50</span><span class="p">,</span><span class="mi">55</span><span class="p">,</span><span class="mi">60</span><span class="p">,</span><span class="mi">65</span><span class="p">,</span><span class="mi">70</span><span class="p">,</span><span class="mi">75</span><span class="p">]</span>
<span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">20</span><span class="p">,</span> <span class="mi">6</span><span class="p">),</span> <span class="n">dpi</span><span class="o">=</span> <span class="mi">50</span><span class="p">,</span> <span class="n">linewidth</span><span class="o">=</span><span class="mi">4</span><span class="p">,</span> <span class="n">frameon</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

<span class="c1"># set titles and axes for the Subscribers histogram</span>
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span><span class="mi">2</span><span class="p">,</span><span class="mi">1</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">chicago_subscribers</span><span class="p">,</span> <span class="n">facecolor</span><span class="o">=</span><span class="s1">&#39;r&#39;</span><span class="p">,</span> <span class="n">alpha</span><span class="o">=</span> <span class="mf">0.7</span><span class="p">,</span> <span class="n">bins</span><span class="o">=</span><span class="n">x_labels</span><span class="p">,</span> <span class="n">rwidth</span><span class="o">=</span><span class="mf">0.5</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Duration of Trips - Subscribers&#39;</span><span class="p">,</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">28</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;Duration(mins)&#39;</span><span class="p">,</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">24</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;Number of Trips&#39;</span><span class="p">,</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">24</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">axis</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">75</span><span class="p">,</span><span class="mi">0</span><span class="p">,</span><span class="mi">21000</span><span class="p">])</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xticks</span><span class="p">(</span><span class="n">x_labels</span><span class="p">,</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">22</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">yticks</span><span class="p">(</span><span class="n">fontsize</span><span class="o">=</span><span class="mi">22</span><span class="p">)</span>

<span class="c1"># set up titles and axes for the Customers histogram</span>
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span><span class="mi">2</span><span class="p">,</span><span class="mi">2</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">chicago_customers</span><span class="p">,</span> <span class="n">facecolor</span><span class="o">=</span><span class="s1">&#39;b&#39;</span><span class="p">,</span> <span class="n">alpha</span><span class="o">=</span><span class="mf">0.7</span><span class="p">,</span> <span class="n">bins</span><span class="o">=</span><span class="n">x_labels</span><span class="p">,</span> <span class="n">rwidth</span><span class="o">=</span><span class="mf">0.5</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Duration of Trips - Customers&#39;</span><span class="p">,</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">28</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;Duration(mins)&#39;</span><span class="p">,</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">24</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;Number of Trips&#39;</span><span class="p">,</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">24</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">axis</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">75</span><span class="p">,</span><span class="mi">0</span><span class="p">,</span><span class="mi">3500</span><span class="p">])</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xticks</span><span class="p">(</span><span class="n">x_labels</span><span class="p">,</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">22</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">yticks</span><span class="p">(</span><span class="n">fontsize</span><span class="o">=</span><span class="mi">22</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAA2IAAAElCAYAAACGbVFvAAAABHNCSVQICAgIfAhkiAAAAAlwSFlz
AAAHsAAAB7AB1IKDYgAAADl0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uIDIuMS4wLCBo
dHRwOi8vbWF0cGxvdGxpYi5vcmcvpW3flQAAIABJREFUeJzs3Xu8XNP9//HXu25xl1BVfkjLt4QW
LXWru2+FqJKGKm3Rr7rUV5WgaFFFaUvR+lJaFN+ve10iFaLq1rq3qEuCCom6B4kgEiKf3x9rjbOz
zz5n5uTMmXNOvJ+PxzzmzNqf2XvtmTmzZu11U0RgZmZmZmZmrfOx3s6AmZmZmZnZR40rYmZmZmZm
Zi3mipiZmZmZmVmLuSJmZmZmZmbWYq6IWa+StJekkLRXb+dlbklaTdIoSa/kc5nY4uPvn4/7jVYe
t7+Q9PP8+mzY23npiKQBOY83ldIvz+nL9VbezMxlVZOO77LKrMQVsX5A0uD85VW8TZf0oqS/SDpe
0iq9nc8qhbxf2Nt56QmS5gOuBYYC1wM/Bc7oIHavivexs9uFrTuT3iNpQUk/kHSvpDclzcyf7Xsl
/UrSWr2dRzOrz2VV3+WyqnkkDZF0lqRxkt7KZdYkSVdK2kmSWpCH1fNrf05PH8t61vy9nQHrkgnA
/+W/FwKWBdYHjgF+JOmXwI+jf61JcC1wL/BSb2dkLn0KGAKcGxH714l9mFT4Fa0D7AjcAdxeEd+I
y/NzX2gwvs+QtADwZ2Az4HngSuA1YAXS63owMAV4pLfy2CIzSef7dm9nxKwJXFb1PS6rmkDSj4AT
8sO/AmOBGcBKwH8CuwBnA//dKxm0fscVsf7l6Yg4rpwoaVPgYuAo4ANSYdcvRMSbwJu9nY9uWD7f
v1wvMCIeplRg5W4uOwK3V723jYiIqcDUuXluH7AXqRJ2PTAiImYVN0paHvh4L+SrpfIP0id6Ox9m
TeKyqu9xWdVNkg4CfgY8TSqvHiltXwDYG/hCL2TP+il3TZwHRMRfSd0NZgI/lLRibZuk43Lz9Rbl
51X1eS92z8hN39dIei2nDc4xwyVdJunp3O3kTUl/lTSivH/g2fxwz1JXhi06ykPh+RtLukHSG5Jm
SHoin88iFbEh6XZJH5d0gaRXJb2bu7e1O/fOSFpa0umSns1dDl6VdIWkNUpxE0lXBwF+Uji3dufS
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
QmCC
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[39]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">print</span><span class="p">(</span><span class="s1">&#39;The maximum number of trips for Subscribers during peak is </span><span class="si">{}</span><span class="s1">:&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">max</span><span class="p">(</span><span class="n">chicago_subscribers</span><span class="p">)))</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;The maximum number of trips for Customers during peak is </span><span class="si">{}</span><span class="s1">:&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">max</span><span class="p">(</span><span class="n">chicago_customers</span><span class="p">)))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>The maximum number of trips for Subscribers during peak is 1272.45:
The maximum number of trips for Customers during peak is 1439.4166666666667:
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a id='eda_continued'></a></p>
<h2 id="Performing-A-Final-Analysis">Performing A Final Analysis<a class="anchor-link" href="#Performing-A-Final-Analysis">&#182;</a></h2><p>So far, we've performed an initial exploration into the data available. We have compared the relative volume of trips made between three U.S. cities and the ratio of trips made by Subscribers and Customers. For Chicago, we have investigated differences between Subscribers and Customers in terms of how long a typical trip lasts. Now it is time to explore a final question.</p>
<p><strong>Question 6</strong>: How does ridership differ by month or season? Which month / season has the highest ridership? Does the ratio of Subscriber trips to Customer trips change depending on the month or season?</p>
<p><strong>Answer</strong>: Ridership differs each season in that the most number of riders occur in the summer months with the least in winter months. June has the highest number of riders. There is approximately double the amount of Subscribers to Customers in the summer months. In the winter months, there is approximately a 1:0 ratio of Subscribers to Customers.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[31]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">condense_Chicago</span><span class="p">(</span><span class="n">in_file</span><span class="p">,</span> <span class="n">out_file</span><span class="p">,</span> <span class="n">city</span><span class="p">):</span>
    <span class="sd">&quot;&quot;&quot;</span>
<span class="sd">    This function takes full data from the specified input file</span>
<span class="sd">    and writes the condensed data to a specified output file. The city</span>
<span class="sd">    argument determines how the input file will be parsed.</span>
<span class="sd">    </span>
<span class="sd">    HINT: See the cell below to see how the arguments are structured!</span>
<span class="sd">    &quot;&quot;&quot;</span>
    <span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">out_file</span><span class="p">,</span> <span class="s1">&#39;w&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f_out</span><span class="p">,</span> <span class="nb">open</span><span class="p">(</span><span class="n">in_file</span><span class="p">,</span> <span class="s1">&#39;r&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f_in</span><span class="p">:</span>
        <span class="c1"># set up csv DictWriter object - writer requires column names for the</span>
        <span class="c1"># first row as the &quot;fieldnames&quot; argument</span>
        <span class="n">out_colnames</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;duration&#39;</span><span class="p">,</span> <span class="s1">&#39;month&#39;</span><span class="p">,</span> <span class="s1">&#39;hour&#39;</span><span class="p">,</span> <span class="s1">&#39;day_of_week&#39;</span><span class="p">,</span><span class="s1">&#39;user_type&#39;</span><span class="p">]</span>        
        <span class="n">trip_writer</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">DictWriter</span><span class="p">(</span><span class="n">f_out</span><span class="p">,</span> <span class="n">fieldnames</span> <span class="o">=</span> <span class="n">out_colnames</span><span class="p">)</span>
        <span class="n">trip_writer</span><span class="o">.</span><span class="n">writeheader</span><span class="p">()</span>
        
        <span class="c1">## TODO: set up csv DictReader object ##</span>
        <span class="n">trip_reader</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">DictReader</span><span class="p">(</span><span class="n">f_in</span><span class="p">)</span>

        <span class="c1"># collect data from and process each row</span>
        <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">trip_reader</span><span class="p">:</span>
            
            <span class="c1"># set up a dictionary to hold the values for the cleaned and trimmed</span>
            <span class="c1"># data point</span>
            <span class="n">new_point</span> <span class="o">=</span> <span class="p">{}</span>

            <span class="c1">## TODO: use the helper functions to get the cleaned data from  ##</span>
            <span class="c1">## the original data dictionaries.                              ##</span>
            <span class="c1">## Note that the keys for the new_point dictionary should match ##</span>
            <span class="c1">## the column names set in the DictWriter object above. ##</span>
            <span class="n">new_point</span><span class="p">[</span><span class="s1">&#39;duration&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">duration_in_mins</span><span class="p">(</span><span class="n">row</span><span class="p">,</span> <span class="n">city</span><span class="p">)</span>
            <span class="n">new_point</span><span class="p">[</span><span class="s1">&#39;month&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">time_of_trip</span><span class="p">(</span><span class="n">row</span><span class="p">,</span> <span class="n">city</span><span class="p">)[</span><span class="mi">0</span><span class="p">]</span>
            <span class="n">new_point</span><span class="p">[</span><span class="s1">&#39;hour&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">time_of_trip</span><span class="p">(</span><span class="n">row</span><span class="p">,</span> <span class="n">city</span><span class="p">)[</span><span class="mi">1</span><span class="p">]</span>
            <span class="n">new_point</span><span class="p">[</span><span class="s1">&#39;day_of_week&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">time_of_trip</span><span class="p">(</span><span class="n">row</span><span class="p">,</span> <span class="n">city</span><span class="p">)[</span><span class="mi">2</span><span class="p">]</span>
            <span class="n">new_point</span><span class="p">[</span><span class="s1">&#39;user_type&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">type_of_user</span><span class="p">(</span><span class="n">row</span><span class="p">,</span> <span class="n">city</span><span class="p">)</span>
            

            <span class="c1">## TODO: write the processed information to the output file.     ##</span>
            <span class="c1">## see https://docs.python.org/3/library/csv.html#writer-objects ##</span>
            <span class="n">trip_writer</span><span class="o">.</span><span class="n">writerow</span><span class="p">(</span><span class="n">new_point</span><span class="p">)</span>                                    <span class="c1">##</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[34]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># This will create a new file from the Chicago city file#</span>
<span class="n">in_file_Chicago</span> <span class="o">=</span> <span class="s1">&#39;Chicago-Divvy-2016.csv&#39;</span>
<span class="n">out_file_Chicago</span> <span class="o">=</span> <span class="s1">&#39;Chicago-Divvy-2016-updated.csv&#39;</span>

<span class="c1"># Perform the helper function stated above #</span>
<span class="n">condense_Chicago</span><span class="p">(</span><span class="n">in_file_Chicago</span><span class="p">,</span> <span class="n">out_file_Chicago</span><span class="p">,</span> <span class="s1">&#39;Chicago&#39;</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[35]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># we will need to index the months </span>
<span class="n">months</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;1&#39;</span><span class="p">,</span> <span class="s1">&#39;2&#39;</span><span class="p">,</span> <span class="s1">&#39;3&#39;</span><span class="p">,</span> <span class="s1">&#39;4&#39;</span><span class="p">,</span> <span class="s1">&#39;5&#39;</span><span class="p">,</span> <span class="s1">&#39;6&#39;</span><span class="p">,</span> <span class="s1">&#39;7&#39;</span><span class="p">,</span> <span class="s1">&#39;8&#39;</span><span class="p">,</span> <span class="s1">&#39;9&#39;</span><span class="p">,</span> <span class="s1">&#39;10&#39;</span><span class="p">,</span> <span class="s1">&#39;11&#39;</span><span class="p">,</span> <span class="s1">&#39;12&#39;</span><span class="p">]</span>

<span class="c1"># create empty lists for each user type </span>
<span class="n">monthly_subs</span> <span class="o">=</span> <span class="p">[]</span> 
<span class="n">monthly_cust</span> <span class="o">=</span> <span class="p">[]</span> 
<span class="n">monthly_total</span> <span class="o">=</span> <span class="p">[]</span>

<span class="k">def</span> <span class="nf">monthly_trips</span><span class="p">(</span><span class="n">month</span><span class="p">):</span>
    <span class="sd">&quot;&quot;&quot; </span>
<span class="sd">    This function takes in the month and data from specified input file and </span>
<span class="sd">    outputs the number of user types by month.</span>
<span class="sd">    &quot;&quot;&quot;</span>
    <span class="c1"># set up csv dictReader object</span>
    <span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">out_file_Chicago</span><span class="p">,</span> <span class="s1">&#39;r&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f_in</span><span class="p">:</span>
        <span class="n">reader</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">DictReader</span><span class="p">(</span><span class="n">f_in</span><span class="p">)</span>

        <span class="c1"># start tally count at 0</span>
        <span class="n">trips_Subs</span> <span class="o">=</span> <span class="mi">0</span>
        <span class="n">trips_Cust</span> <span class="o">=</span> <span class="mi">0</span>
        
        <span class="c1"># tally up the number of user types</span>
        <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">reader</span><span class="p">:</span>
            <span class="k">if</span> <span class="n">row</span><span class="p">[</span><span class="s1">&#39;month&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="n">month</span> <span class="ow">and</span> <span class="n">row</span><span class="p">[</span><span class="s1">&#39;user_type&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Subscriber&#39;</span><span class="p">:</span>
                <span class="n">trips_Subs</span> <span class="o">+=</span> <span class="mi">1</span>
            <span class="k">if</span> <span class="n">row</span><span class="p">[</span><span class="s1">&#39;month&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="n">month</span> <span class="ow">and</span> <span class="n">row</span><span class="p">[</span><span class="s1">&#39;user_type&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Customer&#39;</span><span class="p">:</span>
                <span class="n">trips_Cust</span> <span class="o">+=</span> <span class="mi">1</span>
        
        <span class="c1"># create a total count        </span>
        <span class="n">trips_total</span> <span class="o">=</span> <span class="n">trips_Subs</span> <span class="o">+</span> <span class="n">trips_Cust</span>
        
        <span class="c1"># return the counted groups</span>
        <span class="k">return</span><span class="p">(</span><span class="n">trips_Subs</span><span class="p">,</span> <span class="n">trips_Cust</span><span class="p">,</span> <span class="n">trips_total</span><span class="p">)</span>

<span class="c1"># this loop will takes in month and outputs of &#39;monthly_trips&#39; function</span>
<span class="c1"># and output the monthly type of users.</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">months</span><span class="p">:</span>
    <span class="n">monthly_subs</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">monthly_trips</span><span class="p">(</span><span class="n">i</span><span class="p">)[</span><span class="mi">0</span><span class="p">])</span>
    <span class="n">monthly_cust</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">monthly_trips</span><span class="p">(</span><span class="n">i</span><span class="p">)[</span><span class="mi">1</span><span class="p">])</span>
    <span class="n">monthly_total</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">monthly_trips</span><span class="p">(</span><span class="n">i</span><span class="p">)[</span><span class="mi">2</span><span class="p">])</span>
<span class="c1">#optional test</span>
<span class="c1">#print(monthly_subs)</span>
<span class="c1">#print(monthly_cust)</span>
<span class="c1">#print(monthly_total)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[38]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># import necessary packages and functions</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="o">%</span> <span class="n">matplotlib</span> <span class="n">inline</span>

<span class="c1"># name all months for the x labels later</span>
<span class="n">month</span><span class="o">=</span><span class="p">(</span><span class="s1">&#39;Jan&#39;</span><span class="p">,</span><span class="s1">&#39;Feb&#39;</span><span class="p">,</span><span class="s1">&#39;Mar&#39;</span><span class="p">,</span><span class="s1">&#39;Apr&#39;</span><span class="p">,</span><span class="s1">&#39;May&#39;</span><span class="p">,</span><span class="s1">&#39;Jun&#39;</span><span class="p">,</span><span class="s1">&#39;Jul&#39;</span><span class="p">,</span><span class="s1">&#39;Aug&#39;</span><span class="p">,</span><span class="s1">&#39;Sept&#39;</span><span class="p">,</span><span class="s1">&#39;Oct&#39;</span><span class="p">,</span><span class="s1">&#39;Nov&#39;</span><span class="p">,</span><span class="s1">&#39;Dec&#39;</span><span class="p">)</span>

<span class="c1"># set up the x-ticks</span>
<span class="n">N</span><span class="o">=</span><span class="mi">12</span>
<span class="n">ind</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">arange</span><span class="p">(</span><span class="n">N</span><span class="p">)</span>
<span class="n">width</span> <span class="o">=</span><span class="mf">0.75</span>

<span class="c1"># set up the y-ticks</span>
<span class="n">heights_subs</span> <span class="o">=</span> <span class="n">monthly_subs</span>
<span class="n">heights_cust</span> <span class="o">=</span> <span class="n">monthly_cust</span>

<span class="c1"># plot the both bar charts </span>
<span class="n">bar_1</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">bar</span><span class="p">(</span><span class="n">ind</span><span class="p">,</span> <span class="n">heights_subs</span><span class="p">,</span> <span class="n">width</span><span class="o">=</span><span class="mf">0.75</span><span class="p">)</span>
<span class="n">bar_2</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">bar</span><span class="p">(</span><span class="n">ind</span><span class="p">,</span> <span class="n">heights_cust</span><span class="p">,</span> <span class="n">width</span><span class="o">=</span><span class="mf">0.75</span><span class="p">)</span>

<span class="c1"># set up the x and y ticks</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xticks</span><span class="p">(</span><span class="n">ind</span><span class="p">,</span> <span class="n">month</span><span class="p">,</span> <span class="n">fontsize</span> <span class="o">=</span> <span class="mi">12</span><span class="p">)</span> 
<span class="n">plt</span><span class="o">.</span><span class="n">yticks</span><span class="p">(</span><span class="n">fontsize</span><span class="o">=</span><span class="mi">16</span><span class="p">)</span>

<span class="c1"># set up the titles and axes</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Distribution of Rides per Month and By Rider Type&#39;</span><span class="p">,</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">23</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;Month&#39;</span><span class="p">,</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">20</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;Number of rides&#39;</span><span class="p">,</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">20</span><span class="p">)</span>

<span class="c1"># create a legend for the bar chart</span>
<span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">((</span><span class="n">bar_1</span><span class="p">[</span><span class="mi">0</span><span class="p">],</span> <span class="n">bar_2</span><span class="p">[</span><span class="mi">0</span><span class="p">]),</span> <span class="p">(</span><span class="s1">&#39;Subscribers&#39;</span><span class="p">,</span> <span class="s1">&#39;Customers&#39;</span><span class="p">),</span> <span class="n">fontsize</span><span class="o">=</span><span class="mi">9</span><span class="p">,</span> <span class="n">loc</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>

<span class="c1"># use the magic word to create the bar chart</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
ANC3b1/Pot16b2NIbJxzGw/vibzxDCds31sywxcDnXPiO8XXJXWMW5x67aR1u8rNxjnnnHOuTDyB
ajwnAi+Y2QuZ4Um7pazewFux/VMS11PSpjlxK6hu8zQHaAtsnxMHsM6dgc4555xrGE+gGoGkvoQk
KVv7BKEPqG6S9k3FdwCGxHElQ9aJAAAgAElEQVTpuNaEu/iSuFbAscBD8Q48gAcICdWwzHKGA7P9
DjznnHOu/LwNVOM4EVgF3JYzbgqh5/HJks6nuiNNAT9NgszseUl3AtdKak24k+40Qgecw1Jx70m6
Bhgt6RNgFiHJGkjoFsE555xzZeYJVJnFZOd44AEz+092vJmtkTQYGA/cALQjJFT7mdmCTPhI4Apg
LOFRLi8AB5vZrEzcxcCnwPepfpTLMWZ2b9lWzDnnnHNreQJVZma2EtiylpjFwKj4VyxuGXBe/CsW
t5qQZI0tqbDOuY3fmM3LNJ+Pag158cUXufDCC1m2bBkrVqzgqKOO4rzzip6+1po2bRqdO3fmq1/9
akNL6lyT8ATKOedcg3388ccMHz6cP/3pT2y//faYGQ899FCdp582bRq9evVq9ARq9erVBXsyd64U
3ojcOedcg913330MGTKE7bcPNwRLYtCgQfTq1WttzAEHHMD8+fOZM2cOe++9N/vttx+HHHIIixcv
ZuLEiVxxxRUMGDCA1atX8+tf/5o999yTPffcc+3DhCdOnMgxxxzDEUccQe/evXnggQcYOnQoO+20
E4888ggAL730EgcccAADBw7kmGOOYdmyZQBsu+22nH766Rx22GFMmzaNPfbYg/3224+RI0c28ZZy
GwuvgXLOOddgCxYsYJtttqlT7IMPPsjIkSM55ZRTWLNmDS1atGDEiBH06tWL4cOH8/7773P99dcz
Y8YMAHbffXeGDBkCwKpVq/jjH//IHXfcwQ9/+ENmzJjBSy+9xCWXXML+++/PGWecweTJk+nRowfX
XXcdN910E2eeeSbvvPMOF110ET169ODss89m7NixHHTQQWufr+dcqbwGyjnnXINts802vPXWW0Vj
kkeHjRw5kn/+858MGzaMq666ap24N998kz59+tCmTRvatGlDnz59mDcv9Miy6667AtC9e3f69OlD
y5Yt6d69O4sXhz6D58yZw4knnsiAAQO4/fbbeffddwHo1q0bPXr0AOD8889nypQpDBs2jJtvvrk8
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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a id='conclusions'></a></p>
<h2 id="Conclusions">Conclusions<a class="anchor-link" href="#Conclusions">&#182;</a></h2><p><strong>Question 7</strong>: Putting the bike share data aside, think of a topic or field of interest where you would like to be able to apply the techniques of data science. What would you like to be able to learn from your chosen subject?</p>
<p><strong>Answer</strong>: I would like to apply data science techniques to psychology. For example, I would like to apply predictive analytics to the language that schizophrenics use to detect when they are about to have a relapse.</p>
<blockquote><p><strong>Tip</strong>:</p>
<p>If you are working on this project via the Project Notebook page in the classroom, you can also submit this project directly from the workspace. <strong>Before you do that</strong>, you should save an HTML copy of the completed project to the workspace by running the code cell below. If it worked correctly, the output code should be a 0, and if you click on the jupyter icon in the upper left, you should see your .html document in the workspace directory. Alternatively, you can download the .html copy of your report following the steps in the previous paragraph, then <em>upload</em> the report to the directory (by clicking the jupyter icon).</p>
<p>Either way, once you've gotten the .html report in your workspace, you can complete your submission by clicking on the "Submit Project" button to the lower-right hand side of the workspace.</p>
</blockquote>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[41]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">subprocess</span> <span class="k">import</span> <span class="n">call</span>
<span class="n">call</span><span class="p">([</span><span class="s1">&#39;python&#39;</span><span class="p">,</span> <span class="s1">&#39;-m&#39;</span><span class="p">,</span> <span class="s1">&#39;nbconvert&#39;</span><span class="p">,</span> <span class="s1">&#39;Bike_Share_Analysis.ipynb&#39;</span><span class="p">])</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[41]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>255</pre>
</div>

</div>

</div>
</div>

</div>
    </div>
  </div>
</body>

 


</html>



## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/joleneyao/joleneyao.github.io/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/joleneyao/joleneyao.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
