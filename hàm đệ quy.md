1. Hàm đệ quy
    + Là hàm tự gọi lại chính nó 
        Ex:
            function sayHello(count) {
                if (count <= 0) {
                    return;
                }

                console.log("Hello world!");
                sayHello(count - 1);
                }

                // sayHello 5 lần
                sayHello(5);

2. Các thành phần cơ bản của hàm đệ quy
    + Hai thành phần đặc trưng:
        1. Phần cơ sở : điều kiện để thoát đệ quy
        2. Phần đệ quy : gọi lại chính nó

            Ex:
                function sayHello(count) {
                    // phần cơ sở: điều kiện thoát đệ quy là biến count <= 0
                    if (count <= 0) {
                        return;
                   }

                    // xử lý logic cơ bản
                    console.log("Hello world!");

                    // phần đệ quy: gọi lại chính hàm sayHello
                    sayHello(count - 1);
                }
        * Nếu bỏ qua phần cơ sở code sẽ chạy đến một lúc nào đó thì sẽ bị lỗi phụ thuộc vào JavaScriptEngine
        