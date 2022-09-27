1. Object là gì
    + Về bản chất, object tập hợp một hoặc nhiều cặp key và value. Với key là thuộc tính, còn value là giá trị tương ứng với thuộc tính.
    + Object không có key nào được gọi là object rỗng.

2. Cách lấy ra giá trị của thuộc tính
    + Sử đụng dấu . theo sau là tên thuộc tính.
    + Sử dụng dấu [] bên trong là tên thuộc tính.

        Ex:
            const information = {
                name: "Long",
                address: "Ha Long",
                age: 18
            };

            console.log(information.name); => Long
            console.log(information.address); => Ha Long 
            console.log(information.age); => 18

            console.log(information[name]); => Long
            console.log(information[address]); => Ha Long
            console.log(information[age]); => 18

    + Toán tử dấu chấm . chỉ dùng được trong trường hợp trong tên thuộc tính không có ký tự đặc biệt (ngoại trừ _ và $).
    + Nếu trong tên thuộc tính có dấu cách thì bắt buộc phải dùng toán tử []

        Ex:
            const example = {
                _name: "Long",
                $age: 18,
                "current address": "Ha noi"
            }

            console.log(example._name); => Long
            console.log(example.$age); => 18
            console.log(example["current address"]); => Ha noi
            console.log(example.current address); => Lỗi

3. Thêm, cập nhật, xoá thuộc tính object
    + Sửa thuộc tính:
        let myComputer = {
            type: "laptop",
            brand: "Sony",
            "operating system": "Windows 7",
            "graphic card": "NVIDIA",
        };

        myComputer.type = "desktop";
        myComputer["operating system"] = "Ubuntu";

    + Thêm một thuộc tính:
        let myComputer = {
            type: "laptop",
            brand: "Sony",
            "operating system": "Windows 7",
            "graphic card": "NVIDIA",
        };

        myComputer.status = "sleep";
        myComputer["it is good"] = true;

    + Xoá một thuộc tính, sử dụng toán tử delete
        let myComputer = {
            type: "laptop",
            brand: "Sony",
            "operating system": "Windows 7",
            "graphic card": "NVIDIA",
        };

        delete myComputer.brand;
        delete myComputer["graphic card"];

        console.log(myComputer.brand); => undefined
        console.log(myComputer["graphic card"]); => undefined

        => xoá brand và graphic card rồi thì chúng không tốn tại trong object nữa, và giá trị của chúng bây giờ là undefined    

4. Cú pháp rút gọn thuộc tính khi khởi tạo object
    function makeComputer(type, brand, os, graphicCard) {
        return {
            type,
            brand,
            os,
            graphicCard,
        };
    }

    - Trong trường hợp trên tên thuộc tính trùng với tên tham số truyền vào, nên có thể viết ngắn gọn như vậy

5. Tên
    + Khi đặt tên thuộc tính, có thể sử dụng các từ for, while, var, let,.. mà không gặp vấn đề gì.
    + Tên thuộc tính sẽ tự động chuyển thành kiểu string.
        Ex:
            let obj = {
                var: 1,
                let: "a",
                for: null,
                while: NaN,
            };

            console.log(obj.var); => 1
            console.log(obj.let); => a
            console.log(obj.for); => null
            console.log(obj.while); => NaN

6. Kiểm tra xem một thuộc tính có tồn tại trong object không
    + Sử dụng toán tử in với cú pháp
        "key" in object
            const information = {
                name: "Long",
                address: "Ha Long",
                age: 18
            };
            console.log(name in information); => true
            console.log(poor in information); => false
        
7. Lặp qua tất cả thuộc tính trong một object
    + Sử dụng vòng lặp for in
        Ex: 
            const information = {
                name: "Long",
                address: "Ha Long",
                age: 18
            };

        let(let i in information) {
            console.log(i)
        };

        => name, address, age
        














