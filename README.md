# Download Button
Download Button Only With CSS!

### API Urls
```html
<link rel="stylesheet" href="" />
<link rel="stylesheet" href="https://code.ionicframework.com/ionicons/2.0.1/css/ionicons.min.css" />
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Varela+Round" />
```

### Usage
```html
<div style="body {
	margin: 0;
	padding: 0;
	background: #2D2F33;
	font-family: 'Varela Round', 'Ionicons';
}
::selection { background: #3F8EFC; color: #fff; }
a { text-decoration: none; }

.download {
	position: absolute;
	top: calc(50% - 30px);
	right: calc(50% - 115px);
	width: 230px;
	height: 60px;
	background-image: -webkit-linear-gradient(bottom, rgba(0,0,0,.075), rgba(255,255,255,.045));
	background-image: linear-gradient(to top, rgba(0,0,0,.075), rgba(255,255,255,.045));
    box-shadow: inset 0 -1px 0 rgba(0,0,0,.09),inset 0 1px 0 rgba(255,255,255,.04), 0 0 1px rgba(0,0,0,.3), 0 0 10px rgba(0,0,0,.1);
	border-radius: 100px;
	color: rgba(255,255,255,.9);
	line-height: 60px;
	text-align: center;
	letter-spacing: 5px;
	overflow: hidden;
	transition: all .3s cubic-bezier(.67,.13,.1,.81), transform .15s cubic-bezier(.67,.13,.1,.81);
}
.download:hover {
	right: calc(50% - 200px);
	width: 400px;
}
.download:active {
	transform: translateY(3px);
}
.download:before, .download:after {
	position: absolute;
	top: 0px;
	left: 0px;
	width: 100%;
	height: 100%;
	opacity: 1;
	transition: all .3s cubic-bezier(.67,.13,.1,.81);
}
.download:before {
	content: 'DOWNLOAD';
}
.download:after {
	content: 'Click to select a platform';
	top: -60px;
	opacity: 0;
}
.download:hover:after {
	top: 0px;
	opacity: 1;
}
.download:hover:before {
	top: 60px;
	opacity: 0;
}

.platforms {
	position: absolute;
	top: calc(50% - 100px);
	left: calc(50% - 290px);
	height: 200px;
	width: 580px;
	background: #fff;
	border-radius: 20px;
	visibility: hidden;
	transform: scale(.9);
	opacity: 0;
	overflow: hidden;
	transition: all .3s cubic-bezier(.67,.13,.1,.81);
}
.platforms:target {
	visibility: visible;
	transform: scale(1);
	opacity: 1;
}
.platforms a {
	position: absolute;
	top: 200px;
	left: 10px;
	width: 180px;
	height: 180px;
	border-radius: 10px;
	color: #3F8EFC;
	text-transform: uppercase;
	transition: top .5s cubic-bezier(.67,.13,.1,.81);
}
.platforms a:nth-child(1) {
	transition-delay: .1s;
}
.platforms a:nth-child(2) {
	left: 200px;
}
.platforms a:nth-child(3) {
	left: 390px;
	transition-delay: .1s;
}
.platforms:target a {
	top: 10px;
}
.platforms a:hover {
	background: #E5F4FF;
	box-shadow: 0 0 0 1px #A5CFFF;
}
.platforms a:before {
	content: attr(data-os);
	position: absolute;
	bottom: 0px;
	left: 0px;
	width: 100%;
	height: 60px;
	line-height: 60px;
	text-align: center;
}
.platforms a:after {
	position: absolute;
	top: 0px;
	left: 0px;
	width: 100%;
	height: 120px;
	line-height: 140px;
	text-align: center;
	font-size: 300%;
	transform: scale(1.25);
	transform-origin: center center;
}

.platforms a:nth-child(1):after {
	content: '\f247';
}
.platforms a:nth-child(2):after {
	content: '\f227';
}
.platforms a:nth-child(3):after {
	content: '\f2c5';
}

.installer {
	position: fixed;
	top: calc(50% - 150px);
	left: calc(50% - 300px);
	width: 600px;
	height: 300px;
	background: #fff;
	border-radius: 20px;
	visibility: hidden;
	transform: scale(.9);
	opacity: 0;
	transition: all .3s cubic-bezier(.67,.13,.1,.81);
}
.installer:target {
	visibility: visible;
	transform: scale(1);
	opacity: 1;
}
.installer a.back {
	position: absolute;
	top: 10px;
	left: 10px;
	width: 38px;
	height: 38px;
	line-height: 38px;
	text-align: center;
	font-size: 200%;
	color: #bbb;
}
.installer a.back:before {
	content: '\f129';
}
.installer a.back:after {
	content: 'Back';
	position: absolute;
	top: 7px;
	left: 30px;
	height: 20;
	line-height: 20px;
	font-size: 40%;
	text-align: center;
	color: #cacaca;
	border-radius: 5px;
	pointer-events: none;
	opacity: 0;
	transition: all .2s cubic-bezier(.67,.13,.1,.81);
}
.installer a.back:hover:after {
	left: 38px;
	opacity: 1;
}
.installer a.close {
	position: absolute;
	top: 40px;
	right: 40px;
	font-size: 200%;
	color: #bbb;
}
.installer a.close:before {
	content: '\f405';
}
.installer a.close:after {
	content: 'Close';
	position: absolute;
	top: 7px;
	right: 30px;
	height: 20px;
	line-height: 20px;
	font-size: 40%;
	text-align: center;
	color: #cacaca;
	border-radius: 5px;
	pointer-events: none;
	opacity: 0;
	transition: all .2s cubic-bezier(.67,.13,.1,.81);
}
.installer a.close:hover:after {
	right: 38px;
	opacity: 1;
}

.installer .info {
	position: absolute;
	top: 40px;
	left: 40px;
	height: calc(100% - 80px);
	width: 200px;
}
.installer .info:before {
	position: absolute;
	top: 0px;
	left: 0px;
	width: 180px;
	height: 220px;
	line-height: 220px;
	text-align: center;
	font-size: 1000%;
	color: #3F8EFC;
}
.installer .info:after {
	content: attr(data-weight);
	position: absolute;
	bottom: 0px;
	left: 0px;
	width: 180px;
	height: 60px;
	line-height: 60px;
	text-align: center;
	font-size: 100%;
	font-weight: bolder;
	letter-spacing: 2px;
	color: #aaa;
}
.installer#windows .info:before {
	content: '\f247';
}
.installer#mac .info:before {
	content: '\f227';
}
.installer#linux .info:before {
	content: '\f2c5';
}

.installer .details {
	position: absolute;
	top: 40px;
	right: 40px;
	height: 200px;
	width: calc(100% - 280px);
	padding: 10px;
}
.installer .details p {
	margin: 0px;
	font-weight: bolder;
	font-size: 120%;
	color: #444;
}
.installer .details span {
	color: #cacaca;
}
.installer .details ul {
	padding-left: 0px;
	list-style: none;
	color: #888;
}
.installer .details ul li {
	margin-left: 0px !important;
	margin-bottom: 8px;
	opacity: 0;
	transition: all .3s cubic-bezier(.67,.13,.1,.81);
}
.installer .details ul li:before {
	content: '';
	margin-right: 0;
}
.installer:target .details ul li {
	margin-left: 10px;
	opacity: 1;
}
.installer:target .details ul li:nth-child(1) {
	transition-delay: .1s;
}
.installer:target .details ul li:nth-child(2) {
	transition-delay: .2s;
}
.installer:target .details ul li:nth-child(3) {
	transition-delay: .3s;
}
.installer:target .details ul li:nth-child(4) {
	transition-delay: .4s;
}

.installer label {
	position: absolute;
	bottom: 20px;
	right: 90px;
	height: 40px;
	width: calc(100% - 320px);
	border-radius: 5px;
	overflow: hidden;
	cursor: pointer;
}
.installer label input {
	display: none;
}
.installer label span {
	position: absolute;
	height: 100%;
	width: 100%;
	line-height: 40px;
	text-align: center;
	color: #fff;
	background: #3F8EFC;
}
.installer label input:checked ~ span {
	background: #87E544;
	animation: downloadSuccess 3.1s ease;
}
.installer label span:after {
	content: 'DOWNLOAD';
	position: absolute;
	width: 80%;
	height: 100%;
	top: 0px;
	left: 10%;
}
.installer label input:checked ~ span:after {
	content: 'Thank you for download!';
	animation: downloadState 3s;
}
.installer label span:before {
	content: '';
	position: absolute;
	width: 100%;
	height: 100%;
	top: 0px;
	left: 0px;
	opacity: 0;
	background: rgba(255,255,255,.2);
}
.installer label input:checked ~ span:before {
	animation: downloadProgress 3s cubic-bezier(.67,.13,.1,.81);
}

@keyframes downloadSuccess {
	0%, 90% {
		background: #3F8EFC;
	}
	100% {
		background: #87E544;
	}
}

@keyframes downloadState {
	0%, 95% {
		content: 'DOWNLOADING...'
	}
	100% {
		content: 'Thank you for download!'
	}
}

@keyframes downloadProgress {
	0% {
		width: 5%;
		opacity: 1;
	}
	35% {
		width: 17%;
	}
	64% {
		width: 51%;
	}
	81% {
		width: 70%;
	}
	90% {
		width: 86%;
		opacity: 1;
	}
	100% {
		width: 100%;
		opacity: 0;
	}
}">
<a class="download" href="#platforms"></a>
<div class="platforms" id="platforms">
	<a href="#windows" data-os="windows"></a>
	<a href="#mac" data-os="mac"></a>
	<a href="#linux" data-os="linux"></a>
</div>
<div class="installer" id="windows">
	<div class="info" data-weight="349 KB"></div>
	<div class="details">
		<p>Windows installer</p>
		<span>Version 1.0.6</span>
		<ul>
			<li>The Original App.</li>
			<li>Created By: EitanBileski</li>
			<li>And Create With Batch</li>
			<li>And App Named: cmdMenuSel</li>		
		</ul>
	</div>
	<label for="progressWindows"><input type="radio" id="progressWindows"/><span></span></label>
	<a class="close" href="#"></a>
</div>
<div class="installer" id="mac">
	<div class="info" data-weight="296 KB"></div>
	<div class="details">
		<p>Mac installer</p>
		<span>Version 3.7.1</span>
		<ul>
			<li>The App Created By: EitanBiletski</li>
			<li>To Run The App Download Installer</li>
			<li>Then Drag The App To Apps Folder</li>
			<li>And Create ShortCut In Your Desktop</li>		
		</ul>
	</div>
	<label for="progressMac"><input type="radio" id="progressMac"/><span></span></label>
	<a class="close" href="#"></a>
</div>
<div class="installer" id="linux">
	<div class="info" data-weight="781 KB"></div>
	<div class="details">
		<p>Linux installer</p>
		<span>Version &beta;</span>
		<ul>
			<li>Linux Linux Linux</li>
			<li>The Installer For Linux Is BATA Version</li>
			<li>Enable To Download The App</li>
			<li>Only For: KALI-LINUX 8.5.2</li>		
		</ul>
	</div>
	<label for="progressLinux"><input type="radio" id="progressLinux"/><span></span></label>
	<a class="close" href="#"></a>
</div>
</div>
```
