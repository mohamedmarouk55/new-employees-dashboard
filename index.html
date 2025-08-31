<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>تحليل ادارات الرياض</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * { box-sizing: border-box; margin:0; padding:0; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; }
        body { background-color: #f5f7fa; color:#333; line-height:1.6; }
        .container { max-width:1400px; margin:20px auto; padding:20px; }
        header { background: linear-gradient(135deg,#1e3c72 0%,#2a5298 100%); color:white; padding:25px 0; text-align:center; border-radius:10px; margin-bottom:20px; box-shadow:0 4px 15px rgba(0,0,0,.1); }
        header h1{ font-size:2rem; margin-bottom:6px }
        header p{ opacity:.9 }
        .controls { display:flex; justify-content:space-between; gap:15px; flex-wrap:wrap; background:white; padding:16px; border-radius:10px; box-shadow:0 4px 10px rgba(0,0,0,.05); margin-bottom:18px }
        .search-box { flex:1; min-width:280px; position:relative }
        .search-box input { width:100%; padding:12px 44px 12px 18px; border-radius:50px; border:1px solid #ddd; font-size:15px; outline:none; }
        .search-box i { position:absolute; right:16px; top:50%; transform:translateY(-50%); color:#777 }
        .filter-section { display:flex; gap:10px; align-items:center; flex-wrap:wrap }
        .filter-section select { padding:10px 12px; border-radius:8px; border:1px solid #ddd; background:white; min-width:180px; }
        .stats { display:flex; gap:16px; margin-bottom:18px; flex-wrap:wrap }
        .stat-card { background:white; padding:16px; border-radius:10px; min-width:180px; box-shadow:0 4px 10px rgba(0,0,0,.04); text-align:center }
        .stat-card h3{ font-size:13px; color:#666; margin-bottom:8px }
        .stat-card .value{ font-size:20px; color:#1e3c72; font-weight:700 }
        .department-tabs { display:flex; gap:8px; margin-bottom:12px; flex-wrap:wrap }
        .department-tab{ padding:8px 14px; background:white; border-radius:8px; border:1px solid #ddd; cursor:pointer }
        .department-tab.active{ background:#1e3c72; color:white; border-color:#1e3c72 }
        .table-container { overflow:auto; background:white; border-radius:10px; padding:8px; box-shadow:0 4px 10px rgba(0,0,0,.04); max-height:650px }
        table{ width:100%; border-collapse:collapse; min-width:1000px }
        th, td{ padding:12px 14px; text-align:right; border-bottom:1px solid #eee; font-size:14px }
        th{ background:#f8fafd; color:#1e3c72; position:sticky; top:0; z-index:2 }
        tr:hover{ background:#f9fbfd }
        .salary { font-weight:700; color:#2a5298 }
        .vacation-days { display:inline-block; padding:6px 10px; border-radius:18px; font-weight:600 }
        .vacation-days.low { background:#ffe6e6; color:#d33 }
        .vacation-days.medium { background:#fff8e6; color:#d98b00 }
        .vacation-days.high { background:#e6f7ee; color:#07944b }
        .no-results { padding:30px; text-align:center; color:#777 }
        footer{ text-align:center; margin-top:18px; color:#666; padding:12px }
        @media (max-width:768px){ .controls{flex-direction:column} .department-tabs{overflow:auto} }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1><i class="fas fa-users-cog"></i> تحليل ادارات الرياض </h1>
            <p></p>
        </header>

        <div class="controls">
            <div class="search-box">
                <input id="searchInput" placeholder="ابحث باسم الموظف أو المسمى أو القسم...">
                <i class="fas fa-search"></i>
            </div>
            <div class="filter-section">
                <select id="departmentFilter">
                    <option value="all">جميع الأقسام</option>
                    <option value="الادارة التنفيذية">الادارة التنفيذية - الرياض</option>
                    <option value="الإدارة المالية">الإدارة المالية - الرياض</option>
                    <option value="قسم المشتريات">قسم المشتريات – الرياض</option>
                    <option value="تقنية المعلومات">الإدارة تقنية المعلومات - الرياض</option>
                    <option value="الادارة القانونية">الادارة القانونية - الرياض</option>
                    <option value="ادارة المراجعة">ادارة المراجعة - الرياض</option>
                    <option value="الموارد البشرية">الإدارة الموارد البشرية - الرياض</option>
                    <option value="المستودعات">إدارة المستودعات و الخدمات اللوجستية - الرياض</option>
                    <option value="المبيعات">الإدارة العامة - إدارة المبيعات</option>
                    <option value="الخدمات">قسم الخدمات - الرياض</option>
                </select>

                <select id="sortBy">
                    <option value="name">ترتيب بالأسم</option>
                    <option value="salary">ترتيب بالراتب (من الأعلى)</option>
                    <option value="salary-asc">ترتيب بالراتب (من الأقل)</option>
                    <option value="joinDate">ترتيب بتاريخ الانضمام (الأحدث)</option>
                    <option value="joinDate-asc">ترتيب بتاريخ الانضمام (الأقدم)</option>
                </select>
            </div>
        </div>

        <div class="stats">
            <div class="stat-card"><h3>إجمالي الموظفين</h3><div class="value" id="totalEmployees">0</div></div>
            <div class="stat-card"><h3>متوسط الراتب</h3><div class="value" id="avgSalary">0 ر.س</div></div>
            <div class="stat-card"><h3>أعلى راتب</h3><div class="value" id="maxSalary">0 ر.س</div></div>
            <div class="stat-card"><h3>أقل راتب</h3><div class="value" id="minSalary">0 ر.س</div></div>
        </div>

        <div class="department-tabs" id="deptTabs">
            <div class="department-tab active" data-dept="all">جميع الأقسام</div>
            <div class="department-tab" data-dept="الادارة التنفيذية">الادارة التنفيذية</div>
            <div class="department-tab" data-dept="الإدارة المالية">المالية</div>
            <div class="department-tab" data-dept="قسم المشتريات">المشتريات</div>
            <div class="department-tab" data-dept="تقنية المعلومات">تقنية المعلومات</div>
            <div class="department-tab" data-dept="الادارة القانونية">القانونية</div>
            <div class="department-tab" data-dept="ادارة المراجعة">المراجعة</div>
            <div class="department-tab" data-dept="الموارد البشرية">الموارد البشرية</div>
            <div class="department-tab" data-dept="المستودعات">المستودعات</div>
            <div class="department-tab" data-dept="المبيعات">المبيعات</div>
            <div class="department-tab" data-dept="الخدمات">الخدمات</div>
        </div>

        <div class="table-container">
            <table id="employeesTable">
                <thead>
                    <tr>
                        <th>الرقم الوظيفي</th>
                        <th>الاسم الكامل</th>
                        <th>المسمى الوظيفي</th>
                        <th>القسم</th>
                        <th>تاريخ الالتحاق</th>
                        <th>تاريخ نهاية العقد</th>
                        <th>رصيد الإجازات</th>
                        <th>الراتب الأساسي</th>
                        <th>كامل الراتب</th>
                    </tr>
                </thead>
                <tbody id="tableBody"></tbody>
            </table>
        </div>

    </div>

<script>
// --- بيانات الموظفين (مأخوذة من الجدول الذي زودتني به) ---
const employees = [
  {id:30107,name:"تركي خالد عبدالعزيز النفيسه",position:"مشرف الشؤون الادارية والخدمات",department:"الادارة التنفيذية - الرياض",joinDate:"2025-08-24",endDate:"2026-08-23",vacation:0.46,basicSalary:10000,fullSalary:13000},
  {id:30098,name:"فيء عبدالعزيز عبدالله السلوم",position:"سكرتير تنفيذي",department:"الادارة التنفيذية - الرياض",joinDate:"2025-08-10",endDate:"2026-08-09",vacation:1.26,basicSalary:5402,fullSalary:7293},
  {id:30087,name:"أماني محمد أحمد الجهني",position:"مشرف مشاريع",department:"الادارة التنفيذية - الرياض",joinDate:"2025-07-13",endDate:"2026-07-12",vacation:1.87,basicSalary:9333,fullSalary:12600},
  {id:10503,name:"عبدالله محمد عبدالعزيز الراشد الحميد",position:"أخصائي ادارة مشاريع",department:"الادارة التنفيذية - الرياض",joinDate:"2024-11-13",endDate:"2025-11-12",vacation:4.79,basicSalary:5657,fullSalary:7000},

  {id:1174,name:"أمين سليمان محمد الجلفي",position:"مدير حسابات",department:"الإدارة المالية - الرياض",joinDate:"2006-12-10",endDate:"2026-12-09",vacation:100.75,basicSalary:13717,fullSalary:19000},
  {id:1197,name:"عمر موسي علي موسي",position:"محاسب تكاليف",department:"الإدارة المالية - الرياض",joinDate:"2008-07-01",endDate:"2026-06-30",vacation:132.87,basicSalary:7321,fullSalary:9552},
  {id:10210,name:"محمد خالد محمد ابوالخير عيد",position:"محاسب",department:"الإدارة المالية - الرياض",joinDate:"2019-11-24",endDate:"2025-11-23",vacation:3.69,basicSalary:4370,fullSalary:6318},
  {id:10335,name:"اسلام عبدالمحسن سليمان حسن",position:"رئيس الحسابات",department:"الإدارة المالية - الرياض",joinDate:"2022-05-29",endDate:"2026-05-28",vacation:39.85,basicSalary:6300,fullSalary:8516},
  {id:10342,name:"محمد مبروك عطيه غنيم",position:"محاسب",department:"الإدارة المالية - الرياض",joinDate:"2022-06-22",endDate:"2026-06-21",vacation:11.73,basicSalary:3668,fullSalary:4680},
  {id:10343,name:"احمد محمود محمد عيد",position:"محاسب",department:"الإدارة المالية - الرياض",joinDate:"2022-06-22",endDate:"2026-06-21",vacation:22.84,basicSalary:3385,fullSalary:4350},
  {id:10344,name:"عبدالرحمن محى اسماعيل غريب",position:"محاسب",department:"الإدارة المالية - الرياض",joinDate:"2022-06-22",endDate:"2026-06-21",vacation:1.73,basicSalary:3385,fullSalary:4350},
  {id:10349,name:"وليد احمد طه الناقه",position:"محاسب",department:"الإدارة المالية - الرياض",joinDate:"2022-07-20",endDate:"2026-07-19",vacation:21.10,basicSalary:3700,fullSalary:5025},
  {id:10368,name:"عمرو بدوي محمد عمار",position:"محاسب",department:"الإدارة المالية - الرياض",joinDate:"2022-11-24",endDate:"2026-11-23",vacation:55.14,basicSalary:3385,fullSalary:4350},
  {id:20603,name:"مريم عبدالله أحمد شبيلي",position:"محاسب",department:"الإدارة المالية - الرياض",joinDate:"2019-12-01",endDate:"",vacation:27.47,basicSalary:5232,fullSalary:6540},
  {id:20919,name:"هند محمد عبدالله السعيد",position:"محاسب",department:"الإدارة المالية - الرياض",joinDate:"2023-07-09",endDate:"2026-07-08",vacation:6.01,basicSalary:4800,fullSalary:6000},
  {id:20950,name:"حصه فرج محمد الدوسري",position:"محاسب",department:"الإدارة المالية - الرياض",joinDate:"2023-12-31",endDate:"2025-12-30",vacation:28.48,basicSalary:4800,fullSalary:6000},
  {id:30053,name:"عمر محمد ضياء الدين أحمد",position:"محاسب مراقبة انتاج",department:"الإدارة المالية - الرياض",joinDate:"2025-05-22",endDate:"2027-05-21",vacation:5.86,basicSalary:2473,fullSalary:3491},
  {id:30081,name:"خالد محمد اسماعيل زهران",position:"مشرف تكاليف",department:"الإدارة المالية - الرياض",joinDate:"2025-06-22",endDate:"2027-06-21",vacation:4.08,basicSalary:6000,fullSalary:8000},
  {id:30104,name:"محمد علاء محمد محمد عبدالله",position:"مشرف حسابات",department:"الإدارة المالية - الرياض",joinDate:"2025-08-17",endDate:"2027-08-16",vacation:0.86,basicSalary:4400,fullSalary:6000},

  {id:30094,name:"محمود جمال محمد عبدالرازق",position:"مساعد مدير مشتريات",department:"قسم المشتريات – الرياض",joinDate:"2025-08-04",endDate:"2027-08-03",vacation:1.11,basicSalary:6000,fullSalary:8000},
  {id:30076,name:"وائل عبدالمنعم عبدالحليم عطيه",position:"اخصائي مشتريات خارجية",department:"قسم المشتريات – الرياض",joinDate:"2025-06-22",endDate:"2027-06-21",vacation:4.08,basicSalary:4400,fullSalary:6000},
  {id:1095,name:"علي احمد حسين القارني",position:"مدير إدارة المشتريات",department:"قسم المشتريات – الرياض",joinDate:"1997-05-10",endDate:"2027-05-09",vacation:42.53,basicSalary:11113,fullSalary:13891},
  {id:10026,name:"وائل نعمان شرف الحكيم",position:"اخصائي مشتريات اول",department:"قسم المشتريات – الرياض",joinDate:"2011-02-26",endDate:"2027-02-25",vacation:133.58,basicSalary:6720,fullSalary:8800},
  {id:10103,name:"سامي سليمان عبده سلام",position:"مندوب المشتريات",department:"قسم المشتريات – الرياض",joinDate:"2016-08-03",endDate:"2026-08-02",vacation:104.66,basicSalary:3200,fullSalary:4000},
  {id:10338,name:"فواز حمادي الخلف الكدرو",position:"مندوب المشتريات",department:"قسم المشتريات – الرياض",joinDate:"2022-06-18",endDate:"2026-06-17",vacation:48.24,basicSalary:3000,fullSalary:5000},

  {id:10010,name:"عالم أعظم علي",position:"مهندس شبكات",department:"الإدارة تقنية المعلومات - الرياض",joinDate:"2009-08-11",endDate:"2027-08-10",vacation:39.30,basicSalary:5179,fullSalary:5979},
  {id:1801,name:"هداية الله ديشموخ خان",position:"مدير المشروع اوراكل",department:"الإدارة تقنية المعلومات - الرياض",joinDate:"2006-12-25",endDate:"2026-12-24",vacation:141.74,basicSalary:12000,fullSalary:15400},
  {id:30069,name:"احمد فتحى عبد الفتاح على",position:"مدير إدارة تقنية المعلومات",department:"الإدارة تقنية المعلومات - الرياض",joinDate:"2025-05-11",endDate:"2025-07-10",vacation:3.50,basicSalary:16300,fullSalary:22000},

  {id:30092,name:"صلاح الدين مصطفى محمود مبروك",position:"اخصائي حوكمة",department:"الادارة القانونية - الرياض",joinDate:"2025-07-15",endDate:"2027-07-14",vacation:2.76,basicSalary:4000,fullSalary:5500},
  {id:30089,name:"عبدالعزيز محمد الطويرش",position:"أخصائي قانوني",department:"الادارة القانونية - الرياض",joinDate:"2025-07-13",endDate:"2026-07-12",vacation:2.37,basicSalary:5185,fullSalary:7000},
  {id:10499,name:"علي محمد عثمان المقدم",position:"اخصائي حوكمة",department:"الادارة القانونية - الرياض",joinDate:"2024-10-14",endDate:"2026-10-13",vacation:16.98,basicSalary:5185,fullSalary:7000},

  {id:1196,name:"محمد عبدالله الخضر محمد",position:"مراجع حسابات",department:"ادارة المراجعة - الرياض",joinDate:"2008-07-01",endDate:"2026-06-30",vacation:125.46,basicSalary:9000,fullSalary:11650},
  {id:10468,name:"احمد عبد الخالق غريب عبد المقصود",position:"مدير إدارة المراجعة الداخلية",department:"ادارة المراجعة - الرياض",joinDate:"2024-04-18",endDate:"2026-04-17",vacation:19.74,basicSalary:9000,fullSalary:11650},

  {id:20992,name:"ساره محمد عبدالرحمن الفهدي",position:"اخصائي موارد بشرية",department:"الإدارة الموارد البشرية - الرياض",joinDate:"2024-07-28",endDate:"2026-07-27",vacation:8.90,basicSalary:4444,fullSalary:6000},
  {id:30090,name:"محمد ابراهيم محمد اليحيا",position:"مشرف الموارد بشرية",department:"الإدارة الموارد البشرية - الرياض",joinDate:"2025-07-14",endDate:"2026-07-13",vacation:3.52,basicSalary:8889,fullSalary:12000},
  {id:20940,name:"مريم عماش علي دوح",position:"اخصائي علاقات حكومية",department:"الإدارة الموارد البشرية - الرياض",joinDate:"2023-10-01",endDate:"2025-09-30",vacation:1.23,basicSalary:6480,fullSalary:8500},

  {id:10048,name:"بدرالدين ادريس عبدالرحمن ادريس",position:"اخصائي الخدمات العامة",department:"إدارة المستودعات و الخدمات اللوجستية - الرياض",joinDate:"2012-11-20",endDate:"2025-12-04",vacation:74.26,basicSalary:2700,fullSalary:4500},
  {id:10492,name:"عبدالله مذري راشد الشمري",position:"مدير إدارة المستودعات والخدمات الوجستية",department:"إدارة المستودعات و الخدمات اللوجستية - الرياض",joinDate:"2024-09-01",endDate:"2025-08-31",vacation:12.98,basicSalary:9943,fullSalary:12000},

  {id:1158,name:"ولي د ندا على عبدالنبى",position:"نائب الرئيس التنفيذي للعمليات",department:"الإدارة العامة - إدارة المبيعات",joinDate:"2005-07-23",endDate:"2027-07-22",vacation:121.46,basicSalary:35000,fullSalary:45000},
  {id:30075,name:"رامى حسنى حسين السيد",position:"مندوب مبيعات كبار العملاء",department:"إدارة المبيعات",joinDate:"2025-06-17",endDate:"2027-06-16",vacation:4.37,basicSalary:4000,fullSalary:4667},
  {id:10198,name:"ابراهيم السيد ابراهيم ظهر",position:"مشرف مبيعات",department:"الإدارة العامة - إدارة المبيعات",joinDate:"2019-04-21",endDate:"2027-04-20",vacation:13.91,basicSalary:4000,fullSalary:5000},
  {id:30046,name:"عمر سيد علي سيد",position:"مندوب مبيعات",department:"إدارة المبيعات",joinDate:"2025-04-16",endDate:"2027-04-15",vacation:6.93,basicSalary:2000,fullSalary:2333},
  {id:10027,name:"بلال احمد محمد",position:"سكرتير",department:"الإدارة العامة - إدارة المبيعات",joinDate:"2011-02-28",endDate:"2027-02-27",vacation:1.86,basicSalary:2200,fullSalary:2950},
  {id:10504,name:"عمرو عبدالمنعم عبدالقادر عبدالرازق",position:"مندوب مبيعات",department:"إدارة المبيعات",joinDate:"2024-11-19",endDate:"2026-11-18",vacation:-0.55,basicSalary:2500,fullSalary:2916},
  {id:10497,name:"احمد سمير عبدالقادر بدوى",position:"مندوب مبيعات كبار العملاء",department:"إدارة المبيعات",joinDate:"2024-10-01",endDate:"2026-09-30",vacation:19.23,basicSalary:4000,fullSalary:4666},
  {id:10311,name:"اسامه رمضان قرني سلامه",position:"مشرف مبيعات",department:"الإدارة العامة - إدارة المبيعات",joinDate:"2022-02-07",endDate:"2026-02-06",vacation:70.88,basicSalary:4000,fullSalary:4666},
  {id:2493,name:"كلام عبدالرحمن",position:"مندوب مبيعات",department:"الإدارة العامة - إدارة المبيعات",joinDate:"2019-12-09",endDate:"2025-12-08",vacation:19.24,basicSalary:1800,fullSalary:2250},
  {id:10305,name:"محمد عبدالنبي محمد عيد",position:"مشرف مبيعات",department:"الإدارة العامة - إدارة المبيعات",joinDate:"2021-10-11",endDate:"2025-10-10",vacation:59.41,basicSalary:6000,fullSalary:7500},

  {id:1007,name:"مصطفى كسالي",position:"عامل نظافة",department:"قسم الخدمات - الرياض",joinDate:"1996-12-08",endDate:"2026-12-07",vacation:80.83,basicSalary:1867,fullSalary:2317},
  {id:1670,name:"عبد الله علي عبد الرحمن ابو بناء",position:"معقب",department:"قسم الخدمات - الرياض",joinDate:"2005-07-18",endDate:"",vacation:62.55,basicSalary:4600,fullSalary:5750}
];

// --- DOM elements ---
const searchInput = document.getElementById('searchInput');
const departmentFilter = document.getElementById('departmentFilter');
const sortBy = document.getElementById('sortBy');
const tableBody = document.getElementById('tableBody');
const deptTabs = document.querySelectorAll('.department-tab');
const totalEmployees = document.getElementById('totalEmployees');
const avgSalary = document.getElementById('avgSalary');
const maxSalary = document.getElementById('maxSalary');
const minSalary = document.getElementById('minSalary');

// render table
function renderTable(data) {
  tableBody.innerHTML = '';
  if (data.length === 0) {
    const tr = document.createElement('tr');
    tr.innerHTML = `<td colspan="9" class="no-results"><i class="fas fa-search" style="font-size:28px;display:block;margin-bottom:8px"></i>لا توجد نتائج</td>`;
    tableBody.appendChild(tr);
    updateStats([]);
    return;
  }
  data.forEach(emp => {
    const vacClass = emp.vacation < 1 ? 'vacation-days low' : (emp.vacation < 5 ? 'vacation-days medium' : 'vacation-days high');
    const tr = document.createElement('tr');
    tr.innerHTML = `
      <td>${emp.id}</td>
      <td>${emp.name}</td>
      <td>${emp.position}</td>
      <td>${emp.department}</td>
      <td>${emp.joinDate}</td>
      <td>${emp.endDate || '-'}</td>
      <td><span class="${vacClass}">${emp.vacation}</span></td>
      <td>${emp.basicSalary.toLocaleString()} ر.س</td>
      <td class="salary">${emp.fullSalary.toLocaleString()} ر.س</td>
    `;
    tableBody.appendChild(tr);
  });
  updateStats(data);
}

// update stats
function updateStats(data) {
  totalEmployees.textContent = data.length;
  if (data.length === 0) {
    avgSalary.textContent = '0 ر.س'; maxSalary.textContent = '0 ر.س'; minSalary.textContent = '0 ر.س';
    return;
  }
  const salaries = data.map(d=>d.fullSalary);
  const total = salaries.reduce((s,x)=>s+x,0);
  const avg = Math.round(total / salaries.length);
  avgSalary.textContent = `${avg.toLocaleString()} ر.س`;
  maxSalary.textContent = `${Math.max(...salaries).toLocaleString()} ر.س`;
  minSalary.textContent = `${Math.min(...salaries).toLocaleString()} ر.س`;
}

// filter & sort
function filterAndSortData() {
  const q = searchInput.value.trim().toLowerCase();
  const dept = departmentFilter.value;
  const sortVal = sortBy.value;
  let filtered = employees.filter(e => {
    const matchesQ = e.name.toLowerCase().includes(q) || e.position.toLowerCase().includes(q) || e.department.toLowerCase().includes(q);
    const matchesDept = dept === 'all' || e.department.includes(dept);
    return matchesQ && matchesDept;
  });

  switch(sortVal) {
    case 'name': filtered.sort((a,b)=> a.name.localeCompare(b.name,'ar')); break;
    case 'salary': filtered.sort((a,b)=> b.fullSalary - a.fullSalary); break;
    case 'salary-asc': filtered.sort((a,b)=> a.fullSalary - b.fullSalary); break;
    case 'joinDate': filtered.sort((a,b)=> new Date(b.joinDate) - new Date(a.joinDate)); break;
    case 'joinDate-asc': filtered.sort((a,b)=> new Date(a.joinDate) - new Date(b.joinDate)); break;
  }

  renderTable(filtered);
}

// events
searchInput.addEventListener('input', filterAndSortData);
departmentFilter.addEventListener('change', filterAndSortData);
sortBy.addEventListener('change', filterAndSortData);

deptTabs.forEach(tab=>{
  tab.addEventListener('click', ()=>{
    deptTabs.forEach(t=>t.classList.remove('active'));
    tab.classList.add('active');
    const d = tab.getAttribute('data-dept');
    departmentFilter.value = d === 'all' ? 'all' : d;
    filterAndSortData();
  });
});

// initial render
document.addEventListener('DOMContentLoaded', ()=>{
  renderTable(employees);
});
</script>
</body>
</html>
