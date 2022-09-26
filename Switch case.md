1. Switch case là gì
    + Là một cấu trúc rẽ nhánh dùng để xác định 1 danh sách các trường hợp và khối lệnh tương ứng với mỗi trường hợp
    + Khi giá trị đang xét bằng nghiêm ngặt với trường hợp nào thì khối lệnh tương ứng sẽ được thực thi

2. Cú pháp
    switch(x) {
        case 'value1':  // if (x === 'value1')
            ...
            [break]

        case 'value2':  // if (x === 'value2')
            ...
            [break]

        default:
            ...
            [break]
    }

    - Giá trị x được kiểm tra lần lượt bằng nghiêm ngặt với các giá trị value1, value2,...
    - Khi tìm thấy value thoả mãn thì khối lệnh bắt đầu từ case đó cho đến khi gặp break gần nhất, hoặc kết thúc lệnh switch case
    - Nếu không có trường hợp nào thoả mãn thì khối lệnh ứng với default sẽ được thực thi
        Ex:
            const x = 2 + 3;
            switch (x) {
            case 4:
                console.log("Less than");
                break;
            case 5:
                console.log("Equal");
                break;
            case 6:
                console.log("Greater than");
                break;
            default:
                console.log("Don't know the answer");
            }

3. Nhóm các case
    Ex: 
        const n = 5;
        switch (n) {
        case 3:
            console.log("Hi!");
            break;
        case 4:
            console.log("Hello!");
            break;
        case 5:
            console.log("Hi!");
            break;
        default:
            console.log("Bye!");
        }
    => case 3 và case 5 xử lý giống nhau
    => có thể gộp 2 trường hợp này với nhau như sau: 
        const n = 5;
        switch (n) {
        case 4:
            console.log("Hello!");
            break;
        case 3:
        case 5:
            console.log("Hi!");
            break;
        default:
            console.log("Bye!");
        }

