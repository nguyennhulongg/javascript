1. Prototype
    + Trong JavaScript object có một thuộc tính là [[Prototype]], giá trị có thể là null hoặc là một object 
    + Khi tìm kiếm một thuộc tính trong object, nếu thuộc tính đó không tồn tại thì JS sẽ tự động tìm kiếm trong Prototype
        => Gọi là kế thừa Prototype.
    + [[Prototype]] là một thuộc tính ẩn, nhưng có thể cài đặt thuộc tính này, một trong những cách phổ biến nhất là sử dụng 
        "__proto__"

            Ex: 
            let animal = {
                eats: true,
            };
            let rabbit = {
                jumps: true,
            };

            rabbit.__proto__ = animal; => gán rabbit.[[Prototype]] = animal

    + Nếu đọc một thuộc tính trong rabbit và thuộc tính đó không tồn tại thì JS sẽ tìm kiếm trong animal
        let animal = {
            eats: true,
        };
        let rabbit = {
            jumps: true,
        };

        rabbit.__proto__ = animal; // (*)

        console.log(rabbit.eats); // true (**)
        console.log(rabbit.jumps); // true 

    + Prototype có thể kế thừa móc nối nhau qua nhiều object như sau: 
        let animal = {
            eats: true,
            walk() {
                console.log("Animal walk");
            },
        };

        let rabbit = {
            jumps: true,
            __proto__: animal,
        };

        let longEar = {
            earLength: 10,
            __proto__: rabbit,
        };

        // walk() được lấy thông qua các prototype móc nối nhau
        longEar.walk(); // Animal walk
        console.log(longEar.jumps); // true (lấy từ rabbit)

2. Giới hạn của Prototyoe
    + Không được phép kế thừa Prototype vòng tròn
    + Giá trị của __proto__ có thể là null hoặc object, nhưng các kiểu dữ liệu khác sẽ bị bỏ qua 
        Ex:
            let rabbit = {
                jumps: true,
                __proto__: 1, // bị bỏ qua
            };
    + Protoype không hỗ trợ thay đổi giá trị thuộc tính
        Ex:
            let animal = {
                eats: true,
                walk() {
                    console.log("Animal walk");
                },
            };

            let rabbit = {
                jumps: true,
                __proto__: animal, // gán animal là prototype của rabbit
            };

            // định nghĩa giá trị mới cho rabbit.walk
            rabbit.walk = function () {
                console.log("Rabbit walk");
            };

            rabbit.walk(); // Rabbit walk - giá trị mới
            animal.walk(); // Animal walk - giá trị cũ

3. Vòng lặp for...in khi kế thừa trong Prototype
    + Vòng lặp for...in:
        Ex: 
            let animal = {
                eats: true,
            };

            let rabbit = {
                jumps: true,
                __proto__: animal,
            };

            for (let prop in rabbit) console.log(prop);
            // jumps
            // eats

    + Sử dụng phương thức Object.keys trả về mảng chứa các keys của object, bỏ qua thuộc tính prototype
        Ex: 
            let animal = {
                eats: true,
            };

            let rabbit = {
                jumps: true,
                __proto__: animal,
            };

            console.log(Object.keys(rabbit)); // ['jumps'] 
