## BÁO CÁO: TỔNG QUAN VÀ ỨNG DỤNG CỦA CÔNG CỤ POSTMAN TRONG PHÁT TRIỂN VÀ KIỂM THỬ API

**Ngày báo cáo:** 19 tháng 6 năm 2025

### 1. Giới thiệu

Trong kỷ nguyên phát triển phần mềm hiện đại, Giao diện lập trình ứng dụng (API) đóng vai trò trung tâm, cho phép các hệ thống khác nhau giao tiếp và trao đổi dữ liệu. Với sự phức tạp ngày càng tăng của các hệ thống phân tán và kiến trúc microservices, nhu cầu về các công cụ hiệu quả để tương tác, kiểm thử và quản lý API trở nên cấp thiết hơn bao giờ hết. Postman nổi lên như một giải pháp hàng đầu, cung cấp một nền tảng toàn diện cho các nhà phát triển và kiểm thử viên để làm việc với API một cách hiệu quả.

Báo cáo này sẽ cung cấp cái nhìn tổng quan về Postman, các tính năng chính, lợi ích mà nó mang lại, và các trường hợp sử dụng phổ biến trong vòng đời phát triển phần mềm.

### 2. Postman là gì?

Postman là một nền tảng phát triển API cho phép người dùng thiết kế, xây dựng, kiểm thử và tài liệu hóa các API một cách nhanh chóng và dễ dàng. Ban đầu, Postman chỉ là một tiện ích mở rộng của trình duyệt Chrome, nhưng sau đó đã phát triển thành một ứng dụng độc lập mạnh mẽ, cung cấp một giao diện đồ họa trực quan và thân thiện với người dùng.

Postman loại bỏ sự cần thiết phải viết mã boilerplate cho các yêu cầu HTTP, giúp đơn giản hóa quy trình tương tác với API. Nó hỗ trợ tất cả các phương thức HTTP thông dụng như GET, POST, PUT, DELETE, PATCH, cùng với khả năng cấu hình headers, body, parameters, và authentication.

### 3. Các tính năng chính của Postman

Postman cung cấp một bộ tính năng phong phú, biến nó thành một công cụ không thể thiếu cho bất kỳ ai làm việc với API:

* **Tạo và Gửi Yêu cầu HTTP:** Giao diện trực quan cho phép người dùng dễ dàng tạo các yêu cầu với các phương thức HTTP khác nhau, tùy chỉnh URL, tiêu đề (headers), tham số (parameters), và dữ liệu gửi đi (body).
* **Quản lý Collections (Bộ sưu tập):** Tổ chức các yêu cầu API thành các bộ sưu tập logic, giúp dễ dàng quản lý, chia sẻ và tái sử dụng. Các collection có thể được xuất/nhập, tạo điều kiện thuận lợi cho việc cộng tác nhóm.
* **Biến (Variables) và Môi trường (Environments):**
    * **Variables:** Cho phép định nghĩa các giá trị có thể tái sử dụng trong các yêu cầu (ví dụ: URL cơ sở, khóa API).
    * **Environments:** Quản lý các tập hợp biến khác nhau cho các môi trường triển khai khác nhau (ví dụ: môi trường phát triển, kiểm thử, sản xuất), giúp chuyển đổi cấu hình API một cách nhanh chóng mà không cần thay đổi từng yêu cầu.
* **Kiểm thử API (API Testing):**
    * Postman cho phép viết các script kiểm thử (dựa trên JavaScript) để xác minh phản hồi của API (ví dụ: kiểm tra mã trạng thái HTTP, nội dung phản hồi, thời gian phản hồi).
    * Hỗ trợ chạy tự động các bộ kiểm thử và tích hợp với các hệ thống CI/CD.
* **Scripts tiền yêu cầu (Pre-request Scripts):** Cho phép thực thi các đoạn mã JavaScript trước khi gửi yêu cầu, thường được dùng để tạo dữ liệu động, xử lý xác thực, hoặc thiết lập các biến.
* **Mô tả API (API Documentation):** Tự động tạo tài liệu API đẹp mắt và tương tác từ các collection, giúp các nhà phát triển khác dễ dàng hiểu và sử dụng API.
* **Giám sát API (API Monitoring):** Theo dõi hiệu suất và tính khả dụng của API theo thời gian, gửi cảnh báo khi có sự cố.
* **Workspace (Không gian làm việc):** Cung cấp không gian làm việc cá nhân hoặc nhóm để cộng tác, chia sẻ các API, collection và môi trường.
* **Tích hợp:** Postman có thể tích hợp với nhiều công cụ khác như Git, Jenkins, Slack, và các công cụ quản lý dự án.

### 4. Thực hành các chức năng của Postman
* ** Gửi yêu cầu GET: Lấy danh sách người dùng
* Chúng ta sẽ sử dụng API công cộng JSONPlaceholder để lấy danh sách người dùng. API này cung cấp các dữ liệu giả lập cho mục đích thử nghiệm.

Các bước thực hiện:

Mở Postman: Khởi động ứng dụng Postman.
Tạo một yêu cầu mới: Nhấp vào nút + (dấu cộng) để tạo một tab yêu cầu mới.
Chọn phương thức GET: Trong dropdown menu bên cạnh ô địa chỉ, chọn phương thức GET.
Nhập URL: Nhập URL sau vào ô địa chỉ: https://jsonplaceholder.typicode.com/users
Gửi yêu cầu: Nhấp vào nút Send (Gửi).
Kết quả: 
![{947CDFF4-135B-487A-AD38-217AA9AD0C06}](https://github.com/user-attachments/assets/54e50fb9-97f9-43d1-a57d-3189f09eef7e)
Kết quả kiểm thử chi tiết:
[
    {
        "id": 1,
        "name": "Leanne Graham",
        "username": "Bret",
        "email": "Sincere@april.biz",
        "address": {
            "street": "Kulas Light",
            "suite": "Apt. 556",
            "city": "Gwenborough",
            "zipcode": "92998-3874",
            "geo": {
                "lat": "-37.3159",
                "lng": "81.1496"
            }
        },
        "phone": "1-770-736-8031 x56442",
        "website": "hildegard.org",
        "company": {
            "name": "Romaguera-Crona",
            "catchPhrase": "Multi-layered client-server neural-net",
            "bs": "harness real-time e-markets"
        }
    },
    {
        "id": 2,
        "name": "Ervin Howell",
        "username": "Antonette",
        "email": "Shanna@melissa.tv",
        "address": {
            "street": "Victor Plains",
            "suite": "Suite 879",
            "city": "Wisokyburgh",
            "zipcode": "90566-7771",
            "geo": {
                "lat": "-43.9509",
                "lng": "-34.4618"
            }
        },
        "phone": "010-692-6593 x09125",
        "website": "anastasia.net",
        "company": {
            "name": "Deckow-Crist",
            "catchPhrase": "Proactive didactic contingency",
            "bs": "synergize scalable supply-chains"
        }
    },
    {
        "id": 3,
        "name": "Clementine Bauch",
        "username": "Samantha",
        "email": "Nathan@yesenia.net",
        "address": {
            "street": "Douglas Extension",
            "suite": "Suite 847",
            "city": "McKenziehaven",
            "zipcode": "59590-4157",
            "geo": {
                "lat": "-68.6102",
                "lng": "-47.0653"
            }
        },
        "phone": "1-463-123-4447",
        "website": "ramiro.info",
        "company": {
            "name": "Romaguera-Jacobson",
            "catchPhrase": "Face to face bifurcated interface",
            "bs": "e-enable strategic applications"
        }
    },
    {
        "id": 4,
        "name": "Patricia Lebsack",
        "username": "Karianne",
        "email": "Julianne.OConner@kory.org",
        "address": {
            "street": "Hoeger Mall",
            "suite": "Apt. 692",
            "city": "South Elvis",
            "zipcode": "53919-4257",
            "geo": {
                "lat": "29.4572",
                "lng": "-164.2990"
            }
        },
        "phone": "493-170-9623 x156",
        "website": "kale.biz",
        "company": {
            "name": "Robel-Corkery",
            "catchPhrase": "Multi-tiered zero tolerance productivity",
            "bs": "transition cutting-edge web services"
        }
    },
    {
        "id": 5,
        "name": "Chelsey Dietrich",
        "username": "Kamren",
        "email": "Lucio_Hettinger@annie.ca",
        "address": {
            "street": "Skiles Walks",
            "suite": "Suite 351",
            "city": "Roscoeview",
            "zipcode": "33263",
            "geo": {
                "lat": "-31.8129",
                "lng": "62.5342"
            }
        },
        "phone": "(254)954-1289",
        "website": "demarco.info",
        "company": {
            "name": "Keebler LLC",
            "catchPhrase": "User-centric fault-tolerant solution",
            "bs": "revolutionize end-to-end systems"
        }
    },
    {
        "id": 6,
        "name": "Mrs. Dennis Schulist",
        "username": "Leopoldo_Corkery",
        "email": "Karley_Dach@jasper.info",
        "address": {
            "street": "Norberto Crossing",
            "suite": "Apt. 950",
            "city": "South Christy",
            "zipcode": "23505-1337",
            "geo": {
                "lat": "-71.4197",
                "lng": "71.7478"
            }
        },
        "phone": "1-477-935-8478 x6430",
        "website": "ola.org",
        "company": {
            "name": "Considine-Lockman",
            "catchPhrase": "Synchronised bottom-line interface",
            "bs": "e-enable innovative applications"
        }
    },
    {
        "id": 7,
        "name": "Kurtis Weissnat",
        "username": "Elwyn.Skiles",
        "email": "Telly.Hoeger@billy.biz",
        "address": {
            "street": "Rex Trail",
            "suite": "Suite 280",
            "city": "Howemouth",
            "zipcode": "58804-1099",
            "geo": {
                "lat": "24.8918",
                "lng": "21.8984"
            }
        },
        "phone": "210.067.6132",
        "website": "elvis.io",
        "company": {
            "name": "Johns Group",
            "catchPhrase": "Configurable multimedia task-force",
            "bs": "generate enterprise e-tailers"
        }
    },
    {
        "id": 8,
        "name": "Nicholas Runolfsdottir V",
        "username": "Maxime_Nienow",
        "email": "Sherwood@rosamond.me",
        "address": {
            "street": "Ellsworth Summit",
            "suite": "Suite 729",
            "city": "Aliyaview",
            "zipcode": "45169",
            "geo": {
                "lat": "-14.3990",
                "lng": "-120.7677"
            }
        },
        "phone": "586.493.6943 x140",
        "website": "jacynthe.com",
        "company": {
            "name": "Abernathy Group",
            "catchPhrase": "Implemented secondary concept",
            "bs": "e-enable extensible e-tailers"
        }
    },
    {
        "id": 9,
        "name": "Glenna Reichert",
        "username": "Delphine",
        "email": "Chaim_McDermott@dana.io",
        "address": {
            "street": "Dayna Park",
            "suite": "Suite 449",
            "city": "Bartholomebury",
            "zipcode": "76495-3109",
            "geo": {
                "lat": "24.6463",
                "lng": "-168.8889"
            }
        },
        "phone": "(775)976-6794 x41206",
        "website": "conrad.com",
        "company": {
            "name": "Yost and Sons",
            "catchPhrase": "Switchable contextually-based project",
            "bs": "aggregate real-time technologies"
        }
    },
    {
        "id": 10,
        "name": "Clementina DuBuque",
        "username": "Moriah.Stanton",
        "email": "Rey.Padberg@karina.biz",
        "address": {
            "street": "Kattie Turnpike",
            "suite": "Suite 198",
            "city": "Lebsackbury",
            "zipcode": "31428-2261",
            "geo": {
                "lat": "-38.2386",
                "lng": "57.2232"
            }
        },
        "phone": "024-648-3804",
        "website": "ambrose.net",
        "company": {
            "name": "Hoeger LLC",
            "catchPhrase": "Centralized empowering task-force",
            "bs": "target end-to-end models"
        }
    }
]
* ** Gửi yêu cầu POST: Tạo một bài viết mới
* chúng ta sẽ sử dụng cùng một API để tạo một bài viết mới. Yêu cầu POST thường được sử dụng để gửi dữ liệu lên server để tạo hoặc cập nhật tài nguyên.
Các bước thực hiện:

Tạo một yêu cầu mới: Nhấp vào nút + để tạo một tab yêu cầu mới.

Chọn phương thức POST: Trong dropdown menu bên cạnh ô địa chỉ, chọn phương thức POST.

Nhập URL: Nhập URL sau vào ô địa chỉ: https://jsonplaceholder.typicode.com/posts
Kết quả:
![{23E3F089-B166-4CA5-86C3-0FE011498F9A}](https://github.com/user-attachments/assets/000c1ebb-2f01-4748-8839-84e4908af2dc)

### 5. Lợi ích của việc sử dụng Postman

Việc áp dụng Postman mang lại nhiều lợi ích đáng kể cho quá trình phát triển và kiểm thử API:

* **Tăng tốc độ phát triển:** Giảm thời gian viết mã để gửi yêu cầu và xử lý phản hồi, giúp nhà phát triển tập trung vào logic nghiệp vụ.
* **Cải thiện chất lượng API:** Khả năng kiểm thử mạnh mẽ giúp phát hiện và sửa lỗi sớm, đảm bảo API hoạt động đúng như mong đợi.
* **Thúc đẩy cộng tác:** Các tính năng chia sẻ collection, workspace và tài liệu API giúp các thành viên trong nhóm làm việc hiệu quả hơn và giữ cho mọi người đồng bộ.
* **Đơn giản hóa quy trình học tập:** Giao diện người dùng trực quan giúp ngay cả những người mới bắt đầu cũng có thể nhanh chóng làm quen và sử dụng.
* **Tạo tài liệu tự động:** Tiết kiệm thời gian và công sức trong việc tạo và duy trì tài liệu API, đảm bảo tài liệu luôn được cập nhật.
* **Quản lý phiên bản API:** Có thể quản lý các phiên bản khác nhau của API thông qua các collection và môi trường.

### 6. Các trường hợp sử dụng phổ biến

Postman được sử dụng rộng rãi trong nhiều giai đoạn của vòng đời phát triển phần mềm:

* **Phát triển API:** Các nhà phát triển sử dụng Postman để kiểm tra các endpoint API trong quá trình xây dựng, đảm bảo chúng hoạt động chính xác trước khi tích hợp vào ứng dụng.
* **Kiểm thử chức năng và hồi quy:** Kiểm thử viên sử dụng Postman để thực hiện kiểm thử chức năng cho từng endpoint và kiểm thử hồi quy cho toàn bộ API sau khi có thay đổi.
* **Thiết kế và mô phỏng API:** Sử dụng Postman để tạo các yêu cầu mẫu và mô phỏng phản hồi, giúp thiết kế API trước khi code backend được hoàn thiện.
* **Tích hợp API của bên thứ ba:** Dễ dàng kiểm tra và hiểu cách tương tác với các API của bên thứ ba.
* **Đào tạo và Hướng dẫn:** Postman là một công cụ tuyệt vời để trình bày và giải thích cách hoạt động của API cho người dùng mới hoặc các thành viên trong nhóm.
* **Gỡ lỗi (Debugging):** Xem xét chi tiết các yêu cầu và phản hồi HTTP để xác định nguyên nhân lỗi.

### 7. Kết luận

Postman đã trở thành một công cụ không thể thiếu trong hệ sinh thái phát triển API hiện đại. Với bộ tính năng toàn diện, giao diện thân thiện với người dùng và khả năng cộng tác mạnh mẽ, nó giúp các đội ngũ phát triển đẩy nhanh quá trình thiết kế, xây dựng, kiểm thử và quản lý API, từ đó nâng cao chất lượng sản phẩm và hiệu suất làm việc tổng thể. Việc đầu tư thời gian để thành thạo Postman là một khoản đầu tư đáng giá cho bất kỳ chuyên gia nào trong lĩnh vực phát triển và kiểm thử phần mềm.

---
