1. String
    + Có 3 cách biểu diễn 1 string
        - Sử dụng dấu ""
        - Sử dụng dấu ''
        - Sử dụng dấu ``
            Ex:
                let singleQuote = 'hello';
                let doubleQuote = "hello";
                let backticks = `hello`;
        * Dấu nháy đơn và nháy kép thì hoàn toàn tương đương, còn dấu backtip thì khác hơn.
        * Dấu backtip cho phép viết một biểu thức hoặc gọi hàm bên trong bằng cách sử dụng ${...}
            Ex:
                function add(a, b) {
                    return a + b;
                }

                console.log(`Sum of 1 and 2 is ${add(1, 2)}`); // 3
        * Dấu backtip cho phép viết string trên nhiều dòng
            Ex:
                let userList = `Users:
                    + Alex
                    + John
                    + Anna
                    `;

                console.log(userList);
        Kết quả; 
            => Users:
                + Alex
                + John
                + Anna

2. Biểu diễn kí tự đậc biệt
    Ex: 
        let userList = "Users: \n+ Alex \n+ John \n+ Anna";

        console.log(userList);    
            Users:
                + Alex
                + John
                + Anna
        * /n là kí tự đặc biệt
    + Tổng hợp một số kí tự đặc biệt:
        1. \n: dòng mới
        2. \r: hệ điều hành Windows sử dụng tổ hợp \r\n để thể hiện xuống dòng. Trong khi các hệ điều hành khác Windows chỉ sử dụng kí tự \n.
        3. \' hoặc \": dấu nháy đơn hoặc dấu nháy kép.
        4. \\: dấu backslash.
        5. \t: dấu tab.
        6. \xXX: biểu diễn kí tự unicode, trong đó XX là mã unicode ở hệ thập lục phân. Ví dụ: \x7A tương đương với z.
        7. \uXXXX: biểu diễn symbol unicode, trong đó XXXX là mã unicode ở hệ thập lục phân của symbol với UTF-16. Ví dụ: \u00A9 tương đương với biểu tượng copyright ©.
        8. \u{X..XXX} (từ 1 đến 6 kí tự): biểu diễn symbol unicode, trong đó X..XXX là mã unicode ở hệ thập lục phân của symbol với UTF-32.

3. Thay đổi chữ hoa chữ thường.
    + Dùng toUpperCase() định dạng in hoa cho string.
    + Dùng toLowerCase() định dạng in hoa cho string.
        Ex:
            console.log("Hello".toLowerCase()); // hello
            console.log("Hello".toUpperCase()); // HELLO
    + Tìm kiếm substring
        Ex:
            let str = "I am a js dev";
            console.log(str.indexOf("a", 3)); // 5 - vị trí đầu tiên tìm thấy bắt đầu từ 3
        
4. ES6 Template String:
    + Cho phép viết biểu thức ngay bên trong string, bằng cách cú pháp ${...}
        Ex: 
            let name = "Long Nguyen";
            let greeting = `I'm ${name}`;

            console.log(greeting); // I'm Long Nguyen

    + Ưu điểm khi sử dụng template string 
        1. Nối string
            let firstName = "Long";
            let lastName = "Nguuyen";

            let full3 = `${firstName} ${lastName}.`;
            console.log(full3); => Long Nguyen.

        2. Viết nháy đơn hoặc nháy kép trong string:
            let str = `I'm a "JavaScript Lover".`;
            console.log(str); // I'm a "JavaScript Lover".
        
        3. Viết string trên nhiều dòng:
            let para = `Toi la Long,
                        da xau trai,
                        lai con ngheo`

        4. Viết biểu thức toán học hoặc hàm bên trong string:
            let x = 3;
            let y = 9;

            console.log(`Tổng là: ${x + y}`);
            

