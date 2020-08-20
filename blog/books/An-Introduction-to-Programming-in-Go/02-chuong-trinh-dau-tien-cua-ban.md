<!DOCTYPE html>
<html>
	<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title>Chương trình đầu tiên của bạn | LẬP TRÌNH</title>
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
				<h1 class="page-title">Chương trình đầu tiên của bạn</h1>
				<p>Theo truyền thống chương trình đầu tiên của bạn viết ở bất cứ ngôn ngữ nào được gọi là chương trình &quot;Hello World&quot; - Một chương trình chỉ đơn giản là xuất ra dòng chữ <code>Hello World</code> ra terminal. Hãy bắt đầu viết chương trình này bằng Go.</p>
<p>Đầu tiên tạo thư mục để lưu các phần mềm. Ví dụ như tạo thư mục như sau: <code>~/src/golang-book/chapter2</code>. (Với <code>~</code> có nghĩa là thư mục của bạn) Từ terminal bạn có thể gõ các lệnh sau:</p>
<pre><code class="language-bash">mkdir src/golang-book
mkdir src/golang-book/chapter2</code></pre>
<p>Mở text editor và gõ theo nội dung sau:</p>
<pre><code class="language-go">package main 

import "fmt"

// this is a comment

func main() {
    fmt.Println("Hello World")
}</code></pre>
<p>Lưu ý chắc rằng bạn gõ đúng nội dung như Trên và lưu nó với tên <code>main.go</code> trong thư mục mà chúng ta vừa mới tạo. Mở lại terminal và gõ lệnh sau:</p>
<pre><code class="language-bash">cd src/golang-book/chapter2
go run main.go</code></pre>
<p>Bạn sẽ nhìn thấy dòng chữ <code>Hello World</code> hiển thị trên terminal. Lệnh <code>go run</code> sau đó là tên các file (mỗi file cách nhau bởi dấu cách <code>`), sẽ compile các file này thành một file thực thi và lưu nó ở một thư mục tạm, rồi chạy nó. Nếu bạn không thấy dòng chữ</code>Hello World` hiển thị thì bạn có thể bạn gõ sai gì đó trong chương trình (hãy kiểm tra lại và gõ cho đúng). Go compiler sẽ gợi ý cho bạn nơi mà bị lỗi. Giống như hầu hết các compiler, Go compiler khá gập khuôn và  không chừa một lỗi nào.</p>
<h2>Các đọc một chương trình Go</h2>
<p>Hãy xem lại chương trình trên một cách chi tiết. Các chương trình Go được đọc từ trên xuống, từ trái qua phải. (giống như đọc một quyển sách). Dòng đầu tiên thế này:</p>
<pre><code class="language-go">package main</code></pre>
<p>Dòng này được gọi là &quot;khai báo package&quot;. Tất cả chương trình Go đều phải được bắt đầu bởi dòng khai báo package này. Package là cách mà Go sử dụng để tổ chức cấu trúc và tái sử dụng code. Có 2 loại chương trình Go: thực thi (executables) và thư viện (libraries). Chương trình thực thi là loại chương trình chúng ta có thể chạy trực tiếp từ terminal. (Trên Windows nó định dạng là file <code>.exe</code>)Thư viện là một tập hợp code chúng ta đóng gói (package) lại với nhau, vì vậy chúng có thể sử dụng chúng trong một chương trình khác. Chúng ta đi chi tiết sau về thư viện, giờ thì chúng ta chỉ cần đảm bảo rằng chương trình của chúng ta có dòng khai báo package này.</p>
<p>Dòng kết tiếp là dòng trắng. Trong máy tính biểu diển dấu xuống dòng là một (hoặc vài) kí tự đặc biệt. Dấu dòng mới (newlines), dấu cách (space) dấu tab chúng ta gọi chung là khoảng trắng (whitespace) (bởi vì chúng ta không nhìn thấy nó). Go không quan tâm đến các khoảng trắng này. Chúng ta sử dụng chúng chỉ để dễ dàng đọc hơn. Tức là bạn bỏ dòng này thì chương trình vẫn chạy đúng như thường.</p>
<p>Giờ xem tiếp:</p>
<pre><code class="language-go">import "fmt"</code></pre>
<p>Từ khóa <code>import</code> là các mà chúng ta include code từ một package khác để sử dụng trong chương trình của chúng ta. Package <code>fmt</code> (viết tắt của chữ format) chứa các hàm giúp chúng ta định dạng cho input và output. Dựa vào những gì chúng ta vừa tìm hiểu về các gói, bạn nghĩ các tệp của gói fmt sẽ chứa gì ở đầu chúng?</p>
<p>Lưu ý rằng chữ <code>fmt</code> ở trên được bao bằng đấu ngoặc kép <code>"</code>. Dấu ngoặc kép được dùng để biểu diễn một string (chuỗi kí tự). Trong Go, string được biểu diễn bằng một dãy các kí tự (chữ, số, kí hiệu,...) có độ dài xác định. Chi tiết hơn về string sẽ được mô tả ở chương tiếp theo, bây giờ quan trọng là bạn nhớ được rằng dấu mở <code>"</code> thì phải được có dấu đóng <code>"</code> tương ứng theo sau đó, và bất cứ thứ gì nằm trong cặp ngoặc kép này được là nội dung của string. Quan trọng: nội dung string không bao gồm cặp dấu <code>"</code> này.</p>
<p>Dòng bắt đầu bằng <code>//</code> được xem là &quot;comment&quot;. Go compiler sẽ bỏ qua các comment này. Nó được viết cho bạn và vì bạn (hoặc cho những người đọc source này) [giúp bạn ghi chú lại những gì bạn muốn nhắn nhủ cho người đọc source]. Go hỗ trợ 2 loại comment: loại 1 là comment bắt đầu bằng 2 dấu <code>//</code> cho đến hết dòng, loại 2 là  comment bắt đầu bằng <code>/*</code> và kết thúc bằng <code>*/</code> có thể bao gồm nhiều dòng.</p>
<p>Bây giờ chúng ta xem cách khai báo một function:</p>
<pre><code class="language-go">func main() {
    fmt.Println("Hello World")
}</code></pre>
<p>Functions là một khối trong chương trình Go. Nó có input, output và một chuỗi các bước gọi các câu lệnh được thực hiện theo đúng thứ tự. Tất cả các function được bắt đầu bằng từ khóa <code>func</code> theo sau là tên của function (trường hợp này là <code>main</code>), sau nữa là một danh sách các tham số được bao quanh bở cặp dấu ngoặc đơn <code>(</code> <code>)</code>, sau nữa là một kiểu dữ liệu trả về (có thể có hoặc không) cuối cùng là thân chương trình được bao bằng cặp ngoặc nhọn <code>{</code> <code>}</code>. Function này không có tham số, không có kết quả trả về, và chỉ có một lệnh. Tên chương trình <code>main</code> là một tên đặc biệt, bởi vì nó là function mà sẽ được gọi khi chương trình thực hiện.</p>
<p>Chúng ta xét đến mảnh cuối cùng của chương trình là dòng:</p>
<pre><code class="language-go">    fmt.Println("Hello World")</code></pre>
<p>Dòng lệnh này được tạo ra bởi 3 thành phần. Đầu tiên là chúng ta gọi tên function bên trong một package <code>fmt</code> tên là <code>Println</code> (đó là đoạn <code>fmt.Println</code>, <code>Println</code> là viết tắt của chữ Print Line). Sau đó chúng ta tạo một string mới chứa các kí tự &quot;Hello World&quot; và gọi hàm (tiếng Anh là invoke, call hoặc execute) đó với string vừa được string này là tham số.</p>
<p>Đến đây, chúng ta có khá nhiều thuật ngữ mới, có thể bạn sẽ thấy hơi choáng ngợp. Nên đôi khi đọc to chương trình của bạn ra thành tiếng có thể giúp bạn hiểu hơn. Các &quot;đọc&quot; lại bằng lời chương trình của chúng ta như sau:</p>
<blockquote>
<p>Tạo mới một chương trình thực thi được, tham chiếu đến thư viện <code>fmt</code> và chứa một function tên là <code>main</code>. Function này không có tham số, không trả về gì và thực hiện: Truy cập vào hàm <code>Println</code> trong thư viện <code>fmt</code> và gọi hàm này với một tham số - là chuỗi &quot;Hello World&quot;.</p>
</blockquote>
<p><code>Println</code> là hàm thực sự làm việc trong chương trình này của chúng ta.  Bạn có thể đọc thêm mô tả về hàm này trong terminal bằng lệnh:</p>
<pre><code class="language-bash">go doc fmt Println</code></pre>
<p>Bạn sẽ thấy được đoạn mô tả sau:</p>
<blockquote>
<pre><code>Println formats using the default formats for its operands and writes to standard output. Spaces are always added between operands and a newline is appended. It returns the number of bytes written and any write error encountered.</code></pre>
</blockquote>
<p>Dịch:</p>
<blockquote>
<pre><code>Println sử dụng định dạng mặc định cho các toán hạn (tham số đầu vào) và ghi nó ra thiết bị xuất chuẩn (ở đây là terminal). Các dấu cách (space) được tự động thêm vào giữa các toán hạn và dấu xuống dòng được thêm vào cuối cùng. Nó trả về số lượng bytes đã ghi ra và các lỗi xảy ra nếu có.</code></pre>
</blockquote>
<p>Go là một ngôn ngữ được mô tả tài liệu rất tốt, nhưng ở mô tả này thì có vẻ hơi khó hiểu nếu bạn chưa từng làm quen với ngôn ngữ nào trước đó. Tuy vậy <code>godoc</code> vẫn là một lệnh vô cùng hữu ích và là nơi mà bạn cần tìm khi có câu hỏi nào đó.</p>
<p>Quay trở lại với function này, tài liệu này nói rằng hàm <code>Println</code> sẽ gửi bất cứ cái gì bạn đưa cho ra thiết bị xuất chuẩn - đây là tên của đầu ra là terminal bạn đang làm mở. Đây là hàm giúp cho dòng chữ <code>Hello World</code> được xuất ra màn hình.</p>
<p>Ở chương tiếp theo chúng ta sẽ tìm hiểu xem các Go lưu trữ và trình bày các thứ khác giống như chữ <code>Hello World</code> bằng cách tìm hiểu về  các loại dữ liệu.</p>
<h2>Các câu hỏi</h2>
<ul>
<li>Khoảng trắng là gì?</li>
<li>Comment là gì? Hai cách để viết comment là gì?</li>
<li>Chương trình của chúng ta đã bắt đầu bằng từ khóa <code>pakage main</code>. Vậy thì bắt đầu của các file trong package <code>fmt</code> bắt đầu bằng gì?</li>
<li>Chúng ta đã sử dụng function <code>Println</code> được khai báo trong package <code>fmt</code>. Nếu chúng ta muốn sử dụng function <code>Exit</code> trong package <code>os</code> thì chúng ta cần làm gì?</li>
<li>Chỉnh sửa chương trình chúng ta đã viết ở trên thay vì in ra chữ <code>Hello World</code> thì nó sẽ in ra dòng chữ <code>Hello, my name is</code> theo sau là tên của bạn. </li>
</ul>
<hr />
<p>Source: <a href="http://www.golang-book.com/books/intro/2">http://www.golang-book.com/books/intro/2</a></p>				<p>---</p>
				Phuc Tran Hoang			</div>
			<div id="fb-root"></div>
<script async defer src="https://connect.facebook.net/en_GB/sdk.js#xfbml=1&version=v3.2&appId=&autoLogAppEvents=1"></script>

<div class="fb-comment-embed" data-href="http://hoangphuctv.github.io./blog/books/An-Introduction-to-Programming-in-Go/02-chuong-trinh-dau-tien-cua-ban.md?/mdb" data-width="100%" data-include-parent="false"></div>
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
