1. Array là gì
    + Array giống với object, nhưng khác ở chỗ:
        - Array được thiết kế để lưu trữ dữ liệu theo thứ tự
        - Object bình thường chỉ là tập hợp các cặp key-value

2. Khởi tạo array
    + Có 2 cách khởi tạo array: 
        - Sử dụng dấu ngoặc vuông [].
        - Sử dụng hàm khởi tạo new Array()
            let a1 = [];
            let a2 = new Array();

3. Truy cập đến một phần tử trong mảng
    + Sử dụng array[index], trong đó array là tên array, còn index là index của phần tử
        Ex:
            let letters = ["a", "b", "c"];
            console.log(letters[0]); => a
            console.log(letters[1]); => b

    + Thay đổi giá trị của phần tử trong mảng:
        Ex:
            let letters = ["a", "b", "c"];
            letters[0] = "z"
            console.log(letters[0]); => 0
    
    + Thêm một phần tử vào mảng
        Ex:
            let letters = ["a", "b", "c"];
            letters[3] = "z"
            console.log(letters[3]); => z
    
4. Độ dài của mảng được xác định qua thuộc tính length
    Ex:
        let letters = ["a", "b", "c"];
        console.log(letters.length); => 3

5. Một số phương thức của mảng
    + 4 Phương thức cơ bản:
        - arr.pop() : lấy ra và trả về phần tử cuối cùng của mảng
            Ex: 
                let letters = ["a", "b", "c"];
                let item = letters.pop();

                console.log(item); => c
                console.log(letters); => (2) ['a', 'b']

        - arr.push() : thêm một hoặc nhiều phần tử vào cuối mảng
            Ex:
                let letters = ["a", "b", "c"];

                + Thêm một phần tử vào cuối mảng
                let length = letters.push("d");
                console.log(length); => 4
                console.log(letters); => (4) ['a', 'b', 'c', 'd']

                + Thêm nhiều phần tử vào cuối mảng
                length = letters.push("e", "f");
                console.log(length); => 6
                console.log(letters); => (6) ['a', 'b', 'c', 'd', 'e', 'f']

        - arr.shift() : lấy ra và trả về phần tử đầu tiên của mảng
            Ex: 
                let letters = ["a", "b", "c"];
                let item = letters.shift();

                console.log(item); => a
                console.log(letters); => (2) ['b', 'c']

        - arr.unshift() : thêm một hoặc nhiều phần tử vào đầu mảng
            Ex:
                let letters = ["a", "b", "c"];
                
                + Thêm một phần tử vào đầu mảng
                let length = letters.unshift("d");
                console.log(length); => 4
                console.log(letters); => (4) ['d', 'a', 'b', 'c']

                + Thêm nhiều phần tử vào đầu mảng
                length = letters.unshift("e", "f");
                console.log(length); => 6
                console.log(letters); => (6) ['e', 'f', 'd', 'a', 'b', 'c']

    + Một số phương thức khác
        - arr.splice() : xoá phần tử bất kỳ trong mảng 
            * Cú pháp: arr.splice(start, deleteCount, element1, element2,...)
            * Trong đó: - start là vị trí bắt đầu xoá
                        - deleteCount số lượng phần tử muốn xoá
                        - element phần tử muốn chèn vào vị trí vừa xoá
                Ex:
                    let letters = ["a", "b", "c"];
                    letters.splice(1, 1);
                    console.log(letters); => (2) ['a', 'c']

                    let letters = ["a", "b", "c"];
                    letters.splice(0, 3, "d", "e");
                    console.log(letters); => (2) ['d', 'e']

            * Có thể thêm phần tử, bằng cách cho deleteCount = 0
                Ex:
                    let letters = ["a", "b", "c"];
                    letters.splice("1", 0, "d", "e");
                    console.log(letters); => (5) ['a', 'd', 'e', 'b', 'c']
        
        - arr.slice() : trả về mảng mới bằng cách copy mảng ban đầu từ vị trí start đến vị trí end.
            * Cú pháp: arr.slice(start, end);
            * Trong đó: - start là ví trị khởi đầu
                        - end là vị trí kết thúc
                Ex:
                    let letters = ["a", "b", "c", "d"];

                    let arr1 = letters.slice(1, 3);
                    console.log(arr1); => (2) ['b', 'c']
                    
                    let arr2 = letters.slice(-2);
                    console.log(arr2); => (2) ['c', 'd']

        - arr.concat() : trả về arr mới bao gồm các giá trị của array ban đầu cộng thêm giá trị các phần tử array thêm vào hoặc các giá trị khác.
            * Cú pháp: arr.concat(arg1, arg2,...)
            * Trong đó: arg1, arg2 có thể là mảng hoặc các giá trị khác
                Ex: 
                    let arr1 = [1, 2];

                    + Tạo mảng mới từ mảng arr1 và mảng [3, 4]
                    let arr2 = arr1.concat([3, 4]);
                    console.log(arr2); => (4) [1, 2, 3, 4]

                    + Tạo mảng mới từ mảng arr1 và mảng [3, 4] và [5, 6]
                    let arr3 = arr1.concat([3, 4], [5, 6]);
                    console.log(arr3); => (6) [1, 2, 3, 4, 5, 6]

                    + Tạo mảng mới từ mảng arr1 và mảng [3, 4] cùng với các giá trị 5, 6
                    let arr4 = arr1.concat([3, 4], 5, 6);
                    console.log(arr4); => (6) [1, 2, 3, 4, 5, 6]

        ** Phương thức tìm kiếm trong mảng
            1. arr.indexOf(item, from): tìm kiếm item bắt đầu từ vị trí from.
            2. arr.lastIndexOf(item, from): tìm kiếm item bắt đầu từ vị trí from nhưng từ phải qua trái.
            3. arr.includes(item, from): tìm kiếm item từ vị trí from, nếu tìm thấy trả về true, không tìm thấy trả về false.
                Ex: 
                    let arr = [1, 0, 1, false];

                    console.log(arr.indexOf(0)); => 1
                    console.log(arr.indexOf(false)); => 3
                    console.log(arr.indexOf(null)); => -1

                    console.log(arr.indexOf(1)); => 0
                    console.log(arr.lastIndexOf(1)); => 2

                    console.log(arr.includes(1)); => true

            4. arr.find(fn): Tìm kiếm object trong mảng thoả mãn điều kiện cho trước.
                + Cú pháp: 
                        let result = arr.find(function (item, index, array) {
                            // code xử lý
                        });
                    * Trong đó: - item là phần tử đang duyệt.
                                - index là chỉ số của phần tử đang duyệt.

                        Ex:
                            let users = [
                                { id: 1, name: "Alex" },
                                { id: 2, name: "John" },
                                { id: 3, name: "Anna" },
                            ];

                            let user = users.find((item) => item.id === 2);

                            console.log(user.name); // John        

            5. arr.findIndex():
                    let users = [
                        { id: 1, name: "Alex" },
                        { id: 2, name: "John" },
                        { id: 3, name: "Anna" },
                    ];

                    let index = users.findIndex((item) => item.id === 2);
                    console.log(index); // 1

            6. arr.filter() : tìm kiếm nhiều phân tử thoả mãn 
                + Cú pháp:
                    let results = arr.filter(function (item, index, array) {
                        // code kiểm tra
                    });

                    Ex:
                        let users = [
                            { id: 1, name: "Alex" },
                            { id: 2, name: "John" },
                            { id: 3, name: "Anna" },
                        ];

                        let results = users.filter((item) => item.id <= 2);
                        console.log(results.length); // 2

                        let others = users.filter((item) => item.id > 5);
                        console.log(others.length); // 0

        ** Phương thức biến đổi mảng
            1. arr.map(fn) : thực hiện một hàm trên mỗi phần tử của mảng và trả về một mảng các kết quả
                + Cú pháp: 
                    let result = arr.map(function (item, index, array) {
                        // trả về giá trị mới từ mỗi item
                    });

                    Ex: 
                        let lengths = ["Dog", "Fish", "Elephant"].map((item) => item.length);
                        console.log(lengths); // (3) [3, 4, 8]

            2. arr.sort() : sắp xếp các phần tử theo thứ tự
                Ex:
                    let arr = [1, 2, 15];

                    arr.sort();
                    console.log(arr); // (3) [1, 15, 2]