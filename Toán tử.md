1. Toán tử là công cụ thao tác với dữ liệu.
    + Đối tượng mà toán tử thao tác đến gọi là toán hạng, tuỳ thuộc vào số lượng toán hạng mà JS chia ra thành:
        1. Toán tử 1 ngôi (unary)
        2. Toán tử 2 ngôi (binary)
        3. Toán tử 3 ngôi (ternary)
        4. Toán tử 4 ngôi (n-ary)

2. Các toán tử trong JS
    + Các loại toán tử trong JS:
        1. Toán tử số học.
            - Các toán tử số học trong JS bao gồm:
                1. Toán tử cộng (+).
                2. Toán tử trừ (-).
                3. Toán tử nhân (*).
                4. Toán tử chia (/).
                5. Toán tử chia lấy số dư (%).
                6. Toán tử luỹ thừa (**).
            - Nếu các toán hạng là số: 
                Ex: 
                    console.log(10 / 5) => 2
                    console.log(10 % 5) => 0
                    console.log(10 + 5) => 15
                    console.log(10 - 5) => 5
                    console.log(10 * 5) => 50
                    console.log(10 ** 2) => 100
            - Nếu các toán hạng khác số:
                Ex: 
                    console.log("10" + 5) => "105" => dấu + biến thành toán tử ghép String.
                    console.log("10" / 5) => 2 => JS chuyển chuỗi "10" thành số
                    console.log("10" * 5) => 50 => JS chuyển chuỗi "10" thành số
                    console.log("10Long" / 5) => NaN => "10Long" không chuyển thành số được.
                    console.log("10Long" % 5) => NaN => "10Long" không chuyển thành số được.
                
                * Toán tử ghép string: nếu 1 trong 2 toán hạng là chuỗi thì toán tử + sẽ chuyển thành toán tử ghép string.
                * Toán tử chuyển đổi dữ liệu thành dạng number: khi + là toán tử 1 ngôi thì nó sẽ chuyển đổi toán hạng thành kiểu number
                    Ex: 
                        console.log(+true) => 1

        2. Toán tử gán.
            + Dùng để gán giá trị cho một biến hoặc hằng.
            + Có thể gán giá trị cho biến bằng giá trị của 1 biểu thức.

        3. Toán tử dấu phẩy.
            + Cho phép thức hiện một vài biểu thức (cách nhau bằng dấu phẩy), nhưng chỉ lấy kết quả ở biểu thức cuối cùng
                Ex: 
                    let a = 1;
                    let x = ((a = a + 1), a + 4);

                    console.log(a); // 2
                    console.log(x); // 6

        4. Toán tử bitwise.
            + Các loại toán tử bitwise:
                1. Toán tử AND (&)
                2. Toán tử NOT (!)
                3. Toán tử OR (|)
                4. Toán tử XOR (^)
                5. Toán tử dịch trái (<<)
                6. Toán tử dịch phải (>>)
                7. Toán tử dịch phải (chèn thêm số 0 ở đầu) (>>>)

        5. Toán tử so sánh.
            + Là toán tử 2 ngôi dùng để so sánh giá trị của 2 toán hạng với nhau
            + Các toán so sánh trong JS gồm:
                1. Toán tử so sánh lớn hơn (>), toán tử so sánh nhỏ hơn.
                2. Toán tử so sánh lớn hơn hoặc bằng (>=), toán tử so sánh nhỏ hơn hoặc bằng (<=).
                3. Toán tử so sánh bằng không nghiêm ngặt(==), toán tử so sánh bằng nghiêm ngặt(===).
                4. Toán tử so sánh khác không nghiêm ngặt(!=), toán tử so sánh khác nghiêm ngặt (!==).
            + Kết quả của phép so sánh là True hoặc False.
                Ex:
                    console.log(5 > 6); => false
                    console.log(5 < 6); => true
                    console.log(5 >= 6); => false
                    console.log(5 <= 6); => true
                    console.log(5 == 6); => false
                    console.log(5 === 6); => false
                    console.log(5 != 6); => true
                    console.log(5 !== 6); => true
            + So sánh string
                - So sánh từng chữ cái một(từ trái sang phải).
                    Ex:
                        console.log("A" < "Z"); => true
                        console.log("Small" < "Smart"); => true
                        console.log("Big" < "BigBang"); => true
            + So sánh khác kiểu dữ liệu
                - Khi so sánh khác kiểu dữ liệu, JS sẽ chuyển giá trị toán hạng ra dạng số.
                    Ex:     
                        console.log("5" > 4); => true, vì "5" chuyển thành 5
                        console.log("01" == 1); => true, vì "01" chuyển thành 1
                        console.log("11" == 1); => false, vì "11" chuyển thành 11
                        console.log(true == 1); => true
                        console.log(false == 0); => false
            + So sánh bằng nghiêm ngặt
                - Khi so sánh bằng nghiêm ngặt, JS sẽ không thực hiện chuyển đổi giá trị toán hạng.
                    Ex:
                        console.log("3" === 3); => false
                        console.log(false === 0); => true
                - null và undefined
                    Ex: 
                        console.log(null == undefined); => true
                        console.log(null === undefined); => false

        6. Toán tử logic.
            + Các toán tử logic trong JS
                1. Toán tử OR (||)
                    - Trả về true nếu có ít nhất một số hạng là true và ngược lại là false
                        Ex: 
                            console.log(true || true || true); => true
                            console.log(true || false || true); => true
                            console.log(false || true || false); => true
                            console.log(false || false || false); => false

                2. Toán tử AND (&&)
                    - Trả về true nếu tất cả các toán hạng là true và ngược lại trả về false.
                        Ex: 
                            console.log(true && true && true); => true
                            console.log(true && false && true); => false
                            console.log(false && true && false); => false
                            console.log(false && false && false); => false

                3. Toán tử NOT (!)
                    - Trả về true nếu toán hạng là false và ngược lại 
                        Ex:     
                            console.log(!"hello"); => false ("hello" là truthy)
                            console.log(!100); => false (100 là truthy)
                            console.log(!""); => true ("" là falsy)
                            console.log(!0); => true (0 là falsy)
                            console.log(!null); => true (null là falsy)
                            console.log(!undefined); => true (undefined là falsy)

        7. Toán tử điều kiện rẽ nhánh ?:.
            + Câu lệnh if: 
                - Câu lệnh if sẽ kiểm tra điều kiện trong dấu ngoặc đơn, nếu kết quả là true thì một khối code sẽ được thực thi.
                - Mệnh đề else dùng để thực hiện khối lệnh khi điều kiện trong if là falsy
                    Ex: 
                        const x = 3;
                        if (x % 2 === 0) {
                            console.log("x is an even number");
                        } else {
                            console.log("x is an odd number"); => x is an odd number
                        }
            
            + Toán tử rẽ nhánh trong JS
                - Cách viết ngắn gọn của câu lệnh điều kiện if 
                - Cú pháp: const result = condition ? value1 : value2;
                * Trong đó: condition là điều kiện
                            value1 là giá trị trả về khi condition là truthy
                            value2 là giá trị trả về khi condition là falsy
                    Ex:
                        const age = 24;
                        const enoughAge = age < 18 ? false : true;
                        console.log(enoughAge); => true

        8. Toán tử Nollish Coalescing ??.
            + Toán tử Nullish Coalescing dùng để cung cấp giá trị mặc định cho 1 biến có thể là null hoặc undefined.
                Ex:
                    let name;
                    console.log(name ?? "Người dùng ẩn danh"); => Người dùng ẩn danh


