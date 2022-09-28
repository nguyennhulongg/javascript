1. JSON là gì:
    + Là viết tắt của JavaScript Object Notation. Đây là định dạng chung để biểu diễn các giá trị và object
    + JSON được sử dụng để trao đổi dữ liệu giữa các client (JavaScript) và server (Ruby, PHP,...)
    + JSON trong JS có 2 phương thức là:
        1. JSON.stringify() : chuyển object thành string.
            Cú pháp: 
                let json = JSON.stringify(value[, replacer, space])
                    Ex: 
                        let user = {
                            name: "Alex",
                            age: 28,
                        };

                        let json = JSON.stringify(user);

                        console.log(json); => {"name":"Alex","age":28}
                        console.log(typeof json); => string

            * Trong đó: - value là giá trị đầu vào cần chuyển thành string
                        - replacer là mảng chứa các thuộc tính được dùng để chuyển sang string hoặc một hàm
                        - space là số lượng kí tự dấu cách dùng để format JSON

                Ex:
                    let room = {
                        number: 23,
                    };

                    let meetup = {
                        title: "Conference",
                        participants: [{ name: "Alex" }, { name: "Anna" }],
                        place: room, // meetup tham chiếu đến room
                    };

                    room.occupiedBy = meetup; // room tham chiếu đến meetup

                    console.log(JSON.stringify(meetup, ["title", "participants"]));
                    // {"title":"Conference","participants":[{},{}]}

            2. JSON.parse() : chuyển JSON-string thành giá trị (object, array, các kiểu dữ liệu nguyên thuỷ tương ứng).
                + Cú pháp:
                    let value = JSON.parse(str, [reviver]);

                    Ex:
                        // JSON-string dạng mảng
                        let numbers = "[0, 1, 2, 3]";

                        // parse JSON-string về mảng
                        numbers = JSON.parse(numbers);

                        // sau khi numbers được parse thành array,
                        // bạn có thể truy cập phần tử mảng qua chỉ số
                        console.log(numbers[1]); // 1

                    Hoặc object lồng nhau:
                        let data =
                        '{ "name": "John", "age": 35, "isAdmin": false, "friends": [0,1,2,3] }';

                        let user = JSON.parse(data);

                        console.log(user.friends[1]); // 1

                + Một số lỗi JSON:
                    let json = `{
                        name: "John",           => không hợp lệ: thuộc tính không có nháy kép ""
                        "surname": 'Smith',     => không hợp lệ: giá trị sử dụng nháy đơn ''
                        'isAdmin': false        => không hợp lệ: thuộc tính sử dụng nháy đơn
                        "birthday": new Date(), => không hợp lệ: toán tử new không được phép
                        "friends": [0,1,2,3]    => hợp lệ
                    }`;

2. Tổng kết
    - JSON thực chất là một định dạng dữ liệu độc lập và có nhiều thư viện hỗ trợ xử lý JSON.
    - JSON trong JS hỗ trợ các kiểu dữ liệu như: object nguyên thuỷ, mảng, string, number, boolean và null
        + JSON cung cấp 2 phương thức:
            1. JSON.stringify() : dùng để chuyển giá trị thành JSON.
            2. JSON.parse() : dùng để chuyển JSON thành giá trị tương ứng trong JS.
             

