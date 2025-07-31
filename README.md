# Shadatak-Alina
Order PUBG UC via Bank of Khartoum
<!DOCTYPE html><html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Shadatad Alina - شحن شدات ببجي</title>
  <style>
    body {
      font-family: sans-serif;
      background: #f4f4f4;
      margin: 0;
      padding: 0;
    }
    .container {
      max-width: 500px;
      margin: 50px auto;
      background: white;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    h1 {
      text-align: center;
      color: #333;
    }
    label {
      display: block;
      margin: 10px 0 5px;
    }
    input, select, textarea, button {
      width: 100%;
      padding: 10px;
      margin-bottom: 15px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    button {
      background: #28a745;
      color: white;
      cursor: pointer;
    }
    .hidden {
      display: none;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>شحن شدات ببجي</h1>
    <form id="step1">
      <label>الاسم داخل اللعبة</label>
      <input type="text" required />
      <label>رقم الواتساب</label>
      <input type="text" required />
      <label>ID ببجي</label>
      <input type="text" required />
      <button type="submit">إرسال البيانات</button>
    </form><form id="step2" class="hidden">
  <p>تم إرسال البيانات، الرجاء انتظار التأكيد...</p>
</form>

<form id="step3" class="hidden">
  <label>اختر كمية الشدات</label>
  <select>
    <option value="60">60 شدة</option>
    <option value="180">180 شدة</option>
    <option value="325">325 شدة</option>
  </select>
  <button type="submit">التالي</button>
</form>

<form id="step4" class="hidden">
  <p>الرجاء تحويل المبلغ إلى:</p>
  <p><strong>بنك الخرطوم</strong></p>
  <p>الاسم: محمد أحمد</p>
  <p>رقم الحساب: 123456789</p>
  <label>أرفق إشعار التحويل (صورة)</label>
  <input type="file" accept="image/*" required />
  <button type="submit">رفع الإشعار</button>
</form>

<form id="step5" class="hidden">
  <label>كيف تفضل استلام الشحن؟</label>
  <select>
    <option value="codes">أريد الأكواد</option>
    <option value="direct">أريد أن يتم الشحن لي</option>
  </select>
  <button type="submit">تأكيد</button>
</form>

<div id="step6" class="hidden">
  <p>شكراً لك! سيتم معالجة طلبك...</p>
</div>

  </div>  <script>
    const steps = [
      document.getElementById('step1'),
      document.getElementById('step2'),
      document.getElementById('step3'),
      document.getElementById('step4'),
      document.getElementById('step5'),
      document.getElementById('step6')
    ];

    let currentStep = 0;

    steps[currentStep].addEventListener('submit', function(e) {
      e.preventDefault();
      steps[currentStep].classList.add('hidden');
      currentStep++;
      steps[currentStep].classList.remove('hidden');
      if(currentStep === 1) {
        setTimeout(() => {
          steps[currentStep].classList.add('hidden');
          currentStep++;
          steps[currentStep].classList.remove('hidden');
        }, 2000);
      }
    });

    for (let i = 2; i < 5; i++) {
      steps[i].addEventListener('submit', function(e) {
        e.preventDefault();
        steps[i].classList.add('hidden');
        steps[i + 1].classList.remove('hidden');
      });
    }
  </script></body>
</html>
