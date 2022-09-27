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
            console.log(letters[0]); // a
            console.log(letters[1]); // b

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
        console.log(letters.length); // 3

5. Một số phương thức của mảng
    + arr.pop() : lấy ra và trả về phần tử cuối cùng của mảng
        Ex: 
            let letters = ["a", "b", "c"];
            let item = letters.pop();

            console.log(item); // c
            console.log(letters); // (2) ['a', 'b']

    + arr.push() : thêm một hoặc nhiều phần tử vào cuối mảng
        Ex:
            let letters = ["a", "b", "c"];

            // thêm một phần tử vào cuối mảng
            let length = letters.push("d");
            console.log(length); // 4
            console.log(letters); // (4) ['a', 'b', 'c', 'd']

            // thêm nhiều phần tử vào cuối mảng
            length = letters.push("e", "f");
            console.log(length); // 6
            console.log(letters); // (6) ['a', 'b', 'c', 'd', 'e', 'f']

    + arr.shift() : lấy ra và trả về phần tử đầu tiên của mảng
        Ex: 
            let letters = ["a", "b", "c"];
            let item = letters.shift();

            console.log(item); // a
            console.log(letters); // (2) ['b', 'c']

    + arr.unshift() : thêm một hoặc nhiều phần tử vào đầu mảng
        Ex:
            let letters = ["a", "b", "c"];
            
            // thêm một phần tử vào đầu mảng
            let length = letters.unshift("d");
            console.log(length); // 4
            console.log(letters); // (4) ['d', 'a', 'b', 'c']

            // thêm nhiều phần tử vào đầu mảng
            length = letters.unshift("e", "f");
            console.log(length); // 6
            console.log(letters); // (6) ['e', 'f', 'd', 'a', 'b', 'c']


