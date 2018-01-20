---
layout: post
title: 'Git trên VPS Linux - Hướng dẫn cài đặt và sử dụng'
date: 2018-01-03T01:55:19+00:00
excerpt: '[Git trên VPS Linux] Git là một Hệ thống quản lý phiên bản phân tán (Distributed Version Control System) tuyệt vời và phổ biến nhất hiện nay, chắc hẳn không còn xa lạ với bất kỳ một developer nào hiện nay. Bài viết này sẽ hướng dẫn cách cài đặt, cấu hình và sử dụng Git trên VPS Linux.'
permalink: /git-tren-vps-linux/
categories: [technology]
tags: [cài đặt git, git trên vps linux, kiến thức vps, vps linux]
comments: true
---
Git là một Hệ thống quản lý phiên bản phân tán (Distributed Version Control System) tuyệt vời và phổ biến, chắc hẳn không còn xa lạ với bất kỳ một developer nào hiện nay. Bài viết này sẽ hướng dẫn cách cài đặt, cấu hình và sử dụng Git trên VPS Linux.
<h2>Các bước chuẩn bị cài đặt Git trên VPS Linux</h2>
<strong>Cập nhật Linux -</strong> Trước khi cài đặt Git, bạn cần đảm bảo rằng Linux của bạn đã được cập nhật đầy đủ.

Sử dụng các lệnh sau:
<pre>$ apt-get update
$ apt-get upgrade</pre>
<strong>Tạo SSH Keys</strong> - Chúng ta sẽ sử dụng SSH keys cho việc chứng thực.

Chúng ta cần tạo ra bộ đôi SSH keys, đó là public key và private key (mặc định là: id_rsa và id_rsa.pub). Nếu đang sử dụng macOS hay Linux thì bạn có thể tạo bằng cách sử dụng dòng lệnh sau:
<pre>$ ssh-keygen -C "nghi.dcg@gmail.com"</pre>
(Thay địa chỉ email thành của bạn).

Nếu sử dụng hệ điều hành Windows, bạn có thể sử dụng <a href="https://www.ssh.com/ssh/putty/download" target="_blank" rel="noopener">PuTTY Gen</a> để tạo SSH keys.

Một cách khác là bạn đăng nhập vào VPS của mình, sử dụng "Console" để tạo keys và download về sử dụng.

<strong>Tạo user để sử dụng Git</strong> - Bạn có thể đặt bất kỳ tên nào bạn thích.

Ở đây mình sẽ đặt cho user là "git" cho dễ nhớ.

a. Đăng nhập vào VPS và sử dụng quyền "root":
<pre>$ su -</pre>
(Hoặc sử dụng "sudo" trước mỗi dòng lệnh, thay vì sử dụng lệnh trên).

b. Lần lượt sử dụng các lệnh sau để tạo user và thiết lập mật khẩu đăng nhập:
<pre>$ useradd git
$ passwd git</pre>
<h2>Tiến hành cài đặt và thiết lập Git</h2>
Bây giờ chúng ta cài đặt Git sử dụng các dòng lệnh dưới đây.

Tuỳ thuộc vào distro của Linux mà bạn đang sử dụng trên VPS:
<pre>$ yum install git (CentOS/ Fedora)
$ apt-get install git (Ubuntu/ Debian)</pre>
Tiếp theo, ta cần thêm SSH key đã tạo trước đó vào thư mục "home" của user "git" để SSH daemon biết keys nào sẽ được chấp nhận.

Bạn login bằng user "git" vào hệ thống, sử dụng lệnh:
<pre>$ su git</pre>
Sau đó tạo thư mục là ".ssh" và một file "authorized_keys":
<pre>$ mkdir ~/.ssh &amp;&amp; touch ~/.ssh/authorized_keys</pre>
<strong>Lưu ý:</strong>
<ul>
 	<li>Sử dụng hai dấu "&amp;" để thực hiện lệnh thứ nhất sau đó thực hiện tiếp lệnh thứ hai.</li>
 	<li>Sử dụng dấu "~" trước mỗi đường dẫn để chỉ cho server biết ta đang trỏ về thư mục "home", lúc đó "~" sẽ tương đương với "/home/git/".</li>
</ul>
Ngay sau đây ta sẽ sử dụng lệnh "cat".

Lệnh này sẽ in nội dung của file ra ngay màn hình của command line.

Sau đó dùng "&gt;&gt;" để chèn nội dung vào file "authorized_keys".

Bạn phải cẩn thận khi sử dụng dấu này, nếu lỡ chỉ gõ "&gt;" thì nó sẽ ghi đè toàn bộ nội dung lên file mà bạn chỉ định, thay vì chèn nối tiếp nội dung vào file khi bạn sử dụng "&gt;&gt;":
<pre>$ cat .ssh/id_rsa.pub | ssh git@IP_VPS_của_bạn "cat &gt;&gt; ~/.ssh/authorized_keys"</pre>
(Nếu có nhiều keys thì bạn chỉ việc chèn thêm nội dung các file id_rsa.pub, bằng cách sử dụng lệnh trên).

Để kiểm tra lại nội dung đã được chèn vào file chính xác, ta sử dụng lệnh:
<pre>$ cat ~/.ssh/authorized_keys</pre>
<h2>Thiết lập một Local Repository</h2>
Bạn chỉ cần gõ lệnh "git init" để khởi tạo một repository rỗng cho việc sử dụng sau đó:
<pre>$ git init --bare new-repo.git</pre>
Vậy là ta đã có một server Git trên VPS Linux của mình.

Việc tiếp theo là sử dụng nó như cách ta làm việc trên các dự án có sử dụng Git.
<h2>Sử dụng Git Server từ Local Computer</h2>
Nếu bạn đã có sẵn một local repo và muốn push lên server Git vừa tạo, thì bạn cần thay đổi remote origin.

Sử dụng lệnh dưới đây trên macOS và Linux:
<pre>$ git remote set-url origin git@IP_VPS_của_bạn:new-repo.git</pre>
(Trên Windows bạn sử dụng <a href="https://tortoisegit.org/" target="_blank" rel="noopener">TortoiseGit</a> rất trực quan hoặc sử dụng dòng lệnh với Git Bash).

Còn nếu là một folder mới tinh tươm thì sử dụng lệnh:
<pre>$ git init &amp;&amp; git remote add origin git@IP_VPS_của_bạn:new-repo.git</pre>
Bây giờ bạn có thể thoải mái add, commit, pull, push, ... từ máy tính của bạn lên Git trên VPS Linux.

Để trông chuyên nghiệp hơn, bạn nên config thêm các thông tin như sau:
<pre>$ git config --global user.name "Nguyen Xuan Nghi"
$ git config --global user.email "nghi.dcg@gmail.com"</pre>
(Thay bằng thông tin của bạn).

Xem thêm <a href="https://www.kernel.org/pub/software/scm/git/docs/git-config.html" target="_blank" rel="noopener">Git Config</a>.
<h2>Lời kết</h2>
Trên đây là hướng dẫn để cài đặt, cấu hình và sử dụng Git trên VPS Linux. Hy vọng rằng hữu ích với bạn.

<a href="https://nghi.blog/">Blog</a> mình trước đây sử dụng Git trên VPS Linux tại <a href="https://m.do.co/c/0da53dba0324" target="_blank" rel="noopener">DigitalOcean</a>, cảm thấy khá hài lòng về tốc độ và sự ổn định.