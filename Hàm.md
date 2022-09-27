1. Hàm là gì
    + Hàm trong JS là 1 chương trình con giúp thực hiện những công việc cụ thể.
    + Để định nghĩa 1 hàm, sử dụng từ khoá function với cú pháp:
        function functionName(param1, param2,...) {
            statement1;
            statement2;
            ...
        };
        * Trong đó:
            functionName: tên function.
            param1, param2 (không bắt buộc): là những tham số.
            statement1, statement2: câu lệnh, nằm trong thân hàm trong dấu ngoặc nhọn.

        Ex:
            function handleClick() {
                console.log("Long dep trai");
            };
    + Để gọi hàm, ghi tên hàm sau đó thêm dấu ngoặc đơn phía sau ():
        Ex:
            function callMe() {
                console.log("Long");
            };

            callMe(); => gọi hàm
    
    + Biến cục bộ bên trong hàm:
        - Một biến được khai báo bên trong hàm, chỉ có thể sử dụng bên trong hàm đó gọi là biến cục bộ:
            Ex:
                function callMe() {
                    const NAME = "Long";
                    console.log(NAME);
                };
            
            callMe(); => Long
            console.log(NAME) => lỗi

    + Biến ngoài hàm 
        - Một hàm có thể truy cập đến một biến được khai báo bên ngoài hàm:
            Ex: 
                const NAME = "Long";
                function name() {
                    console.log(NAME);
                };
                name(); => Long
        Hơn nữa, còn có thể thay đổi giá trị của biến bên trong hàm:
            Ex: 
                let name = "Long";
                function info() {
                    name = "Son";
                    console.log(name);
                };

                name(); => Son

2. Truyền tham số vào hàm:
    + Thay vì biến toàn cục, có thể truyền tham số vào hàm:
        Ex:
            function sayHello(message) {
                console.log(message);
            };

            sayHello("Hello"); => Hello

    + Giá trị mặc định của tham số:
        - Trong trường hợp có tham số nhưng không truyền giá trị cho nó, thì giá trị của tham số đó sẽ là undefined.
            Ex: 
                function sayHello(message, site) {
                    console.log(message + "from" site);
                };
                sayHello("Hello"); => Hello from undefined

        - Trong trường hợp này, có thể gán giá trị mặc định cho tham số bằng cách sử dụng toán tử gán.
            Ex:            
                function sayHello(message, site = "Facebook") {
                    console.log(message + "from" site);
                };
                sayHello("Hello"); => Hello from Facebook

3. Return trong hàm:
    + Hàm có thể trả về giá trị khi được gọi.
        Ex: 
            function sum(a, b) {
                return a + b 
            };
            const res = sum(5, 10);
            console.log(res); => 15

    + Có thể dùng nhiều từ khoá return trong 1 hàm:
        Ex:
            function sum(a, b) {
                if (a === null || a === undefined) {
                    console.log("Tham số không hợp lệ!");
                    return;
                }

                if (b === null || b === undefined) {
                    console.log("Tham số không hợp lệ!");
                    return;
                }

                return a + b;
                }

            const result1 = sum(); // Tham số không hợp lệ!

        * Hàm trên để tính tổng a và b, trong trường hợp a và b đều bằng null hoặc undefined thì thôi return luôn mà không tính tổng.
        * Trong ví dụ trên, return không có giá trị nào, khi đó giá trị trả về mặc định là undefined 

4. Đặt tên hàm sao cho đẹp trai
    + Tên hàm nên đặt theo chuẩn con lạc đà (camel).
    + Tên hàm nên bắt đầu từ 1 động từ.
        * Một số động từ hay dùng khi đặt tên hàm: get, set, check, display. 
            
5. Hàm thuần khiết và hàm không thuần khiết            
    + Hàm thuần khiết (pure function): là hàm không phụ thuộc vào yếu tố bên ngoài như biến toàn cục, môi trường thực thi,...
        Ex:
            function pureFunc(number, factor) {
                return number * factor;
                }
            let ret = pureFunc(2, 10);
            console.log(ret); // 20

    + Hàm không thuần khiết thì ngược lại.
        Ex: 
            let factor = 10;
            function nonPureFunc(number) {
                return number * factor;
            }

            let ret = nonPureFunc(2);
            console.log(ret); // 20

            factor = 11;
            ret = nonPureFunc(2);
            console.log(ret); // => 22

        * Hàm này phụ thuộc vào biến factor nên không thuần khiến
