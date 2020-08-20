<!DOCTYPE html>
<html>
	<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title>http://www.golang-book.com/books/intro/7 | LẬP TRÌNH</title>
	<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/yegor256/tacit@gh-pages/tacit-css.min.css"/>
	<!-- Global site tag (gtag.js) - Google Analytics -->
	<script async src="https://www.googletagmanager.com/gtag/js?id="></script>
	<script>
	  window.dataLayer = window.dataLayer || [];
	  function gtag(){dataLayer.push(arguments);}
	  gtag('js', new Date());

	  gtag('config', '');
	</script>

</head>
	<body>
		<div class="container">
	<h2><a class="navbar-brand mr-auto mr-lg-0" href="/">LẬP TRÌNH</a></h2>

	<script>
	  function search_submit(){
		  var q = document.body.querySelector('#text-q');
		  console.log(q )
		  q.value = q.value + " site:" + location.hostname;
		  return true;
	  };
	</script>
	<form class="form-inline my-2 my-lg-0" id="frmsearch" action="https://google.com/search" onsubmit="search_submit(this)">
		<input class="form-control mr-sm-2" name="q" id="text-q" type="text" placeholder="Search on google" aria-label="Search">
	    <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
	  </form>

	<p class="separator"></p>
</div>
		<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/github-markdown-css/3.0.1/github-markdown.min.css">
		<div class="container">
			<div class="markdown-body">
				<h1 class="page-title">http://www.golang-book.com/books/intro/7</h1>
								<p>---</p>
				Phuc Tran Hoang			</div>
			<div id="fb-root"></div>
<script async defer src="https://connect.facebook.net/en_GB/sdk.js#xfbml=1&version=v3.2&appId=&autoLogAppEvents=1"></script>

<div class="fb-comment-embed" data-href="http://hoangphuctv.github.io./blog/books/An-Introduction-to-Programming-in-Go/07-functions.md?/mdb" data-width="100%" data-include-parent="false"></div>
		</div>
		<br/>
		<div class="container">
			<hr>
						<div class="my-3 p-3 bg-white rounded shadow-sm">
	<h6 class="border-bottom border-gray pb-2 mb-0">Các bài viết khác</h6>
		<div class="media text-muted pt-3">
		<p class="media-body pb-3 mb-0 small lh-125 border-bottom border-gray">
		<strong class="d-block text-gray-dark">
			<a href="/blog/books/An-Introduction-to-Programming-in-Go/00-gioi-thieu.md">An Introduction to Programming in Go - Giới thiệu lập trình bằng ngôn ngữ Go</a>
		</strong>
		<br>
		<small>Phuc Tran Hoang</small>
		<small></small>
		</p>
	</div>
		<div class="media text-muted pt-3">
		<p class="media-body pb-3 mb-0 small lh-125 border-bottom border-gray">
		<strong class="d-block text-gray-dark">
			<a href="/blog/books/An-Introduction-to-Programming-in-Go/01-bat-dau.md">Bắt đầu</a>
		</strong>
		<br>
		<small>Phuc Tran Hoang</small>
		<small></small>
		</p>
	</div>
		<div class="media text-muted pt-3">
		<p class="media-body pb-3 mb-0 small lh-125 border-bottom border-gray">
		<strong class="d-block text-gray-dark">
			<a href="/blog/books/An-Introduction-to-Programming-in-Go/02-chuong-trinh-dau-tien-cua-ban.md">Chương trình đầu tiên của bạn</a>
		</strong>
		<br>
		<small>Phuc Tran Hoang</small>
		<small></small>
		</p>
	</div>
		<div class="media text-muted pt-3">
		<p class="media-body pb-3 mb-0 small lh-125 border-bottom border-gray">
		<strong class="d-block text-gray-dark">
			<a href="/blog/books/An-Introduction-to-Programming-in-Go/03-kieu-du-lieu.md">Kiểu dữ liệu - Types</a>
		</strong>
		<br>
		<small>Phuc Tran Hoang</small>
		<small></small>
		</p>
	</div>
		<div class="media text-muted pt-3">
		<p class="media-body pb-3 mb-0 small lh-125 border-bottom border-gray">
		<strong class="d-block text-gray-dark">
			<a href="/blog/books/An-Introduction-to-Programming-in-Go/04-bien.md">http://www.golang-book.com/books/intro/4</a>
		</strong>
		<br>
		<small>Phuc Tran Hoang</small>
		<small></small>
		</p>
	</div>
		<div class="media text-muted pt-3">
		<p class="media-body pb-3 mb-0 small lh-125 border-bottom border-gray">
		<strong class="d-block text-gray-dark">
			<a href="/blog/books/An-Introduction-to-Programming-in-Go/05-cau-truc-dieu-khien.md">http://www.golang-book.com/books/intro/5</a>
		</strong>
		<br>
		<small>Phuc Tran Hoang</small>
		<small></small>
		</p>
	</div>
		<div class="media text-muted pt-3">
		<p class="media-body pb-3 mb-0 small lh-125 border-bottom border-gray">
		<strong class="d-block text-gray-dark">
			<a href="/blog/books/An-Introduction-to-Programming-in-Go/06-arrays-slices-va-maps.md">http://www.golang-book.com/books/intro/6</a>
		</strong>
		<br>
		<small>Phuc Tran Hoang</small>
		<small></small>
		</p>
	</div>
		<div class="media text-muted pt-3">
		<p class="media-body pb-3 mb-0 small lh-125 border-bottom border-gray">
		<strong class="d-block text-gray-dark">
			<a href="/blog/books/An-Introduction-to-Programming-in-Go/07-functions.md">http://www.golang-book.com/books/intro/7</a>
		</strong>
		<br>
		<small>Phuc Tran Hoang</small>
		<small></small>
		</p>
	</div>
		<div class="media text-muted pt-3">
		<p class="media-body pb-3 mb-0 small lh-125 border-bottom border-gray">
		<strong class="d-block text-gray-dark">
			<a href="/blog/books/An-Introduction-to-Programming-in-Go/08-con-tro.md">http://www.golang-book.com/books/intro/8</a>
		</strong>
		<br>
		<small>Phuc Tran Hoang</small>
		<small></small>
		</p>
	</div>
		<div class="media text-muted pt-3">
		<p class="media-body pb-3 mb-0 small lh-125 border-bottom border-gray">
		<strong class="d-block text-gray-dark">
			<a href="/blog/books/An-Introduction-to-Programming-in-Go/09-struct-va-interface.md">http://www.golang-book.com/books/intro/9</a>
		</strong>
		<br>
		<small>Phuc Tran Hoang</small>
		<small></small>
		</p>
	</div>
		<div class="media text-muted pt-3">
		<p class="media-body pb-3 mb-0 small lh-125 border-bottom border-gray">
		<strong class="d-block text-gray-dark">
			<a href="/blog/books/An-Introduction-to-Programming-in-Go/10-concurrency.md">http://www.golang-book.com/books/intro/10</a>
		</strong>
		<br>
		<small>Phuc Tran Hoang</small>
		<small></small>
		</p>
	</div>
		<div class="media text-muted pt-3">
		<p class="media-body pb-3 mb-0 small lh-125 border-bottom border-gray">
		<strong class="d-block text-gray-dark">
			<a href="/blog/books/An-Introduction-to-Programming-in-Go/11-package.md">http://www.golang-book.com/books/intro/11</a>
		</strong>
		<br>
		<small>Phuc Tran Hoang</small>
		<small></small>
		</p>
	</div>
		<div class="media text-muted pt-3">
		<p class="media-body pb-3 mb-0 small lh-125 border-bottom border-gray">
		<strong class="d-block text-gray-dark">
			<a href="/blog/books/An-Introduction-to-Programming-in-Go/12-testing.md">http://www.golang-book.com/books/intro/12</a>
		</strong>
		<br>
		<small>Phuc Tran Hoang</small>
		<small></small>
		</p>
	</div>
		<div class="media text-muted pt-3">
		<p class="media-body pb-3 mb-0 small lh-125 border-bottom border-gray">
		<strong class="d-block text-gray-dark">
			<a href="/blog/books/An-Introduction-to-Programming-in-Go/13-core-package.md">http://www.golang-book.com/books/intro/13</a>
		</strong>
		<br>
		<small>Phuc Tran Hoang</small>
		<small></small>
		</p>
	</div>
		<div class="media text-muted pt-3">
		<p class="media-body pb-3 mb-0 small lh-125 border-bottom border-gray">
		<strong class="d-block text-gray-dark">
			<a href="/blog/books/An-Introduction-to-Programming-in-Go/14-cac-buoc-ke-tiep.md">http://www.golang-book.com/books/intro/14</a>
		</strong>
		<br>
		<small>Phuc Tran Hoang</small>
		<small></small>
		</p>
	</div>
	</div>					</div>

		<div class="container footer">
	<hr>
	<div class="row">
		<div class="col-12">
			<p class="text-center"> &copy; Phuc Tran Hoang 2019 | Powered by <a href="https://github.com/hoangphuctv/mdblog">mdblog</a> & Github</p>
		</div>
	</div>
</div>
<style>
	pre {border-left:1.8px solid #275a90;}
	code {color:#275a90;}
	.container {width: 1024px; margin:0 auto;}
</style>	</body>
</html>
