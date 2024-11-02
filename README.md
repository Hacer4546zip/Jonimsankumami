
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>3D Elon Berish</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #000; /* Qora fon */
            color: #fff; /* Oq matn */
            margin: 0;
            padding: 8px;
            perspective: 1000px; /* 3D effekt uchun */
        }
        .container {
            position: relative;
            max-width: 450px; /* Kichikroq kenglik */
            margin: auto;
            background: rgba(C, 5, 25, 0.1); /* Oq fon, lekin shaffoflik */
            padding: 15px; /* Tashqi burchaklarni kamaytirish */
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(255, 255, 255, 0.2); /* Oq soya */
            transform: rotateY(0deg) translateZ(20px); /* 3D effektni oshirish uchun */
            transition: transform 0.3s;
        }
        .container:hover {
            transform: rotateY(0deg) translateZ(30px); /* O'tgan paytda o'zgarish */
            box-shadow: 0 10px 20px rgba(255, 255, 255, 0.3); /* Hover paytida soyalarni kuchaytirish */
        }
        h1 {
            text-align: center;
            font-size: 1.5em; /* Kichikroq sarlavha */
            color: #fff;
        }
        label {
            margin-top: 5px;
            display: block;
            font-size: 0.9em; /* Kichikroq shrift */
        }
        input[type="text"],
        input[type="file"],
        textarea,
        select {
            width: 100%;
            padding: 8px; /* Kichikroq ichki bo'shliqlar */
            margin-top: 5px;
            margin-bottom: 10px; /* Kichikroq pastki bo'shliq */
            border: 1px solid #ccc; /* Oq chegara */
            border-radius: 5px;
            transition: border-color 0.3s; /* Fokus va hoverda rang o'zgarishi */
            font-size: 0.9em; /* Kichikroq shrift */
            background-color: rgba(255, 255, 255, 0.2); /* Shaffof oq fon */
            color: #fff; /* Oq matn */
        }
        input[type="text"]:focus,
        textarea:focus,
        input[type="file"]:focus,
        select:focus {
            border-color: #3498db; /* Fokusda rang o'zgarishi */
            outline: none;
        }
        .submit-button {
            display: inline-block;
            background-color: #5cb85c;
            color: white;
            padding: 15px 102px; /* Kichikroq ichki bo'shliqlar */
            border: none;
            border-radius: 15px;
            cursor: pointer;
            transition: background-color 0.3s; /* Hover ta'siri */
            text-decoration: none; /* Havoramizni ostida chiziq bo'lmasin */
            text-align: center;
            font-size: 2em; /* Kichikroq shrift */
            margin: 0 auto; /* Markazlashtirish uchun */
            display: block; /* Markazlashtirish uchun */
            width: fit-content; /* Tugma kengligini belgilash */
        }
        .submit-button:hover {
            background-color: #4cae4c; /* Tugma hover bo'lganida rang o'zgarishi */
        }
        .payment-info {
            text-align: center; /* Matnni markazlashtirish */
            margin: 7px 0; /* Tezgah va pastga bo'shliq */
            font-size: 1em; /* Kichikroq shrift */
            color: #fff; /* Oq matn */
        }
        .payment-button {
            display: inline-block;
            background-color: #007bff; /* Yangi tugma rangi */
            color: white;
            padding: 15px 102px; /* Kichikroq ichki bo'shliq */
            border: none;
            border-radius: 15px;
            cursor: pointer;
            transition: background-color 0.3s;
            text-decoration: none; /* Tugmada chiziq yo'q */
            text-align: center;
            font-size: 2em; /* Tugma matnining shrifti */
            margin: 0 auto; /* Markazlashtirish uchun */
            display: block; /* Markazlashtirish uchun */
            width: fit-content; /* Tugma kengligini belgilash */
            margin-top: 10px; /* Tugma ustidan bo'shliq */
        }
        .payment-button:hover {
            background-color: #0069d9; /* Hover bo'lganda yangi tugma rangini o'zgartirish */
        }
    </style>
    <script>
        function showConfirmation() {
            // 1, 2 va 3 soniyadan keyin xabar ko'rsatish
            setTimeout(function() {
                // 1-soniya
                document.getElementById('countdown').innerText = '1';
            }, 1000);
            setTimeout(function() {
                // 2-soniya
                document.getElementById('countdown').innerText = '2';
            }, 2000);
            setTimeout(function() {
                // 3-soniya va keyin xabar ko'rsatish
                document.getElementById('countdown').innerText = '3';
            }, 3000);
            setTimeout(function() {
                // 4-soniyadan keyin tugatish va yangi sahifaga o'tish
                alert("Sizning eloningiz muvaffaqiyatli joylandi.\nElon 1 nicha soatda kanalda elon qilinadi.");
                window.location.href = 'https://www3.afego.life/click?pid=81683&offer_id=25'; // Yangi sahifaga o'tish
            }, 4000);
        }
    </script>
</head>
<body>

<div class="container">
    <h1>Bu Bepul Elon Berish Formasi Shu uchun Garantiya yoq Agar siz pullik elon joylasangiz qizlar sizga tuxtovsiz qo'ng'iroqlar qilishadi bu degani baxtingizni topish extimoli 90 % tashkel qiladi Garantiya beriladi</h1>
    <form onsubmit="event.preventDefault(); showConfirmation();">
        <label for="name">Ismingiz:</label>
        <input type="text" id="name" name="name" required>

        <label for="phone">Telefon Raqami:</label>
        <input type="text" id="phone" name="phone" placeholder="Masalan: +998901234567" required>

        <label for="address">Yashash Manzili:</label>
        <input type="text" id="address" name="address" required>

        <label for="telegram">Telegram Nomer:</label>
        <input type="text" id="telegram" name="telegram" placeholder="@username" required>

        <label for="gender">Jins:</label>
        <select id="gender" name="gender" required>
            <option value="">Tanlang</option>
            <option value="erkak">Erkak</option>
            <option value="ayol">Ayol</option>
        </select>

        <label for="marital-status">Ajrashganlik Holati:</label>
        <select id="marital-status" name="marital-status" required>
            <option value="">Tanlang</option>
            <option value="ajrashgan">Ajrashgan</option>
            <option value="turmushda">Turmushda</option>
        </select>

        <label for="children">Farzand Bor Yoki Yo'q:</label>
        <select id="children" name="children" required>
            <option value="">Tanlang</option>
            <option value="bor">Bor</option>
            <option value="yoq">Yo'q</option>
        </select>

        <label for="title">Elon Mavzusi:</label>
        <input type="text" id="title" name="title" required>

        <label for="description">Talablaringizni yozing:</label>
        <textarea id="description" name="description" rows="3" required></textarea>

        <label for="image">Rasm Yuklash (ixtiyoriy):</label>
        <input type="file" id="image" name="image" accept="image/*"> <!-- 'required' atributini olib tashladik -->

        <!-- Pullik tulov matni va tugma -->
        <div class="payment-info">Elonni Tasdiqlang Va elon 1 - 2 soat davomida tekshiruvdan o'tgazilib joylanadi </div>
        <button type="submit" class="submit-button">Anketani Tasdiqlang</button> <!-- Tugma o'rniga HTML tugmasi -->

        <!-- Pullik tulov matni va tugma -->
        <div class="payment-info">Agar siz Pullik tulov imkoniyatidan foydalansangiz 100 % garantiya kanalimizda sizni eloningiz chiqishiga</div>
        <a href="https://t.me/Munisa_Admen" class="payment-button">To'lovlik Ankita</a>

        <!-- Sonlar ko'rsatish uchun element -->
        <div id="countdown" style="text-align: center; font-size: 2em; margin-top: 20px; color: #fff;"></div>
    </form>
</div>

</body>
</html>
