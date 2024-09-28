<html lang="en-US">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Xây dựng trang web thực hiện công việc sau</title>
<script>
    function Tinhtongtu1denN() {
        const n = parseInt(document.getElementById('number1').value, 10);
        let sum = 0;
        for (let i = 1; i <= n; i++) {
            sum += i;
        }
        document.getElementById('result1').textContent = `Tổng từ 1 đến ${n} là: ${sum}`;
    }

    function TinhtongsochandenN() {
        const n = parseInt(document.getElementById('number2').value, 10);
        let sum = 0;
        for (let i = 2; i <= n; i += 2) {
            sum += i;
        }
        document.getElementById('result2').textContent = `Tổng các số chẵn từ 1 đến ${n} là: ${sum}`;
    }   
    function TinhtongsoledenN() {
            const n = parseInt(document.getElementById('number3').value, 10);
            let sum = 0;
            for (let i = 1; i <= n; i += 2) {
                sum += i;
            }
            document.getElementById('result3').textContent = `Tổng các số lẻ từ 1 đến ${n} là: ${sum}`;
        }
    function Kiemtrasonguyento() {
            const n = parseInt(document.getElementById('number4').value, 10);
            let isPrime = true;

            if (n <= 1) {
                isPrime = false;
            } else {
                for (let i = 2; i <= Math.sqrt(n); i++) {
                    if (n % i === 0) {
                        isPrime = false;
                        break;
                    }
                }
            }

            if (isPrime) {
                document.getElementById('result4').textContent = `${n} là số nguyên tố.`;
            } else {
                document.getElementById('result4').textContent = `${n} không phải là số nguyên tố.`;
            }
        }
        function Timuocchung() {
            const a = parseInt(document.getElementById('number5').value, 10);
            const b = parseInt(document.getElementById('number6').value, 10);

            let gcd = calculateGCD(a, b);

            document.getElementById('result5').textContent = `UCLN của ${a} và ${b} là: ${gcd}`;
        }

        function calculateGCD(x, y) {
            while (y) {
                let t = y;
                y = x % y;
                x = t;
            }
            return Math.abs(x);
        }
</script>
</head>
<body>

    <h1>Tính tổng từ 1 đến n</h1>
    <label for="number1">Nhập giá trị của n: </label>
    <input type="number" id="number1">
    <button onclick="Tinhtongtu1denN()">Tính tổng</button>
    <p id="result1"></p>
    
    <h1>Tính tổng các số chẵn từ 1 đến n</h1>
    <label for="number2">Nhập giá trị của n: </label>
    <input type="number" id="number2">
    <button onclick="TinhtongsochandenN()">Tính tổng</button>
    <p id="result2"></p>

    <h1>Tính tổng các số lẻ đến n</h1>
    <label for="number3">Nhập giá trị của n: </label>
    <input type="number" id="number3">
    <button onclick="TinhtongsoledenN()">Tính tổng</button>
    <p id="result3"></p>

    <h1>Kiểm tra số nguyên tố</h1>
    <label for="number4">Nhập số n: </label>
    <input type="number" id="number4">
    <button onclick="Kiemtrasonguyento()">Kiểm tra</button>
    <p id="result4"></p>

    <h1>Tìm UCLN của 2 số</h1>
    <label for="number5">Nhập số thứ nhất (a): </label>
    <input type="number" id="number5">
    <label for="number6">Nhập số thứ hai (b): </label>
    <input type="number" id="number6">
    <button onclick="Timuocchung()">Tìm UCLN</button>
    <p id="result5"></p>
</body>
</html>
