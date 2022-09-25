- Javacript là gì: 
    + Là ngôn ngữ lập trình web phổ biến nhất hiện nay.
    + Là ngôn ngữ thông dịch, được thêm vào thẻ HTML để trang web trở nên sống động hơn.
    + JS là ngôn ngữ thông dịch nên không cần chuẩn bị công cụ nào để biên dịch chương trình trước khi chạy.
    + Giờ đây JS là ngôn ngữ lập trình độc lập và được chuẩn hoá bởi tài liệu ECMAScript.

- Ứng dụng của Javascript:
    + JS được sử dụng ở tất cả mọi nơi.
    + Frontend: JS và HTML, CSS trở thành 3 thứ không thể thiếu khi lập trình web.ư
    + Backend: với sự ra đời của Node.js, ta có thể sử dụng JS phía server. 
    + Ứng dụng máy tính: có thể dùng framework để tạo nên ứng dụng đa nền tàng trển máy tính.
    + Ứng dụng điện thoại: ReactNative, NativeScript,... giúp xây dựng ứng dụng trên điện thoại ở cả Android và IOS.
        * Để chạy JS ở khắp mọi nơi, thì nơi đó cần có 1 thứ gọi là JS engine.

- JS engine là gì:
    + JS engine là 1 chương trình máy tính thực thi các đoạn code JS.
    + Một vài JS engine như: 
        1. V8: trên trình duyệt Opera, Chrome, Edge.
        2. SpiderMonkey: trên trình duyệt Firefox.
        3. Chakra: trên trình duyệt IE.
        4. JS core, Nitro, SquirreFish trên trình duyệt Safari.
        ...
        
- JS không làm được gì:
    + Đọc, ghi, sao chép, thực thi chương trình trên máy người dùng
    + Trang web không có quyền truy cập trực tiếp đến Camera/Microphone.
    + Các trang web ở các tab khác nhau sẽ không biết nhau, code JS từ 1 trang web không thể truy cập và láy thông tin từ trang còn lại.
    + JS có thể dễ dàng giao tiếp với Server thông qua API nếu như trang web và server có cùng tên miền, trong trường hợp khác tên miền thì sẽ bị lỗi CORS nếu như Server không cho phép truy cập.