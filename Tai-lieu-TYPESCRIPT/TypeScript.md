# TypeScript (TS)
### 1. Introduction:
- Là thêm cú pháp lên trên JavaScript, cho phép các nhà phát triển thêm types
- Là một siêu tập hợp cú pháp nó chia sẻ cú pháp cơ bản giống như JS, nhưng thêm một số thứ vào đó.
#### 1.1. Nên dùng TS vì:
- Js là một ngôn ngữ có typed lỏng lẻo. Có thể khó hiểu loại dữ liệu nào đang được truyền trong JS.
- Trong JS, các tham số và biến của function không có bất kỳ thông tin nào.
- TS cho phép chỉ định các loại dữ liệu được truyền trong mã và có khả năng báo cáo lỗi khi các loại dữ liệu không khớp.
- **NOTE:** ***TypeScript*** kiểm tra xem các types được chỉ định có khớp hay không trước khi chạy code chứ không phải trong khi chạy code.
#### 1.2. Cách sử dụng TS: 
- cách phổ biển là sử dụng TypeScript compiler, dịch mã TS thành JS.
### 2. TypeScript Types: 
#### 2.1. Type: 
- gồm 2 loại là: keyword type và data-type
- việc định nghĩa kiểu dữ liệu sẽ thể hiện cho biết biến số có những thuộc tính và function nào.
#### 2.2. Các loại data-types vs TS:
- Tương tự như JS, TS datatype bao gồm: 
  - Kiểu dữ liệu nguyên thủy: String, number, boolean, null, undefined, symbol, bigint.
  - Kiểu dữ liệu tham chiếu: Objects, Array, Function.
- Khi tạo biến, có 2 cách chính TS gán một type: rõ ràng(explicit) và ngầm(implicit).
- Explicit Type: thể hiện loại rõ ràng dễ đọc hơn và có chủ ý hơn.
    ```ts
    let firstName:string = "Hao";
    ```
- Implicit Type: TS sẽ đoán type dựa trên giá trị được chỉ định:
    ```ts
    let firstName = "Hao";
    ```
#### 2.3. Type inference vs Type annotations: 
- ***Type inference:*** TS sẽ đoán kiểu dữ liệu dựa vào thuật toán của nó. Được sử dụng khi ko biết rõ hàm hay biến đó sẽ return sẽ trả về type nào.
- ***Type annotations:*** ép buộc chính xác kiểu dữ liệu. Được sử dụng khi khai báo biến và gán giá trị cho nó ngày sau đó hoặc ép kiểu, muốn ép kiểu trả về giá trị mong muốn.
### 3. TS Object Type: 
- Ts có cú pháp đặc biệt cho Object.
- Syntax: 
    ```ts
    const car:{type: string, model: string, year: number}={
      type: "Honda",
      model: "Mazda",
      year: 2023
    };
    ```
### 3. TS Array Type: 
- Ts có cú pháp cụ thể cho mảng.
    ```ts 
    const name:string[]=[];
    name.push("Hao"); // no error
    // name.push(45) // error: type number no use string 
    ```
- Keyword ***readonly:*** có thể ngăn mảng thay đổi.
    ```ts
    const name: readonly string[]=["Hào"]
    //name.push("Hehe"); //Error: thuộc tính push ko tồn tại trong dạng readonly
    ```
- Có thể mix nhiều dạng dữ liệu trong mảng:
    ```ts
    const name: (string|number|boolean)[]=["Hao",24,true]
    ```

### 4. TS Tuples: 
- Là một mảng được định kiểu vs độ dài và kiểu được xác định trước cho mỗi chỉ mục.
- Tuples rất tuyệt vời, vì cho phép mỗi phần tử trong mảng trở thành một loại giá trị đã biết.
- Ví dụ: 
    ```ts
    const lists :[number, boolean, string]=[5, true, "Hao"];
    ```
### 5. TS Enum: 
- Là một "class" đặc biệt đại diện cho một nhóm các hằng số(các biến ko thể thay đổi).
- Enum có 2 loại chuỗi và số
#### 5.1. Numeric Enums - Default: 
- Theo mặc định, enums sẽ khởi tạo giá trị đầu tiên thành 0 và thêm 1 vào mỗi giá trị bổ sung: 
- Ví dụ: 
    ```ts
    enum directions{
      North, //0
      East, //1
      South, //2
      West //3
    };
    let currentDirection = directions.North;
    console.log(currentDirection) // return log = 0
    ```
#### 5.2. String Enums: 
- Enums cũng có thể chứa string, điều nayfphoor biến hơn số vì tính dễ đọc và mục đích của chúng.
- Ví dụ: 
    ```ts
    enum directions {
      North = "North",
      East = "East",
      South = "South",
      West = "West"
    }
    ```
### 6. TS Any Type: 
- Đôi khi dùng biến lưu giá trị nhưng lại ko chắc chắn về kiểu dữ liệu của biến đấy, để không bị "compiler" của TS báo lỗi thì ta nên sử dụng ***```any type```***.
- Với any type chúng ta báo cho "compiler" không check kiểu giá trị.
- Ví dụ: 
    ```ts
    let name: any = "Hao";
    name = 20;
    ```
- Trả về bất cứ thứ gì áp dụng cho function và variable
### 7. TS void Type:
- ***void*** được sử dụng khi không có dữ liệu như một hàm không trả về bất kỳ giá trị nào thì có thể chỉ định void làm kiểu trả về.
- Không cần trả ra dữ liệu thực chất vẫn trả ra, không cần keyword return, chủ yếu dùng cho function.
- Ví dụ: 
    ```ts
    const handleLogs = (message: string): void => {
      console.log("check message: ", message)
    };
    ```
### 8. TS Never Type: 
- Không bảo giờ trả ra giá trị.
- Được sử dụng khi ta chắc chắn rằng một điều gì đó sẽ không bao giờ xảy ra.
- Ví dụ: 
    ```ts 
    function handleException(errorMessage: string): never{
      throw Error(errorMessage)
    }
    ```

### 9. TS Function Type: 
- Có một cú pháp cụ thể cho các tham số function và giá trị return.
#### 9.1. Return Type: 
- Loại giá trị được function trả về có thể được xác định rõ ràng.
- Nếu ko có kiểu trả về được xác định, TS sẽ cố suy ra nó thông qua các kiểu biến hoặc biểu thức được trả về.
- Ví dụ: 
    ```ts
    const sum = (a: number, b: number):number=>{
      return a+b;
    };
    ```
#### 9.2. Void return type:
- Type ***void*** có thể được sử dụng để chỉ ra function không trả về bất kì giá trị nào
- Ví dụ: 
    ```ts
    const printHello = ():void=>{
      console.log("Hello!");
    };
    ```
### 10. TS Rest Parameters:
- Rest parameter có các rules sau: 
  - 1 function chỉ có 1 tham số duy nhất rest parameter.
  - phải là tham số cuối cùng trong danh sách tham số.
  - phải sử dụng với array type.
- Syntax: 
    ```ts
    function fn(...rest: type[]){
      // code block
    }
    ```
- Ví dụ: 
    ```ts
    const multiply = (n: number, ...m: number[])=>{
      return m.map(x)=> n * x;
    }
    const test = multiply(15,1,2,3,4)
    console.log("check test: ",test);
    // return 15,30,45,60.
    ```
### 11. Ts Classes:
- Class (properties & methods) được nhập bằng cách sử dụng các chú thích type, tương tự như các biến.
- Syntax: 
    ```ts 
    class Persons{
      ssn: string;
      firstName: string;
      lastName: string;
    }
    constructor(ssn: string, firstName: string, lastName: string){
      this.ssn = ssn;
      this.firstName = firstName;
      this.lastName = lastName;
    }

    getFullName():string{
      return `${this.firstName} ${this.lastName}`
    }

    const person = new Persons("456", "Thanh Hào", "Phan")
    console.log("check person: ", person.getFullName())
    // return: check person Thanh Hào Phan
    ```
   
#### 11.1. Access modifiers:
- Các phần tử trong class cũng được cung cấp các sửa đổi đặc biệt ảnh hưởng đến khả năng hiển thị.
- Có 3 công cụ sửa đổi mức độ hiển thị chính trong TS:
  - ***```public```***: (default) cho phép truy cập các phần tử trong class từ mọi nơi.
  - ***```private```***: chỉ cho phép truy cập các phần tử trong class từ bên trong class.
  - ***```protecte```***: cho phép truy cập các phần tử trong class từ chính nó và bất kỳ class kế thừa nó. Class cha có thể truy cập class con, class con ko thể truy cập class cha.

- Ví dụ: 
    ```ts 
    class Persons{
      public firstName: string;
      private lastName: string;
      constructor(firstName: string, lastName: string){
        this.firstName = firstName;
        this.lastName = lastName;
      }
    }
    const person = new Persons("adf","jfd");
    person.firstName = "Hào";
    person.lastName = "Phan";// Error không thể truy cập vì đã để chế độ private.
    ```
#### 11.2. TS Readonly: 
- Chỉ đọc không Modify(update/delete)
- Ví dụ: 
    ```ts
    class Persons{
      readonly birthDate: Date;
      constructor(birthDate: Date){
        this.birthDate = birthDate;
      }
    }
    let person = new Person(new Date(2000,10,04))
    person.birthDate = new Date(2001, 10, 04); // Compile error
    ```
#### 11.3. TS Getter và Setter:
- Với kiểu dữ liệu private không thể truy cập t có thể sử dụng getter và setter để xử lý điều đó.
- Ví dụ: 
    ```ts
    class Persons{
      private _age: number;
      public firstName: string;
      public lastName: string;
      
      constructor(_age: string, firstName: string, lastName: string){
        this._age = _age;
        this.firstName = firstName;
        this.lastName = lastName;
      }

      get getAge(){
        return this._age
      }

      set setAge(age:number){
        if(age <0 || age> 150){
          throw Error("Error age")
        }
        this._age = age
      }
    }
    let person = new Person(45, "Hào", "Phan")
    let checkAge = person.getAge()  // getter để lấy tuổi return 45
    person.setAge(25)  // setter thay đổi tuổi 
    console.log(person) // return {25, Hào, Phan}
    ```   


