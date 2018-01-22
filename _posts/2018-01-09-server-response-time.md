---
title: 'Server Response Time - Làm thế nào để cải thiện?'
date: 2018-01-09T22:56:39+00:00
excerpt: Server Response Time (thời gian phản hồi của máy chủ) là khoảng thời gian cần thiết để hiển thị HTML trên trình duyệt người dùng, từ một yêu cầu gửi đến máy chủ. Đây là một yếu tố quan trọng ảnh hưởng đến tốc độ trang web, chất lượng SEO và trải nghiệm người dùng.
layout: post
permalink: /server-response-time/
categories:
  - blogging
  - seo
tags:
  - page speed
  - server response time
---
Server Response Time (thời gian phản hồi của máy chủ) là khoảng thời gian cần thiết để hiển thị HTML trên trình duyệt người dùng, từ một yêu cầu gửi đến máy chủ. Đây là một yếu tố quan trọng ảnh hưởng đến tốc độ trang web, chất lượng SEO và trải nghiệm người dùng.

Một trang web SEO tốt luôn được xếp hạng cao hơn trong kết quả của các công cụ tìm kiếm.

Trang web của bạn xuất hiện càng nhiều trong kết quả tìm kiếm, càng có nhiều lưu lượng truy cập.

Server Response Time là một trong nhiều yếu tố ảnh hưởng đến SEO trên trang web của bạn.

Vậy thì:
<h2>Làm thế nào giảm Server Response Time?</h2>

Theo công cụ Google Page Speed, thì thời gian phản hồi của máy chủ lý tưởng là dưới 200ms (0.2s).

Bạn có thể tự kiểm tra máy chủ mình đang sử dụng bằng công cụ <a href="https://developers.google.com/speed/pagespeed/insights/" target="_blank" rel="noopener">Google Page Speed Insight</a>.

Ngoài ra, có các công cụ phổ biến khác như: <a href="https://tools.pingdom.com/" target="_blank" rel="noopener">Pingdom</a>, <a href="https://www.webpagetest.org/" target="_blank" rel="noopener">WebPagetest</a> hay <a href="https://gtmetrix.com/" target="_blank" rel="noopener">GTmetrix</a>.

Nếu thời gian phản hồi của máy chủ đang chậm, hãy cùng tìm ra những yếu tố đang tác động để từ đó có hướng khắc phục.
<h3>1. Dịch vụ Hosting</h3>
Dịch vụ hosting là yếu tố chính đầu tiên ảnh hưởng đến Server Response Time.

Ngày nay với rất nhiều nhà cung cấp uy tín và giá thành hợp lý, người dùng có nhiều cơ hội hơn để lựa chọn cho mình một hosting chất lượng.

Một hosting chất lượng đồng nghĩa với các thông số rõ ràng và sự mạnh mẽ của CPU, RAM, tốc độ truy xuất, khả năng bảo mật, ...

Cá nhân tôi đang sử dụng một gói Shared Hosting để lưu trữ các website giới thiệu công ty, không đòi hỏi về lưu lượng truy cập và một VPS phục vụ cho mục đích <a href="https://nghi.blog/topic/#blogging">viết blog</a>.

Bạn biết đấy, không vơ đũa cả nắm nhưng thực sự chất lượng Shared Hosting ở Việt Nam quá tệ, lỡ mua rồi thì sống chung với lũ thôi.

Trừ khi bạn có nhiều tiền để đầu tư những gói Shared Hosting khủng. Thôi, thà chuyển qua sử dụng VPS.

Xin được liệt kê danh sách một số nhà cung cấp dịch vụ hosting tốt nhất, bạn có thể tham khảo:
<ul>
 	<li><a href="https://www.bluehost.com/" target="_blank" rel="noopener">BlueHost</a> (Được khuyên dùng cho các website, blog sử dụng WordPress).</li>
 	<li><a href="https://www.stablehost.com/" target="_blank" rel="noopener">StableHost</a> (Đang có chương trình giảm giá 50% trọn đời, thời điểm này vẫn còn tham gia được).</li>
 	<li><a href="https://www.siteground.com/" target="_blank" rel="noopener">SiteGround</a></li>
 	<li><a href="http://www.hostgator.com/" target="_blank" rel="noopener">HostGator</a></li>
</ul>
<h3>2. Cơ sở dữ liệu (Database)</h3>
Hầu hết các website hiện nay đều có sử dụng cơ sở dữ liệu.

Nếu không, đó gọi là những static website. Phổ biến hiện nay là các <a href="https://www.staticgen.com/" target="_blank" rel="noopener">static site generator</a> như Jekyll hay Hugo.

Khi thực hiện các truy vấn cơ sở dữ liệu chậm và phức tạp sẽ làm tăng thời gian phản hồi của máy chủ.

Vì vậy, thời gian phản hồi của máy chủ bị giảm rất nhiều tùy thuộc vào việc tối ưu hóa cơ sở dữ liệu và tốc độ truy vấn của bạn là bao nhiêu.
<h4>Làm cách nào để tối ưu hóa cơ sở dữ liệu và tốc độ truy vấn?</h4>
Bài viết này sẽ không đi sâu vào chi tiết về cách tối ưu hóa cơ sở dữ liệu.

Tuy nhiên, có bốn cách chính để tối ưu hóa hiệu suất truy vấn của bạn như sau:
<ul>
 	<li><strong>Viết lại các truy vấn</strong>: Kiểm tra xem bạn đang chạy bao nhiêu truy vấn. Các truy vấn của bạn chỉ nên trả về những gì cần thiết.</li>
 	<li><strong>Lập chỉ mục thích hợp</strong>: Việc lập chỉ mục thích hợp sẽ giúp bạn truy vấn nhanh hơn.</li>
 	<li><strong>Thay đổi schema</strong>: Schema được biết đến với vai trò nhóm các đối tượng giúp quản lý hiệu quả và phân quyền để tăng cường bảo mật cho cơ sở dữ liệu.</li>
 	<li><strong>Sử dụng cache</strong>: Bạn nên xem xét di chuyển một số lượng tải ra front-end để giảm tải cho back-end.</li>
</ul>
<h3>3. Hình ảnh chưa được tối ưu</h3>
Sử dụng hình ảnh giúp website trông bắt mắt, thu hút hơn nhưng đó thực sự là một gánh nặng đối với máy chủ.

Dung lượng các file ảnh càng lớn thì server tải càng lâu hơn, đó là điều dĩ nhiên.

Giải pháp là bạn phải nén hình ảnh trước khi upload lên website.

Có rất nhiều công cụ giúp giảm dung lượng nhưng không ảnh hưởng quá nhiều tới chất lượng ảnh.

Công cụ tôi thường sử dụng nhất đó là <a href="https://tinypng.com/" target="_blank" rel="noopener">TinyPNG</a> nền tảng web hoặc ImageOptim trên macOS.
<h3>4. Các tài nguyên và số lượng request giữa Client và Server</h3>
Số lượng của các requests tương ứng với những lần giao tiếp giữa client và server.

Các trang web thường chứa các tập tin HTML, CSS và JavaScript. Nếu số lượng này càng nhiều thì Server Response Time càng tăng theo cấp số nhân.

Do đó, bạn nên tối ưu các tài nguyên, giảm thiểu các requests giúp giảm thời gian phản hồi của máy chủ.

Bằng cách:
<ul>
 	<li>Gom các file CSS, JS lại thành một file tương ứng.</li>
 	<li>Nén các file HTML, CSS, JS với các công cụ online bạn có thể tìm thấy rất nhiều trên internet.</li>
</ul>
Nếu đang sử dụng WordPress, bạn có thể cấu hình <strong>Minify</strong> trong các plugin tuyệt vời như: W3 Total Cache, WP Fastest Cache hay WP Super Cache, ...
<h2>5. Phần mềm máy chủ.</h2>
Cũng góp phần quan trọng không kém đó là phần mềm trên máy chủ.

Hiện nay có hai phần mềm máy chủ web được sử dụng phổ biến nhất đó là <a href="https://www.apache.org/" target="_blank" rel="noopener">Apache</a> và <a href="https://www.nginx.com/" target="_blank" rel="noopener">Nginx</a>.

Theo mình biết và nhiều người đánh giá, thì Nginx có tốc độ và hiệu suất cao hơn Apache rất nhiều.
<h2>Lời kết</h2>
Mặc dù thời gian phản hồi của máy chủ chỉ chiếm khoảng 10% tổng thời gian trễ trong việc hiển thị trang web cho người dùng, nhưng bạn nên xem xét và có hướng xử lý để giảm thời gian cần thiết cho máy chủ, với những yếu tố được liệt kê trên.