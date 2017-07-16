# Tìm hiểu về thiết kế hệ thống
## Nguồn
* [The System Design Primer](https://github.com/donnemartin/system-design-primer)
* [Neo4j](./database/neo4j.md)

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
    * Clones
    * Cơ sở dữ liệu
    * Caches
    * Bất đồng bộ (Asynchronism)

### Hiệu năng (Performance) và Khả năng mở rộng (Scalability)
1. Hiệu năng: Tốc độ để sử lý một task nào đó
2. Khả năng mở rộng: Một dịch vụ được coi là có tính mở rộng (scalable) nếu nó mang lại kết quả hoạt động tăng theo tỉ lệ với các tài nguyên (resource) được thêm vào. Tăng hiệu năng có thể được hiểu là một lúc làm được nhiều việc hơn hay làm được một việc lớn hơn.  
### Độ trễ (Latency) và Thông lượng (Throughput)
1. Độ trễ: là thời gian để thực hiện một số hành động hoặc để tạo ra một số kết quả.
2. Thông lượng: là số hành động được thực hiện hay số kết quả được đưa ra trong một đơn vị thời gian 

* Thông thường, mục đích sẽ là cực đại thông lượng với độ trễ chấp nhận được.
### Tính sẵn sàng (Availability) và Tính nhất quán (Consistency)
1. Định lý CAP
### Các mẫu nhất quán (Consistency patterns)
### Availability patterns
#### Failover
#### Nhân bản (Replication)
### Domain name system
### Content delivery network
### Bộ cân bằng tải (Load Balancer)
### Reverse proxy (web server)
### Application layer
## Cơ sở dữ liệu (Database)
### Cơ sở dữ liệu quan hệ
### Cơ sở dữ liệu NoSQL
* Key - Value
* Document
* Wide column
* Graph
### Cache
### Asynchronism
### Communication
### Security