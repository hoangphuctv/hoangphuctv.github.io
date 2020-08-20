<!DOCTYPE html>
<html>
	<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title>Redirect - Chuyển hướng trang bằng PHP | LẬP TRÌNH</title>
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
				<h1 class="page-title">Redirect - Chuyển hướng trang bằng PHP</h1>
				<p>Trong việc lập trình web bạn không thể thiếu việc chuyển người dùng từ trang này qua trang kia. Ví dụ như sau khi login thì chuyển người dùng về trang chủ. Hoặc vào các nội dung cần xác thực thì phải chuyển người dùng về trang login.</p>
<h2>1. Chuyển trang bằng HTTP header</h2>
<p>PHP hỗ trợ chuyển trang bằng cách trả về <a href="https://en.wikipedia.org/wiki/HTTP_location">HTTP header Location</a> theo đặc tả của <a href="https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol">giao thức HTTP</a>. Khi trình duyệt nhận được response từ server có HTTP header &quot;Location&quot; thì trình duyệt sẽ tự động chuyển hướng đến url được chỉ định.</p>
<p>HTTP header:</p>
<pre><code>Location: &lt;new_URL&gt;</code></pre>
<p>Cách thực hiện đơn giản như sau.</p>
<pre><code class="language-php">&lt;?php 
// các xử lí
// Tiến hành chuyển hướng
header("Location: /index.php");
exit;

// có thể các còn các xử lí khác không được thực hiện.
?&gt;</code></pre>
<p>Trường hợp bạn muốn chuyển hướng ra trang ngoài không phải trang hiện tại của bạn. Thì bạn hãy để đầy đủ đường dẫn URL.</p>
<pre><code class="language-php">&lt;?php 
header("Location: https://google.com");
exit;</code></pre>
<h3>Các lỗi thường gặp khi sử dụng chuyển hướng bằng header</h3>
<h4>Lỗi 1: <code>Warning: Cannot modify header information</code></h4>
<p>Khi thực hiện chuyển trang bằng cách này. Tức là bạn đang thay đổi các giá trị HTTP header mặc định. Rất có thể bạn sẽ bị thông báo lỗi khi sau: <code>Warning: Cannot modify header information</code>. Để khác phục được lỗi này. Bạn cần hiểu bản chất vấn được được giải thích như sau. <strong>Nếu bạn đang gấp Bỏ qua cách chuyển hướng này và sử dụng các cách chuyển hướng ở bên dưới.</strong></p>
<p>Giải thích:</p>
<p>Theo đặc tả một gói tin HTTP có cấu trúc như sau:</p>
<pre><code>HEADER
&lt;cách 2 dòng&gt;
BODY</code></pre>
<p>Mỗi dấu xuống dòng ở trên là cặp kí tự <code>\r\n</code>;</p>
<p>Ví dụ khi bạn xuất dòng chữ &quot;Hello world&quot;.
File hello.php</p>
<pre><code>&lt;?php
echo "Hello world";</code></pre>
<p>Thì cấu trúc của gói tin trả về như sau: </p>
<pre><code>HTTP/1.1 200 OK
Server: nginx/1.17.6
Content-Type: text/html
Connection: keep-alive

Hello world</code></pre>
<p>Dòng header khác này, có thể có hoặc không có, hoặc có nhiều hơn các thông tin - chỉ thị khác. Vì vậy trong các ví dụ sau mình giảm bớt các dòng header không liên quan tới nội dung bài viết.</p>
<pre><code>Server: nginx/1.17.6
Content-Type: text/html
Connection: keep-alive</code></pre>
<p>Nếu chúng ta đặt lệnh header phía trước lệnh echo sẽ thành ra như thế này:</p>
<pre><code>&lt;?php
header("Location: /index.php");
echo "Hello world";
</code></pre>
<p>Thì cấu trúc của gói tin trả về như sau: </p>
<pre><code>HTTP/1.1 200 OK
Location: /index.php

Hello world</code></pre>
<p>Vậy nếu ta đổi ngược 2 lệnh trên. Thì kết quả sẽ được như sau:</p>
<pre><code>&lt;?php
echo "Hello world";
header("Location: /index.php");</code></pre>
<p>Chúng ta sẽ bị lỗi <code>Warning: Cannot modify header information</code>;
Nhưng trong trường hợp tắt warning, website vẫn chạy được.</p>
<p>Trong các trường hợp thực tế, ta hay để code php bên trong đoạn mở <html> như sau:</p>
<pre><code>&lt;html&gt;
&lt;?php
// xử lí ...
header("Location: /index.php");
?&gt;</code></pre>
<p>Như vậy ta cũng bị lỗi  <code>Warning: Cannot modify header information</code>;</p>
<blockquote>
<p>Chúng ta phải đảm bảo các lệnh <code>header</code> được gọi trước tất cả các output khác.</p>
</blockquote>
<h4>Lỗi 2: <code>ERR_TOO_MANY_REDIRECTS</code></h4>
<p>Một lỗi thứ 2 thường bị khi sử dụng cách này là lỗi <code>ERR_TOO_MANY_REDIRECTS</code> thường thấy mã lỗi này trên Chrome. Ở các trình duyệt khác, hình thức hiện lỗi có thể khác. <strong>Nguyên nhân lỗi là bị điều hướng liên tục.</strong> </p>
<p>Ví dụ như trình duyệt đang ở trang index.php, nhưng lại có lệnh <code>header("Location: /index.php");</code>. Vậy là khi ta vào trang index.php lại bị đá về index.php, liên tục như vậy. Đến một số lần quy định, Chrome sẽ không thèm chuyển hướng theo chỉ thị Location header nữa. Mà báo ra lỗi này.</p>
<p>Để giải quyết, chúng ta phải check điều kiện chuyển trang. <strong>Nếu đang ở trang hiện tại, thì không được chuyển nữa.</strong> Ví dụ như URL hiện tại của chúng ta là <code>http://localhost/index.php</code> thì ta phải kiểm tra thông tin <code>$_SERVER['REQUEST_URI']</code> cho ta được đoạn sau domain <code>/index.php</code>.</p>
<pre><code>&lt;?php
// file index.php
if ($_SERVER['REQUEST_URI'] != '/index.php') {
    header('Location: /index.php');
}</code></pre>
<p>Nhưng các bạn tự lưu ý là, đối với index.php là 1 trường hợp khá đặc biệt. Vì chúng ta vào url <code>http://localhost/</code> thì thông thường cũng là truy cập vào file <code>index.php</code>. Tức là tương tự như vào <code>http://localhost/index.php</code>. Lúc này, <code>$_SERVER['REQUEST_URI']</code> cho chúng ta giá trị là <code>/</code>. Vậy ta sửa lại như sau:</p>
<pre><code>&lt;?php
// file index.php
if ($_SERVER['REQUEST_URI'] != '/index.php'
     &amp;&amp; $_SERVER['REQUEST_URI'] != '/' ) {
    header('Location: /index.php');
}</code></pre>
<p>Nếu bạn đang cảm thấy mơ hồ hoặc thấy khó khăn, thì vui lòng đọc tiếp các cách khác bên dưới.</p>
<h2>2. Chuyển trang bằng HTML</h2>
<p>Ngoài cách điều hướng bằng php, chúng ta có thể dùng html tag. như sau:</p>
<pre><code class="language-html">&lt;meta http-equiv="refresh" content="0;url=index.php"&gt;</code></pre>
<p>Với số <code>0</code> là số giây sẽ delay. Sau đó sẽ truyển trang về url được khai báo. Như ta muốn chuyển về google.com sau 5s thì ta sẽ ghi như sau: </p>
<pre><code class="language-html">&lt;meta http-equiv="refresh" content="5;url=https://google.com"&gt;</code></pre>
<p>Với số <code>0</code> là chuyển ngay lập tức.</p>
<h4>Lưu ý:</h4>
<p>Sử dụng cách này các bạn cũng không thể tránh khỏi lỗi chuyển trang liên tục như trên. Khi chuyển trang không chuyển về trang hiện tại.</p>
<h2>3. Chuyển trang bằng JavaScript</h2>
<p>Chúng ta biết rằng JS được dùng để sử lí giao diện là trùm luôn. Vì vậy chuyển trang đối với JS chỉ là chuyện nhỏ. Cách thực hiện như sau:</p>
<pre><code class="language-html">&lt;script&gt;
    location.href = '/index.php';
&lt;/script&gt;</code></pre>
<h4>Lưu ý:</h4>
<p>Tương tự, sử dụng cách này các bạn cũng không thể tránh khỏi lỗi chuyển trang liên tục như trên. Khi chuyển trang không chuyển về trang hiện tại.</p>
<h2>Tổng hợp</h2>
<p>Chuyển trang bằng PHP:</p>
<pre><code class="language-php">&lt;?php 
header("Location: /index.php");</code></pre>
<p>Chuyển trang bằng HTML:</p>
<pre><code>&lt;meta http-equiv="refresh" content="0;url=index.php"&gt;</code></pre>
<p>html
Chuyển trang bằng JavaScript:</p>
<pre><code class="language-html">&lt;script&gt;
    location.href = '/index.php';
&lt;/script&gt;</code></pre>
<p>Mọi thắc mắc các bạn vui lòng để lại comment. </p>
<p>Bài viết gốc được đăng tại <a href="https://hocmoingay.top/">https://hocmoingay.top/</a></p>
<p>Người viết <strong>Hoàng Phúc</strong></p>				<p>---</p>
				Phuc Tran Hoang			</div>
			<div id="fb-root"></div>
<script async defer src="https://connect.facebook.net/en_GB/sdk.js#xfbml=1&version=v3.2&appId=&autoLogAppEvents=1"></script>

<div class="fb-comment-embed" data-href="http://hoangphuctv.github.io./blog/hoc-php-qua-vi-du/redirect.md?/mdb" data-width="100%" data-include-parent="false"></div>
		</div>
		<br/>
		<div class="container">
			<hr>
						<div class="my-3 p-3 bg-white rounded shadow-sm">
	<h6 class="border-bottom border-gray pb-2 mb-0">Các bài viết khác</h6>
		<div class="media text-muted pt-3">
		<p class="media-body pb-3 mb-0 small lh-125 border-bottom border-gray">
		<strong class="d-block text-gray-dark">
			<a href="/blog/hoc-php-qua-vi-du/php-json.md">Làm việc với JSON trong PHP.</a>
		</strong>
		<br>
		<small>Phuc Tran Hoang</small>
		<small></small>
		</p>
	</div>
		<div class="media text-muted pt-3">
		<p class="media-body pb-3 mb-0 small lh-125 border-bottom border-gray">
		<strong class="d-block text-gray-dark">
			<a href="/blog/hoc-php-qua-vi-du/php-web-server.md"></a>
		</strong>
		<br>
		<small>Phuc Tran Hoang</small>
		<small></small>
		</p>
	</div>
		<div class="media text-muted pt-3">
		<p class="media-body pb-3 mb-0 small lh-125 border-bottom border-gray">
		<strong class="d-block text-gray-dark">
			<a href="/blog/hoc-php-qua-vi-du/redirect.md">Redirect - Chuyển hướng trang bằng PHP</a>
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
