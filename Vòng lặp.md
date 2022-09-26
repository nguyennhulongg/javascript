1. While: 
    + Cú pháp 
        while(condition) {
            ...
        }
    Trong đó condition là điều kiện thực hiện vòng lặp, khi condition có giá trị truthy thì vòng lặp thực thi, và nếu có giá trị falsy thì vòng lặp kết thúc
        Ex: 
            let count = 1;
            while (count <= 3) {
                console.log(count); => 1, 2, 3
                count++;
            }

2. Do while:
    + Cú pháp
        do {
            ...code
        } while (condition);
    
    Khác với while, vòng lặp do while luôn thực hiện ít nhất 1 lượt lặp, sau đó mới kiểm tra điều kiện
        Ex: 
            let count = 1;
            do {
                console.log(count);
                count++;
            } while (count <= 3);

3. For:
    + Cú pháp:
        for([khởi tạo]; [điều kiện]; [cập nhật]){
        // code
        }

        Khởi tạo: thục hiện 1 lần lúc băt đầu vòng lặp.
        Điều kiện: kiểm tra trước mỗi vòng lặp
        Cập nhật: Thực hiện ở cuối mỗi vòng lặp
            Ex:
                for (let count = 1; count <= 3; count++) {
                   console.log(count); => 1, 2, 3
                }

        * Chú ý: không thể dùng biến count ngoài vòng lặp for,
            Để sử dụng biến count, cần khai báo biến count ngoài vòng lặp for

                const count; 
                for (count = 1; count <= 3; count++) {
                    console.log(count);
                }

                console.log(count);

    + Bất kể phần nào trong vòng lặp for cũng đều có thể bỏ qua được:
        - Bỏ qua phần khởi tạo
            let count = 1;
            for (; count <= 3; count++) {
                console.log(count);
            }
        - Bỏ qua phần cập nhật
            let count = 1;
            for (; count <= 3; ) {
                console.log(count++);
            }
        - Bỏ qua phần điều kiện (lặp vô hạn)
            let count = 1;
            for (;;) {
                console.log(count++);
            }

    + Từ khoá break
        - Dùng để thoát ra khỏi vòng lặp
            Ex: 
                for (let number = 8; ; number++) {
                    if (number % 7 === 0) {
                        console.log(number); => 14
                        break;
                    }
                }

    + Từ khoá continue 
        - Dùng để dừng lượt lặp hiện tại và chuyển tới lượt lặp tiếp theo
            Ex:
                for (let number = 8; ; number++) {
                    if (number % 2 === 0) continue;
                    if (number % 7 === 0) {
                        console.log(number);
                        break;
                    }
                }
                => 21
    