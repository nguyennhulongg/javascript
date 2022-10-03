1. forEach():
    + forEach được sử dụng để lặp qua tất cả các phần tử của mảng
        Ex:
            Tìm tổng của tất cả số trong mảng số
            let sum = 0;
            const array = [1, 2, 3, 4, 5];

            array.forEach((number) => {
                sum += number; 
            })

2. map(): 
    + Lặp qua tất cả các phần tử của mảng, sửa đối chúng, trả về mảng mới mà không làm thay đổi mảng cũ
        Ex:
            const numbers = [1, 2, 3, 4, 5];

            // nhân từng phần tử với 2
            let double = numbers.map((num) => {
                return num * 2;
            });

            console.log(double); // [2, 4, 6, 8, 10]

3. filter()
    + Lặp qua các phần tử của mảng và lọc ra các phần tử thoả mãn điều kiện cho trước
        Ex:
            let objects = [
                { flag: 1, a: 1 },
                { flag: 0, a: 2 },
                { flag: 1, a: 3 },
            ];

            const newArray = objects.filter((object) => {
                return object.flag === 1;
            });

            newArray.forEach((item) => {
                console.log("flag:" + item.flag + ", a:" + item.a);
            });

4. find()
    + Trả về phần tử đầu tiên trong mảng thoả mãn điều kiện cho trước
    + Nếu không tìm được phần tử nào thoả mãn thì find() sẽ trả về undefined
        Ex:
            let objects = [
                { flag: 1, a: 1 },
                { flag: 0, a: 2 },
                { flag: 1, a: 3 },
                { flag: 0, a: 4 },
            ];

            const item = objects.find((object) => {
                return object.flag === 0;
            });

            console.log(item);
            // {flag: 0, a: 2}


    * Chú ý: phương thức find() trả về một phần tử, còn phương thức filter() trả về mảng các phần tử