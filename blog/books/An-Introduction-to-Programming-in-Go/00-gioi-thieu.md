<!DOCTYPE html>
<html>
	<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title>An Introduction to Programming in Go - Giới thiệu lập trình bằng ngôn ngữ Go | LẬP TRÌNH</title>
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
				<h1 class="page-title">An Introduction to Programming in Go - Giới thiệu lập trình bằng ngôn ngữ Go</h1>
				<p><img src="http://www.golang-book.com/public/img/intro/cover.4194045234.png" alt="img" /></p>
<h2>Installers</h2>
<p>Tác giả không còn hỗ trợ installer nữa. Các cài đặt các bạn có thể xem online tại đây <a href="http://www.golang-book.com/guides/machine_setup">Machine Setup</a>.</p>
<h2>The Book</h2>
<p>An Introduction to Programming in Go.
Copyright © 2012 by Caleb Doxsey
ISBN: 978-1478355823</p>
<p>Quyển sách này không còn bán nữa, nhưng nó vẫn còn có thể <a href="http://www.golang-book.com/books/intro">đọc bản online</a> miễn phí  hoặc <a href="http://www.golang-book.com/public/pdf/gobook.3186517259.pdf">đọc bản PDF</a>. </p>
<p>Một bản cập nhật khác của quyển sách này đang có bán tại <a href="http://shop.oreilly.com/product/0636920046516.do">O'Reilly</a></p>
<p>Mọi thắc mắc, bình luận, đính chính và mối quan tâm các bạn có thể liên hệ trực tiếp tới [tác giả] <a href="mailto:admin@golang-book.com">Caleb Doxsey</a></p>
<p>Mục lục</p>
<ol>
<li>
<p>Bắt đầu</p>
<ul>
<li>Files và Folders</li>
<li>Terminal</li>
<li>Text Editors</li>
<li>Go Tools</li>
</ul>
</li>
<li>
<p>Chương trình đầu tiên</p>
<ul>
<li>Cách đọc một chương trình Go</li>
</ul>
</li>
<li>
<p>Kiểu dữ liệu</p>
<ul>
<li>Numbers</li>
<li>Strings</li>
<li>Booleans</li>
</ul>
</li>
<li>
<p>Variables</p>
<ul>
<li>Cách đặt tên biến</li>
<li>Tầm vực biến - Scope</li>
<li>Constants</li>
<li>Khai báo biến</li>
<li>Chương trình ví dụ</li>
</ul>
</li>
<li>
<p>Cấu trúc điều khiển</p>
<ul>
<li>For</li>
<li>If</li>
<li>Switch</li>
</ul>
</li>
<li>
<p>Arrays, Slices và Maps</p>
<ul>
<li>Arrays</li>
<li>Slices</li>
<li>Maps</li>
</ul>
</li>
<li>
<p>Functions</p>
<ul>
<li>Hàm thứ 2 của bạn</li>
<li>Return nhiều giá trị</li>
<li>Variadic Functions</li>
<li>Closure</li>
<li>Recursion</li>
<li>Defer, Panic &amp; Recover</li>
</ul>
</li>
<li>
<p>Con trỏ Pointers</p>
<ul>
<li>Operators * và &amp;</li>
<li>new</li>
</ul>
</li>
<li>
<p>Structs và Interfaces</p>
<ul>
<li>Structs</li>
<li>Methods</li>
<li>Interfaces</li>
</ul>
</li>
<li>
<p>Xử lí đồng thời Concurrency</p>
<ul>
<li>Goroutines</li>
<li>Channels</li>
</ul>
</li>
<li>
<p>Packages</p>
<ul>
<li>Tạo Packages</li>
<li>Tài liệu</li>
</ul>
</li>
<li>
<p>Testing</p>
</li>
<li>
<p>The Core Packages</p>
<ul>
<li>Strings</li>
<li>Input / Output</li>
<li>Files &amp; Folders</li>
<li>Errors</li>
<li>Containers &amp; Sort</li>
<li>Hashes &amp; Cryptography</li>
<li>Servers</li>
<li>Parsing Command Line Arguments</li>
<li>Synchronization Primitives</li>
</ul>
</li>
<li>
<p>Bước tiếp theo</p>
<ul>
<li>Study the Masters</li>
<li>Làm gì đó đi</li>
<li>Lập nhóm</li>
</ul>
</li>
</ol>
<h3>Lời người dịch</h3>
<p>Mình sẽ để đa số các từ ngữ chuyên ngành là tiếng Anh mà không dịch ra tiếng Việt để mọi người có thể nhớ được keyword cần thiết. Ví dụ như: File, Folder, Server, Client, Team, Input/Output,...</p>
<p>Nếu bạn có thể đọc tiếng Anh thì bạn có thể đọc trực tiếp sách của tác giả: <a href="http://www.golang-book.com/books/intro">http://www.golang-book.com/books/intro</a></p>
<p>Bài dịch cá nhân chỉ để lấy làm động lực để đọc hết quyển sách và tăng kĩ năng dịch thuật.  Chưa có hỏi qua ý kiến tác giả.</p>
<p>Người dịch
Trần Hoàng Phúc</p>
<hr />
<p>Source: <a href="http://www.golang-book.com/books/intro">http://www.golang-book.com/books/intro</a></p>				<p>---</p>
				Phuc Tran Hoang			</div>
			<div id="fb-root"></div>
<script async defer src="https://connect.facebook.net/en_GB/sdk.js#xfbml=1&version=v3.2&appId=&autoLogAppEvents=1"></script>

<div class="fb-comment-embed" data-href="http://hoangphuctv.github.io./blog/books/An-Introduction-to-Programming-in-Go/00-gioi-thieu.md?/mdb" data-width="100%" data-include-parent="false"></div>
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
