1. Đông bộ và Bất đồng bộ
    - Đồng bộ: công việc A phải thực hiện xong thì mới công việc B mới băt đầu thực hiện
    - Bất đồng bộ: khi A bắt đầu thực hiện, B bắt đầu thực hiện mà không đợi A kết thúc

2. Xử lý bất đồng bộ bằng Callback
    Ex:
        function doAsync(url, onSuccess, onError) {
            const xhr = new XMLHttpRequest();
            xhr.open("GET", url);
            xhr.onload = () => onSuccess(xhr.responseText);
            xhr.onerror = () => onError(xhr.statusText);
            xhr.send();
        }
        // Usage:
        doAsync(
            "https://something.com",
            (value) => {
                // 'value' is corresponding with 'xhr.responseText'
            },
            (error) => {
                // 'error' is corresponding with 'xhr.statusText'
            }
        );

3. Xử lý bất đồng bộ bằng Promise
    - Cú pháp:
        let promise = new Promise(function (resolve, reject) {
            // Code here
        });
        * Trong đó hàm được truyền vào new Promise() được gọi là executor
    
    - Ban đầu promise có state là pending và kết quả value là undefined, khi executor hoàn thành công việc, nó sẽ gọi đến 1 trong 2 hàm được truyền vào:
        + resolve(value) : xác định rằng công việc đã thành công
            * state chuyển qua thành fulfilled
            * kết quả là value
        + reject(error) : xác định rằng công việc đã thất bại
            * state chuyển qua thành reject
            * kết quả là error

    Ex:
        function doAsync(url) {
            return new Promise((resolve, reject) => {
                const xhr = new XMLHttpRequest();
                xhr.open("GET", url);
                xhr.onload = () => resolve(xhr.responseText);
                xhr.onerror = () => reject(xhr.statusText);
                xhr.send();
            });
        }

        // Usage:
        doAsync("https://something.com")
        .then((value) => {
            // 'value' is corresponding with 'xhr.responseText'
        })
        .catch((error) => {
            // 'error' is corresponding with 'xhr.statusText'
        });

4. Xử lý bất đồng bộ với asyn/await
    - Async/await giúp làm việc với promise dễ dàng hơn 
        Ex:
            function doAsync(url) {
                return new Promise((resolve, reject) => {
                    const xhr = new XMLHttpRequest();
                    xhr.open("GET", url);
                    xhr.onload = () => resolve(xhr.responseText);
                    xhr.onerror = () => reject(xhr.statusText);
                    xhr.send();
                });
            }

            // Usage:
            async function run() {
                let responseText1, responseText2;

                try {
                    responseText1 = await doAsync("https://something.com");
                    responseText2 = await doAsync("https://other.com");
                } catch (error) {
                    /*
                    * 'error' is corresponding with 'xhr.statusText'
                    * from either 'https://something.com' or 'https://other.com'
                    */
                }
            }

            run();




