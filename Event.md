1. Cách đăng kí và huỷ đăng kí sự kiện JS
    + Đăng ký nhận sự kiện: 
        Node.addEventListener('tên sự kiện', hàm xử lý);
        * Trong đó: - Node là một phần tử của DOM như: document, h1, p ,...
                    - Tên sự kiện ứng với sự kiện muốn nhận như: mouseover, click, mouseup,...
                    - Hàm được gọi: là hàm được gọi khi sự kiện đăng ký xảy ra với Node trên.
            
            Ex: 
                function func1() {
                    console.log("function 1");
                }
                function func2() {
                    console.log("function 2");
                }

                addEventListener("click", func1);
                addEventListener("click", func2);
            
        * Với một JS event, có thể đăng ký nhiều hàm xử lý. Khi đó, hàm đăng ký trước sẽ được gọi trước.

    + Huỷ đăng ký sự kiện: 
        Node.removeEventListener('tên sự kiện', hàm xử lý);
            * Trong đó: - Node là một phần tử của DOM như: document, h1, p ,...
                        - Tên sự kiện ứng với sự kiện muốn xoá như: mouseover, click, mouseup,..

            Ex:
                function func1() {
                    console.log("function 1");
                }
                function func2() {
                    console.log("function 2");
                }

                addEventListener("click", func1);
                addEventListener("click", func2);

                removeEventListener("click", func1);

2. Một số Event cơ bản
    + KeyEvent: 
        1. keydown: được gọi khi nhấn xuống một key 
        2. keyup: được gọi khi nhả key đó ra 
        3. keypress: được gọi khi nhấn và giữ key
        ...

            Ex:
                addEventListener("keydown", function (event) {
                    console.log("keydown", event.keyCode);
                });
                addEventListener("keyup", function (event) {
                    console.log("keyup", event.keyCode);
                });
                addEventListener("keypress", function (event) {
                    console.log("keypress", event.keyCode);
                });
    
        * Ngoài ra còn có thể xử lý việc nhấn tổ hợp phím:

            addEventListener("keydown", function(event) {
                if (event.ctrlKey)
                    console.log("keydown", "ctrlKey", event.keyCode);
            );
            addEventListener("keydown", function(event) {
                if (event.shiftKey)
                    console.log("keydown", "shiftKey", event.keyCode);
            });
            addEventListener("keydown", function(event) {
                if (event.altKey)
                    console.log("keydown", "altKey", event.keyCode);
            });

    + MouseEvent:
        1. click: được gọi khi nhấn chuột một lần
        2. dblclick: được gọi khi nhấn chuột nhanh hai lần
        3. mousedown: được gọi khi nhấn chuột xuống lần
        4. mouseup: được gọi khi nhả chuột ra
        5. mousemove: được gọi khi nhấn và kéo chuột
        ...

3. Huỷ hàm thực hiện mặc định 
    + Sử dụng phương thức preventDefault ngăn không cho trang web reload khi thực hiên event.
        <a href="https://developer.mozilla.org/">MDN</a>
        <script>
            var link = document.querySelector("a");
            link.addEventListener("click", function (event) {
                console.log("Nope.");
                event.preventDefault();
            });
        </script>