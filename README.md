<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>崇明灶花</title>
	<style type="text/css">
		@import 'https://fonts.googleapis.com/css?family=Montserrat:300, 400, 700&display=swap';
	* {
		padding: 0;
		margin: 0;
		box-sizing: border-box;
	}
	html {
		font-size: 10px;
		font-family: 'Montserrat', sans-serif;
		scroll-behavior: smooth;
	}
	a {
		text-decoration: none;
	}
	.container {
		min-height: 100vh;
		width: 100%;
		display: flex;
		align-items: center;
		justify-content: center;
	}
	img {
		height: 100%;
		width: 100%;
		object-fit: cover;
	}
	p {
		color: black;
		font-size: 1.4rem;
		margin-top: 5px;
		line-height: 2.5rem;
		font-weight: 300;
		letter-spacing: .05rem;
	}
	p3{
			color: #485563;
			font-weight: bold;
		}
	p4{
		color: #ebe697;
		font-weight: bold;
		}
	.section-title {
		font-size: 4rem;
		font-weight: 400;
		color: black;
		margin-bottom: 10px;
		text-transform: uppercase;
		letter-spacing: .2rem;
		text-align: center;
	}
		
	.section-title span {
/*		color: crimson;*/
/*		#90a057 绿绿的*/
/*		#85ac9a 深绿*/
/*		#dbe8b0 浅绿*/
		color: #ebe697; 
	}

	.cta {
		display: inline-block;
		padding: 10px 30px;
		color: white;
		background-color: transparent;
		border: 3px solid #ebe697;
		font-size: 2rem;
		text-transform: uppercase;
		letter-spacing: .1rem;
		margin-top: 30px;
		transition: .3s ease;
		transition-property: background-color, color;
	}
	.cta:hover {
		color: white;
		background-color: #ebe697;
	}
	.brand h1 {
		font-size: 2rem;
		text-transform: uppercase;
		color: white;
	}
	.brand h1 span {
		color: #ebe697;
	}
	 .box {
     width: 1000px;
     height: 320px;
     margin: 45px auto;
     overflow: hidden;
     transition: all .3s;
	 }
	 .box li {
		 float: left;
		 position: relative;
		 width: 200px;
		 height: 320px;
		 transition: all .3s;
	 }
	 .box:hover li {
		 width: 90px;
	 }
	 .box li:hover {
		 width: 640px;
	 }

	/* Header section */
	#header {
		position: fixed;
		z-index: 1000;
		left: 0;
		top: 0;
		width: 100vw;
		height: auto;
	}
	#header .header {
		min-height: 8vh;
		background-color: rgba(31, 30, 30, 0.24);
		transition: .3s ease background-color;
	}
	#header .nav-bar {
		display: flex;
		align-items: center;
		justify-content: space-between;
		width: 100%;
		height: 100%;
		max-width: 1300px;
		padding: 0 10px;
	}
	#header .nav-list ul {
		list-style: none;
		position: absolute;
		background-color: rgb(31, 30, 30);
		width: 100vw;
		height: 100vh;
		left: 100%;
		top: 0;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		z-index: 1;
		overflow-x: hidden;
		transition: .5s ease left;
	}
	#header .nav-list ul.active {
		left: 0%;
	}
	#header .nav-list ul a {
		font-size: 2.5rem;
		font-weight: 500;
		letter-spacing: .2rem;
		text-decoration: none;
		color: white;
		text-transform: uppercase;
		padding: 20px;
		display: block;
	}
	#header .nav-list ul a::after {
		content: attr(data-after);
		position: absolute;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%) scale(0);
		color: rgba(240, 248, 255, 0.021);
		font-size: 13rem;
		letter-spacing: 50px;
		z-index: -1;
		transition: .3s ease letter-spacing;
	}
	#header .nav-list ul li:hover a::after {
		transform: translate(-50%, -50%) scale(1);
		letter-spacing: initial;
	}
	#header .nav-list ul li:hover a {
		color: #ebe697;
	}
	#header .hamburger {
		height: 60px;
		width: 60px;
		display: inline-block;
		border: 3px solid white;
		border-radius: 50%;
		position: relative;
		display: flex;
		align-items: center;
		justify-content: center;
		z-index: 100;
		cursor: pointer;
		transform: scale(.8);
		margin-right: 20px;
	}
	#header .hamburger:after {
		position: absolute;
		content: '';
		height: 100%;
		width: 100%;
		border-radius: 50%;
		border: 3px solid white;
		animation: hamburger_puls 1s ease infinite;
	}
	#header .hamburger .bar {
		height: 2px;
		width: 30px;
		position: relative;
		background-color: white;
		z-index: -1;
	}
	#header .hamburger .bar::after,
	#header .hamburger .bar::before {
		content: '';
		position: absolute;
		height: 100%;
		width: 100%;
		left: 0;
		background-color: white;
		transition: .3s ease;
		transition-property: top, bottom;
	}
	#header .hamburger .bar::after {
		top: 8px;
	}
	#header .hamburger .bar::before {
		bottom: 8px;
	}
	#header .hamburger.active .bar::before {
		bottom: 0;
	}
	#header .hamburger.active .bar::after {
		top: 0;
	}
	/* End Header section */

	/* Hero Section */
	#hero {
		background-image: url("images/bgimg3.png");
		background-size: cover;
		background-position: top center;
		position: relative;
		z-index: 1;
	}
	#hero::after {
		content: '';
		position: absolute;
		left: 0;
		top: 0;
		height: 100%;
		width: 100%;
		background-color: black;
		opacity: .3;
		z-index: -1;
	}
	#hero .hero {
/*		max-width: 1200px;*/
		max-width: 1000px;
		margin: 0 auto;
/*		padding: 0 50px;*/
		padding: 200px 50px 0px 20px;
		justify-content: flex-start;
	}
	#hero h1 {
		display: block;
		width: fit-content;
		font-size: 4rem;
		position: relative;
		color: transparent;
		animation: text_reveal .5s ease forwards;
		animation-delay: 1s;
	}
	#hero h1:nth-child(1) {
		animation-delay: 1s;
	}
	#hero h1:nth-child(2) {
		animation: text_reveal_name .5s ease forwards;
		animation-delay: 2s;
	}	
/*
	#hero h1:nth-child(2) {
		animation-delay: 2s;
	}
	#hero h1:nth-child(3) {
		animation: text_reveal_name .5s ease forwards;
		animation-delay: 3s;
	}
*/
	#hero h1 span {
		position: absolute;
		top: 0;
		left: 0;
		height: 100%;
		width: 0;
		background-color: #ebe697;
		animation: text_reveal_box 1s ease;
		animation-delay: .5s;
	}
	#hero h1:nth-child(1) span {
		animation-delay: .5s;
	}
	#hero h1:nth-child(2) span {
		animation-delay: 1.5s;
	}
/*
	#hero h1:nth-child(2) span {
		animation-delay: 1.5s;
	}
	#hero h1:nth-child(3) span {
		animation-delay: 2.5s;
	}
*/
	/* End Hero Section */

	/* Services Section */
	#services .services {
		flex-direction: column;
		text-align: center;
		max-width: 1500px;
		margin: 0 auto;
		padding: 100px 0px 0px 0px;
	}
	#services .service-top {
		max-width: 1000px;
		margin: auto;
	}
	#services .service-top h3{
		font-size: 2rem;
		line-height: 40px;
		text-align: justify;
		font-style: italic;
		font-weight: normal;
	}
	#services .service-top p{
		font-size: 2rem;
		line-height: 35px;
		text-align: justify;
	}	
	#services .service-bottom {
		display: flex;
		align-items: center;
		justify-content: center;
		flex-wrap: wrap;
		margin-top: 50px;
	}
	#services .service-item {
		flex-basis: 80%;
		display: flex;
		align-items: flex-start;
		justify-content: center;
		flex-direction: column;
		padding: 30px;
		border-radius: 10px;
		background-image: url(./img/img-1.png);
		background-size: cover;
		margin: 10px 5%;
		position: relative;
		z-index: 1;
		overflow: hidden;
	}
	#services .service-item::after {
		content: '';
		position: absolute;
		left: 0;
		top: 0;
		height: 100%;
		width: 100%;
		background-image: linear-gradient(60deg, #29323c 0%, #485563 100%);
		opacity: .9;
		z-index: -1;
	}
	#services .service-bottom .icon {
		height: 80px;
		width: 80px;
		margin-bottom: 20px;
	}
	#services .service-item h2 {
		font-size: 2rem;
		color: white;
		margin-bottom: 10px;
		text-transform: uppercase;
	}
	#services .service-item p {
		color: white;
		text-align: left;
	}
	/* End Services Section */

	/* Projects section */
	#projects .projects {
		flex-direction: column;
		max-width: 1000px;
		margin: 0 auto;
		padding: 100px 0px 0px 0px;
	}
	#projects p{
		font-size: 2rem;
		line-height: 35px;
		text-align: justify;
	}
	#projects .projects-header h1 {
		margin-bottom: 10px;
	}
	#projects .all-projects {
		display: flex;
		align-items: center;
		justify-content: center;
		flex-direction: column;
	}
	#projects .project-item {
		display: flex;
		align-items: center;
		justify-content: center;
		flex-direction: column;
		width: 80%;
		margin: 20px auto;
		overflow: hidden;
		border-radius: 10px;
	}
	#projects .project-info {
		padding: 30px;
		flex-basis: 50%;
		height: 100%;
		display: flex;
		align-items: flex-start;
		justify-content: center;
		flex-direction: column;
		background-image: linear-gradient(60deg, #29323c 0%, #485563 100%);
		color: white;
	}
	#projects .project-info h1 {
		font-size: 2rem;
		font-weight: 500;
	}
	#projects .project-info h2 {
		font-size: 1.8rem;
		font-weight: 500;
		margin-top: 10px;
	}
	#projects .project-info p {
		color: white;
	}
	#projects .project-img {
		flex-basis: 50%;
		height: 300px;
		overflow: hidden;
		position: relative;
	}
	#projects .project-img:after {
		content: '';
		position: absolute;
		left: 0;
		top: 0;
		height: 100%;
		width: 100%;
		background-image: linear-gradient(60deg, #29323c 0%, #485563 100%);
		opacity: .2;
	}
	#projects .project-img img {
		transition: .3s ease transform;
	}
	#projects .project-item:hover .project-img img {
		transform: scale(1.1);
	}
	/* End Projects section */

	/* About Section */
	#about .about {
		flex-direction: column-reverse;
		text-align: center;
		max-width: 1000px;
		margin: 0 auto;
		padding: -200px 20px -200px 20px;
	}
		#about img{
			width: 200px;
		}
		
	#about p{
		font-size: 2rem;
		line-height: 35px;
		text-align: justify;
	}
		
	#about .col-left {
		width: 150px;
		height: 360px;
	}
	#about .col-right {
		width: 100%;
	}
	#about h3{
		font-size: 2rem;
		line-height: 40px;
		text-align: justify;
		font-style: italic;
		font-weight: normal;
		max-width: 800px;
		
	}
	#about .col-right h2 {
		font-size: 1.8rem;
		font-weight: 500;
		letter-spacing: .2rem;
		margin-bottom: 10px;
	}
	#about .col-right p {
		margin-bottom: 20px;
	}
	#about .col-right .cta {
		color: black;
		margin-bottom: 50px;
		padding: 10px 20px;
		font-size: 2rem;
	}
	#about .col-left .about-img {
		height: 100%;
		width: 100%;
		position: relative;
		border: 10px solid white;
	}
	#about .col-left .about-img::after {
		content: '';
		position: absolute;
		left: -33px;
		top: 19px;
		height: 98%;
		width: 98%;
		border: 7px solid #ebe697;
		z-index: -1;
	}
	/* End About Section */

	/* contact Section */
	#contact .contact {
		flex-direction: column;
		max-width: 1000px;
		margin: 0 auto;
	}
		
	#contact p{
		font-size: 2rem;
		line-height: 35px;
		text-align: justify;
	}
		#contact img{
			width: 200px;
		}
	/*End contact Section */

	/* Footer */
	#footer {
		background-image: linear-gradient(60deg, #29323c 0%, #485563 100%);
	}
	#footer .footer {
		min-height: 200px;
		flex-direction: column;
		padding-top: 40px;
		padding-bottom: 30px;
	}
	#footer h2 {
		color: white;
		font-weight: 500;
		font-size: 1.8rem;
		letter-spacing: .1rem;
		margin-top: 10px;
		margin-bottom: 10px;
	}
	
	#footer p {
		color: white;
		font-size: 1.5rem;
		text-align: center;
	}
	/* End Footer */

	/* Keyframes */
	@keyframes hamburger_puls {
		0% {
			opacity: 1;
			transform: scale(1);
		}
		100% {
			opacity: 0;
			transform: scale(1.4);
		}
	}
	@keyframes text_reveal_box {
		50% {
			width: 100%;
			left: 0;
		}
		100% {
			width: 0;
			left: 100%;
		}
	}
	@keyframes text_reveal {
		100% {
			color: white;
		}
	}
	@keyframes text_reveal_name {
		100% {
			color: #ebe697;
			font-weight: 500;
		}
	}
	/* End Keyframes */

	/* Media Query For Tablet */
	@media only screen and (min-width: 768px) {
		.cta {
			font-size: 2.5rem;
			padding: 20px 60px;
		}
		h1.section-title {
			font-size: 4rem;
		}

		/* Hero */
		#hero h1 {
/*			font-size: 3rem;*/
			font-size: 7rem;
		}
		/* End Hero */

		/* Services Section */
		#services .service-bottom .service-item {
			flex-basis: 45%;
			margin: 2.5%;
		}
		/* End Services Section */

		/* Project */
		#projects .project-item {
			flex-direction: row;
		}
		#projects .project-item:nth-child(even) {
			flex-direction: row-reverse;
		}
		#projects .project-item {
			height: 400px;
			margin: 0;
			width: 100%;
			border-radius: 0;
		}
		#projects .all-projects .project-info {
			height: 100%;
		}
		#projects .all-projects .project-img {
			height: 100%;
		}
		/* End Project */

		/* About */
		#about .about {
			flex-direction: row;
		}
		#about .col-left {
			width: 400px;
			height: 400px;
			padding-left: 60px;
		}
		#about .about .col-left .about-img::after {
			left: -45px;
			top: 34px;
			height: 98%;
			width: 100%;
			border: 10px solid #ebe697;
		}
		#about .col-right {
			text-align: left;
			padding: 30px;
		}
		#about .col-right h1 {
			text-align: left;
		}
		/* End About */

		/* contact  */
		#contact .contact {
			flex-direction: column;
			padding: 100px 0;
			align-items: center;
			justify-content: center;
			min-width: 20vh;
		}
		#contact h3{
		font-size: 2rem;
		line-height: 40px;
		text-align: justify;
		font-style: italic;
		font-weight: normal;
		max-width: 800px;
	}
		#contact .contact-items {
			width: 100%;
			display: flex;
			flex-direction: row;
			justify-content: space-evenly;
			margin: 0;
		}
		#contact .contact-item {
			width: 30%;
			margin: 0;
			flex-direction: row;
		}
		#contact .contact-item .icon {
			height: 100px;
			width: 100px;
		}
		#contact .contact-item .icon img {
			object-fit: contain;
		}
		#contact .contact-item .contact-info {
			width: 100%;
			text-align: left;
			padding-left: 20px;
		}
		/* End contact  */
	}
	/* End Media Query For Tablet */

	/* Media Query For Desktop */
	@media only screen and (min-width: 1200px) {
		/* header */
		#header .hamburger {
			display: none;
		}
		#header .nav-list ul {
			position: initial;
			display: block;
			height: auto;
			width: fit-content;
			background-color: transparent;
		}
		#header .nav-list ul li {
			display: inline-block;
		}
		#header .nav-list ul li a {
			font-size: 1.8rem;
		}
		#header .nav-list ul a:after {
			display: none;
		}
		/* End header */

		#services .service-bottom .service-item {
			flex-basis: 22%;
			margin: 1.5%;
		}
	}
	/* End  Media Query For Desktop */

	</style>
</head>
	
<body>
  <!-- Header -->
  <section id="header">
    <div class="header container">
      <div class="nav-bar">
        <div class="brand">
          <a href="#hero"><h1>上海非遗之崇明灶花：<span>江畔风情，人间烟火</span></h1></a>
        </div>
        <div class="nav-list">
          <div class="hamburger"><div class="bar"></div></div>
          <ul>
            <li><a href="#hero" data-after="HOME">首页</a></li>
            <li><a href="#sec1" data-after="PAST">乡情“育”灶花</a></li>
            <li><a href="#projects" data-after="PRESENT">灶花何处“开”</a></li>
            <li><a href="#contact" data-after="FUTURE">灶花“别样红”</a></li>
          </ul>
        </div>
      </div>
    </div>
  </section>
  <!-- End Header -->


  <!-- Hero Section  -->
  <section id="hero">
    <div class="hero container">
      <div>  
		<h1>上海非遗之崇明灶花<span></span></h1>
	    <h1>江畔风情，人间烟火<span></span></h1>
        <a href="https://www.mugeda.com/client/content_preview.html?id=ace18196" type="button" class="cta" target="_blank">进入灶花VR博物馆</a>
      </div>
    </div>
  </section>
  <!-- End Hero Section  -->

  <!-- Service Section -->
  <section id="services">
    <div class="services container">
      <div class="service-top">
        <div style="float:left;margin-top: 11px;margin-left: -20px; width: 3px;height: 135px; background: darkgray;"></div>
        <h3>今天，如果问一个上海人“灶花是什么”，很可能会得到“不知道”的回答。崇明灶花是上海市首批市级非物质文化遗产，它并非草木之花，而是灶台上带有美好寓意的装饰图案，是乡情凝结而成的艺术之花。文化意涵丰富的灶花沉淀着上海最初的城市记忆，却在上海的高度城镇化中“逐渐枯萎”。<p3>面对“可沟通城市”的发展需要，如何理解灶花艺术的存在价值？如何让灶花以更加多元多样的形式在新时代“重新绽放”？</p3></h3>
		 <div id="sec1"><br><br><br><br><br><br></div>
		  <h1 class="section-title">乡情<span>“育”</span>灶花</h1>
		  <br><br>
		  <p>灶花的起源可以追溯到南宋时期，至今已有<p3>800多年历史</p3>。当时，崇明岛上建起盐场，大批囚犯被官府押至崇明烧盐。繁重的劳动之余，有人用烧盐时未燃尽的柴火在灶上涂画来自娱自乐。后来人们开始在岛上定居，这个习俗也被保留了下来。旧时的工匠们在绘制灶花时常常就地取材，将<p3>锅底深黑色的灰粉</p3>刮下，再用崇明老白酒将其调成黑色液体当作颜料用，因此灶花图案主要以黑色线条勾勒为主。建国后，随着社会经济的发展和生活水平的提高，人们在绘制灶花时开始追求艺术效果，于是彩色的灶花逐渐出现，并且图案形式也变得更加丰富多彩。</p><br><br>
		  <p>灶花曾在崇明十分流行，以<p3>“福、禄、寿、喜、财”</p3>五福图案为主，承载着劳动人民<p3>向往美好未来、追求幸福生活</p3>的祝愿，寓意着平安喜庆。</p>
			
		  <div>
			  <ul class="box">
				<li><img src="./images/福.jpg" alt=""></li>
				<li><img src="./images/禄.jpg" alt=""></li>
				<li><img src="./images/寿.jpg" alt=""></li>
				<li><img src="./images/喜.jpg" alt=""></li>
				<li><img src="./images/财.jpg" alt=""></li>
			   </ul>
			</div>
		  <br>
		  
			  	<p>今年已经69岁的黄汉生是崇明灶花这一市级非物质文化遗产的代表性传承人之一，他介绍说，画灶花要趁灶头刚砌好、<p3>泥灰半湿半干之际</p3>迅速完成。这样一气呵成画出的灶花，其色彩会渗透进潮湿的墙皮中，经风干和烘干后，<p3>日久光鲜依旧</p3>，历经几十年而不褪色。据说这和西洋湿壁画的原理是一样的。</p><br><br>
				<p>而黄汉生的灶花之路还要从40多年前说起。他自小便喜欢画画，后来跟着一个泥水匠师傅学习手艺。因为有点画画的基础，师傅就教他画灶花。对于人生的第一幅作品，他仍然历历在目。那是一幅“龙凤呈祥”，尽管师傅对爱徒的这幅作品十分满意，但黄汉生却觉得龙身上最重要的眼睛部分没有点出他想要的神采来。为了能够将灶花画得更加传神，当时每天只有两块工钱的他攒了三个月的钱，终于买了一台价值38块的红梅牌相机以及两卷胶卷。从此，他每次出门都会随身携带相机，以便将遇到的所有可以用作灶花素材的东西都拍下来。几年后，黄汉生成为了乡镇里远近闻名的灶花能手。</p><br><br>
				<p>2019年9月，黄汉生接到了一项重要任务——为即将在10月中旬召开的灶花艺术节画一幅解放前的向化老街。为了完成这个任务，黄汉生每天带着相机走街串巷地找当地老人询问向化老街当年的情形，用了整整40天才完成了一幅10米长卷。最终这幅运用灶花技法绘制而成的《向化老街》成为当年灶花艺术节上最引人注目的作品，被参观者誉为向化镇的“清明上河图”。</p><br><br><br>
			 	<video width="950px" controls="controls">
					<source src="images/intviewvideo2.mp4" type="video/mp4">
					Your browser does not support the video tag.
				</video> 						
      	 </div>		  
      </div>
  </section>
  <!-- End Service Section -->

  <!-- Projects Section -->
  <section id="projects">
    <div class="projects container">
      <div class="projects-header">
        <h1 class="section-title">灶花何处<span>“开”</span></h1>
		  <br><br>
		  <p>崇明灶花是上海重要的文化现象，是崇明乃至江浙沪地区农村灶文化的代表，<p3>见证着乡村面貌的变迁，承载着乡村生活的记忆</p3>。同时，崇明灶花也展现了当地人民<p3>乐观活泼、积极向上</p3>的精神状态和<p3>质朴勤勉、热爱生活</p3>的价值观念。因此灶花可以说是崇明岛民间文化最重要的一张名片。</p><br>
		  <p>然而，在<p3>城市化发展</p3>的背景下，灶花的传承与发展<p3>正面临困境</p3>。乡间农家烧饭做菜的<p3>土灶</p3>逐渐被全新的<p3>燃气灶</p3>所取代，作为<p3>灶花载体</p3>的传统灶头数量持续减少，<p3>灶花的需求量不断降低</p3>。同时乡里的年轻人们慢慢流向城市，灶花技艺的<p3>传承人数量大幅减少</p3>。据统计，目前崇明区的灶花传承人共有73人，其中年龄最小的也有45岁，年龄最大的近百岁。另外，伴随着<p3>生产工艺的进步</p3>、生活水平的提高，人们审美观念发生转变，替代灶花的装饰品涌现。即使是家里有灶头的乡间人家，也倾向于购买已经<p3>印有图案的瓷砖</p3>来装饰灶头，而非请灶花师傅绘制图案。</p><br>		  
		  <p>自从国家开展非物质文化遗产的保护工作以来，<p3>崇明的文化部门</p3>十分重视对灶花艺术的<p3>抢救与传承</p3>。</p><br><br><br>			
      </div>
		
      <div class="all-projects">
        <div class="project-item">
          <div class="project-info">
            <h1>崇明文化部门收集现存的灶花作品，进行拍摄与保存，设立艺术档案，并建成了一个具有相当规模的<p4>灶文化博物馆</p4>。</h1>
          </div>
          <div class="project-img">
            <img src="images/博物馆.jpg" alt="img">
          </div>
        </div>
        <div class="project-item">
          <div class="project-info">
            <h1>为了更好地宣传与弘扬灶花艺术，向化镇从2005年起每年举办<p4>灶花大赛</p4>，成立了<p4>灶文化研究协会</p4>。</h1>            
          </div>
          <div class="project-img">
            <img src="images/大赛.jpg" alt="img">
          </div>
        </div>
        <div class="project-item">
          <div class="project-info">
            <h1>为了能吸引更多当地年轻人加入灶花传承队伍，向化镇还与<p4>镇上中学的美术班</p4>进行联系，在其开设的美术课中增加有关灶花的知识和对于绘制特点的讲解。</h1>
          </div>
          <div class="project-img">
            <img src="images/学校.jpg" alt="img">
          </div>
        </div>        
      </div>
		
	  <br><br><br><p>然而，<p3>效果却不容乐观</p3>。灶花的绘制看似行云流水、一气呵成，既不打草稿，中间也不会停留修改，但其背后却是<p3>积年累月的实践历练</p3>。在过去，崇明就业机会少，当一个泥瓦匠以灶花谋生或许算是一个不错的选择，但在<p3>就业机会良多与日趋减少的灶花需求</p3>面前，年轻人也只能打退堂鼓。我们在向化镇采访到了一位民一中学的初一学生，他说：“今年学校组织过画灶花，美术和科学老师教的，每个年级都画了。”但是他也表示自己对灶花的了解<p3>仅限于学校组织的活动</p3>，也没有参观过灶花博物馆。</p><br><br>
	  <p>可以发现，崇明县文化部门的确重视灶花，通过各项实际措施保护和传承灶花艺术，尝试在城市化发展的新时期为灶花找到更多的<p3>载体和受众</p3>，让更多的人了解灶花艺术。正如这位学生在学校里学习过画灶花，灶花艺术在崇明向化的孩子心中多少会留下印记，增强他们对这片<p3>土地的归属感</p3>和对<p3>传统艺术的情感</p3>。但是，如果要继续扩大灶花的影响力，让这一民间艺术走出向化镇、走出崇明岛，赢得更多人的喜爱，传统的宣传方式恐怕还是不够的，势必要在图案、载体上进行创新。</p><br><br>
	  <p>事实上，灶花创作者们也确实在努力<p3>跟上时代潮流</p3>，在保留灶花特点的前提下进行创新，以适应乡村城市化的趋势。除了继承原本寓意喜庆、企盼和谐、追求美满、向往富足、祈求幸福的吉祥图案外，一批批<p3>拥抱新时代、体现新气象、反映新生活</p3>的灶花作品也出现在人们的视野中，如代表着前景广阔的火车疾驰、代表科技发达的卫星升天、代表城乡繁荣的高楼林立等。也有灶花创作者将<p3>传统图案与时事发展</p3>相结合，创造出一幅幅<p3>古今交织、虚实交融</p3>的优秀作品，如孙悟空在云端眺望长江口大桥的落成，金凤凰从鸟巢体育馆中飞出等等。</p><br><br>
	  <p>除了图案内容上的变化，黄汉生在采访中也提到，现在的灶花载体更加丰富了。乡镇政府鼓励他们这些灶花艺术家在<p3>街道墙面</p3>上创作装饰画，当地一些酒店也会请他们在<p3>店内墙上</p3>绘制灶花。而<p3>“灶花上墙”</p3>给予了灶花艺术更多的应用场景，还证明了灶花艺术独特的魅力。</p><br><br><br>

    </div>
  </section>
  <!-- End Projects Section -->

  <!-- Contact Section -->
  <section id="contact">
    <div class="contact container">
		<h1 class="section-title">灶花 <span>“别样红”</span></h1>
       <br><br><p>部分人认为灶花仅仅是一种农业社会的产物，其审美趣味已经与现代社会脱节，被放置在博物馆中作为历史文化供人参观学习就可以了。但<p3>城市的历史</p3>若能铭刻在城市空间、镶嵌于当下日常生活，就能连接起过去和现在，让现实对话传统，给城市创造独一无二的景观。城市并非孤立地存在，而是与社区、乡村之间形成了<p3>多维的连接</p3>。</p><br><br>
		<p>我们有理由相信，城市的发展对于灶花艺术的影响，绝不仅仅是负面的。上海这座城市以现代化、国际化闻名，但同样也充满<p3>包容性</p3>，具有历史底蕴。乡村与城市不可避免地存在审美和生活方式的差异，我们需要尊重这种差异，理解灶花存在的意义。崇明灶花代表的是上海的<p3>乡土文化</p3>，对于颇受欢迎的海派风格、国际元素是一种很好的补充，其丰富的内涵、特别的形式也完全可能成为当代流行风潮的灵感来源。</p><br><br>
		<p>那么灶花是否可以脱离灶台样式的束缚，以更加多元多样的方式存在，从而成为城市的一部分？在历史上的不同时期，灶花是有所发展、有所变化的，那么在一些人眼中显得“老土”的灶花，是否能够容纳更具活力和新意的图像呢？目前，崇明灶花的内容主题与呈现形式不适应时代与技术的发展，这也导致灶花的受众很大部分都是情怀与兴趣使然的年纪长者，没有真正获得广大青少年的认可。要真正打入年轻人的群体，灶花还需要以<p3>年轻人喜闻乐见</p3>的方式和<p3>符合时代发展</p3>的主题去赢得关注。</p><br><br>
		<p>数字技术也许是解决问题的一个方法。城市从来不是一个简单的“经济体”，它也是<p3>文化的创造与存储的空间</p3>，是<p3>结合实体与虚拟空间的纽带</p3>。应用动作捕捉技术的土家族传统仪式“撒叶儿嗬”、应用虚拟现实（VR）全景视频的扬州木偶戏、应用全息影像的蒙古族筷子舞、应用直播的木活字印刷等，这些“技术+非遗”的组合给我们以启发。</p><br><br>
		<br><br>
		
		
    </div>
  </section>
  <!-- End Contact Section -->
	
<!-- About Section -->
  <section id="about">
    <div class="about container">
      <div class="col-left">
        <div class="about-img">
          <img src="images/vrgif.gif" alt="vrGIF">
        </div>
      </div>
      <div class="col-right">
		  <p>利用<p3>数字手段</p3>对灶花艺术进行分析、解构、重塑，采用新形式，结合<p3>网络</p3>进行传播，也许就能推动古老的灶花艺术走向新生。例如，建立<p3>VR博物馆</p3>，将承载着记忆与情感的线下场所在互联网上“重现”，让灶花艺术“触手可及”，拉近用户和灶花的距离，便于传播；或是通过<p3>H5技术</p3>允许用户拖拽各类灶花图案元素进行排版设计、个性填色，辅助<p3>增强现实（AR）</p3>等技术，将用户自行设计的图案投映在平面上，甚至进行互动，提高趣味性和智能性，吸引用户的关注，在新的历史条件下展现传统文化魅力。</p>
		<br><br>
      </div>
    </div><br><br><br>	
	  <div align="center">
		  <br><br><br><br><br>
			<hr width="800px" size=2 color=black style="FILTER: alpha(opacity=100,finishopacity=0,style=3)"> 
			<br><br><br>
			 <h3>崇明灶花诞生至今，经过了800余年的风风雨雨，见证了时代的变迁与社会的变革，成为了<p3>本土文化</p3>的一部分。所以，保护这一非物质文化遗产，不仅是在保护一种装饰图案和绘画技艺，更是在<p3>熟悉一段永不褪色的历史、了解一个代代相传的故事、体会一份难以割舍的情怀、继承一种历久弥新的精神</p3>。灶花对我们、对地区、对城市的意义莫过于此。增强上海的<p3>城市沟通力</p3>，就需要为这座国际化大都市留住自己的<p3>文化符号和历史记忆</p3>，为这朵美丽的“艺术之花”拭去灰尘，使其<p3>焕发生机、再次绽放</p3>！</h3><br><br>
    </div><br><br><br>	
  </section>
  <!-- End About Section -->
	
  <!-- Footer -->
  <section id="footer">
    <div class="footer container">
      <p>制作团队：<br>马冬平、孟繁羽、王静颐、谢沁伶（姓名首字母排列）<br>
		复旦大学新闻学院2020级新媒体专业硕士<br>
		全媒体内容生产课程作品</p><br>
      <p>资料来源：<br>
		  [1]孙玮.可沟通:构建现代城市社会传播网络[J].探索与争鸣,2016(12):31-33.<br>
[2]复旦大学信息与传播研究中心课题组,谢静.可沟通城市:网络社会的新城市主张[J].新闻与传播研究,2015,22(07):16-24+126.<br>
[3]复旦大学信息与传播研究中心课题组,谢静,潘霁,孙玮.可沟通城市评价体系[J].新闻与传播研究,2015,22(07):25-34+126.<br>
		  [4]顾锦春.崇明灶花民俗艺术保护与传承的思考[J].上海农村经济,2020(08):34-36.<br>
		  [5]柴焘熊.乡间诗意的沉淀——崇明灶花[M].上海文艺出版社,2016.<br>
		  [6]柴焘熊、程宣猷等.崇明灶花诗词篇[M].文汇出版社,2011.<br>
		  [7]黄汉生、张伦、龚德文等.崇明灶花作品集[M].文汇出版社,2011.<br>
		  部分图片来自网络<br></p><br>
	  <p>特别感谢：<br>崇明区文化馆<br>崇明区向化镇灶文化博物馆<br>灶花代表性传承人-黄汉生<br>崇明区非物质文化遗产办公室-姜中其</p><br><br>
    </div>
  </section>
  <!-- End Footer -->
  <script src="./app.js"></script>
</body>
</html>
