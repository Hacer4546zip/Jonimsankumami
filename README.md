<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tasodifiy E'lonlar</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: url('https://img1.akspic.ru/attachments/crops/5/2/2/9/6/169225/169225-atmosfera-geometriya-krasochnost-svet-purpur-1440x2560.jpg') no-repeat center center fixed;
            background-size: cover;
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            overflow: hidden;
        }
        .container {
            position: relative;
            width: 90%;
            max-width: 400px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        .profile-container {
            background-color: rgba(0,0,0,0.285);
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            transition: transform 0.5s ease, opacity 0.5s ease; /* Yangi */
            width: 100%;
            opacity: 1; /* Yangi */
        }
        .profile-image img {
            width: 100%;
            border-radius: 15px;
        }
        .details {
            margin-top: 20px;
            text-align: left;
            font-size: 18px;
            line-height: 1.8;
        }
        .button {
            margin-top: 20px;
            text-align: center;
        }
        .button a {
            display: inline-block;
            padding: 15px 25px;
            background-color: red;
            color: white;
            font-size: 18px;
            font-weight: bold;
            text-decoration: none;
            border-radius: 10px;
        }
        .button a:hover {
            background-color: darkred;
        }
        .announcement {
            position: absolute;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            background-color: rgba(0,0,0,0.214);
            padding: 10px;
            border-radius: 10px;
            display: none;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="announcement" id="announcement"></div>
        <div class="profile-container" id="profileContainer">
            <script>
                // Tasodifiy kontentni tanlash
                const profiles = [
                    `
                    <div class="profile-image">
                        <img src="https://cdn5-images.motherlessmedia.com/images/A7C54C5.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>salom men 2005 yil qiz bola man turmushga chiqish uchun elon bergan man kuyovni manzilini farqi bor shu buxorolik bulsin eltimos</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://ggirls.cc/wp-content/uploads/2021/01/3577-1.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>men 2004 yil ajrashgan man</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://i.pinimg.com/originals/29/07/a6/2907a62546ac0a944c050daaf89c8308.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>салом мен делрабо 1998 йил ажрашганаёл ман турмушга чикмокчиман киз бола ман майли ажрашишган буса хам тегишга рози ман менга ёзинг танишамиз кунгимдаги инсонимни излаябман</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://64.media.tumblr.com/f68b065f7fac80f4eb7fc69cfcf0475c/tumblr_ppy2000qo01urdzu3_1280.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>салом мени исмим ойгул 1997 йил ман турмушдан ажрашишганман 1 нафар кизим бор 4 ёшда хакикий бахтимни излаябман яшаш манзилим сир дарё</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://i.pinimg.com/736x/29/c3/80/29c380611f5b9cc83bf8408c3f513416.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Мадина исмим 1992 йил ман магазинда ишлайман 2 та углим бор турмушга чиқмаган бахтимни кидириб элон жойладим муносиб куёв буса манга ёзинг ман термиз шахридан ман </p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://thumb-p6.xhcdn.com/a/cfpgDZnpUHjtaHvWVJIhyw/000/409/147/826_1000.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Исмим Латофат 1984 йил ман ажрашган Фарзандим ю ёлгиз яшайман эрим вафот этган менга ички кёв кирак ёш чигараси 28 40 ёшгача бусин</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://pbs.twimg.com/media/DbvJD3PXcAEUPd9.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>2001 йил ман киз бола ман турмушга чикмаган ман узим 5 махал номоз укийман турмушга чикиш учун элон бердим</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://i.pinimg.com/736x/5d/6c/4c/5d6c4c4613578b6a2ab67fac41385b80.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Oila qurmoqchiman ismim Gulhayo navoi viloyatidan man 2006 yil man aldangan man turisi man xaqiqatni sevaman yashiradigon serim yoq oila qurmoqchiman kim mani borimcha qabul qilsa manga yozing yoki telefon qiling manga tushuntiraman</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://i.pinimg.com/736x/69/e9/23/69e92388b6aa2bcfca01960bc998d6ff.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Salom man Nelufar 2 marta turmushim o'xshamadi shu sababli ajrashgan man farzandim bor 3 yoshda o'g'lim oila qurmoqchiman to'liq malumotni telegramda yoki manga telefon qiling agar imkoniz bulsa hozir</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://i.pinimg.com/originals/39/77/7f/39777fc4753d8abe8cc9cd911d575173.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Man baxtimni izlayab man 2004 yil man qiz bola man oila qurushni istayman vaxtiz bormi manga sms yozing gaplashamiz yoki telegramimga yozvoring</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://i.pinimg.com/originals/cc/ec/13/ccec13d370d555afa937e6fd1ab06ab3.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Salom Man Bonu 2005 yil ajrashganman 1 yoshli qizim bor erim.bilan kelishmay qoldim 2 oy yashab ajrashganman baxtimni islab elon beryab man eltimos yaxshi odamlar manga yozsin bekorchilar yozmaylar</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://thumb-p3.xhcdn.com/a/swp6gkwdiGUWTBq84OOyZQ/000/239/372/033_1000.jpg"Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Ismim Anora 1997 yil man vaznim 50 kg erga tegaman o'zim ajrashgan man ko'p yashamagan man erim bilan yaxshi kuyov topilsa turmushga chiqardim</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://thumb-p7.xhcdn.com/a/QJtzSHZ9NcCZxMkOE6AhFA/000/410/707/107_1000.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Salom man 18 yosh man Aldangan man qiz bola mas man shuni bila turub manga uylanishga tayor insonni izlayab man agar shunday nomzod bu elonimni o'qib qolsa manga yozing yoki telefon qiling</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://thumb-p5.xhcdn.com/a/TnvvzXSB-T71vw-swkwt7w/000/068/418/045_1000.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Мен 1995 йил бева аел ман 1 кизим бор 12 ёш мен ойла курмокчиман куёга талабим ёк куёв кайда буса бирга уща жойда бир умур яшашга таёр ман манга ёзишингизни интизорлик билан кутуб коламан</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://d18fr84zq3fgpm.cloudfront.net/jiya-indian-girl-indian-escort-in-dubai-2937224_original.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Менга Бирга яшашга эр кирак хамма шароетим бор мани узим ёлгиз яшайман уй бор машинам бор спарк</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://thumb-p7.xhcdn.com/a/9VoYXq4m-1xyqN1Pio1PMQ/000/278/402/227_1000.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Бирга яшаб йуруш учун яхши кучкор кирак манга ёшим 26 да озгин ким эмас ман бекорга кизикишга ёзманг</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://thumb-p1.xhcdn.com/a/RH-ZbiFoJRGOa7C5kim6QQ/000/353/607/021_1000.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Манга яхши секс киладигон эр кирак излаб йуриб ман пули хам булиши керак чунки мани расходим бор ижарада яшайман</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://thumb-p9.xhcdn.com/a/hi5YpJgcduZ5e5Th6ig--g/000/353/607/009_1000.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Сексга кизикадигон борми манга шунака эркак кирак жуда коп сексга кизикаман ёши кичикрок булишини хохлайман хар замонда чакираман уйим бор тенч жой</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://thumb-p3.xhcdn.com/a/3ln_yU3zx1iodlsm1L5E3g/000/353/607/103_1000.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Салом манга хам яхши секс киладигон эркак кирак ёшини фарки ю эркакни уйи бусин манга махтончок пули борла ёкмайди опитни эркак кирак</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://thumb-p4.xhcdn.com/a/UoJ2q-T5ewU09XzdMk75zQ/000/278/295/764_1000.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Салом манга секс учун 23 30 ёшли йигит кирак ман сексга кизикаман реални пул сурамайман шунчаки уз хохишларимни кондириш учун керак 💜</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://thumb-p8.xhcdn.com/a/b-7jxq9gOoNbECLDOxhmeA/000/278/296/108_1000.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Salom man 20 yosh man qiz bola emas man seksga qiziqadigon suxbatdosh qidiryab man uzimga opitni kelishgan o'zoq sekadigon yegit izlayab man joy busa chaqirsa boraman buyim 170 vaznim 50 kg</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://thumb-p9.xhcdn.com/a/rP9r6HpM3lKA8knCV2wWCg/000/409/147/939_1000.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Tanishgani yegit izlayab man turisini aytadigon bulsam manga seksga qiziquvchan yegit kerak yosh busin uzimga uxshagan yashash manzilin Andijonlik man</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://thumb-p7.xhcdn.com/a/MNDD2jL6I2SGA8fUm_kxyQ/000/427/556/827_1000.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Manashu yotgan qiz o'zimni rasmim manga yegit kerak sekishadigon realni joyi bo'lishi shart boraman birga yashaymiz judayam seksni hohlayman jalab foxshaga teng qiluvchilar yozmasin silarga pashol naxxuy yoq bulib qollaring manga realni kerak</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://pbs.twimg.com/media/EMzz-BPW4AAFnno.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Realni Ko'rishaman joyim yoq yoshim 19 da ko'rishib gapashamiz buyerda ko'p gapirgandan foydasi yoq jonkalarim sizlarni real hayotda ko'tub qolaman</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://pbs.twimg.com/media/ENXOL6-XYAAYRAp.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Jonim ismim Diana metiska man 18 plusga qiziqaman manday qiziqadigon bormi mani telegramimga yozing tanishamiz agar yoqib qolsangiz realni siz bilan ko'rishib gaplashaman</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://pbs.twimg.com/media/FY5eoMmWQAEo5X2.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Manga real gaplashadigon kerak uyim bor xar kelganda uyimga tulib toshib kelishi shart yosh bolam bor 2 xonalik uyda turaman manzilib jizzax shaxarni ichida domda yashayman uyim sharoiti yaxshi chumilishga sharoit bor</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://thumb-p3.xhcdn.com/a/U_KecleAIPV-nHQWyt8VCg/000/164/341/833_1000.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Салом 35 ёш ман оела курушга эркак излаябман манга алокага чикинг ман сиз билан гаплашиб куришни истайман</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://jjgirls.com/filipinofuck/christine/hot-christine-spreads-her-legs-and-exposes-her-pussy/000001l.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Salom Madina man 19 yosh sekis haqida gaplashadigon odam kerak faqat telegramda real yoq real deb yozmayla bazi qizlarga uxshab karta bermayman manga yozing tanishaman</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://thumb-p8.xhcdn.com/a/rhkXi288Z1_jy7K_eV7t_g/000/269/617/238_1000.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Salom Mani Ota onam oq qilib yuborgan mani borimcha qabul qilib mani hurmat qiladigon odam kirak oldiga chaqirsa boraman agar chit davlatda busa man rozi man siz bilan birga yashashga boriga qonoat qilib yashashga rozi man juda zerikib kittim hayotimdan kim mani elonimni tug'ri tushunadi bilmadim yaxshi maxsadda elon berdim baxtli yashaga haqqim bor mani</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://thumb-p1.xhcdn.com/a/-BAY1EFhQCtk_OtuBj9Kzg/000/379/012/701_1000.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Salom man Germaniyada ishlayman manga bitta uziga ishongan uzini bosib olgan 23 30 yoshli yegit kerak mayli ajrashgan busa ham rozi man oldimga chaqiraman belitga pul junataman mani oldimga kelib birga ishlashi kerak ishlab topgan pulimizga uy olamiz sharoitni qilamiz agar sizdan homlodor bulsam siz bilan butun umrumni utgazishga rozi man</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://i.pinimg.com/736x/b7/d5/c9/b7d5c94ecf3c7933bafb9c8166c2b7c2.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Салом мени исмим Ойша 1987 йил ман манга секс кирак 65 70 ёшли эркак билан танишаман реални танишаман расмдаги узимни расмим кук плафка кук безгалтирда ман яшаш манзилим Кукон узимни уйим бор олдин гаплашиб курайлик макул килсангиз уйга чакираман</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://thumb-p6.xhcdn.com/a/UY3Ox5y3YWsTHKZcN6tqJA/000/365/741/906_1000.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Салом манга асьоби котта бола кирак миллатим рус мени шу узимни расмим кора ливчик такиб олган ман буйнимда кристик бор манга ёзинг танишаман ёшим 20 да</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://i.imgur.com/pTADAzQ.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Салом асалим бу мени расмим кук левчик кизил трускада ман манга реални асьоби котта болла ёкади телеграмдан манга ёзинг асбобингиз ничи см аник расмга тушуриб жунатинг ёкиб колса куришаман жой бор манда тошкент сергилида манзилим</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://img1.wlresources.com/photo/14728566/gallery/NatyMiss-sex-cam-live-show-22-1894722.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Салом мен розивий кофта кийган киз ман 21 ёш ажрашган ман эрга тегиш учун элон бердим куёв номзодни ёши 33 ёшгача ёзиши мумкун яшаш манзилини кизиги ю</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://static-ca-cdn.eporner.com/gallery/iI/6E/36VbEfb6EiI/451981-posing.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Salom men Shamg'i rangl va oq burukdagi qiz man shu o'zimni rasmim yoshim 23 yosh ajrashgan man 1 ta o'g'lim bor samarqanda shaxrida yashayman baxtimni izlayab man millatim tojik🫡</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://i.pinimg.com/originals/0a/13/d8/0a13d83e33d83e66160faa4d3bb30723.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Salom sochi buynidan qirqilgan qiz man yoshim 21 da ajrashgan man buxoro viloyatidan man erim afto xalokatda vafot qilgan man baxtimni qidirib elon berdim 👋</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://i.pinimg.com/736x/54/b7/c7/54b7c7a13275225e4b83080ca016edf2.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Erga tegaman yoshim 22 da ajrashgan man 1 o'g'ilim bor o'g'lim bilan ijarada yashayman ota onam yoq mani yolgiz man yaxshi yegit busa 2 chi ruzg'orlikka tegardim sharoitimni qilib bersin tegaman</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://i.pinimg.com/736x/cf/12/cb/cf12cbfa5c6702d2f2b50f691b643a32.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Salom man toshkentda ishlayman ismim Munira 20 yosh man aldanib qolgan man erga tegmoqchiman mani rasmim o'zimniki ko'rishib hammasini gaplashmoqchiman agar sizga maqul kelsam manga yozing yoki tel qiling vaziyatga qarab ko'rishamiz</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgFlzjnkbUt3RioAPA8FZxcd1PuI4CJjiRzuF2AFaxTEPzKwOHqnTgL-ds4YLhmO6CKz2PQ6pP9b2Ju8JWkBj2LAC0t_CzI32yzaEvIHrueIzYos4EEkN-mheGSNv23VxIE5SHzOrQaGmY/s1600/IMG_20161016_095443.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Salom man 17 yosh man erga tegaman kim mani yana 1 yil ko'ta olsa 1 yilgacha gaplashib yurmoqchiman ota onam rozi mayli didila 20 28 yoshli yegit yozsa tanishaman telfon raqamimni telegramimda beraman</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://i.pinimg.com/736x/c5/7f/c0/c57fc08f06e82ce30762bbd7e616578f.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>16 Yosh man tanishaman xaqiqiy sevgimni izlab elon berdim</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://pbs.twimg.com/media/CpMiQFWVIAAWp4m.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Salom ismim sevara 19 yosh man erga tegaman aldanib qolgan man tuy qilib uylanasiz manga manzilim Namangan shaxar</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://pbs.twimg.com/media/FjlUgc4UAAAVM3i.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>ismim Muhlisabonu yoshim 18 da aldangan man tuy qilib manga uylanishga rozi yegit izlayab man</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://pbs.twimg.com/media/CxQFIw9UAAAFa_Y.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>Ismim Hilola millatim Kozoq 21 yosh man aldangan qiz man tanishishni hohlayab man</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://thumb-p2.xhcdn.com/a/Z2ODi06g0_FnfMit_uwG4A/000/098/512/912_1000.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>❤️ Manga Seksga qiziquvchi yegit kirak homlador man judayam seks hohlayab man yegitim tashab kitgan mani telegramda bushanaman yoqib qolsa usha yegit ko'rishaman aniq man bazi erkaklardan ko'ra mart man</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://d18fr84zq3fgpm.cloudfront.net/tania-indian-escort-in-dubai-3057238_original.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>1. Ёши: 2006
2. Миллати: Узбек 
3. Турмушдаги холати: Qiz bola 
4. Фарзанди: Йук 
5. Маълумоти: Урта 
6. Иш жойи: Узига айтилади 
7. Ёш чегараси: 31
9. Соґлиги: Соглом 
10. Характери: Яхши 
11. Ку‌риниши: Яхши 
12. Ку‌шимча маьлумот: Ozini fikriga ega bolsin ichmasa chekmasa Ollohga ishonsa Andijon shahridan bolsin</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://thumb-p9.xhcdn.com/a/WbBGHKcHQF8dROevcjPr0g/000/340/311/409_1000.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>1. Ёши: 20
2. Миллати: Узбек 
3. Турмушдаги холати: Ажрашган 
4. Фарзанди: Бор 1 угил 
5. Маълумоти: Урта 
6. Иш жойи: Уй бекаси 
7. Ёш чегараси: 29/30
9. Соґлиги: Соглом 
10. Характери: Яхши 
11. Ку‌риниши: Яхши 
12. Ку‌шимча маьлумот: нияти жиддийлар ёзсин факат фаргоналилар ёзсин тулик малумот ва расм билан ёзин.

13. Яшаш жойи: #Фаргона шахар</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://thumb-p7.xhcdn.com/a/I3B1x8hqCDA_JP4_rt6b5w/000/321/039/807_1000.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>1. Ёши: 20
2. Миллати: Узбек 
3. Турмушдаги холати: Ажрашган 
4. Фарзанди: Бор 
5. Маълумоти: Узига айтилади 
6. Иш жойи: Узига айтилади 
7. Ёш чегараси: 29/34
9. Соґлиги: Соглом 
10. Характери: Яхши 
11. Ку‌риниши: Яхши</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://thumb-p3.xhcdn.com/a/RvjZKnKG-z7-qx7DabVjIA/000/434/903/613_1000.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>эрга тегаман 30 еш ман</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://thumb-p7.xhcdn.com/a/xLXpH1mnkuM8cwiSyx4M8w/000/156/413/907_1000.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>1. Ёши: 20
2. Миллати: узбек
3. Турмушдаги холати: ажрашган
4. Фарзанди: 1та
5. Маълумоти: олий
6. Иш жойи: .
7. Ёш чегараси: 25-35
9. Соґлиги: яхши
10. Характери: яхши
11. Ку‌риниши: яхши
12. Ку‌шимча маьлумот: узига айтилади
13. Яшаш жойи: фаргона</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://thumb-p9.xhcdn.com/a/YQ-CKeaUgjS-oex6xn-kCg/000/311/088/379_1000.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>1. Ёши: 21
2. Миллати: Узбек 
3. Турмушдаги холати: Ажрашган 
4. Фарзанди: Бор 
5. Маълумоти: Урта 
6. Иш жойи: Уй бекаси 
7. Ёш чегараси: 25/32
9. Соґлиги: Соглом </p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `,
                    `
                    <div class="profile-image">
                        <img src="https://1.bp.blogspot.com/-VOUzxs0MDtk/XR4DOTGiylI/AAAAAAAAQhw/QyRlV6m-SDQgV_m26PnaFSxaTyBro7WMQCLcBGAs/s1600/www.femalemms.com++%287%29.jpg" alt="Profil rasmi">
                    </div>
                    <div class="details">
                        <p>🔚 Кизлар Коп Жуда 🔜</p>
                        <p>💜1. Ёши: 20
2. Миллати: Метиска дадамла узбек ойим Арман 
3. Турмушдаги холати: ажрашган
4. Фарзанди: йок
5. Маълумоти: урта
6. Иш жойи: уй бекаси
7. Ёш чегараси: 40 йошгача
8. Яшаш жойи: #Москвада🇷🇺 онажоним акам блан</p>
                    </div>
                    <div class="button">
                        <a href="https://www1.affhone.fyi/click?pid=81683&offer_id=25" target="_blank">Send Messages</a>
                    </div>
                    `
                ];

                let currentProfileIndex = Math.floor(Math.random() * profiles.length);
                document.getElementById("profileContainer").innerHTML = profiles[currentProfileIndex];

                const announcements = [
                    "Бугун катта чора танлашни унутманг!",
                    "Янги туғилган сўзларни кутинг!",
                    "Эшитдингизми? Янги мосламалар кутмоқда!",
                    "Ката узадиган билдиришлар кутинг!",
                    "Янги сессияни почтага ёзинг!"
                ];

                function showAnnouncement(text) {
                    const announcementElement = document.querySelector('.announcement');
                    announcementElement.textContent = text;
                    announcementElement.style.display = "block";
                    setTimeout(() => {
                        announcementElement.style.display = "none";
                    }, 5000);
                }

                function updateProfile() {
                    const profileContainer = document.getElementById("profileContainer");
                    profileContainer.style.opacity = "0"; // Kichrayib boradi
                    setTimeout(() => {
                        currentProfileIndex = Math.floor(Math.random() * profiles.length);
                        profileContainer.innerHTML = profiles[currentProfileIndex];
                        showAnnouncement(announcements[Math.floor(Math.random() * announcements.length)]);
                        profileContainer.style.opacity = "1"; // Qaytadan ko'rsatish
                    }, 500); // 0.5 soniya
                }

                function moveProfile(direction) {
                    const profileContainer = document.getElementById("profileContainer");
                    let translateX = 0;
                    let translateY = 0;

                    switch(direction) {
                        case 'left':
                            translateX = -100;
                            break;
                        case 'right':
                            translateX = 100;
                            break;
                        case 'up':
                            translateY = -100;
                            break;
                        case 'down':
                            translateY = 100;
                            break;
                    }

                    profileContainer.style.transform = `translate(${translateX}%, ${translateY}%)`;
                    profileContainer.style.opacity = "0"; // Kichrayib boradi
                    setTimeout(() => {
                        updateProfile(); // Profilni yangilash
                        profileContainer.style.transform = "translate(0%, 0%)"; // Qayta o'z o'rniga qaytarish
                        profileContainer.style.opacity = "1"; // Qaytadan ko'rsatish
                    }, 500); // 0.5 soniya
                }

                // Klavishlarni boshqarish
                document.addEventListener('keydown', (event) => {
                    if (event.key === 'ArrowLeft') {
                        moveProfile('left');
                    } else if (event.key === 'ArrowRight') {
                        moveProfile('right');
                    } else if (event.key === 'ArrowUp') {
                        moveProfile('up');
                    } else if (event.key === 'ArrowDown') {
                        moveProfile('down');
                    }
                });

                // Touch hodisalarini boshqarish
                let startY; // Boshlang'ich Y nuqtasi
                let endY; // Tugash Y nuqtasi
                let startX; // Boshlang'ich X nuqtasi
                let endX; // Tugash X nuqtasi

                document.addEventListener('touchstart', (event) => {
                    startY = event.touches[0].clientY; // Boshlanish nuqtasi
                    startX = event.touches[0].clientX; // Boshlanish nuqtasi
                });

                document.addEventListener('touchmove', (event) => {
                    endY = event.touches[0].clientY; // Harakat paytida nuqtani yangilash
                    endX = event.touches[0].clientX; // Harakat paytida nuqtani yangilash
                });

                document.addEventListener('touchend', () => {
                    if (Math.abs(endY - startY) > 50) { // Pastga yoki yuqoriga siljish
                        if (endY > startY) {
                            moveProfile('down'); // Pastga
                        } else {
                            moveProfile('up'); // Yuqoriga
                        }
                    } else if (Math.abs(endX - startX) > 50) { // Chapga yoki o'ngga siljish
                        if (endX > startX) {
                            moveProfile('right'); // O'ngga
                        } else {
                            moveProfile('left'); // Chapga
                        }
                    }
                });

            </script>
        </div>
    </div>
</body>
</html>
