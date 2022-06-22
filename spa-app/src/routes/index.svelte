<script>
// import BlogArrow from "$components/Blog-Arrow.svelte";

import Icon from "../components/Icon.svelte";
import ArrowWithText from "../components/ArrowWithText.svelte";
// import ProjectsArrow from '$components/Projects-Arrow.svelte';
// import {
// faGithub as faGithub,
// faPinterest as faPinterest
// } from "@fortawesome/free-brands-svg-icons";
import {
faGlobeAmericas as faGlobe,
faRocket
} from "@fortawesome/free-solid-svg-icons";
</script>

<div class="fullscreen">
	<div id="top">
		<div class="contents">
      <img class="logo-and-title" src="/content/blog/images/logo_name.svg" alt="Gareth Williams" />
			<img class="logo" src="logo.svg" alt="logo" />
			<div class="home-title">
				<span style="font-weight: bolder;">Gareth</span>
				<span style="font-weight: lighter;">Williams</span>
			</div>
		</div>
	</div>
	<div id="bottom">
		<div class="contents">		
			<div class="quote">
				<span class="quote-text">'Ace, what a guy'</span> <span class="quote-author">- Anonymous</span>
			</div>

			<div class="social-container">
				<!-- <a
					href="https://github.com/Gaweph"
					class="btn-github icon-container"
					target="_blank"
					rel="external">
					<Icon class="large" icon={faGithub} />
					<span class="screen-reader-only">Gaweph on Github</span>
				</a> -->
        <!-- <a
					href="https://uk.pinterest.com/gaweph"
					class="btn-pinterest icon-container"
					target="_blank"
					rel="external">
					<Icon class="large" icon={faPinterest} />
					<span class="screen-reader-only">gaweph on Pinterest</span>
				</a>         -->
				<!-- <div class="btn-projects icon-container">          
					<a
						preload="true"
						href="projects"
						>
						<Icon class="large" icon={faRocket} />	
						<ProjectsArrow ref="projects-arrow" />
						<span class="screen-reader-only">Projects</span>
					</a>
        </div>		 -->
				<div class="btn-blog icon-container">
					<a
						preload="true"
						href="blog"
						>
						<Icon class="large" icon={faGlobe} />		
						<ArrowWithText ref="blog-arrow" />						
						<span class="screen-reader-only">Blog</span>
					</a>
				</div>
			</div>
		</div>
	</div>
</div>

<style lang="scss">

  $projects-color: #158ca9;
  $blog-color: #ed553b;
  $github-color: #191919;
  $pinterest-color: #cb2027;
  $underline-text-border-width: 0px; //1px

	.fullscreen {
		position: absolute;
		top:0px;
		bottom:0px;
		left:0px;
		right:0px;
	}

	.logo {
    height: 200px;
    max-width: 100%;
  }
  
  .logo-and-title
  {
    display: none;
    height: 100px;
    max-width: 100%;
  }

  #top,
  #bottom {
    position: relative;
    height: 50%;
  }

  .contents {
    position: absolute;
    width: 100%;
    margin: 0 auto;
    display: table;
    text-align: center;
  }

  #top {
    background-color: #222;
    .contents {
      bottom: 10px;
      color: #f5f5f5;
    }
  }
  
  #bottom {
    background-color: #f5f5f5;
    .contents {
      top: 10px;
      color: #222;
    }
  }
	  
  a,
  a:hover,
  a:focus {
    /* text-decoration: none; */
    border: none;
  }

  .social-container a {
    color: #ccc;
    fill: #ccc;
    stroke: #ccc;
    text-decoration: none;
  }

  .btn-github:hover,
  .btn-github:focus {
    color: $github-color;
  }
  .btn-pinterest:hover,
  .btn-pinterest:focus {
    color: $pinterest-color;
  }

  .btn-blog a:hover,
  .btn-blog a:focus {
    color: $blog-color;
    fill: $blog-color;
    stroke: $blog-color;
  }

  .btn-projects a:hover,
  .btn-projects a:focus {
    color: $projects-color;
    fill: $projects-color;
    stroke: $projects-color;
  }

  // :global([ref=projects-arrow]) {
  //   border-bottom: $underline-text-border-width solid $projects-color;
  // }
  
  // #blog-arrow {
  //   border-bottom: $underline-text-border-width solid $blog-color;
  // }

  .home-title {
    text-transform: uppercase;
    font-size: 4em;
  }

  .tagline, .quote {
    font-size: 1.2em;
  }

  .quote-text {
    font-style: italic
  }

  .social-container {
    font-size: 1.5em;
    letter-spacing: 0.2em;
    margin: 20px;
  }
  @media (max-width: 850px) {        
    .logo {
      height: 100px;
      max-width: 100%;
    }
    .home-title {
      font-size: 2em;
    }
    .tagline, .quote {
      font-size: 1em;
    }
    .fa-svelte {
      width: 1.2em;
      height: 1.2em;
    }
  }

  @media (max-height: 560px)
  {
    .logo {
      height: 100px;
      max-width: 100%;
    }
  }

  @media (max-height: 560px)
  {
    // Inline logo and name
    .logo-and-title {
      display: inline-block;
    }
    .logo, .home-title {
      display: none;
    }
  }

  .icon-container {
    position: relative;
    display: inline-block;
  }

  :global([ref=blog-arrow]) {
    height: 50px;
    position: absolute;
    top: 20px;
    margin-left: 5px;
  }
  
  :global([ref=projects-arrow]) {
      height: 100px;
      position: absolute;
      top: 20px;
      margin-left: -36px;
  }
  .screen-reader-only {
      position:absolute;
      width:1px;
      height:1px;
      padding:0;
      overflow:hidden;
      text-indent: -9999px;
  }
</style>