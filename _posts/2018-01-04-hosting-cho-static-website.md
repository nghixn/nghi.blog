---
title: Hosting cho static website miễn phí với tên miền riêng
date: 2018-01-04T01:01:44+00:00
excerpt: Với sự phổ biến của việc sử dụng website tĩnh (static website), rất nhiều dịch vụ cho phép bạn lưu trữ trang web tĩnh miễn phí. Hãy cùng điểm qua Top 3 hosting cho static website miễn phí tốt nhất hiện nay, từ đó có một lựa chọn phù hợp nhất cho dự án của bạn.
layout: post
permalink: /hosting-cho-static-website/
categories:
  - blogging
  - technology
tags:
  - hosting miễn phí
  - static hosting
---
Việc sử dụng website tĩnh (static website) với nhiều mục đích khác nhau như giới thiệu công ty, sản phẩm, <a href="https://jotodi.com/" target="_blank" rel="noopener">mobile app</a>, viết blog, hay thậm chí là ecommerce đang ngày càng trở nên phổ biến. Hãy cùng xem top 3 hosting cho static website qua bài viết này.

Lợi ích thấy rõ nhất của web tĩnh là không cần tương tác cơ sở dữ liệu nên cho tốc độ truy cập cực nhanh và hạn chế được nhiều mối hiểm hoạ từ các cuộc tấn công trên internet.

Bên cạnh đó còn nhiều lợi ích khác, nên không còn nghi ngờ khi các static site generator được gọi là "The next big thing".

Có rất nhiều static site generator như <a href="https://jekyllrb.com/" target="_blank" rel="noopener">Jekyll</a> và <a href="https://gohugo.io/" target="_blank" rel="noopener">Hugo</a> cho phép bạn dễ dàng xây dựng các trang web tĩnh. Hoặc bạn có thể tự viết riêng cho mình bằng HTML, CSS và JavaScript bằng cách sử dụng các mẫu thiết kế miễn phí có sẵn hoặc thiết kế của riêng bạn.

Rất nhiều dịch vụ cho phép bạn lưu trữ trang web tĩnh miễn phí.

Một số hosting còn cho phép bạn sử dụng CDN, SSL, ... tất nhiên là hoàn toàn miễn phí.

Tuy nhiên, không phải tất cả các dịch vụ này đều cho phép bạn trỏ một tên miền riêng (custom domain) đến trang web của mình, mà thường là phải sử dụng sub-domain của dịch vụ đó.

Dưới đây là danh sách Top 3 hosting cho static website miễn phí.

Hãy cùng xem xét và lựa chọn sử dụng cho website của mình.
<h2>Top 3 hosting cho static website miễn phí với tên miền riêng</h2>
<h3><a href="https://pages.github.com/" target="_blank" rel="noopener">GitHub Pages</a></h3>
Đầu tiên là phải kể đến GitHub Pages.

Cho phép bạn lưu trữ các trang web tĩnh trực tiếp từ kho (repository) trên GitHub của bạn và trỏ các tên miền riêng về.

<img src="/img/uploads/github-pages.png" alt="GitHub Pages" width="908" height="616" />

GitHub Pages cung cấp sự hỗ trợ cực tốt cho các site sử dụng Jekyll.

(Jekyll là một <a href="https://www.staticgen.com/" target="_blank" rel="noopener">static site generator</a> phổ biến nhất hiện nay).

GitHub Pages cũng hỗ trợ chuyển đổi định dạng <a href="https://en.wikipedia.org/wiki/Markdown" target="_blank" rel="noopener">Markdown</a> thành nội dung trên website.

Với hầu hết các static site generator bạn có thể sử dụng các dịch vụ CI (Continuous Integration) như Travis.

Hoặc build static trên máy tính của bạn, sau đó push lên GitHub.

GitHub Pages giới hạn 1GB dung lượng, 100GB băng thông/tháng và 10 builds/giờ.

Với các thông số này thì bạn có thể sử dụng thả ga rồi.

GitHub Pages chỉ hỗ trợ SSL khi bạn sử dụng sub-domain.

Tuy nhiên, bạn có thể dùng dịch vụ như Cloudflare để thiết lập SSL miễn phí cho website của mình.
<h3><a href="https://about.gitlab.com/features/pages/" target="_blank" rel="noopener">GitLab Pages</a></h3>
Tương tự GitHub, bạn cũng có thể sử dụng GitLab để lưu trữ website tĩnh của mình và trỏ các tên miền riêng.

<img src="/img/uploads/gitlab-pages.png" alt="GitLab Pages" width="823" height="580" />

Điểm lợi thế của GitLab đó là không giới hạn số lượng các repo private.

Trong khi GitHub, nếu không muốn cho phép mọi người xem được source code của mình thì phải trả một khoản phí.

Một điểm lợi thế khác của GitLab là nó cung cấp một hệ thống <a href="https://about.gitlab.com/gitlab-ci/" target="_blank" rel="noopener">CI nâng cao</a> hoàn toàn miễn phí.

Chúng ta sử dụng CI để build tự động hầu hết các static site generator.

Các thông tin về dung lượng, băng thông hay SSL cũng tương tự với GitHub Pages.
<h3><a href="https://www.netlify.com/" target="_blank" rel="noopener">Netlify</a></h3>
Netlify là một cái tên "nổi như cồn" thời gian gần đây.

Cung cấp khá nhiều tiện ích miễn phí không chỉ dành riêng cho static website mà còn cả các ứng dụng single-page hay web với mục đích thương mại.

<img src="/img/uploads/netlify.png" alt="Netlify - Hosting cho static website" width="1014" height="484" />

Nếu như GitHub Pages và GitLab Pages phải trải qua các bước cấu hình khá rườm rà đối với một người mới bắt đầu, thì với Netlify có vẻ dễ dàng hơn rất nhiều.

(Mình sẽ có một bài hướng dẫn sau về "Netlify cho người mới bắt đầu").

Hiện tại mình đang sử dụng Netlify để deploy cho các dự án của team như <a href="https://nepbean.com/" target="_blank" rel="noopener">Nepbean</a> hay <a href="https://jotodi.com/" target="_blank" rel="noopener">jotodi</a>.

Gói miễn phí theo mình thì quá đủ để dùng.

Tuy nhiên, nếu bạn muốn có các tính năng nâng cao tuyệt vời hơn thì có thể tham khảo <a href="https://www.netlify.com/pricing/" target="_blank" rel="noopener">bảng giá</a> để chọn cho mình một gói phù hợp.

Các thông số của gói Netlify miễn phí:
<ul>
 	<li><strong>Dung lượng lưu trữ:</strong> 100GB.</li>
 	<li><strong>Băng thông:</strong> 100GB/tháng.</li>
 	<li><strong>Hỗ trợ SSL:</strong> Có</li>
 	<li><strong>CI miễn phí:</strong> Có</li>
</ul>
<h2>Các static hosting miễn phí phổ biến khác</h2>
Ngoài top 3 hosting cho static website miễn phí trên thì còn nhiều dịch vụ khác cũng rất tốt.

Bạn có thể tham khảo thêm:
<ul>
 	<li><a href="https://firebase.google.com/" target="_blank" rel="noopener">Firebase Hosting</a></li>
 	<li><a href="https://cloud.google.com/appengine/" target="_blank" rel="noopener">Google App Engine</a></li>
 	<li><a href="https://www.heroku.com/" target="_blank" rel="noopener">Heroku</a></li>
 	<li><a href="https://aws.amazon.com/free/" target="_blank" rel="noopener">Amazon Web Service (AWS)</a></li>
 	<li><a href="https://surge.sh/" target="_blank" rel="noopener">Surge</a></li>
</ul>
<h2>Lời kết</h2>
Trên đây là tổng hợp Top 3 hosting cho static website miễn phí với tên miền riêng.

Cảm ơn bạn đã theo dõi bài viết!

Hãy chia sẽ nếu bạn thấy hữu ích, hoặc bổ sung thêm các dịch vụ hosting miễn phí cho static website mà bạn biết, bằng cách sử dụng comment bên dưới đây.