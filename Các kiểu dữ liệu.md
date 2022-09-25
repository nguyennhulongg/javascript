* JS có 8 kiểu dữ liệu 
    - Trong đó thì có 7 kiểu dữ liệu nguyên thuỷ (primitive) đó là:
        1. Boolean (true và false)
        2. Number (1, 2, 3, 4732, 10000)
        3. Null
        4. Underfined
        5. BigInt
        6. String
        7. Symbol
    => Kiểu dữ liệu nguyên thuỷ là kiểu có giá trị không thay đổi được, đây là kiểu dữ liệu có level thấp nhất trong ngôn ngữ lập trình

    - Và có 1 kiểu dữ liệu dạng tham chiếu: 
        1. Object
    => Là tập hợp các thuộc tính (key) và giá trị (value), mà số lượng các key có thể thay đổi ứng với giá trị của key cũng theo đổi theo => do đó giá trị của kiểu dữ liệu tham chiếu cũng có thể thay đổi được

   
    1. Kiểu dữ liệu Boolean:
        + Là kiểu dữ liệu logic chỉ bao gồm 2 giá trị là true (đúng) và false (sai).
            Ex: 
                let isWebLoaded = true; // => Trang web đã được tải xong
                console.log(isWebLoaded); // true

                let isProgramRunning = false; // Chương trình đang không chạy
                console.log(isProgramRunning); // false
    
    2. Kiểu dữ liệu null: 
        + Là kiểu dữ liệu đặc biệt chỉ bao gồm 1 giá trị duy nhất là null
            Ex: 
                let language = null;
                console.log(language); // null
            => Trong ví dụ trên biến language được hiểu là không biết giá trị hoặc không có giá trị.
    
    3. Kiểu dữ liệu undefined:
        + Tương tự như kiểu null, undefined chỉ có 1 giá trị duy nhất là undefined.
            Ex:
                let language = undefined;
                console.log(language); // undefined
            => Kiểu dữ liệu undefined có nghĩa là giá trị chưa đuọc gán
    
        + Sự khác nhau giữa null và undefined đó là
            - Kiểu null là kiểu dữ liệu được gán cho biến, thường được hiểu là không biết, không có.
            - Kiểu undefined là kiểu dữ liệu mặc định của biến sau khi khai báo biến mà không gán giá trị cho biến.
                Ex: 
                    Khai báo biến mà không gán giá trị cho nó 
                        let language;
                        console.log(language); // undefined

        + Trong trường hợp mà biến đã có giá trị rồi, ta vẫn có thể gán lại giá trị cho biến là undefined, tuy nhiên điều này là không nên
            let language = "JavaScript";
            console.log(language); // JavaScript

            // KHÔNG NÊN
            language = undefined;
            console.log(language); // undefined

            // NÊN
            language = null;
            console.log(language); // null

    4. Kiểu dữ liệu number:
        + Là kiểu dữ liệu dạng số. Number trong JS chỉ cần viết số là ra
        + Number trong JS có 2 loại số là kiểu số nguyên và kiểu số thực:
            Ex: 
                let n1 = 66; // số nguyên dương
                let n2 = -66; // số nguyên âm
                let n3 = 3.14; // số thực dương
                let n4 = -3.14; // số thực âm
                let n5 = 2e3; // => 2*10^3 = 2000
                let n6 = 2e-3; // => 2*10^(-3) = 0.002
                let n7 = 0xff; // số dạng hexa (hệ cơ số 16): 15*16 + 15 = 255
                let n8 = 067; // số dạng octa (hệ cơ số 8): 6*8 + 7 = 55
                let n9 = 0b11; // số dạng nhị phân (hệ cơ số 2): 1*2 + 1 = 3
        + Ngoài những loại số trên JS còn có thêm 3 loại số đặc biệt là:
            1. Infinity
                - Là số dương vô cùng, đây là số đặc biệt và nó lớn hơn bất kỳ số nào khác.
                - Có thể sử dụng giá trị này trực tiếp: console.log(Infinity);
                - Hoặc lấy 1 số dương bất kỳ chia cho 0: console.log(1/0);
            2. -Infinity
                - Là số âm vô cùng, đây là số nhỏ hơn bất kỳ 1 số nào khác.
                - Có thể sử dụng giá trị này trực tiếp hoặc lấy 1 số âm bất kỳ chia cho 0 
            3. NaN (Not a Number)
                - Là viêt tắt của Not a Number.
                - Sử dụng đại diện cho những trường hợp tính toán sai
                    Ex: 
                        console.log(0/0) => NaN
                        console.log("Long" / 2) => NaN
                        console.log(Infinity - Infinity) => NaN
    
    5. Kiểu dữ liệu BigInt: 
        + Trong JS, kiểu dữ liệu number không thể biểu diễn được 1 số nguyên lớn hơn (2^53 - 1) và nhỏ hơn -(2^53 - 1)
            => BigInt ra đời nhằm giải quyết vấn đề đó
        + Để biểu diễn số nguyên với kiểu BigInt ta chỉ cần thêm chữ "n" vào sau
            Ex: 
                const reallyBigNumber = 12345678987654321012345678987654321n;
                console.log(reallyBigNumber); // 12345678987654321012345678987654321n 
    
    6. Kiểu dữ liệu string: 
        + String là kiểu dữ liệu dùng để biểu diễn chữ, văn bản, đoạn văn bản,...
        + Có 3 cách để biểu diễn string: 
            1. Dùng dấu nháy đơn ''
            2. Dùng dấu nháy kép ""
            3. Dùng dấu backtip ``
                Ex: 
                    const msg1 = 'Đây là string dùng dấu nháy đơn';
                    const msg2 = "Đây là string dùng dấu nháy kép";
                    const msg3 = `Đây là string dùng dấu backtick`;
        + Dấu nháy đơn và dấu nháy kép là giống nhau
        + Riêng dấu backtip thì ta có thể truyền biến, hằng, thậm chí 1 biểu thức vào string bằng cách sử dụng cú pháp ${...}
            Ex: 
                // Truyền biến vào trong dấu "backtick"
                let name = "Lam";
                console.log(`My name is ${name}`); // My name is Lam

                // Truyền hằng vào trong dấu "backtick"
                const language = "JavaScript";
                console.log(`You are learning ${language}`); // You are learning JavaScript

                // Truyền vào biểu thức
                console.log(`1 + 2 = ${1 + 2}`); // 1 + 2 = 3
        + String trong JS có thể chỉ gồm 1 ký tự "l" nhiều kí tự "Long dep trai" hoặc không có kí tự nào ""

    7. Kiểu dữ liệu symbol:
        + Là 1 kiểu dữ liệu nguyên thuỷ dùng để tạo ra các giá trị duy nhất (unique value) và bất biến (immutable)
        + Symbol thường được dùng làm key cho kiểu dữ liệu object         
        
    8. Kiểu dữ liệu object:
        + Là kiểu dữ liệu tham chiếu, có thể hiểu object là 1 tập hợp các cặp key - value 
        + Kiểu dữ liệu của key có thể là String hoặc Symbol
        + Value ứng với key có thể là bất kỳ kiểu dữ liệu nào

* Cách xác định kiểu dữ liệu của biến
    - Có 2 cú pháp để xác định kiểu dữ liệu của biến:
            1. Dạng toán tử: typeof x
            2. Dạng hàm typeof(x)
        => Kết quả trả về sẽ ở dạng String tương ứng với kiểu dữ liệu
            Ex: 
                let x;
                console.log(typeof x); => undefined

                x = true;
                console.log(typeof x); => boolean

                x = 1;
                console.log(typeof x); => number

                x = 1234567891234567890123456789125345362n;
                console.log(typeof x); => bigint

                x = "hello";
                console.log(typeof x); => string

                x = Symbol("id");
                console.log(typeof x); => symbol

                x = { n: 1 };
                console.log(typeof x); => object

                x = null;
                console.log(typeof x); => object