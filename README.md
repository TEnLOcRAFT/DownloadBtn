# Download Button
Download Button Only With CSS!

## Installation
```
npm install @TEnLOcRAFT/DownloadBtn
```
```html
<link rel="stylesheet" href="" />
<link rel="stylesheet" href="https://code.ionicframework.com/ionicons/2.0.1/css/ionicons.min.css" />
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Varela+Round" />
```

## Usage
```html
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
```
