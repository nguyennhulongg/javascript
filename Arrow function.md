1. Arrow function là gì
    + Cũng là hàm nhưng mà đẹp trai hơn hàm được định nghĩa bằng từ khoá function
    + Được định nghĩa bằng dấu mũi tên (dấu kamekameha) "=>"
    + Cú pháp:
        const functionName = (param1, param2,..) => {
            ...code
        };
    + Nếu chỉ có 1 tham số thì bỏ dấu ngoặc đơn đi cũng được
        const functionName = param1 => {
            ...code
        };
    + Nếu không có tham số
        const functionName = () => {
            ...code
        };

        Ex: 
            const sum = (a, b) => {
                console.log(a + b);
            };

            sum(5, 10); => 15
        
2. Sử dụng arrow function làm hàm callback
    Ex:
        function ask(question, handleYes, handleNo) {
            const answer = confirm(question);
            if (answer) {
                handleYes();
            } else {
                handleNo();
            }
        }

        ask(
            "Bạn muốn tiếp tục thực hiện chương trình không?",
            () => console.log("You chose Yes!"),
            () => console.log("You chose No!")
        );