1. Biến là gì: 
    + Là tên biểu tượng dùng để đại diện cho 1 giá trị, giá trị của biến có thể thay đổi trong chương trình.
    + Cách khai báo biến: let <tên biến>
        Ex: let name = "Long"
        * Hoặc sử dụng toán tử gán "=".
            let name;
            name = "Long"; 
        * Nếu có nhiều biến có thể dùng dấu phẩy để ngăn cách các biến
            let name = "Long", address = "Ha noi"
        * Hoặc viết nhiều dòng:
            let name = "Long",
                address = "Ha noi"
        * Khai báo biến mỗi biến trên 1 dòng:
            let name = "Long";
            let address = "Ha noi"

- Một số lỗi khi khai báo biến trong JS:
    + Khai báo biến nhiều lần:
            let language = "JavaScript";
            let language = "React";
        => lỗi  Uncaught SyntaxError: Identifier 'language' has already been declared
    + Gán giá trị cho biến trước khi khai báo:
            message = "hello";
            console.log(message);

2. Hằng là gì: 
    + Hằng là tên biểu tượng đại diện cho một giá trị không thay đổi trong chương trình.
    + Cách khai báo hằng: const <tên hằng> = <giá trị của hằng>;
        Ex: const PI = 3.141519,
        * Nếu có nhiều hằng có thể dùng dấu phẩy để ngăn cách các biến
            const PI = 3.141519, MAX_ITEM = 100000000;
        * Hoặc viết nhiều dòng
            const PI = 3.141519,
                MAX_ITEM = 100000000
        * Khai báo mỗi hằng số trên 1 dòng:
            const PI = 3.141519;
            const MAX = 100000000;

- Một số lỗi với hằng trong JS:
    + Không gán giá trị cho hằng khi khởi tạo
        * const PI; => SyntaxError
    + Thay đổi giá trị của hằng
       * const PI = 3.14159;
            PI = 10; => TypeError
        
