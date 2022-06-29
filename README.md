# Thiết kế hệ thống cho người mới

## Nguồn dịch thuật
* [The System Design Primer](https://github.com/donnemartin/system-design-primer)

<p align="center">
  <img src="http://i.imgur.com/jj3A5N8.png">
  <br/>
</p>

## Động lực (Motivation)

> Học cách thiết kế các hệ thống có khả năng mở rộng cao.
>
> Làm tài liệu chuẩn bị cho các buổi phỏng vấn về thiết kế.

### Học cách thiết kế các hệ thống có khả năng mở rộng cao

Học cách thiết kế hệ thống có khả năng mở rộng sẽ giúp bạn trở thành một kỹ sư tốt hơn.

Thiết kế hệ thống là một chủ đề rất rộng. Có **hằng hà sa số các tài nguyên rải rác trên web** về các nguyên lý thiết kế hệ thống.

Repo này là một **bộ sưu tập đã được tổ chức** các tài nguyên để giúp bạn học cách xây dựng các hệ thống có khả năng mở rộng.

### Học từ cộng đồng mã nguồn mở

Đây là một dự án mã nguồn mở được cập nhật liên tục.

[Các đóng góp](#các-đóng-góp) luôn được hoang nghênh!

### Chuẩn bị cho việc phỏng vấn thiết kế hệ thống

Bên cạnh việc được phỏng vấn kỹ năng code, thiết kế hệ thống cũng là một phần **bắt buộc** trong **vòng phỏng vấn kỹ thuật** của rất nhiều công ty công nghệ.

**Luyện tập các câu phỏng vấn thiết kế hệ thống phổ biến** và **so sánh** câu trả lời của bạn với các đáp án mẫu: các cuộc thảo luận, code và các sơ đồ.

Các chủ đề bổ sung cho việc chuẩn bị phỏng vấn:

* [Study guide](#study-guide)
* [How to approach a system design interview question](#how-to-approach-a-system-design-interview-question)
* [System design interview questions, **with solutions**](#system-design-interview-questions-with-solutions)
* [Object-oriented design interview questions, **with solutions**](#object-oriented-design-interview-questions-with-solutions)
* [Additional system design interview questions](#additional-system-design-interview-questions)

## Anki flashcards

<p align="center">
  <img src="https://github.com/donnemartin/system-design-primer/blob/master/images/zdCAkB3.png">
  <br/>
</p>

Bản [Anki flashcard decks](https://apps.ankiweb.net/) này sử dụng sự lặp lại ngắt quãng để giúp bạn ghi nhớ các khái niệm thiết kế hệ thống chính.

* [System design deck](https://github.com/donnemartin/system-design-primer/tree/master/resources/flash_cards/System%20Design.apkg)
* [System design exercises deck](https://github.com/donnemartin/system-design-primer/tree/master/resources/flash_cards/System%20Design%20Exercises.apkg)
* [Object oriented design exercises deck](https://github.com/donnemartin/system-design-primer/tree/master/resources/flash_cards/OO%20Design.apkg)

Cực kỳ thích hợp cho các bạn cần tính di động.

### Tài nguyên coding: Interactive Coding Challenges

Bạn đang tìm kiếm tài nguyên để chuẩn bị cho [**Coding Interview**](https://github.com/donnemartin/interactive-coding-challenges)?

<p align="center">
  <img src="https://github.com/donnemartin/system-design-primer/blob/master/images/b4YtAEN.png">
  <br/>
</p>

Hãy thử xem qua repo cùng tác giả [**Interactive Coding Challenges**](https://github.com/donnemartin/interactive-coding-challenges), nơi có thêm một Anki deck nữa:

* [Coding deck](https://github.com/donnemartin/interactive-coding-challenges/tree/master/anki_cards/Coding.apkg)

## Các đóng góp

> Học tập từ cộng đồng.

Hãy thoải mái submit các pull request để giúp chúng tôi:

* Sửa các lỗi
* Cải thiện các chủ đề đã viết
* Thêm chủ đề mới
* [Dịch thuật](https://github.com/donnemartin/system-design-primer/issues/28)

Các nội dung đang phát triển được liệt kê ở [under development](#under-development).

Bạn có thể xem thêm [Hướng dẫn đóng góp](https://github.com/donnemartin/system-design-primer/blob/master/CONTRIBUTING.md).

## Mục lục
<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Khởi động](#kh%E1%BB%9Fi-%C4%91%E1%BB%99ng)
  - [Bước 1: Bài giảng về khả năng mở rộng](#b%C6%B0%E1%BB%9Bc-1-b%C3%A0i-gi%E1%BA%A3ng-v%E1%BB%81-kh%E1%BA%A3-n%C4%83ng-m%E1%BB%9F-r%E1%BB%99ng)
  - [Bước 2: Bài báo về khả năng mở rộng](#b%C6%B0%E1%BB%9Bc-2-b%C3%A0i-b%C3%A1o-v%E1%BB%81-kh%E1%BA%A3-n%C4%83ng-m%E1%BB%9F-r%E1%BB%99ng)
- [Hiệu năng và Khả năng mở rộng](#hi%E1%BB%87u-n%C4%83ng-v%C3%A0-kh%E1%BA%A3-n%C4%83ng-m%E1%BB%9F-r%E1%BB%99ng)
- [Độ trễ và Thông lượng](#%C4%91%E1%BB%99-tr%E1%BB%85-v%C3%A0-th%C3%B4ng-l%C6%B0%E1%BB%A3ng)
- [Tính sẵn sàng và Tính nhất quán](#t%C3%ADnh-s%E1%BA%B5n-s%C3%A0ng-v%C3%A0-t%C3%ADnh-nh%E1%BA%A5t-qu%C3%A1n)
  - [Định lý CAP](#%C4%91%E1%BB%8Bnh-l%C3%BD-cap)
- [Các mẫu nhất quán (Consistency patterns)](#c%C3%A1c-m%E1%BA%ABu-nh%E1%BA%A5t-qu%C3%A1n-consistency-patterns)
  - [Nhất quán yếu (Weak consistency)](#nh%E1%BA%A5t-qu%C3%A1n-y%E1%BA%BFu-weak-consistency)
  - [Eventual consistency (Nhất quán đến cuối cùng)](#eventual-consistency-nh%E1%BA%A5t-qu%C3%A1n-%C4%91%E1%BA%BFn-cu%E1%BB%91i-c%C3%B9ng)
  - [Nhất quán mạnh (Strong consistency)](#nh%E1%BA%A5t-qu%C3%A1n-m%E1%BA%A1nh-strong-consistency)
- [Availability patterns](#availability-patterns)
  - [Failover](#failover)
  - [Nhân bản](#nh%C3%A2n-b%E1%BA%A3n)
- [Domain name system](#domain-name-system)
- [Content delivery network (CDN)](#content-delivery-network-cdn)
  - [Push CDN](#push-cdn)
  - [Pull CDN](#pull-cdn)
  - [Một số tài nguyên CDN miễn phí](#m%E1%BB%99t-s%E1%BB%91-t%C3%A0i-nguy%C3%AAn-cdn-mi%E1%BB%85n-ph%C3%AD)
- [Bộ cân bằng tải (Load Balancer)](#b%E1%BB%99-c%C3%A2n-b%E1%BA%B1ng-t%E1%BA%A3i-load-balancer)
  - [Layer 4 load balancing](#layer-4-load-balancing)
  - [Layer 7 load balancing](#layer-7-load-balancing)
  - [Mở rộng theo chiều ngang (Horizontal scaling)](#m%E1%BB%9F-r%E1%BB%99ng-theo-chi%E1%BB%81u-ngang-horizontal-scaling)
- [Reverse proxy (web server)](#reverse-proxy-web-server)
  - [Load balancer vs reverse proxy](#load-balancer-vs-reverse-proxy)
- [Application layer](#application-layer)
  - [Microservices](#microservices)
  - [Service Discovery](#service-discovery)
- [Cơ sở dữ liệu (Database)](#c%C6%A1-s%E1%BB%9F-d%E1%BB%AF-li%E1%BB%87u-database)
  - [Relational database management system (RDBMS)](#relational-database-management-system-rdbms)
  - [Cơ sở dữ liệu NoSQL](#c%C6%A1-s%E1%BB%9F-d%E1%BB%AF-li%E1%BB%87u-nosql)
  - [SQL hay NoSQL](#sql-hay-nosql)
- [Cache](#cache)
  - [Client caching](#client-caching)
  - [CDN caching](#cdn-caching)
  - [Web server caching](#web-server-caching)
  - [Database caching](#database-caching)
  - [Application caching](#application-caching)
  - [Caching at the database query level](#caching-at-the-database-query-level)
  - [Caching at the object level](#caching-at-the-object-level)
  - [Khi nào nên cập nhật cache](#khi-n%C3%A0o-n%C3%AAn-c%E1%BA%ADp-nh%E1%BA%ADt-cache)
- [Bất đồng bộ (Asynchronism)](#b%E1%BA%A5t-%C4%91%E1%BB%93ng-b%E1%BB%99-asynchronism)
  - [Message queues](#message-queues)
  - [Task queues](#task-queues)
  - [Back pressure](#back-pressure)
- [Communication](#communication)
  - [Hypertext transfer protocol (HTTP)](#hypertext-transfer-protocol-http)
  - [Transmission control protocol (TCP)](#transmission-control-protocol-tcp)
  - [User datagram protocol (UDP)](#user-datagram-protocol-udp)
  - [Remote procedure call (RPC)](#remote-procedure-call-rpc)
  - [Representational state transfer (REST)](#representational-state-transfer-rest)
  - [So sánh RPC and REST](#so-s%C3%A1nh-rpc-and-rest)
- [Bảo mật (Security)](#b%E1%BA%A3o-m%E1%BA%ADt-security)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Khởi động
### Bước 1: Bài giảng về khả năng mở rộng
[CS75 (Summer 2012) Lecture 9 Scalability Harvard Web Development David Malan](https://www.youtube.com/watch?v=-W9F__D3oY4)
* Các chủ đề được đề cập:
    * Mở rộng theo chiều dọc (Vertical scaling)
    * Mở rộng theo chiều ngang (Horizontal scaling)
    * Caching
    * Cân bằng tải (Load balancing)
    * Nhân bản cơ sở dữ liệu (Database replication)
    * Phân mảnh cơ sở dữ liệu (Database partitioning)

### Bước 2: Bài báo về khả năng mở rộng
[Scalability for Dummies](http://www.lecloud.net/tagged/scalability)
* Các chủ đề được đề cập:
    * [Clones](http://www.lecloud.net/post/7295452622/scalability-for-dummies-part-1-clones)
    * [Cơ sở dữ liệu](http://www.lecloud.net/post/7994751381/scalability-for-dummies-part-2-database)
    * [Caches](http://www.lecloud.net/post/9246290032/scalability-for-dummies-part-3-cache)
    * [Bất đồng bộ (Asynchronism)](http://www.lecloud.net/post/9699762917/scalability-for-dummies-part-4-asynchronism)

### Bước tiếp theo

Tiếp theo là một số khái niệm ở mức cao hơn

* **Hiệu năng (Performance)** và **Khả năng mở rộng (Scalability)**
* **Độ trễ (Latency)** và **Thông lượng (Throughput)**
* **Tính sẵn sàng (Availability)** và **Tính nhất quán (Consistency)**

## Hiệu năng và Khả năng mở rộng 

Một dịch vụ được coi là có tính **mở rộng (scalable)** nếu nó mang lại kết quả hoạt động tăng theo tỉ lệ thuận với các tài nguyên (resource) được thêm vào. Tăng hiệu năng có thể được hiểu là một lúc làm được nhiều việc hơn hay làm được một việc lớn hơn.<sup><a href=http://www.allthingsdistributed.com/2006/03/a_word_on_scalability.html>1</a></sup>

Một cách nhìn khác về hiệu năng và khả năng mở rộng:

* Nếu bạn có vấn đề về **hiệu năng**, hệ thống của bạn sẽ chậm khi phục vụ một người dùng đơn nhất.
* Nếu bạn có vấn đề về **khả năng mở rộng**, hệ thống của bạn sẽ nhanh khi phục vụ người dùng đơn và sẽ chậm nếu phải chịu tải lớn.

### Nguồn và tài liệu đọc thêm
* [A word on scalability](http://www.allthingsdistributed.com/2006/03/a_word_on_scalability.html)
* [Scalability, availability, stability, patterns](http://www.slideshare.net/jboner/scalability-availability-stability-patterns/)

## Độ trễ và Thông lượng
**Độ trễ** là thời gian để thực hiện một số hành động hoặc để tạo ra một số kết quả.
**Thông lượng** là số hành động được thực hiện hay số kết quả được đưa ra trong một đơn vị thời gian 

Thông thường, mục đích sẽ là cực đại thông lượng với độ trễ chấp nhận được.

### Nguồn và tài liệu đọc thêm
* [Understanding latency vs throughput](https://community.cadence.com/cadence_blogs_8/b/sd/archive/2010/09/13/understanding-latency-vs-throughput)

## Tính sẵn sàng và Tính nhất quán

### Định lý CAP

<p align="center">
  <img src="http://i.imgur.com/bgLMI2u.png">
  <br/>
  <i><a href=http://robertgreiner.com/2014/08/cap-theorem-revisited>Source: CAP theorem revisited</a></i>
</p>

Ở một hệ thống tính toán phân tán (distributed) (bạn nên tìm hiểu thêm về decentralized), Bạn chỉ có thể cung cấp hai trong số các tính đúng đắn dưới đây:

* **Tính nhất quán (Consistency)** - Mọi sự kiện đọc (read) đều nhận được phiên bản mới nhất của sự kiện ghi (write) gần nhất hoặc lỗi.
* **Tính sẵn sàng (Availability)** - Mọi request đều nhận một response, không cần đảm bảo dữ liệu nhận được là phiên bản mới nhất. 
* **Tính chịu đựng phân mảnh (Partition Tolerance)** - Hệ thống vẫn tiếp tục hoạt động mặc cho sự phân mảnh tùy ý (arbitrary partitioning) bị gây ra do lỗi mạng.

*Môi trường mạng là không đáng tin cậy, vì vậy bạn sẽ cần tính chịu đựng phân mảnh. Bạn sẽ cần cân nhắc giữa tính nhất quán và tính sẵn sàng.*

#### CP - consistency and partition tolerance

Đợi một response từ node được phân mảnh có thể gây ra timeout error.  CP là một lựa chọn tốt nếu bạn cần một ứng dụng đọc ghi nguyên tử.

#### AP - availability and partition tolerance

Responses trả về phiên bẻn gần nhất của dữ liệu có trên node đó, có thể không phải là mới nhất.  Việc ghi có thể tốn một lượng thời gian cho việc lan truyền.

AP sẽ tốt đối với các ứng dụng cần [eventual consistency](#eventual-consistency) hoặc các ứng dụng yêu cầu vẫn hoạt động mặc cho có lỗi từ bên ngoài.

## Các mẫu nhất quán (Consistency patterns)
Với nhiều bản sao của cùng một dữ kiệu, Chúng ta phải đối mặt với các lựa chọn về cách đồng bộ chúng để client có một cái nhìn nhất quán về dữ liệu.

### Nhất quán yếu (Weak consistency)

Sau khi ghi, việc đọc có thể nhìn thấy hoặc không. 
Nhất quán yếu sẽ hoạt động tốt với ứng dụng VoIP, video chat, game online (Các ứng dụng cần phản hồi nhanh và có thể chấp nhận mất mát thông tin). 

### Eventual consistency (Nhất quán đến cuối cùng)

Sau khi ghi, việc đọc cuối cùng sẽ thấy nó (có thể sau một thời gian). Dữ liệu được nhân bản một cách bất đồng bộ. Loại này được recommmend cho các ứng dụng cần tính sẵn sàng cao (Mô hình BASE).

### Nhất quán mạnh (Strong consistency)

Sau việc ghi, việc đọc sẽ thấy nó. Dữ liệu được nhân bản một cách đồng bộ.
Nó có thể được thấy ở các hệ thống file hay hệ cơ sở dữ liệu quan hệ. Nó sẽ hữu ích với các ứng dụng dùng giao tác (Mô hình ACID).

### Nguồn và tài liệu đọc thêm
* [Transactions across data centers](http://snarfed.org/transactions_across_datacenters_io.html)

## Availability patterns

Có hai mẫu chính để hỗ trợ tính sẵn sàng cao: **fail-over** và **nhân bản (replication)**.

### Failover

#### Active-passive

Với active-passive fail-over, heartbeats được gửi giữa các mấy chủ chủ động (active server) và mấy chủ bị động (passive server) sẽ ở trạng thái chờ (standby).  Nếu heartbeat bị ngắt quãng, Máy chủ thụ động lấy địa chỉ ip của máy chủ chủ động và tiếp tục dịch vụ, việc đổi ip này có nhiều cách giải quyết, bạn có thể xem [Zookeeper](https://zookeeper.apache.org/).

#### Active-active

Trong mô hình active-active, tất cả server đều quản lý trafic, chia sẽ tải cho nhau.

Nếu các server đều ở trạng thái public-facing, DNS sẽ cần biết các địa chỉ IP công khai của các server này. Nếu các server ở trạng thái internal-facing, nghiệp vụ của chương trình sẽ phải biết về tất cả các server này.

Active-active failover có thể được gọi với cái tên khác là master-master failover.

### Nhược điểm: failover

* Fail-over cần thêm phần cứng và phức tạp hơn.
* Vẫn có khả năng mất mát dữ liệu nếu server active sập trước khi dữ liệu mới được ghi chưa được nhân bản ở server passive.

### Nhân bản

#### Master-slave and master-master

Chủ đề này sẽ được bàn luận sâu hơn ở phần [Database](#database):

* [Master-slave replication](#master-slave-replication)
* [Master-master replication](#master-master-replication)

## Domain name system

<p align="center">
  <img src="http://i.imgur.com/IOyLj4i.jpg">
  <br/>
  <i><a href=http://www.slideshare.net/srikrupa5/dns-security-presentation-issa>Source: DNS security presentation</a></i>
</p>

Một Domain Name System (DNS) dịch một tên miền như www.example.com thành địa chỉ IP (ngoài ra nó có thể sử dụng để cân bàng tải).

DNS có tính thứ bậc (hierarchical), với một vài server chính chủ (authoritative server) ở mức cao nhất. Router hoặc ISP cung cấp thông tin về DNS server nào sẽ được liên lạc khi có việc tra cứu. Các server DNS ở mức thấp hơn được dùng cho cache mappings, chúng có thể không được cập nhật mới nhất do độ trễ từ việc lan truyền.  kết quả DNS có thể được cache bởi trình duyệt hoặc hệ điều hành trong một khoảng thời gian sống [time to live (TTL)](https://en.wikipedia.org/wiki/Time_to_live).

* **NS record (name server)** - chỉ định DNS servers cho tên miền/tên miền con.
* **MX record (mail exchange)** - chỉ định mail servers cho việc chấp nhận các tin nhắn.
* **A record (address)** - ánh xạ một tên đến một địa chỉ IP.
* **CNAME (canonical)** - ánh xạ một tên đến một tên khác hoặc `CNAME` (example.com to www.example.com) hoặc đến một bản ghi `A`.

Dịch vụ như [CloudFlare](https://www.cloudflare.com/dns/) và [Route 53](https://aws.amazon.com/route53/) cung cấp các dịch vụ DNS được quản lý.  Một vài DNS service có thể định tuyến trafic với rất nhiều phương pháp:

* [Weighted round robin](http://g33kinfo.com/info/archives/2657)
    * chặn các traffic đến server đang bảo trì
    * Cân bằng giữa các size cluster khác nhau
    * A/B testing
* (Dựa vào độ trễ) Latency-based
* (Dựa vào vị trí địa lý) Geolocation-based

### Nhược điểm: DNS

* Truy cập DNS sẽ tạo ra một độ trễ nhỏ, mặc dù đã được giảm bớt từ việc cache.
* quản lý DNS server có thể phức tạp, mặc dù chúng đã được quản lý bởi [governments, ISPs, and large companies](http://superuser.com/questions/472695/who-controls-the-dns-servers/472729).
* DNS services có thể bị tấn công [DDoS attack](http://dyn.com/blog/dyn-analysis-summary-of-friday-october-21-attack/), làm cho người dùng không thể truy cập đúng địa chỉ IP.

### Nguồn và tài liệu đọc thêm

* [DNS architecture](https://technet.microsoft.com/en-us/library/dd197427(v=ws.10).aspx)
* [Wikipedia](https://en.wikipedia.org/wiki/Domain_Name_System)
* [DNS articles](https://support.dnsimple.com/categories/dns/)

## Content delivery network (CDN)

<p align="center">
  <img src="http://i.imgur.com/h9TAuGI.jpg">
  <br/>
  <i><a href=https://www.creative-artworks.eu/why-use-a-content-delivery-network-cdn/>Source: Why use a CDN</a></i>
</p>

Một content delivery network (CDN) là một mạng phân tán toàn cầu các proxy server, phục vụ các nội dung từ các địa điểm gần hơn cho người dùng. Thông thường, các nội dung tĩnh như HTML/CSS/JS, ảnh, và video được phục vụ bởi CDN, mặc dù một vài CDN như Amazon's CloudFront cung cấp các nội dung động. Một DNS resolution sẽ nói cho client biết lấy nội dung từ CDN nào.

Việc cung cấp nội dung từ CDN có thể được tối ưu hiệu năng đáng kể nhờ hai yếu tố:

* Người dùng nhận nội dung tại trung tâm dữ liệu gần họ
* Server sẽ không phải phục vụ các request mà CDN đã xử lý

### Push CDN

<p align="center">
  <img src="https://i.cdn.net/wp-content/uploads/2016/12/Picture1-1.png">
  <br/>
  <i>Source: cdn.net</i>
</p>

Push CDNs nhận nội dung mới bất cứ khi nào có sự thay đổi từ server. Bạn chịu hoàn toàn trách nhiệm cho việc cung cấp nội dung, upload trực tiếp lên CDN và viết lại URL để trỏ tới CDN. Bạn có thể cấu hình khi nội dung hết hạn và khi nào được cập nhật. Nội dung chỉ được cập nhật khi nó là mới hoặc được cập nhật lại, tối thiểu hóa traffic, nhưng tối đa hóa storage.

Site với một lượng traffic nhỏ hoặc site với nội dung ít phải cập nhật sẽ hoạt động tốt nhất với CDN này. Nội dung được đặt ở CDN một lần, thay vì được pull lại sau một khoảng thời gian nhất định.

### Pull CDN

<p align="center">
  <img src="https://i.cdn.net/wp-content/uploads/2016/12/Picture2-1.png">
  <br/>
  <i>Source: cdn.net</i>
</p>

Pull CDN lấy nội dung mới từ server khi người dùng đầu tiên yêu cầu nội dung.  Bạn để nội dung ở server của bạn và viết lại URL để trỏ đến CDN. Kết quả là các request sẽ được phục vụ chậm hơn khi nội dung chưa kịp cache lại.

Khoảng thời gian sống [time-to-live (TTL)](https://en.wikipedia.org/wiki/Time_to_live) xác định khoảng thời gian nội dung được cache. Pull CDNs tối thiểu hóa lượng dữ liệu phải lưu trữ trên CDN, nhưng nó có thể tạo ra các traffic thừa nếu nội dung hết hạn và được pull lại trước khi nó thực sự được thay đổi.

Các site với lượng traffic lớn sẽ hoạt động tốt với pull CDNs, vì traffic được phân đều ra do chỉ có các nội dung được yêu cầu gần đây được lưu ơ CDN.

### Một số tài nguyên CDN miễn phí
* [CloudFlare](https://www.cloudflare.com/)
* [Photon](https://jetpack.com/support/photon/)
* [jsDelivr](https://www.jsdelivr.com/)
* [Google Hosted Library](https://developers.google.com/speed/libraries/)

### Nhược điểm: CDN

* Chi phí cho CDN có thể đáng kể dựa vào lượng truy cập. Nhưng vẫn cần cân nhắc với những chi phí bạn phải gánh chịu nếu không sử dụng CDN.
* Nội dung có thể cũ nếu nó vẫn trong thời gian sống tại CDN mà lại được cập nhật ở server.
* CDN yêu cầu việc viết lại URL để trỏ tới nó.

### Nguồn và tài liệu đọc thêm

* [Globally distributed content delivery](http://repository.cmu.edu/cgi/viewcontent.cgi?article=2112&context=compsci)
* [The differences between push and pull CDNs](http://www.travelblogadvice.com/technical/the-differences-between-push-and-pull-cdns/)
* [Wikipedia](https://en.wikipedia.org/wiki/Content_delivery_network)

## Bộ cân bằng tải (Load Balancer)

<p align="center">
  <img src="http://i.imgur.com/h81n9iK.png">
  <br/>
  <i><a href=http://horicky.blogspot.com/2010/10/scalable-system-design-patterns.html>Source: Scalable system design patterns</a></i>
</p>

Load balancers phân tán các request đến các tài nguyên tính toán ví dụ như các server và database. Ở mỗi trường hợp, load balancer trả về một response từ tài nguyên tính toán đến một client thích hợp. Load balancers hiệu quả trong:

* Ngăn các request đến các server đang có vấn đề
* Ngăn chặn việc một tài nguyên bị quá tải
* Giúp loại bỏ điểm chết (single points of failure)

Load balancers có thể được cài đặt với phần cứng (đắt đỏ) hoặc bằng phần mềm như HAProxy.

Một vài lợi ích khác:

* **SSL termination** - Giải mã các request đến và mã hóa các response trả về vì vậy backend không phải lo việc này nữa
    * Không cần cài đặt [X.509 certificates](https://en.wikipedia.org/wiki/X.509) cho mỗi server một
* **Session persistence** - cung cấp các cookie và định tuyến các request cụ thể đến cùng một instance nếu ứng dụng web không theo dõi session. 

Để bảo vệ trước lỗi, thường phải cài đặt nhiều load balancer, cả active-passive và active-active.

Load balancer có thể định tuyến trafic dựa trên nhiều độ đo, bao gồm:

* Ngẫu nhiên
* Ít được load nhất
* Session/cookies
* [Round robin or weighted round robin](http://g33kinfo.com/info/archives/2657)
* Layer 4
* Layer 7

### Layer 4 load balancing

Layer 4 load balancer nhìn vào thông tin ở lớp transport để quyết định phân tán request. Thông thường, nó bao gồm các địa chỉ IP của nguồn đích và port ở phần header, nhưng không có nội dung của package.  Layer 4 load balancer chuyển tiếp các gói tin đến và từ các upstream server, biểu diễn [Network Address Translation (NAT)](https://www.nginx.com/resources/glossary/layer-4-load-balancing/).

### Layer 7 load balancing

Layer 7 load balancer xem thông tin tại lớp [application layer] để phân tán request.  Nó có thể bao gồm thông tin của header, message, và cookies.  Layer 7 load balancer ngắt network traffic, đọc nội dung tin, đưa ra quyết định, sau đó mở một kết nối đến server được lựa chọn. Ví dụ, một layer 7 load balancer có thể chỉ đường video traffic tới các server chứa video trong khi chỉ đường cho các traffic nhạy cảm hơn tới những server có tính bảo mật cao (security-hardened server).

Nói về chi phí cho sự linh hoạt, layer 4 load balancing yêu cầu ít thời gian và tài nguyên tính toán hơn Layer 7, mặc dù tác động của hiệu năng có thể là tối thiểu ở các hệ thống được trang bị hiện đại.

### Mở rộng theo chiều ngang (Horizontal scaling)

Load balancer có thể cũng giúp ích cho horizontal scaling, nâng cao hiệu năng và khả năng mở rộng. Mở rộng sử dụng thêm  các bộ máy là hiệu quả hơn và kết quả là tính sẵn sàng cao hơn là mở rộng bằng cách nâng cấp một server bằng các phần cứng đắt hơn, gọi là **Mở rộng theo chiều dọc (Vertical Scaling)**.  Cũng dễ dàng hơn để thuê các tài năng làm việc trên các hệ thống thương mại so với các hệ thống doanh nghiệp đặc biệt.

#### Nhược điểm: horizontal scaling

* Mở rộng ngang yêu cầu phức tạp hơn và cần có clone server
    * Server nên để stateless: chúng không nên lưu trữ bất kỳ dữ liệu nào liên quan đến người dùng như sessions hay ảnh cá nhân
    * Sessions có thể lưu ở một trung tâm dữ liệu như một database (SQL, NoSQL) hoặc cache bằng Redis hay Memcached
* Downstream server ví dụ như cache hay database cần xử lý nhiều kết nối đồng thời bởi vì upstream server được mở rộng

### Nhược điểm: load balancer

* The load balancer có thể trở thành thắt cổ chai nếu không có đủ tài nguyên hoặc không được cấu ình tốt.
* Có thể tăng sự phức tạp.
* Một load balancer đơn lẻ là một điểm lỗi, nếu dùng nhiều load balancer thì việc cấu hình lại phức tạp hơn.

### Nguồn và tài liệu đọc thêm

* [NGINX architecture](https://www.nginx.com/blog/inside-nginx-how-we-designed-for-performance-scale/)
* [HAProxy architecture guide](http://www.haproxy.org/download/1.2/doc/architecture.txt)
* [Scalability](http://www.lecloud.net/post/7295452622/scalability-for-dummies-part-1-clones)
* [Wikipedia](https://en.wikipedia.org/wiki/Load_balancing_(computing))
* [Layer 4 load balancing](https://www.nginx.com/resources/glossary/layer-4-load-balancing/)
* [Layer 7 load balancing](https://www.nginx.com/resources/glossary/layer-7-load-balancing/)
* [ELB listener config](http://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-listener-config.html)

## Reverse proxy (web server)

<p align="center">
  <img src="http://i.imgur.com/n41Azff.png">
  <br/>
  <i><a href=https://upload.wikimedia.org/wikipedia/commons/6/67/Reverse_proxy_h2g2bob.svg>Source: Wikipedia</a></i>
  <br/>
</p>

Một reverse proxy là một web server tập trung các dịch vụ bên trong (internal services) và cung cấp giao diện được chuẩn hóa ra bên ngoài.  Requests từ clients được chuyển tiếp đến server có khả năng hoàn thành nó trước khi reverse proxy trả về response của server cho client.

Các lợi ích kèm theo bao gồm:

* **Tăng tính bảo mật** - Che dấu các thông tin về backend servers, blacklist IPs, số kết nối tối đa được cấp cho mỗi client
* **Tăng khả năng mở rộng và linh hoạt** - Client chỉ nhìn thấy địa chỉ IP của reverse proxy, cho phép mở rộng thêm server hoặc thay đổi cấu hình của những server này.
* **Chấm dứt SSL (SSL termination)** - đã nói ở phần cân bằng tải
* **Nén (Compression)** - nén server response
* **Caching** - trả về các response đã được cache
* **Các nội dung tĩnh (Static content)** - Nếu client yêu cầu các nội dung tĩnh không cần đến server xử lý, reverse proxy có thể trả về trực tiếp các nội dung này. 
    * HTML/CSS/JS
    * Photos
    * Videos
    * Etc

### Load balancer vs reverse proxy

* Triển khai một load balancer là có lợi nếu bạn có nhiều server. Một cách thường xuyên, load balancer định tuyến traffic đến một tạp các server phục vụ cùng một chức năng.
* Reverse proxy có thể hữu dụng ngay cả với chỉ một web server, với các lợi tích đã nêu trên.
* Giải pháp ví dụ như NGINX và HAProxy có thể hỗ trợ cả layer 7 reverse proxying và load balancing.

### Nhược điểm: reverse proxy

* Tăng thêm tính phức tạp.
* Một reverse proxy đơn lẻ là một điểm lỗi đơn, cấu hình nhiều reverse proxy (ví dụ một [failover](https://en.wikipedia.org/wiki/Failover)) thì lại thêm tính phức tạp.

### Nguồn và tài liệu đọc thêm

* [Reverse proxy vs load balancer](https://www.nginx.com/resources/glossary/reverse-proxy-vs-load-balancer/)
* [NGINX architecture](https://www.nginx.com/blog/inside-nginx-how-we-designed-for-performance-scale/)
* [HAProxy architecture guide](http://www.haproxy.org/download/1.2/doc/architecture.txt)
* [Wikipedia](https://en.wikipedia.org/wiki/Reverse_proxy)

## Application layer

<p align="center">
  <img src="http://i.imgur.com/yB5SYwm.png">
  <br/>
  <i><a href=http://lethain.com/introduction-to-architecting-systems-for-scale/#platform_layer>Source: Intro to architecting systems for scale</a></i>
</p>

Chia ra web layer từ the application layer (còn được biết đến như platform layer) cho phép bạn mở rộng và cấu hình cả hai một cách độc lập. Thêm một API mới kết quả chỉ là thêm một application server mà không cần thêm một web server.

**Single responsibility principle** ủng hộ cho việc có các service nhỏ và tự trị làm việc cùng với nhau. Các team nhỏ với các dịch vụ nhỏ có thể trù hoạch mạnh mẽ hơn cho sự phát triển nhanh chóng.

Worker ở application layer có thể cho phép bất đồng bộ (asynchronism).

### Microservices

Vấn đề bàn đến là [microservices](https://en.wikipedia.org/wiki/Microservices), có thể được miêu tả như một bộ các service được triển khai độc lập, nhỏ và hướng module.  Mỗi service chạy ở một tiến trình riêng biệt và giao tiếp thông qua một cơ chế gọn nhẹ, được xác định rõ hàng để thực hiện một nghiệp vụ. <sup><a href=https://smartbear.com/learn/api-design/what-are-microservices>1</a></sup>

Pinterest, như là một ví dụ, có thể có các microservice sau đây: user profile, follower, feed, search, photo upload, ...

### Service Discovery

Các hệ thống như [Consul](https://www.consul.io/docs/index.html), [Etcd](https://coreos.com/etcd/docs/latest), and [Zookeeper](http://www.slideshare.net/sauravhaloi/introduction-to-apache-zookeeper) có thể giúp các service tìm được các service khác bằng việc theo dõi các tên, địa chỉ, và cổng đã được đăng ký.  [Health checks](https://www.consul.io/intro/getting-started/checks.html) giúp kiểm chứng sự toàn vẹn của các service thường được thực hiện bằng cách sử dụng HTTP endpoint. Cả Consul và Etcd được xây dựng trên key-value store rất hữu dụng cho việc lưu trữ các giá trị cấu hình và các dữ liệu được chia sẻ khác.

### Nhược điểm: application layer

* Thêm một application layer với các dịch vụ kết đôi lỏng lẻo yêu cầu cách tiếp cận khác về kiến trúc, vận hành, và các quan điểm quá trình (process viewpoint) (so với một monolithic system).
* Microservices có thể thêm độ phức tạp trông việc triển khai và vận hành.

### Nguồn và tài liệu đọc thêm

* [Intro to architecting systems for scale](http://lethain.com/introduction-to-architecting-systems-for-scale)
* [Crack the system design interview](http://www.puncsky.com/blog/2016/02/14/crack-the-system-design-interview/)
* [Service oriented architecture](https://en.wikipedia.org/wiki/Service-oriented_architecture)
* [Introduction to Zookeeper](http://www.slideshare.net/sauravhaloi/introduction-to-apache-zookeeper)
* [Here's what you need to know about building microservices](https://cloudncode.wordpress.com/2016/07/22/msa-getting-started/)

## Cơ sở dữ liệu (Database)

<p align="center">
  <img src="http://i.imgur.com/Xkm5CXz.png">
  <br/>
  <i><a href=https://www.youtube.com/watch?v=vg5onp8TU6Q>Source: Scaling up to your first 10 million users</a></i>
</p>

### Relational database management system (RDBMS)

Một CSDL quan hệ như SQL là một bộ sưu tập các data được tổ chức dưới dạng bảng.

**ACID** là một tập các thuộc tính của RDBMS [transactions](https://en.wikipedia.org/wiki/Database_transaction).

<p align="center">
  <img src="https://tedu.com.vn/UploadData/images/acid-600x338.png">
  <br/>
</p>

* **Atomicity** - Mỗi transaction hoặc là tất cả các thao tác thành công hoặc tất cả thất bại
* **Consistency** - Bất kỳ transaction nào cũng đưa CSDL từ một trạng thái hợp lệ này sang một trạng thái hợp lệ khác
* **Isolation** - Các giao dịch phải tách biệt nhau
* **Durability** - Các dữ liệu đã commit là bền vững

Có rất nhiều kỹ thuật để mở rộng RDBMS: **master-slave replication**, **master-master replication**, **federation**, **sharding**, **denormalization**, và **SQL tuning**.

#### Master-slave replication

Server master phục vụ đọc và ghi, nhân bản các dữ liệu được ghi ra slave, nơi mà dữ liệu chỉ được đọc. Các slave có thể nhân bản ra các slave khác (dạng cây). Nếu master sập, hệ thống sẽ ở trạng thái chỉ đọc cho đến khi một slave được thăng lên làm master hoặc master được khôi phục.

<p align="center">
  <img src="http://i.imgur.com/C9ioGtn.png">
  <br/>
  <i><a href=http://www.slideshare.net/jboner/scalability-availability-stability-patterns/>Source: Scalability, availability, stability, patterns</a></i>
</p>

##### Nhược điểm: master-slave replication

* Cần thêm các logic để xác định cơ chế chuyển một slave nên master.

#### Master-master replication

Tất cả đều hỗ trợ đọc ghi, các server là ngang hàng về việc ghi. Nếu một master sập, hệ thống vẫn tiếp tục đọc ghi.

<p align="center">
  <img src="http://i.imgur.com/krAHLGg.png">
  <br/>
  <i><a href=http://www.slideshare.net/jboner/scalability-availability-stability-patterns/>Source: Scalability, availability, stability, patterns</a></i>
</p>

##### Nhược điểm: master-master replication

* Bạn sẽ cần một load balancer hoặc sẽ cần thay đổi logic của application để quết định ghi ở đâu.
* Hầu hết hệ thống master-master là nhất quán lỏng lẻo (xâm phạm ACID) hoặc sẽ trễ trong việc ghi để đồng bộ.
* Giải quyết xung đột sẽ càng phức tạp nếu thêm server ghi.

##### Nhược điểm: replication

* Có khả năng mất mát dữ liệu nếu master chết trước khi nhân bản được hoàn thành.
* Mỗi lần ghi sẽ sinh ra các lần nhân bản. Nếu có rất nhiều ghi, việc nhân bản có thể bị sa lầy và không thể làm như các hệ thống nhiều đọc.
* Càng nhiều read slave, bạn càng cần nhân bản nhiều, độ trễ càn lớn.
* Ở một vài hệ thống, viết lên master có thể sinh nhiều luồng ghi song song, khi nhân bản chỉ cung cấp viết tuần tự với một luồng đơn.
* Nhân bản cần thêm phần cứng và độ phức tạp.

##### Nguồn và tài liệu đọc thêm: replication

* [Scalability, availability, stability, patterns](http://www.slideshare.net/jboner/scalability-availability-stability-patterns/)
* [Multi-master replication](https://en.wikipedia.org/wiki/Multi-master_replication)

#### Federation

<p align="center">
  <img src="http://i.imgur.com/U3qV33e.png">
  <br/>
  <i><a href=https://www.youtube.com/watch?v=vg5onp8TU6Q>Source: Scaling up to your first 10 million users</a></i>
</p>

Federation (or hoặc phân chia theo hàm) chia database bằng hàm. Ví dụ, thay vì dùng một database đơn, bạn có thể có ba database: **forums**, **users**, và **products**, kết quả là sẽ ít traffic đọc ghi cho mỗi database và cuối cùng ít lag cho nhân bản. Database nhỏ hơn kết quả là nhiều dữ liệu có thể được vừa cho memory, có thể tạo nên nhiều cache hit hơn và cải thiện cache một cách cục bộ. Do có nhiều database bạn có thể ghi song song, cải thiện thông lượng.

##### Nhược điểm: federation

* Federation không hiệu quả nếu schema yêu cầu hàm hoặc bảng lớn.
* Bạn sẽ cần cập nhật application logic để xác định ghi và đọc trên database nào.
* Join bảng sẽ rất phức tạp với một [server link](http://stackoverflow.com/questions/5145637/querying-data-by-joining-two-tables-in-two-database-on-different-servers).
* Federation cần thêm phần cứng và độ phức tạp.

##### Nguồn và tài liệu đọc thêm: federation

* [Scaling up to your first 10 million users](https://www.youtube.com/watch?v=vg5onp8TU6Q)

#### Sharding

<p align="center">
  <img src="http://i.imgur.com/wU8x5Id.png">
  <br/>
  <i><a href=http://www.slideshare.net/jboner/scalability-availability-stability-patterns/>Source: Scalability, availability, stability, patterns</a></i>
</p>
 
Sharding phân tán dữ liệu xuyên suốt các database khác nhau như mỗi database giữ một phần của dữ liệu. Lấy user database làm ví dụ, Nếu càng nhiều user, càng nhiều shard sẽ được thêm vào cluster.

Tương tự như ưu điểm của federation, sharding. kích cỡ index được giảm đi, cải thiện hiệu năng và truy vấn nhanh hơn. Nếu một shard sập các shard khác vẫn họat động, mặc dù bạn vẫn cần nhân bản để tránh mất mát dữ liệu. Như federation, bạn có thể ghi một cách song song.

Bạn có thể dùng họ hoặc vị trí địa lý để shard một bảng có nhiều người dùng.

##### Nhược điểm: sharding

* Cần cập nhật lại logic.
* Dữ liệu có thể bị lõm ở shard.  Ví dụ, Sẽ có nhiều request vào một shard trong khi các shard khác rảnh rỗi.
    * Cân bằng lại yêu cầu thêm độ phức tạp. Một hàm cho sharding dựa trên [consistent hashing](http://www.paperplanes.de/2011/12/9/the-magic-of-consistent-hashing.html) có thể giảm hiểu lượng dữ liệu phải di chuyển qua lại khi có thay đổi.
* Join từ nhiều shard có thể phức tạp.
* Sharding yêu cầu thêm phần cứng và độ phức tạp.

##### Nguồn và tài liệu đọc thêm: sharding

* [The coming of the shard](http://highscalability.com/blog/2009/8/6/an-unorthodox-approach-to-database-design-the-coming-of-the.html)
* [Shard database architecture](https://en.wikipedia.org/wiki/Shard_(database_architecture))
* [Consistent hashing](http://www.paperplanes.de/2011/12/9/the-magic-of-consistent-hashing.html)

#### Denormalization

Denormalization mục tiêu là tối ưu hóa đọc bằng một vài chi phí cho việc ghi. Các bản copy thừa của dữ liệu được thêm vào các bảng để hạn chế nhiều lệnh join. Một vài RDBMS như [PostgreSQL](https://en.wikipedia.org/wiki/PostgreSQL) và Oracle cung cấp [materialized views](https://en.wikipedia.org/wiki/Materialized_view) để xử lý công việc lưu trữ dư thừa và giũ chúng nhất quán.

Một khi dữ liệu phân tán từ các kỹ thuật như [federation](#federation) và [sharding](#sharding), việc join sẽ rất phức tạp. Denormalization sẽ giảm thiểu việc phải join một cách phức tạp.

Ở hầu hết các hệ thống, việc đọc thường gấp 100 thậm chí 1000:1 việc ghi. việc đọc lại yêu cầu các phép join tốn kém, tốn một khoảng thời gian lớn cho việc truy xuất.

##### Nhược điểm: denormalization

* Dữ liệu bị trùng lặp.
* Phải đồng bộ hóa dư thừa, thiết kế database phức tạp hơn.
* Không sử dụng cho các ứng dụng có lượng ghi lớn.

###### Nguồn và tài liệu đọc thêm: denormalization

* [Denormalization](https://en.wikipedia.org/wiki/Denormalization)

#### SQL tuning

SQL tuning là một chủ đề lớn của rất nhiều [sách](https://www.amazon.com/s/ref=nb_sb_noss_2?url=search-alias%3Daps&field-keywords=sql+tuning) đã được viết như một nguồn tham khảo.

Nó rất quan trọng để **benchmark** và **profile** để mô phỏng và phát hiện các nút thắt cổ chai.

* **Benchmark** - Mô phỏng trường hợp tải cao với công cụ như [ab](http://httpd.apache.org/docs/2.2/programs/ab.html).
* **Profile** - Công cụ kiểm định như [slow query log](http://dev.mysql.com/doc/refman/5.7/en/slow-query-log.html) để theo dõi các vấn đề về hiệu năng.

Benchmarking và profiling có thể giúp cho bạn cải thiện hiệu năng theo những cách sau.

##### Làm chặt hơn schema

* MySQL dumps vào đĩa bằng các block liên tiếp cho việc truy cập nhanh.
* Sử dụng `CHAR` thay vì `VARCHAR` cho các trường có độ dài cố định.
    * `CHAR` cho phép random access một cách hiệu quả, trong khi với `VARCHAR`, bạn phải tìm đến hết string trước khi chuyển sang cái tiếp theo.
* Sử dụng `TEXT` cho một lượng lớn ký tự như một bài đăng của blog. `TEXT` còn cho phép boolean seach. Sử dụng `TEXT` lưu một con trỏ tới đĩa để lưu trũ text block.
* Sử dụng `INT` cho các số từ 2^32 hoặc 4 tỉ.
* Sử dụng `DECIMAL` cho đơn vị tiền tệ.
* Tránh sử dụng `BLOBS` lớn, thay vào đó lưu địa chỉ của tài nguyên.
* `VARCHAR(255)` là số ký tự lớn nhất có thể đếm được bằng số 8-bit, thường tối đa hóa việc sử dụng byte trong một số RDBMS.
* Set `NOT NULL` ở các trường có thể dùng để tăng hiệu năng [improve search performance](http://stackoverflow.com/questions/1017239/how-do-null-values-affect-performance-in-a-database-search).

##### Sử dụng việc đánh chỉ số tốt

* Cột mà bạn truy vấn (`SELECT`, `GROUP BY`, `ORDER BY`, `JOIN`) có thể nhanh hơn nhờ index.
* Index thường được biểu diễn dưới dạng cây cân bằng [B-tree](https://en.wikipedia.org/wiki/B-tree) giữa cho dữ liệu được sắp xếp để tìm kiếm, truy cập tuần tự, thêm, và xóa đọ phức tạp logarit.
* Việc index yêu cầu thêm không gian lưu trữ.
* Việc viết có thể chậm hơn nếu dùng index.
* Khi loading một lượng lớn dữ liệu, có thể nhanh hơn nếu vô hiệu hóa index, load dữ liệu, sau đó xây dựng lại index.

##### Tránh join

* Denormalize, khi hiệu năng yêu cầu đến nó.

##### Phân mảnh bảng

* Chia bảng bằng cách đặt các điểm nóng trong một bảng riêng biệt để giúp giữ nó trong memory.

##### Điều chỉnh query cache

* Trong một vài trường hợp, [query cache](http://dev.mysql.com/doc/refman/5.7/en/query-cache) có thể dẫn đến [các vấn đề về hiệu năng](https://www.percona.com/blog/2014/01/28/10-mysql-performance-tuning-settings-after-installation/).

##### Nguồn và tài liệu đọc thêm: SQL tuning

* [Tips for optimizing MySQL queries](http://20bits.com/article/10-tips-for-optimizing-mysql-queries-that-dont-suck)
* [Is there a good reason i see VARCHAR(255) used so often?](http://stackoverflow.com/questions/1217466/is-there-a-good-reason-i-see-varchar255-used-so-often-as-opposed-to-another-l)
* [How do null values affect performance?](http://stackoverflow.com/questions/1017239/how-do-null-values-affect-performance-in-a-database-search)
* [Slow query log](http://dev.mysql.com/doc/refman/5.7/en/slow-query-log.html)

### Cơ sở dữ liệu NoSQL
* [List Of NoSQL Databases](http://nosql-database.org/)

NoSQL is là một tập các dữ liệu được biểu hiện theo cách **key-value store**, **document-store**, **wide column store**, hoặc là một **graph database**.  Dữ liệu là không chuẩn hóa, và phép join được sử dụng ở mức code. Hầu hết chúng không dùng ACID mà dùng [eventual consistency](#eventual-consistency).

**BASE** thường được dùng trong NoSQL. Theo [CAP Theorem](#cap-theorem), BASE chọn tính sẵn sàng cao hơn tính nhất quán.

* **Basically available** - hệ thống đảm bảo tính sẵn sàng.
* **Soft state** - Trạng thái có thể thay đổi theo thời gian, kể cả không có input.
* **Eventual consistency** - Hệ thống sẽ nhất quán sau một khoảng thời gian nhất định.

Thêm vào đó chọn [SQL hay NoSQL](#sql-or-nosql), rất hữu ích để hiểu được NoSQL phù hợp với ca sử dụng nào nhất. Chúng tôi sẽ review **key-value stores**, **document-stores**, **wide column stores**, và **graph databases** ở phần tiếp theo.

#### Key-value store
> Abstraction: Bảng băm(hash table)

Một CSDL key-value thông thường cho độ phức tạp O(1) cho việc đọc ghi và thường được sử dụng trên RAM hoặc SSD để tối ưu hóa tốc độ. CSDL có thể duy trì khóa theo [thứ tự từ điển (lexicographical order)](https://en.wikipedia.org/wiki/Lexicographical_order), cho phép truy xuất hiệu quả các vùng khóa (key range).  Nó có thể cho phép lưu giá trị (value) dưới dạng siêu dữ liệu (metadata).

CSDL cung cấp hiệu năng cao và thường được sử dụng cho mô hình dữ liệu đơn giản hoặc các dữ liệu thay đổi nhanh, ví dụ như các dữ liệu được lưu ở lớp in-memory cache. Bởi vì chúng chỉ cung cấp một tập hữu hạn các toán tử, các toán tử phức tạp sẽ được chuyển đến lớp application.

CSDL key-value là nền tảng cho các hệ thống phức tạp hơn như CSDL dạng document, và trong một số trường hợp là graph database.

##### Nguồn và tài liệu đọc thêm: key-value store

* [Key-value database](https://en.wikipedia.org/wiki/Key-value_database)
* [Disadvantages of key-value stores](http://stackoverflow.com/questions/4056093/what-are-the-disadvantages-of-using-a-key-value-table-over-nullable-columns-or)
* [Redis architecture](http://qnimate.com/overview-of-redis-architecture/)
* [Memcached architecture](https://www.adayinthelifeof.nl/2011/02/06/memcache-internals/)

#### Document store

> Abstraction: key-value store với documents được lưu như một giá trị

Một document store lấy văn bản (document) làm trung tâm (XML, JSON, binary, ...), một document có thể lưu mọi thông tin của một đối tượng.  Document stores cung cấp các API hoặc một ngôn ngữ truy vấn để truy vấn dựa trên cấu trúc nội tại của văn bản.  *Ghi chú, nhiều key-value store có bao gồm các tính năng để làm việc với siêu dữ liệu, làm mờ ranh giới giữa 2 loại CSDL.*

Dựa trên phần cài đặt phía dưới, văn bản được tổ chức dưới dạng các collection, tag, metadata, hoặc directorie.  Mặc dù các văn bản có thể được tổ chức hoặc nhóm lại với nhau, Văn bản có thể chứa các trường khác hoàn toàn với phần còn lại.

Một vài CSDL nổi tiếng như [MongoDB](https://www.mongodb.com/mongodb-architecture) và [CouchDB](https://blog.couchdb.org/2016/08/01/couchdb-2-0-architecture/) cung cấp ngôn ngữ truy vấn giống SQL.  [DynamoDB](http://www.read.seas.harvard.edu/~kohler/class/cs239-w08/decandia07dynamo.pdf) cung cấp cả dạng key-value và document.

Document stores cung cấp độ linh hoạt cao và thường được dùng với những loại dữ liệu phải thay đổi đột ngột.

##### Nguồn và tài liệu đọc thêm: document store

* [Document-oriented database](https://en.wikipedia.org/wiki/Document-oriented_database)
* [MongoDB architecture](https://www.mongodb.com/mongodb-architecture)
* [CouchDB architecture](https://blog.couchdb.org/2016/08/01/couchdb-2-0-architecture/)
* [Elasticsearch architecture](https://www.elastic.co/blog/found-elasticsearch-from-the-bottom-up)

#### Wide column store

<p align="center">
  <img src="http://i.imgur.com/n16iOGk.png">
  <br/>
  <i><a href=http://blog.grio.com/2015/11/sql-nosql-a-brief-history.html>Source: SQL & NoSQL, a brief history</a></i>
</p>

> Abstraction: nested map `ColumnFamily<RowKey, Columns<ColKey, Value, Timestamp>>`

Đơn vị dữ liệu cơ bản của wide column store là một cột (cặp name/value). Một cột có thể được nhóm vào một họ các cột (column family) (tương tự như một bảng bên SQL).  Super column family là sự nhóm lại của các column family. Bạn có thể truy cập mỗi cột một cách độc lập với một row key, và các cột với cùng một row key tạo thành một dòng. Mỗi giá trị bao gồm một timestamp cho việc tạo phiên bản (versioning) và để giải quyết các sung đột.

Google giới thiệu [Bigtable](http://www.read.seas.harvard.edu/~kohler/class/cs239-w08/chang06bigtable.pdf) như là wide column store đầu tiên, nó tác động tới dự án open-source [HBase](https://www.mapr.com/blog/in-depth-look-hbase-architecture) thường được sử dụng trong hệ sinh thái Hadoop, và [Cassandra](http://docs.datastax.com/en/archived/cassandra/2.0/cassandra/architecture/architectureIntro_c.html) từ Facebook.  Các CSDL ví dụ như BigTable, HBase, và Cassandra duy trì khóa theo thứ tự bảng chữ cái.

Wide column stores cung cấp tính sẵn sàng và mở rộng cao. Chúng thường được sử dụng để giải quyết lượng dữ liệu rất lớn.

##### Nguồn và tài liệu đọc thêm: wide column store

* [SQL & NoSQL, a brief history](http://blog.grio.com/2015/11/sql-nosql-a-brief-history.html)
* [Bigtable architecture](http://www.read.seas.harvard.edu/~kohler/class/cs239-w08/chang06bigtable.pdf)
* [HBase architecture](https://www.mapr.com/blog/in-depth-look-hbase-architecture)
* [Cassandra architecture](http://docs.datastax.com/en/archived/cassandra/2.0/cassandra/architecture/architectureIntro_c.html)

#### Graph database

<p align="center">
  <img src="http://i.imgur.com/fNcl65g.png">
  <br/>
  <i><a href=https://en.wikipedia.org/wiki/File:GraphDatabase_PropertyGraph.png>Source: Graph database</a></i>
</p>

> Abstraction: graph

Trong CSDL đồ thị (graph database), mỗi nút(node) là một bản ghi và mỗi cạnh là một quan hệ (relationship) giữa hai nút. Graph databases được tối ưu cho việc biểu diễn dữ liệu với các quan hệ phức tạp với rất nhiều khóa ngoại hay quan hệ nhiều nhiều.

Graphs databases cung cấp hiệu năng cao cho mô hình dữ liệu với các quan hệ phức tạp, ví dụ mạng xã hội. Chúng tương đối mới và chưa được sử dụng rộng rãi; Sẽ khó hơn cho bạn trong việc tìm tài nguyên hay công cụ phát triển. Nhiều CSDL dạng này chỉ có thê truy cập qua [REST APIs](#representational-state-transfer-rest).

##### Nguồn và tài liệu đọc thêm: graph
* [Graph database](https://en.wikipedia.org/wiki/Graph_database)
* [Neo4j](https://neo4j.com/)
* [CQL](https://neo4j.com/developer/cypher-query-language/)
* [FlockDB](https://blog.twitter.com/2010/introducing-flockdb)

#### Nguồn và tài liệu đọc thêm: NoSQL

* [Explanation of base terminology](http://stackoverflow.com/questions/3342497/explanation-of-base-terminology)
* [NoSQL databases a survey and decision guidance](https://medium.com/baqend-blog/nosql-databases-a-survey-and-decision-guidance-ea7823a822d#.wskogqenq)
* [Scalability](http://www.lecloud.net/post/7994751381/scalability-for-dummies-part-2-database)
* [Introduction to NoSQL](https://www.youtube.com/watch?v=qI_g07C_Q5I)
* [NoSQL patterns](http://horicky.blogspot.com/2009/11/nosql-patterns.html)

### SQL hay NoSQL

<p align="center">
  <img src="http://i.imgur.com/wXGqG5f.png">
  <br/>
  <i><a href=https://www.infoq.com/articles/Transition-RDBMS-NoSQL/>Source: Transitioning from RDBMS to NoSQL</a></i>
</p>

Lý do cho **SQL**:

* Dữ liệu có cấu trúc
* schema chặt chẽ
* Dữ liệu có tính quan hệ cao
* Cần các phép nối phức tạp
* Cần đến Transaction (đảm bảo ACID)
* Các mẫu rõ ràng cho việc mở rộng
* Được hỗ trợ nhiều hơn từ: developers, community, code, tools, ...
* Tra cứu trên index rất nhanh

Lý do cho **NoSQL**:

* Dữ liệu có tính bán cấu trúc
* schema động và linh hoạt
* Dữ liệu ít có tính quan hệ
* Không cần các phép nối phức tạp
* Lưu dữ liệu nhiều đên mữ TB, PB
* Cần chịu tải rất lớn
* Cần thông lượng cao cho IOPS

Các dữ liệu mẫu thích hợp cho NoSQL:

* Rapid ingest of clickstream and log data
* Leaderboard or scoring data
* Temporary data, such as a shopping cart
* Frequently accessed ('hot') tables
* Metadata/lookup tables

##### Nguồn và tài liệu đọc thêm: SQL or NoSQL

* [Scaling up to your first 10 million users](https://www.youtube.com/watch?v=vg5onp8TU6Q)
* [SQL vs NoSQL differences](https://www.sitepoint.com/sql-vs-nosql-differences/)

## Cache

<p align="center">
  <img src="http://i.imgur.com/Q6z24La.png">
  <br/>
  <i><a href=http://horicky.blogspot.com/2010/10/scalable-system-design-patterns.html>Source: Scalable system design patterns</a></i>
</p>

Caching cải thiện thời gian tải trang và giảm thiểu việc phải tương tác với database của server. Ở mô hình này, Bộ điểu phối (Dispatcher) trước tiên sẽ tra cứu nếu request đã được thực hiện trước đó và cố gắng tìm kết qủa trước đó để trả lại, để tiết kiệm thời gian thực thi.

Cơ sở dữ liệu thường hoạt động tốt nhờ việc phân phối đồng đều các lần đọc ghi trên các phân vùng của nó. Các item phổ biến sẽ làm mất cân bằng phân phối, gây nghẽn cổ trai. Đưa một bộ nhơ đệm (cache) ở phía trước cơ sở dữ liệu có thể giải quyết vấn đề tải không đều và sự tăng đột biến lượng truy cập.

### Client caching

Caches có thể được đặt bên phía client (Hệ điều hành hoặc trình duyệt), [server side](#reverse-proxy), hoặc ở một lớp bộ nhớ đệm khác.

### CDN caching

[CDNs](#content-delivery-network) được coi là một loại bộ nhớ cache.

### Web server caching

[Reverse proxies](#reverse-proxy-web-server) và cache ví dụ như [Varnish](https://www.varnish-cache.org/) có thể phục vụ trực tiếp các nội dung tĩnh và động.  Web servers còn có thể cache lại request, trả về responses mà không cần giao tiếp với application server.

### Database caching

Cơ sở dữ liệu thường bao gồm một vài mức cache ở cấu hình mặc định, tối ưu hóa cho việc sử dụng chung nhất. Tinh chỉnh các cấu hình này cho các trường hợp sử dụng đặc thù có thể làm tăng thêm hiệu suất.


### Application caching

In-memory caches ví dụ như Memcached và Redis là các giá trị key-value giữa ứng dụng và your data storage.  Bởi vì dữ liệu được giữ trên RAM, nó sẽ nhanh hơn rất nhiều so với dữ liệu được lấy từ database (lưu trên đĩa). Dung lượng RAM hạn chế hơn dung lượng đĩa, vì vậy thuật toán [cache invalidation](https://en.wikipedia.org/wiki/Cache_algorithms) ví dụ [least recently used (LRU)](https://en.wikipedia.org/wiki/Cache_algorithms#Least_Recently_Used) có thể bỏ các dữ liệu ít dùng và giữ lại các dữ liệu thường xuyên được sử dụng trên RAM.

Redis có các tính năng bổ sung dưới đây:

* Tùy chọn lưu trữ lâu dài (Persistence option)
* Cấu trúc dữ liệu dựng sẵn ví dụ như sorted sets và list

Có nhiều mức cache được xếp vào hai loại chính: **database queries** và **objects**:

* Row level
* Query-level
* Fully-formed serializable objects
* Fully-rendered HTML

Thông thường bạn nên cố tránh cache trên tệp, ví nó làm cho việc nhân bản và tự động mở rộng trở nên khó khăn hơn.

### Caching at the database query level

Bất kì khi nào bạn truy vấn, băm truy vấn thành một khóa và lưu kết quả vào cache. 

Cách tiếp cận này có những vấn đề sau:

* Khó để xóa các dữ liệu đã cache với truy vấn phức tạp
* Nếu một mảnh dữ liệu thay đổi ví dụ như một ô trên bảng, bạn phải xóa toàn bộ các truy vấn đã cache có chứa ô bị thay đổi đó.

### Caching at the object level

Coi dữ liệu như các đối tượng, tương tự với việc bạn làm với mã nguồn.  Have your application assemble the dataset from the database into a class instance or a data structure(s):

* Xóa đối tượng nếu dữ liệu ở mức dưới có sự thay đổi.
* Cho phép xử lý bất đồng bộ: workers tập hợp các đối tượng bằng cách tiêu thụ các đối tượng được cache gần nhất.

Gợi ý các thành phần nên cache:

* User sessions
* Fully rendered web pages
* Activity streams
* User graph data

### Khi nào nên cập nhật cache

Bởi vì bạn chỉ có thể lưu một lượng giới hạn dữ liệu trong cache, bạn cần chọn chiến lược cập nhật phù hợp với trường hợp của mình.

#### Cache-aside

<p align="center">
  <img src="http://i.imgur.com/ONjORqk.png">
  <br/>
  <i><a href=http://www.slideshare.net/tmatyashovsky/from-cache-to-in-memory-data-grid-introduction-to-hazelcast>Source: From cache to in-memory data grid</a></i>
</p>

Hệ thống chịu trách nhiệm đọc và ghi từ bộ nhớ. Bộ nhớ đệm không trực tiếp tương tác với cơ sở dữ liệu. Hệ thống sẽ làm những việc sau:

* Tra cứu entry trong cache, nếu cache-miss
* Tải entry lên từ đĩa
* Thêm entry vào cache
* Trả về entry

```
def get_user(self, user_id):
    user = cache.get("user.{0}", user_id)
    if user is None:
        user = db.query("SELECT * FROM users WHERE user_id = {0}", user_id)
        if user is not None:
            key = "user.{0}".format(user_id)
            cache.set(key, json.dumps(user))
    return user
```
[Memcached](https://memcached.org/) thường được dùng trong trường hợp này.

Đọc tuần tự dữ liệu được thêm vào cache thì nhanh. Cache-aside cũng được gọi là lazy loading. Chỉ những dữ liệu yêu cầu mới được cache, tránh đưa vào cache những dữ liệu không được yêu cầu.

#### Write-through

<p align="center">
  <img src="http://i.imgur.com/0vBc0hN.png">
  <br/>
  <i><a href=http://www.slideshare.net/jboner/scalability-availability-stability-patterns/>Source: Scalability, availability, stability, patterns</a></i>
</p>

Hệ thống sử dụng cache như một nơi lưu trữ chính, đọc và ghi dữ liệu lên nó, trong khi cache đóng vai trò đọc và ghi dữ liệu trên database:

* Hệ thống thêm, sửa entry trên cache
* Cache ghi một cách đồng bộ lên 
* Trả về kết quả

Application code:

```
set_user(12345, {"foo":"bar"})
```

Cache code:

```
def set_user(user_id, values):
    user = db.query("UPDATE Users WHERE id = {0}", user_id, values)
    cache.set(user_id, user)
```

Write-through là chậm trên tổng thể do thao tác ghi, nhưng đọc tuần tự trên các dữ liệu vừa được ghi là nhanh. Người dùng thường dễ chấp nhận độ trễ cho cập nhật dữ liệu hơn là khi đọc dữ liệu. Dữ liệu trong cache không bị cũ.

#### Write-behind (write-back)

<p align="center">
  <img src="http://i.imgur.com/rgSrvjG.png">
  <br/>
  <i><a href=http://www.slideshare.net/jboner/scalability-availability-stability-patterns/>Source: Scalability, availability, stability, patterns</a></i>
</p>

Trong write-behind, Ứng dụng sẽ làm các bước sau:

* Thêm, cập nhật vào cache
* Ghi bất đồng bộ ra database, cải thiện hiệu năng ghi

##### Nhược điểm: write-behind

* Có thể mất mát dữ liệu nếu dữ liệu mới chỉ được ghi vào cache mà chưa được ghi vào data.
* Cài đặt có thể khó hơn write-through hoặc cache aside.

#### Refresh-ahead

<p align="center">
  <img src="http://i.imgur.com/kxtjqgE.png">
  <br/>
  <i><a href=http://www.slideshare.net/tmatyashovsky/from-cache-to-in-memory-data-grid-introduction-to-hazelcast>Source: From cache to in-memory data grid</a></i>
</p>

Bạn có thể cấu hình cache làm mới tự động các entry được truy cập gần đây trước thời gian nó hết hạn.

Refresh-ahead có thể giảm độ trễ với read-through nếu cache có thể dự đoán chính xác item nào có thể được truy cập trong tương lai.

##### Bất lợi: refresh-ahead

* Việc tiên đoán có thể làm ảnh hưởng đến hiệu năng.

### Nhược điểm: cache

* Cần đảm bảo thông tin là đúng và nhất quán giũa cache và database, [Các giải thuật về cache](https://en.wikipedia.org/wiki/Cache_algorithms).
* Cần thay đổi ứng dụng nếu thêm Redis hay Memcache.
* Chiến lược cập nhật cache là tương đối khó và có sự đặc thù cho các ứng dụng khác nhau.

### Nguồn và tài liệu đọc thêm

* [From cache to in-memory data grid](http://www.slideshare.net/tmatyashovsky/from-cache-to-in-memory-data-grid-introduction-to-hazelcast)
* [Scalable system design patterns](http://horicky.blogspot.com/2010/10/scalable-system-design-patterns.html)
* [Introduction to architecting systems for scale](http://lethain.com/introduction-to-architecting-systems-for-scale/)
* [Scalability, availability, stability, patterns](http://www.slideshare.net/jboner/scalability-availability-stability-patterns/)
* [Scalability](http://www.lecloud.net/post/9246290032/scalability-for-dummies-part-3-cache)
* [AWS ElastiCache strategies](http://docs.aws.amazon.com/AmazonElastiCache/latest/UserGuide/Strategies.html)
* [Wikipedia](https://en.wikipedia.org/wiki/Cache_(computing))

## Bất đồng bộ (Asynchronism)

<p align="center">
  <img src="http://i.imgur.com/54GYsSx.png">
  <br/>
  <i><a href=http://lethain.com/introduction-to-architecting-systems-for-scale/#platform_layer>Source: Intro to architecting systems for scale</a></i>
</p>

Các luồng làm việc bất đồng bộ (Asynchronous workflow) giúp giảm thiểu thời gian yêu cầu cho những tác vụ tốn tài nguyên mà bình thường chứng được xử lý đồng bộ. Chúng cũng giúp đỡ bằng cách làm những việc tốn thời gian trước, ví dụ như tập hợp dữ liệu một cách định kỳ.

### Message queues

Message queues nhận, giữ, và vận chuyển các tin nhắn. Nếu một tác vụ mất nhiều thời gian để xử lý một các đồng bộ, bạn có thể dùng một message queue với luồng công việc dưới đây:

* Một ứng dụng công bố (publish) một công việc đến hàng đợi, sau đó thông báo cho người dùng trạng thái của coong việc
* Một worker lấy (pick up) công việc từ hang đợi, xử lý nó, sau đó thông báo là công việc đã hoàn thành

Người dùng không đợi cho đến khi công việc xử lý xong và công việc được xử lý dưới nền. Trong suốt thời gian này, phía client có thể làm một chút xử lý nhó để làm như công việc đã xửu lý xong. Ví dụ, Nếu đăng lên tweet, tweet sẽ ngay lập tức được đưa lên timeline, nhưng có thể phải mất một chút thời gian để tweet của bạn thực sự được đưa đến những người theo dõi.

**Redis** là hữu dụng nư một message broker đơn giản nhưng tin nhắn có thể bị mất.

**RabbitMQ** phổ biến nhưng yêu cầu bạn làm cho hệ thống tương thích với giao thức 'AMQP' và quản lý các node của bạn.

**Amazon SQS**, được tổ chức (hosted) nhưng có độ trễ cao và có thể tin nhắn sẽ được gửi đi đến hai lần (lặp).

### Task queues

Các Tasks queue nhận các task và những dữ liệu liên quan, chạy chúng, sau đó chuyển đi các kết quả của chúng. Task queue hỗ trợ lập lịch cà có thể chạy các công việc đòi hỏi tính toán nhiều ở trong nền.

**Celery** hỗ trợ lạp lịch và chủ yếu hỗ trợ python.

### Back pressure

Nếu các hàng đợi lớn lên đáng kể, kích cỡ hàng đợi có thể lớn hơn bộ nhớ, dẫn đến cache mis, đọc từ đĩa, và hiệu năng chậm đi đáng kể. [Back pressure](http://mechanical-sympathy.blogspot.com/2012/05/apply-back-pressure-when-overloaded.html) có thể giới hạn kích cỡ hàng đợi, qua đó duy trì một tỉ lệ băng thông cao và thời gian phản hồi tốt cho các công việc có trong hàng đợi. Khi mà hàng đợi đầy, client sẽ nhận phản hồi bận từ server hoặc mã trạng thái HTTP 503 để thử lại lần nữa. Client có thể thử request sau đó, có thể với [exponential backoff](https://en.wikipedia.org/wiki/Exponential_backoff).

### Nhược điểm: asynchronism

* Các ca sử dụng như các tính toán nhẹ và các luồng xử lý thời gian thực có thể sẽ thích hợp hơn nếu dùng xử lý đồng bộ, trong khi xử lý bất đồng bộ có thể chậm và phức tạp.

### Nguồn và tài liệu đọc thêm

* [It's all a numbers game](https://www.youtube.com/watch?v=1KRYH75wgy4)
* [Applying back pressure when overloaded](http://mechanical-sympathy.blogspot.com/2012/05/apply-back-pressure-when-overloaded.html)
* [Little's law](https://en.wikipedia.org/wiki/Little%27s_law)
* [What is the difference between a message queue and a task queue?](https://www.quora.com/What-is-the-difference-between-a-message-queue-and-a-task-queue-Why-would-a-task-queue-require-a-message-broker-like-RabbitMQ-Redis-Celery-or-IronMQ-to-function)

## Communication

<p align="center">
  <img src="http://i.imgur.com/5KeocQs.jpg">
  <br/>
  <i><a href=http://www.escotal.com/osilayer.html>Source: OSI 7 layer model</a></i>
</p>

### Hypertext transfer protocol (HTTP)
### Transmission control protocol (TCP)
### User datagram protocol (UDP)

### Remote procedure call (RPC)

<p align="center">
  <img src="http://i.imgur.com/iF4Mkb5.png">
  <br/>
  <i><a href=http://www.puncsky.com/blog/2016/02/14/crack-the-system-design-interview/>Source: Crack the system design interview</a></i>
</p>

Trong RPC, một client tạo nên một thủ tục có thể được thực thi ở một địa chỉ khác, thường là server từ xa. Thủ tục được mã hóa như thể nó là một cuộc gọi cục bộ, trừu tượng hóa các công đoạn cụ thể làm thế nào để server liên lạc với client. Gọi từ xa thường chậm hơn và ít phụ thuộc hơn so với gọi cụ bộ nên nó rất hữu dụng để để phân biệc một RPC call hay cuộc gọi cục bộ. RPC frameworks phổ biến bao gồm [Protobuf](https://developers.google.com/protocol-buffers/), [Thrift](https://thrift.apache.org/), và [Avro](https://avro.apache.org/docs/current/).

RPC là một giao thức request-response:

* **Client program** - gọi stub procedure bên client.  Tham số được thêm vào ngăn xếp như là gọi thủ tục cục bộ.
* **Client stub procedure** - Marshals (gói) id và các tham số của thủ tục vào một request mesage.
* **Client communication module** - Hệ điều hành gửi mesage từ client lên server.
* **Server communication module** - hệ điều hành chuyển message đến stub procedure bên server.
* **Server stub procedure** -  Unmarshalls (giải nén) kết quả, gọi các thủ tục phía server phù hợp với id của thủ tục được gửi đến và truyền vào các tham số nhận được.
* server phàn hồi bằng cách lặp lại các bước trên ở thứ tự ngược lại.

gọi RPC mẫu:

```
GET /someoperation?data=anId

POST /anotheroperation
{
  "data":"anId";
  "anotherdata": "another value"
}
```

RPC tập trung vào các hành vi. RPC thường được sử dụng cho vấn đề về hiệu năng với những giao tiếp nội tại, vì bạn có thể gọi bản địa (native call) một cách thủ công để phù hợp hơn với ca sử dụng (khác REST).

Chọn một native library (aka SDK) khi:

* Bạn biết nền tảng nhắm tới.
* Bạn muốn kiểm soát "logic được truy cập như thế nào".
* Bạn muốn kiểm soát cơ chế kiểm soát lỗi xảy ra như thế nào trong thư viện của bạn.
* Hiệu năng và trải nghiệm người dùng cuối là điều lo lắng chính của bạn.

HTTP API dưới đây **REST** có xu hướng được sử dụng nhiều hơn cho public API.

#### Nhược điểm: RPC

* RPC client có liên kết chặt chẽ với việc cài đặt phía server.
* Một API mới sẽ phải định nghĩa lại cho tất cả tác vụ hoặc ca sử dụng.
* Khó để có thể debug RPC.
* You có thể không có khả năng nâng cấp các công nghệ đang có. Ví dụ, có thể yêu cầu thêm nỗ lực để chắc chắn [RPC call đã được cache](http://etherealbits.com/2012/12/debunking-the-myths-of-rpc-rest/) ở server cache như [Squid](http://www.squid-cache.org/).

### Representational state transfer (REST)

REST is là một kiểu kiến trúc thi hành một mô hình client/server mà client thực hiện hành vi trên một tập các tài nguyên được quản lý bới server. Server cung cấp một đại diện cho tài nguyên và hành vi mà có thể được vận dụng cũng như lấy một đại diện mới của các tài nguyên. Tất cả giao tiếp phải là stateless và có thể cache được.

Có 4 tiêu chí chất lượng cho một giao diện RESTful:

* **(Xác định tài nguyên) (URI trong HTTP)** - sử dụng cùng một URI cho bất kỳ tác vụ nào.
* **Thay đổi với representations (Verbs trong HTTP)** - sử dụng verb, header, and body.
* **Self-descriptive error message (status response trong HTTP)** - Sử dụng status code, "đừng phát minh lại chiếc bánh xe".
* **[HATEOAS](http://restcookbook.com/Basics/hateoas/) (HTML interface for HTTP)** - web service của bạn nên được truy cập đầy đủ trong một trình duyệt.

Mẫu cho việc sử dụng REST:

```
GET /someresources/anId

PUT /someresources/anId
{"anotherdata": "another value"}
```

REST lại tập trung vào việc phơi bày (expose) dữ liệu. tối hiểu hóa sự liên kết giữ client/server và thường được sử dụng trong các public HTTP API. REST sử dụng method một cách chuẩn mực và chung chung hơn thông qua API, [đại diện thông qua header](https://github.com/for-GET/know-your-http-well/blob/master/headers.md), và các hành vi thông qua verbs như GET, POST, PUT, DELETE, và PATCH.  Là stateless, REST là rất tuyệt cho việc mở rộng theo chiều ngang và phân mảnh.

#### Nhược điểm: REST

* Với việc REST tập trung vào dữ liệu được phơi bày (exposing data), nó có thể không hoàn toàn tương thích nếu tài nguyên không được tổ chức theo nguyên tắc hoặc được truy cập dưới dạng phân cấp đơn giản. Ví dụ, trả về tất cả các bản ghi đã được cập nhật từ giờ trước match với một tập các sự kiện không dễ để thể hiện với một đường dẫn. Với REST, Nó như là một sự cài đặt với sự kết hợp của đường dẫn URI, query parameter, và có thể còn request body nữa.
* REST thông thường phụ thuộc vào một vài verbs (GET, POST, PUT, DELETE, và PATCH) đôi khi không phù hợp với ca sử dụng của bạn. Ví dụ, chuyển một tài liệu đã hết hạn đến một thư mục có thể không hoàn toàn phù hợp với những verb này.
* Việc nạp các tài nguyên phức tạp với phân cấp lồng nhau yêu cầu nhiều lần kết nối giũa client và server để render một giao diện, ví dụ. nạp nội dung cho một blog và bình luận cho blog đó. Đối với các thiết bị di động hoạt động trên mỗi trường mạng bất ổn, việc này sẽ có vấn đề.
* Theo thời gian, nhiều trường được thêm vào API response và các client cũ phải nhận thêm các trường dữ liệu mới này, mặc cho chúng không hề cần các trường đó, như một hệ quả, nó làm tăng kích thước của payload và dẫn đến độ trễ gia tăng.

### So sánh RPC and REST

| Operation | RPC | REST |
|---|---|---|
| Signup	| **POST** /signup | **POST** /persons |
| Resign	| **POST** /resign<br/>{<br/>"personid": "1234"<br/>} | **DELETE** /persons/1234 |
| Read a person | **GET** /readPerson?personid=1234 | **GET** /persons/1234 |
| Read a person’s items list | **GET** /readUsersItemsList?personid=1234 | **GET** /persons/1234/items |
| Add an item to a person’s items | **POST** /addItemToUsersItemsList<br/>{<br/>"personid": "1234";<br/>"itemid": "456"<br/>} | **POST** /persons/1234/items<br/>{<br/>"itemid": "456"<br/>} |
| Update an item	| **POST** /modifyItem<br/>{<br/>"itemid": "456";<br/>"key": "value"<br/>} | **PUT** /items/456<br/>{<br/>"key": "value"<br/>} |
| Delete an item | **POST** /removeItem<br/>{<br/>"itemid": "456"<br/>} | **DELETE** /items/456 |

<p align="center">
  <i><a href=https://apihandyman.io/do-you-really-know-why-you-prefer-rest-over-rpc/>Source: Do you really know why you prefer REST over RPC</a></i>
</p>

#### Nguồn và tài liệu đọc thêm: REST and RPC

* [Do you really know why you prefer REST over RPC](https://apihandyman.io/do-you-really-know-why-you-prefer-rest-over-rpc/)
* [When are RPC-ish approaches more appropriate than REST?](http://programmers.stackexchange.com/a/181186)
* [REST vs JSON-RPC](http://stackoverflow.com/questions/15056878/rest-vs-json-rpc)
* [Debunking the myths of RPC and REST](http://etherealbits.com/2012/12/debunking-the-myths-of-rpc-rest/)
* [What are the drawbacks of using REST](https://www.quora.com/What-are-the-drawbacks-of-using-RESTful-APIs)
* [Crack the system design interview](http://www.puncsky.com/blog/2016/02/14/crack-the-system-design-interview/)
* [Thrift](https://code.facebook.com/posts/1468950976659943/)
* [Why REST for internal use and not RPC](http://arstechnica.com/civis/viewtopic.php?t=1190508)

## Bảo mật (Security)

Phần này sẽ cần cập nhật thêm.

Bảo mật là một chủ đề rất rộng. Nên ở đây chỉ nêu một vài vấn đề cơ bản

* Mã hóa trong chuyển tiếp cũng như trong lưu trữ.
* Khử độc(Sanitize) tất cả đầu vào của người dùng để tránh tấn công [XSS](https://en.wikipedia.org/wiki/Cross-site_scripting) và [SQL injection](https://en.wikipedia.org/wiki/SQL_injection).
* Sử dụng các truy vấn có thể truyền tham số để tránh SQL Injection (Các thư viện đều hỗ trợ, tốt hơn là nên dùng ORM).
* Sử dụng định lý [least privilege](https://en.wikipedia.org/wiki/Principle_of_least_privilege). Nên dùng các quy luật chặt chẽ để phân quyền trên các tiến trình và tài nguyên.

### Nguồn và tài liệu đọc thêm : Security

* [Security guide for developers](https://github.com/FallibleInc/security-guide-for-developers)
* [OWASP top ten](https://www.owasp.org/index.php/OWASP_Top_Ten_Cheat_Sheet)

<!-- Bổ sung về authentication bằng token -->
### Sử dụng JWT cho việc định danh (authentication) 

<p align="center">
  <img src="https://cdn.auth0.com/blog/cookies-vs-tokens/cookie-token-auth.png">
  <br/>
  <i><a href=https://auth0.com/blog/cookies-vs-tokens-definitive-guide/>Source: auth0</a></i>
</p>

* Lợi thế của JWT hay token-based authentication nói chung
    * **phi trạng thái (stateless), khả năng mở rộng (scalable) và tách biệt (decoupled):** có lẽ lợi thế lớn nhất của jwt so với dùng session là phi trạng thái. Server không phải lưu lại bản ghi của token mà chỉ cần xác nhận token đấy có hợp lệ hay không, bản thân token nó đã mang các thông tin cần thiết rồi.
    * **Cross Domain và CORS:** Session sẽ gặp khó khăn khi phải quản lý ở nhiều domain khác nhau, jwt có thể xử lý vấn đề này
    * **Store Data in the JWT:** jwt có thể lưu lại bất kỳ dữ liệu nào, nếu nó là một JSON hợp lệ. Bạn có thể lưu lại các thông tin cần thiết cho hệ thống của bạn.
    * **Hiệu năng:** Từ những lợi thế trên, ta sẽ có lợi thế về hiệu năng. Khi dùng session thông thường, server phải mở một hoặc nhiều kết nối để tìm kiếm trong CSDL trong khi dùng token thì bạn chỉ cần mở kết nối khi cần lấy dữ liệu mà thôi, tất cả thông tin về authentication cũng như authorization đều được lưu trong jwt.
    * **Mobile Ready:** Không phải thiết bị nào cũng hỗ trợ tốt cho cookie, jwt là một sự thay thế không tồi.

* Làm cách nào để vô hiệu hóa một jwt (cho việc đăng xuất cũng như hủy đăng nhập từ các thiết bị khác)
    * Xây dựng một danh sách đen (blacklist) các jwt bị vô hiệu hóa.
    * Set thời gian sống cho mỗi jwt thật ngắn, sau đó refresh lại token vào mốc thời gian cần thiết.

#### Nguồn và tài liệu đọc thêm: JWT
* [Cookies vs Tokens: The Definitive Guide](https://auth0.com/blog/cookies-vs-tokens-definitive-guide/)
* [Stop using JWT for sessions](http://cryto.net/~joepie91/blog/2016/06/13/stop-using-jwt-for-sessions/)

### Các kiểu tấn công web phổ biến
* [OWASP Top Ten Cheat Sheet](https://www.owasp.org/index.php/OWASP_Top_Ten_Cheat_Sheet)
### Tường lửa ứng dụng web
* Ruled base (Blacklist)
* Anormaly Detection (Whitelist)

## TODO
1. Centralized vs Decentralized vs Distributed
2. Apache vs Nginx
3. Redis Architecture
4. Zoo Keeper, ETCD


