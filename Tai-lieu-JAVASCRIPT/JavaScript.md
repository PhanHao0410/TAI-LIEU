# JavaScript

### 1. Introduction: 
- là một ngôn ngữ lập trình Web
- dùng để lập trình hành vi của các trang Web.

### 2. JS Variables: Let, Const và Var.
- Keywords let và const được thêm vào JS từ năm 2015.
- Keywords var chỉ nên được sử dụng trong code viết cho những trình duyệt cũ hơn

#### 2.1. JS Let: 
- Biến được xác định ko được khai báo lại.
- Có phạm vi trong khối (trong {}) - các biến được khai báo trong khối {} không thể được truy cập từ bên ngoài khối.
- Phải khai báo trước khi sử dụng.
- Chỉ sử dụng let nếu không thể sử dụng const.
#### 2.2. JS Const: 
- Biến được xác định không được khai báo lại.
- Không thể được gán lại giá trị.
- Có phạm vi trong khối (Block Scope).
- Các biến const phải được gán 1 giá trị khi nó được khai báo.
- Được sử dụng nếu không nên thay đổi giá trị hoặc loại.
- Sử dụng khi muốn khai báo: một mảng mới, một object mới, một function mới, một RegExp mới.
#### 2.3. JS Var: 
- Có thể khai báo lại.
- Không có phạm vi.
- Có thể gán giá trị sau đó mới khai báo.
### 3. JS có 8 kiểu dữ liệu: 
- String
- Number
- BigInt
- Boolean
- Undefined
- Null
- Symbol
- Object
#### 3.1. Object: 
- Đối tượng là những thứ, sự việc, vật ta thấy được ngoài đời đưa vào code.
- Đối tượng gồm có thuộc tính và phương thức.
- Object có 3 kiểu dữ liệu đặc biệt: 
    - An object.
    - An Arrar
    - An date
#### 3.2. Array: 
- Là một biến đặc biệt có thể chứa nhiều giá trị.
- Mảng là một dạng đặc biệt của object.
### 4. So sánh: ==, ===, empty, null, undefined.
- So sánh "==": value.
- So sánh "===": type và value.
- Empty: một object rỗng
- Undefined: khi tạo biến mà ko gắn giá trị.
- Null: một object rỗng nhưng ko đến địa chỉ bộ nhớ nào.
### 5. Vòng lặp: 
#### 5.1 Js For Loop: 
- Vòng lặp có thể thực thi một khối mã nhiều lần.
- Syntax:
    ```js
    for(exp 1; exp 2; exp3){
        // code block to be executed
    }
    ```
    Note: 
    - Exp 1: gán giá trị cho biến được thực thi một lần trước khi thực khi khối mã.
    - Exp 2: xác định điều kiện để thực thi khối mã.
    - Exp 3: thực thi nhiều lần sau khi khối mã được thực thi
#### 5.2. JS While Loop: 
- Lặp một khối code miễn là điều kiện chỉ định là đúng.
- Dùng trong những tình huống ko biết chính xác số lần lặp, có thể tạo điều kiện true hoặc false.
    ```js
    while (condition){
        // code block to be executed
    }
    ```
#### 5.3. JS Do While:
- Khác vs vòng lặp while, vòng lặp do while sẽ thực thi khối code một lần sau đó mới kiểm tra đến điều kiện, nếu diều kiện là đúng nó sẽ lặp lại khối code đó tiếp tục. (Trong vòng lặp này nếu điều kiện sai thì mã lệnh đều được thực hiện 1 lần).
- Syntax:
    ```js
    do{
        // code block to be executed
    }
    while(condition)
    ```

### 6. Điều kiện if/else:
- Sử dụng để thực hiện các hành động khác nhau dựa trên các điều kiện khác nhau.
- Syntax: 
    ```js 
    if (condition){
        // block of code to be executed if the condition is true
    else {
        // block of code to be executed if the condition is false
    }
    }
    ```
### 7. Câu lệnh break/continue:
#### 7.1. break: 
-  Câu lệnh break nhảy ra khỏi vòng lặp.
- Ví dụ: 
    ```js
    for(let i = 0; i<10;i++){
        if(i===3){break;}
        text += "the number is" +i + "<br>";
    }
    // tại đây vòng lặp sẽ chạy đến khi i = 3 thì sẽ thoát ra khỏi vòng lặp
    ```
#### 7.2. continue: 
- Bỏ qua một lần lặp nếu điều kiện chỉ định xảy ra và tiếp tục với lần lặp tiếp theo trong vòng lặp.
- Ví dụ: 
    ```js
    for(let i = 0; i<10;i++){
        if(i===3){continue;}
        text += "the number is" +i + "<br>";
    }
    // tại đây vòng lặp sẽ chạy và in ra dòng text đến khi i =3 nó sẽ ko chạy đến dòng code tiếp theo mà lặp sang 4 luôn
    ```
### 8. Switch/case: 
- Sử dụng để thực hiện các hành động khác nhau dựa trên các điều kiện khác nhau.
- Syntax: 
    ```js
    switch (expression){
        case x: 
        // code block
        break;
        case y: 
        // code block
        break;
        default:
        // code block
    }
    ```
### 9. JS Function: 
#### 9.1. Function:
- là một khối mã được thiết kế để thực hiện một tác vụ cụ thể.
- được thực thi khi một thứ gì đó gọi nó.
- có thể sử dụng mã nhiều lần, cùng một mã với các đối số khác nhau để tạo kết quả khác nhau.
- Vd: 
    ```js
    function myFunction(p1,p2){
        return p1*p2;
    }
    ```
- Syntax: 
    ```js
    function name(parameter1, parameter2,....){
        // code to be executed
    }
    ```
- Khi js gặp câu lệnh return hàm sẽ ngừng thực thi và thoát khỏi function đó.
#### 9.2. Arrow function:
- Cho phép viết cú pháp function ngắn hơn.
- Syntax:
    ```js
    const myFunction=(a,b)=>{
        return a*b;
    }
    ```
#### So sánh function và method:
- function: free (ko cần phải viết trong object hoặc class).
- method: member (phải viết trong obj hoặc class)

### 10. JS Callback: 
- Là một function được truyền dưới dạng đối số cho function khác.
- Kỹ thuật này cho phép một function gọi một function khác.
- function callback có thể chạy sau khi function khác kết thúc.
- Sử dụng trong các hàm không đồng bộ, trong đó một hàm phải chờ một hàm khác.
- Ví dụ: 
    ```js 
    const myDisplay=(some)=>{
        console.log("check sum: ", some)
    }
    const mySum = (a,b,myCallBack)=>{
        let sum = a+b;
        myCallBack(sum)
    };
    mySum(10,20,myDisplay);
    // Tại đây sẽ hiển thị là 30.
    ```
### 11. Method Array: 
#### 11.1. Array.filter():
- Tạo ra mảng mới được sao chép lọc lại những phần tử từ mảng đã cho thỏa mãn điều kiện hàm cung cấp.
- Ví dụ:
    ```js
    const arrNumber = [2,19,4,12,20,5];
    const result = arrNumber.filter((item, index)=>{
        return item&&item >10;
    })
    console.log("check result: ", result);
    // kết quả được trả về sẽ là: result =[19,12,20]
    ```
#### 11.2. Array.find():
- Trả về phần tử đầu tiên của mảng đã cho thỏa mãn điều kiện hàm cung cấp. Nếu ko có phần tử nào thỏa mãn sẽ trả về ***undefined***
- Ví dụ:
    ```js
    const arrNumber = [2,19,4,12,20,5];
    const result = arrNumber.find((item, index)=>{
        return item&&item >10;
    })
    console.log("check result: ", result);
    // kết quả được trả về sẽ là: result =19
    ```
#### 11.3. Array.map():
- Trả về một mảng mới được sao chép lặp lại mảng đã cho ban đầu mà ko làm ảnh hưởng đến mảng ban đầu.
- Ví dụ: 
    ```js
    const arrNumber = [1,2,3,4,5];
    const result = arrNumber.map((item, index)=>{
        return item*2;
    })
    console.log("check result: ", result);
    // kết quả được trả về sẽ là: result =[2,4,6,8,10]
    ```
#### 11.4. Array.reduce():
- Thực thi hàm rút gọn cho phần tử mảng.
- Trả về một giá trị duy nhất: kết quả tích lũy của hàm.
- Không thực thi hàm cho các phần tử mảng trống.
- Không thay đổi mảng ban đầu.
- Ví dụ: 
    ```js
    const numbers = [2,5,12,6];
    const result = numbers.reduce(tinhTong,10)
    const tinhTong = (total, num)=>{
        return total + num
    };
    console.log("check result: ", result);
    // Tại đây kết quả sẽ là: 10 + 2 +5 +12 + 6= 35;
    ```
#### 11.5. Array.sort():
- Sắp xếp các phần tử của một mảng tại chỗ và trả về tham chiếu đến cùng một mảng. Thứ tự sắp xếp mặc định là tăng dần 
- Ví dụ: 
    ```js
    const numbers = [1,5,3,8,2];
    numbers.sort((a,b)=>{
        return a - b
    })
    // Tai đây numbers = [1,2,3,5,8]
    numbers.sort((a,b)=>{
        return b-a
    })
    // Tại đây numbers = [8,5,3,2,1]
    ```
### 12. JS Async (Asynchronous):
- Là một kỹ thuật cho phép chương trình bắt đầu một tác vụ có khả năng chạy lâu và vẫn có thể phản hồi vs các sự kiện khác trong khi tác vụ đó chạy thay vì phải đợi cho đến khi tác vụ đó kết thúc. Khi nhiệm vụ đó hoàn thành, chương trình sẽ hiển thị kết quả.
### 13. JS XMLHttpRequest Object: 
- có thể được sử dụng để yêu cầu dữ liệu từ một web server.
    - Cập nhật một trang web mà không cần phải tải lại.
    - Yêu cầu dữ liệu từ server sau khi trang được tải.
    - Nhận dữ liệu từ server sau khi trang được tải.
    - Gửi dữ liệu đến server ở chế độ nền. 
#### 13.1. Status code: 
- Cho biết một yêu cầu HTTP có được hoàn thành thành công hay không.
- Chia làm 5 loại: 
  - Informational Responses (100-199)
  - Successful responses (200-299)
  - Redirection messages (300-399)
  - Client error responses (400-499)
  - Server error responses (500-599)
### 14. JSON Data: 
- là viết tắt của JavaScript Object Notation.
- Là một định dạng để lưu trữ và truyền tải dữ liệu.
- Là một ngôn ngữ độc lập. Thường được sử dụng khi dữ liệu được gửi từ máy chủ đến trang web.
- Ví dụ:
    ```JSON
    {
    "employees":[
    {"firstName":"John", "lastName":"Doe"},
    {"firstName":"Anna", "lastName":"Smith"},
    {"firstName":"Peter", "lastName":"Jones"}
    ]
    }
    // json luôn được định dạng là một văn bản
    ```
- Quy tắc: 
  - Dữ liệu nằm trong cặp tên/giá trị.
  - Dữ liệu được phân tách bằng dấu phẩy.
  - Ngoặc nhọn giữ object và ngoặc vuông giữ array.
#### 14.1: Chuyển đổi a JSON text thành một object js:
- JSON đọc dữ liệu từ máy chủ web và hiển thị dữ liệu trong trang web. Vì thế có thể được thể hiện bằng cách sử dụng một chuỗi làm đầu vào.
- Sau đó sử dụng hàm ***JSON.parse()*** của js để chuyển đổi chuỗi thành đối tượng JS:
    ```js
    const obj = JSON.parse(text)
    // text là chuỗi dữ liệu nhận từ JSON.
    ```
#### 14.2: Chuyển đổi 1 object js thành một chuỗi JSON:
- Để chuyển đổi ta sẽ dùng hàm ***JSON.stringify()*** để biến đổi một object js thành một chuỗi JSON:
    ```js
    const text = JSON.stringify(obj)
    // obj là một object js
    ```
### 15. Callback Hell:
- là các callback lồng nhau được xếp chồng lên nhau tạo thành cấu trúc kim tự tháp( hoặc có thể callback này lấy return callback khác làm đối số). Mỗi callback đều phụ thuộc/chờ callback trước đó, do đó tạo ra cấu trúc kim tự tháp ảnh hưởng đến khả năng đọc và bảo trì mã.
- Ví dụ: 
    ```js
    firstFunction(args, function(){
        secondFunction(args, function(){
            thirdFunction(args, function(){
                //........
            })
        })
    })
    ```
- Có 4 giải pháp cho callback hell: 
  - Viết comments
  - Chia functions thành functions nhỏ hơn
  - Sử dụng Promises
  - Sử dụng Async/await
### 16. JS Promise, Async/Await: 
#### 16.1. JS Promise:
- Là một đối tượng được trả về mà đính kèm các lệnh callback thay vì chuyển các lệnh callback vào một function.
- Là một đối tượng thể hiện sự hoàn thành hoặc thất bại cuối cùng của một hoạt động không đồng bộ 
- Giúp giải quyết vấn đề callback hell khiến update hoặc bảo trì code trở nên dễ dàng hơn.
- Ví dụ:
    ```js 
    let myPromise = new Promise(function(myResolve, myReject) {
    let req = new XMLHttpRequest();
    req.open('GET', "mycar.html");
    req.onload = function() {
    if (req.status == 200) {
      myResolve(req.response);
    } else {
      myReject("File not Found");
    }
    };
    req.send();
    });

    myPromise()
    .then(data=>{console.log("check success: ",data)})
    .catch(error =>{console.log("check error: ",error)})
    ```
- Một Promise Object có thể là:
  - ***Pending***: promise được tạo và chứ năng async được liên kết vẫn chưa thành công hoặc thất bại, yêu cầu vẫn đang được thực hiện. Sẽ Return ***```Undefined```***
  -  ***fulfilled***: async function dã thành công, hàm xử lý ***```then()```*** sẽ được gọi. Sẽ Return ***```a result value```***
  -  ***rejected***: async function đã thất bại, hàm xử lý ***```catch```*** sẽ được gọi. Sẽ Return ***```a error object```***

#### 16.2. JS Async/Await: 
- Làm cho Promise dễ viết hơn.
- async: làm cho function trả về Promise.
- await: làm cho một function chờ một promise.
- Ví dụ: 
    ```js
    const getData = async (id)=>{
        let response = await fetch(`https://jsonplaceholder.typicode.com/todos/${id}`)
        let data = await response.json();
        return data
    }
    getData(1)
    .then(data=>{console.log("check data: ", data)})
    ```


### 17. JS Fetch API: 
- Cung cấp giao diện JS để truy cập và thao tác các phần của giao thức như yêu cầu và phản hồi.
- Fetch dựa trên Promise và cung cấp giải pháp thay thế tố hơn. Tích hợp các khái niệm HTTP nâng cao như CORS và các tiện ích mở rộng khác cho HTTP.
- Ví dụ: 
    ```js
    fetch(file)
    .then(x=>x.text())
    .then(y=>myDisplay(y))
    ```

### 18. Js Error:
#### 18.1. Throw Error: 
- Xác định một lỗi tùy chỉnh.
- Khi xảy ra lỗi, JS sẽ dừng và tạo thông báo lỗi.
- Lỗi tạo ra có thể là: string, number, boolean hoặc object:
- Ví dụ: 
    ```js
    throw "Too big"; //throw a text
    throw 500 //throw a number
    ```
#### 18.2. JS try/catch:
- Statement ***```try```*** Cho phép xác định một khối code để kiểm tra lỗi trong khi nó đang được thực thi.
- Statement ***```catch```*** cho phép xác định khối code sẽ được thực thi nếu xảy ra lỗi trong khối thử.
- Syntax: 
    ```js 
    try{
        Block of code to try
    }
    catch(err){
        Block of code to handle errors
    }
    ```
#### 18.3. Error Object: 
- tích hợp cung cấp thông tin lỗi khi xảy ra lỗi.
- Cung cấp 2 thuộc tính hữu ích: name và message

