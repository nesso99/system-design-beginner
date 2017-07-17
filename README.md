# Tìm hiểu về thiết kế hệ thống

## Mục lục 
1. [Hiệu năng và Khả năng mở rộng](#perfomance-scalability)

## Nguồn
* [The System Design Primer](https://github.com/donnemartin/system-design-primer)

## Động lực (Motivation)
* Học cách để thiết kế một hệ thống lớn có khả năng mở rộng
* Làm output cho đợt thực tập hè 2017 

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

#### Bước 2: Bài báo về khả năng mở rộng
[Scalability for Dummies](http://www.lecloud.net/tagged/scalability)
* Các chủ đề được đề cập:
    * [Clones](http://www.lecloud.net/post/7295452622/scalability-for-dummies-part-1-clones)
    * [Cơ sở dữ liệu](http://www.lecloud.net/post/7994751381/scalability-for-dummies-part-2-database)
    * [Caches](http://www.lecloud.net/post/9246290032/scalability-for-dummies-part-3-cache)
    * [Bất đồng bộ (Asynchronism)](http://www.lecloud.net/post/9699762917/scalability-for-dummies-part-4-asynchronism)

### Bước tiếp theo
Một số khái niệm ở mức cao hơn
* **Hiệu năng (Performance)** và **Khả năng mở rộng (Scalability)**
* **Độ trễ (Latency)** và **Thông lượng (Throughput)**
* **Tính sẵn sàng (Availability)** và **Tính nhất quán (Consistency)**

<div id="perfomance-scalability"></div>

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

Ở một hệ thống tính toán phân tán, Bạn chỉ có thể cung cấp hai trong số các tính đúng đắn dưới đây:

* **Tính nhất quán (Consistency)** - Mọi sự kiện đọc (read) đều nhận được phiên bản mới nhất của sự kiện ghi (write) gần nhất hoặc lỗi.
* **Tính sẵn sàng (Availability)** - Mọi request đều nhận một response, không cần đảm bảo dữ liệu nhận được là phiên bản mới nhất. 
* **Tính chịu đựng phân mảnh (Partition Tolerance)** - Hệ thống vẫn tiếp tục hoạt động mặc cho sự phân mảnh tùy ý (arbitrary partitioning) bị gây ra do lỗi mạng.

*Môi trường mạng là không đáng tin cậy, vì vậy bạn sẽ cần tính chịu đựng phân mảnh. Bạn sẽ cần cân nhắc giữa tính nhất quán và tính sẵn sàng.*

#### CP - consistency and partition tolerance

Waiting for a response from the partitioned node might result in a timeout error.  CP is a good choice if your business needs require atomic reads and writes.

#### AP - availability and partition tolerance

Responses return the most recent version of the data available on the a node, which might not be the latest.  Writes might take some time to propagate when the partition is resolved.

AP is a good choice if the business needs allow for [eventual consistency](#eventual-consistency) or when the system needs to continue working despite external errors.

## Các mẫu nhất quán (Consistency patterns)
Với nhiều bản sao của cùng một dữ kiệu, Chúng ta phải đối mặt với các lựa chọn về cách đồng bộ chúng để client có một cái nhìn nhất quán về dữ liệu.

### Nhất quán yếu (Weak consistency)

### Eventual consistency

### Nhất quán mạnh (Strong consistency)

### Nguồn và tài liệu đọc thêm
* [Transactions across data centers](http://snarfed.org/transactions_across_datacenters_io.html)

## Availability patterns

Có hai mẫu chính để hỗ trợ tính sẵn sàng cao: **fail-over** và **nhân bản (replication)**.

### Failover

#### Active-passive

Với active-passive fail-over, heartbeats được gửi giữa các mấy chủ chủ động (active server) và mấy chủ bị động (passive server) sẽ ở trạng thái chờ (standby).  Nếu heartbeat bị ngắt quãng, Máy chủ thụ động lấy địa chỉ ip của máy chủ chủ động và tiếp tục dịch vụ.

The length of downtime is determined by whether the passive server is already running in 'hot' standby or whether it needs to start up from 'cold' standby.  Only the active server handles traffic.

Active-passive failover can also be referred to as master-slave failover.

#### Active-active

In active-active, both servers are managing traffic, spreading the load between them.

If the servers are public-facing, the DNS would need to know about the public IPs of both servers.  If the servers are internal-facing, application logic would need to know about both servers.

Active-active failover can also be referred to as master-master failover.

### Nhân bản

#### Master-slave and master-master

Chủ đề này sẽ được bàn luận sâu hơn ở phần [Database](#database):

* [Master-slave replication](#master-slave-replication)
* [Master-master replication](#master-master-replication)

### Domain name system
### Content delivery network
### Bộ cân bằng tải (Load Balancer)
## Reverse proxy (web server)

<p align="center">
  <img src="http://i.imgur.com/n41Azff.png">
  <br/>
  <i><a href=https://upload.wikimedia.org/wikipedia/commons/6/67/Reverse_proxy_h2g2bob.svg>Source: Wikipedia</a></i>
  <br/>
</p>

Một reverse proxy là một web server tập trung các dịch vụ bên trong (internal services) và cung cấp giao diện được chuẩn hóa ra bên ngoài.  Requests từ clients được chuyển tiếp đến server có khả năng hoàn thành nó trước khi reverse proxy trả về response của server cho client.

Các lợi ích kèm theo bao gồm:

* **Tăng tính bảo mật** - Hide information about backend servers, blacklist IPs, limit number of connections per client
* **Tăng khả năng mở rộng và linh hoạt** - Clients only see the reverse proxy's IP, allowing you to scale servers or change their configuration
* **Chấm dứt SSL (SSL termination)** - Decrypt incoming requests and encrypt server responses so backend servers do not have to perform these potentially expensive operations
    * Removes the need to install [X.509 certificates](https://en.wikipedia.org/wiki/X.509) on each server
* **Nén (Compression)** - Compress server responses
* **Caching** - Return the response for cached requests
* **Các nội dung tĩnh (Static content)** - Nếu client yêu cầu các nội dung tĩnh không cần đến server xử lý, reverse proxy có thể trả về trực tiếp các nội dung này. 
    * HTML/CSS/JS
    * Photos
    * Videos
    * Etc

## Application layer

<p align="center">
  <img src="http://i.imgur.com/yB5SYwm.png">
  <br/>
  <i><a href=http://lethain.com/introduction-to-architecting-systems-for-scale/#platform_layer>Source: Intro to architecting systems for scale</a></i>
</p>

## Cơ sở dữ liệu (Database)
### Cơ sở dữ liệu quan hệ
### Cơ sở dữ liệu NoSQL
* Key - Value
* Document
* Wide column
* Graph

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

Hệ thống chịu trách nhiệm đọc và ghi từ bộ nhớ. Bộ nhớ đệm không trực tiếp tương tasc với cơ sở dữ liệu. Hệ thống sẽ làm những việc sau:

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

### Asynchronism
### Communication

## Bảo mật (Security)

### Các kiểu tấn công web phổ biến
* [OWASP Top Ten Cheat Sheet](https://www.owasp.org/index.php/OWASP_Top_Ten_Cheat_Sheet)
### Tường lửa ứng dụng web
* Ruled base (Blacklist)
* Anormaly Detection (Whitelist)


