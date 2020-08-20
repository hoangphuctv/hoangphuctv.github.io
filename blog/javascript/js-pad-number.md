<!DOCTYPE html>
<html>
	<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title>JS pad number, cách thêm số 0 vào trước số cho đủ vị trí. | LẬP TRÌNH</title>
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
				<h1 class="page-title">JS pad number, cách thêm số 0 vào trước số cho đủ vị trí.</h1>
				<p>Pad string là khái niệm dùng để chỉ việc thêm số 0 vào 1 con số hoặc 1 chuỗi kí tự nằm lắp đầy chỗ chống.
Ví dụ thường gặp nhất là chúng ta muốn xuất ra ngày tháng năm với định dạng 2 con số: <code>2020/01/01</code>.
Các hàm lấy ngày mặc định của JS chỉ trả ra cho chúng ta 1 con sô 1-&gt;9. Nên ta phải thêm 1 con số 0 vào. để tạo ra được dãy số <code>2020/01/01</code>.</p>
<p>Để tổng quát hóa, đồng thời giới thiệu cho các bạn các thêm 1 custom method vào 1 &quot;class&quot; có sẵn của JS.</p>
<pre><code>Number.prototype.pad = function(length, char, pad_left){
    if (typeof char == 'undefined') {
        char = ' ';
    }

    if (typeof pad_left == 'undefined') {
        pad_left = 1;
    }

    var v = this.valueOf() + "";
    if (v.length &lt; length) {
        for (i = v.length; i&lt;length;i++) {
            if (pad_left) {
                v = char + v
            }else {
                v += char;
            }
        }
    }
    return v;
}</code></pre>
<p>// Test
var n = 1;
console.log(&quot;pad left&quot;, n.pad(5, '0'));
console.log(&quot;pad right&quot;, n.pad(5, '0', !!0));</p>				<p>---</p>
				Phuc Tran Hoang			</div>
			<div id="fb-root"></div>
<script async defer src="https://connect.facebook.net/en_GB/sdk.js#xfbml=1&version=v3.2&appId=&autoLogAppEvents=1"></script>

<div class="fb-comment-embed" data-href="http://hoangphuctv.github.io./blog/javascript/js-pad-number.md?/mdb" data-width="100%" data-include-parent="false"></div>
		</div>
		<br/>
		<div class="container">
			<hr>
						<div class="my-3 p-3 bg-white rounded shadow-sm">
	<h6 class="border-bottom border-gray pb-2 mb-0">Các bài viết khác</h6>
		<div class="media text-muted pt-3">
		<p class="media-body pb-3 mb-0 small lh-125 border-bottom border-gray">
		<strong class="d-block text-gray-dark">
			<a href="/blog/javascript/chuyen-tieng-viet-thanh-slug.md">Chuyển tiếng Việt thành slug không dấu</a>
		</strong>
		<br>
		<small>Phuc Tran Hoang</small>
		<small></small>
		</p>
	</div>
		<div class="media text-muted pt-3">
		<p class="media-body pb-3 mb-0 small lh-125 border-bottom border-gray">
		<strong class="d-block text-gray-dark">
			<a href="/blog/javascript/js-pad-number.md">JS pad number, cách thêm số 0 vào trước số cho đủ vị trí.</a>
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