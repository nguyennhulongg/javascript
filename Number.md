1. Cách biểu diễn Number
    + Thay vì viết số 1 tỷ như này
        const billion = 1000000000;
    thì có thể viết như này dễ nhìn hơn
        const billion = 1_000_000_000
    hoặc dùng chữ e
        const a = 1e3 <=> 3 số 0 <=> 1000
        const b = 1e-3 <=> 0.001

2. Phương thức toString(base)
    + Phương thức num.toString(base) trả về biểu diễn string biểu diễn số num ở hệ cơ số base
        Ex: 
            let num = 255;
            * Chuyển sang hệ cơ số 16
            console.log(num.toString(16)); // ff

            * Chuyển sang hệ cơ số 2
            console.log(num.toString(2)); // 11111111

        * Base có giá trị từ 2 đến 36. Mặc định là 10
            - Base = 16 hay dùng để biểu diễn mã màu hexa, string đã được encode... các chữ số từ 0-9 hoặc A-F (không phân biệt chữ hoa chữ thường)
            - Base = 2 được dùng để debug các số sử dụng trong toán tử bitwise, với các chữ số lầ 0 hoặc 1
            - Base = 36 dùng để biểu diễn chữ số dưới dạng ngắn gọn hơn
                Ex: console.log(1234567890..toString(36)); // kf12oi
                    * Nếu muuốn gọi phương thức của number, phải dùng 2 dấu chấm.

3. Làm tròn Number trong JS
    + Math.floor : làm tròn dưới 
        Ex: 3.1 => 3

    + Math.ceil : làm tròn lên
        Ex: 2.1 => 3
    
    + Math.round : trả về số nguyên gần nhất, có thể làm tròn lên hoặc làm tròn xuống
        Ex: 3.4 => 3

    + Math.trunc : trả về số nguyên bằng cách xoá tất cả các số sau dấu phẩy
        Ex: 5.6 => 5

    + toFixed : làm tròn số và trả về string với chính xác n chữ số sau dấu n
        Ex: let a = 5.76533
            let b = a.toFixed(2)
            console.log(b) => "5.77"

4. Hàm parseInt và parseFloat
    + Hàm parseInt sẽ tách lấy số nguyên
    + Hàm parseFloat sẽ tách lấy số thực
        Ex: 
            console.log(parseInt("100px")); // 100
            console.log(parseFloat("1.1em")); // 1.1

            console.log(parseInt("1.2")); // 1
            console.log(parseFloat("1.2.3")); // 1.2

5. Hàm toán học
    + Math.random() : random ra 1 số trong khoảng từ 0 đến 1
        Ex:
            console.log(Math.random()); // 0.7097565480172887

    + Math.max(a, b, c,....) và Math.min(a, b, c,....) : trả về số lớn nhất (nhỏ nhất) từ các số a, b, c,... đã cho
        Ex: 
            console.log(Math.max(1, 3.2, -1, 10, 4)); // 10
            console.log(Math.min(1, 3.2, -1, 10, 4)); // -1

    + Math.pow(n, base) : trả về n mũ base 
        Ex: 
            console.log(Math.pow(2, 3)); // 8 - vì bằng 2 mũ 3        








        


