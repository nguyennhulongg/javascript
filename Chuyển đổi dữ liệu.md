1. Chuyển đổi dữ liệu sang String
    + Dùng hàm String(value)
        Ex: 
            console.log(String(1)); => "1"
            console.log(String(true)); => "true"
            console.log(String(false)); => "false"
            console.log(String(NaN)); => "NaN"
            console.log(String(null)); => "null"

2. Chuyển đổi dữ liệu sang Number
    + Khi thực hiện tính toán, JS sẽ chuyển đổi các kiểu dữ liệu về kiểu dữ liệu Number.
        Ex:
            console.log("10" / "2"); => 5
    + Dùng hàm Number(value)
        Ex: 
            console.log(Number("")) => 0
            console.log(Number("Long")) => NaN
            console.log(Number("10")) => 10
            console.log(Number(true)) => 1
            console.log(Number(false)) => 0
            console.log(Number(null)) => 0
            console.log(Number(undefined)) => NaN
    
3. Chuyển đổi dữ liệu sang kiểu Boolean
    + Có thể dùng hàm Boolean(value)
        * Quy luật chuyển đổi dữ liệu sang kiểu Boolean:
            - Những giá trị "empty" như số 0, string rỗng "", null, undefined, NaN sẽ trở thành false
            - Những giá trị còn lại sẽ chuyển thành true
                Ex:
                    console.log(Number(0)) => false
                    console.log(Number("")) => false
                    console.log(Number(null)) => false
                    console.log(Number(undefined)) => false
                    console.log(Number(1)) => true
                    console.log(Number("Long")) => true
                    console.log(Number(" ")) => true

                            