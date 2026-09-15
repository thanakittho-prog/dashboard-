<!DOCTYPE html>
<html lang="th">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Dashboard สุขภาพประจำสัปดาห์</title>
  <style>
    body {
      font-family: Arial, 'Helvetica Neue', Helvetica, sans-serif;
      color: #333333;
      line-height: 1.5;
      background-color: #f8f9fa;
      margin: 0;
      padding: 20px;
    }
    .container {
      max-width: 900px;
      margin: 0 auto;
      background: #ffffff;
      padding: 25px;
      border-radius: 12px;
      box-shadow: 0 2px 10px rgba(0,0,0,0.05);
    }
    h1 {
      color: #1a365d;
      font-size: 24px;
      margin-top: 0;
      margin-bottom: 20px;
      border-bottom: 2px solid #e2e8f0;
      padding-bottom: 10px;
    }
    h2 {
      color: #2b6cb0;
      font-size: 18px;
      margin-top: 25px;
      margin-bottom: 15px;
    }
    /* Grid Layout สำหรับ KPI */
    .kpi-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
      gap: 15px;
      margin-bottom: 25px;
    }
    .kpi-card {
      background-color: #f7fafc;
      border: 1px solid #e2e8f0;
      border-radius: 8px;
      padding: 15px;
      text-align: center;
    }
    .kpi-title {
      font-size: 13px;
      color: #4a5568;
      margin-bottom: 8px;
      font-weight: bold;
    }
    .kpi-value {
      font-size: 24px;
      font-weight: bold;
      color: #2d3748;
    }
    .kpi-unit {
      font-size: 12px;
      color: #718096;
      font-weight: normal;
    }
    /* ตารางข้อมูล */
    .data-table {
      width: 100%;
      border-collapse: collapse;
      margin-bottom: 25px;
      border: 1px solid #e2e8f0;
    }
    .data-table th {
      background-color: #ebf8ff;
      color: #2b6cb0;
      font-weight: bold;
      text-align: left;
      padding: 12px;
      border-bottom: 2px solid #cbd5e0;
    }
    .data-table td {
      padding: 12px;
      border-bottom: 1px solid #e2e8f0;
    }
    .data-table tr:nth-child(even) {
      background-color: #f7fafc;
    }
    /* Visual Progress Bar */
    .bar-container {
      background-color: #edf2f7;
      border-radius: 4px;
      height: 16px;
      width: 100%;
      overflow: hidden;
      margin-bottom: 4px;
    }
    .bar-sleep {
      background-color: #4c51bf;
      height: 100%;
      border-radius: 4px;
    }
    .bar-water {
      background-color: #3182ce;
      height: 100%;
      border-radius: 4px;
    }
    .val-text {
      font-size: 11px;
      color: #4a5568;
    }
  </style>
</head>
<body>

<div class="container">
  <h1>Dashboard สุขภาพประจำสัปดาห์ (น้ำหนักตัว 85 กก.)</h1>

  <!-- 1. KPI Cards -->
  <div class="kpi-grid">
    <div class="kpi-card">
      <div class="kpi-title">วันออกกำลังกาย</div>
      <div class="kpi-value">5 <span class="kpi-unit">/ 7 วัน</span></div>
    </div>
    <div class="kpi-card">
      <div class="kpi-title">เวลารวมออกกำลังกาย</div>
      <div class="kpi-value">195 <span class="kpi-unit">นาที</span></div>
    </div>
    <div class="kpi-card">
      <div class="kpi-title">ชั่วโมงนอนเฉลี่ย</div>
      <div class="kpi-value">7.3 <span class="kpi-unit">ชม./วัน</span></div>
    </div>
    <div class="kpi-card">
      <div class="kpi-title">ปริมาณน้ำเฉลี่ย</div>
      <div class="kpi-value">2.1 <span class="kpi-unit">ลิตร/วัน</span></div>
    </div>
  </div>

  <!-- 2. Daily Log Table -->
  <h2>รายการกิจกรรมและสุขภาพรายวัน (7–13 ก.ย.)</h2>
  <table class="data-table">
    <thead>
      <tr>
        <th>วันที่</th>
        <th>กิจกรรมออกกำลังกาย</th>
        <th>ระยะเวลา</th>
        <th>ระยะเวลานอน</th>
        <th>ปริมาณน้ำที่ดื่ม</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>7 ก.ย. (จันทร์)</td>
        <td>วิ่ง</td>
        <td>30 นาที</td>
        <td>7.2 ชม.</td>
        <td>1.8 ลิตร</td>
      </tr>
      <tr>
        <td>8 ก.ย. (อังคาร)</td>
        <td>ปั่นจักรยาน</td>
        <td>45 นาที</td>
        <td>6.5 ชม.</td>
        <td>1.5 ลิตร</td>
      </tr>
      <tr>
        <td>9 ก.ย. (พุธ)</td>
        <td>พักผ่อน (Rest Day)</td>
        <td>-</td>
        <td>8.0 ชม.</td>
        <td>2.5 ลิตร</td>
      </tr>
      <tr>
        <td>10 ก.ย. (พฤหัสบดี)</td>
        <td>วิ่ง</td>
        <td>30 นาที</td>
        <td>7.5 ชม.</td>
        <td>2.2 ลิตร</td>
      </tr>
      <tr>
        <td>11 ก.ย. (ศุกร์)</td>
        <td>เวทเทรนนิ่ง</td>
        <td>40 นาที</td>
        <td>6.8 ชม.</td>
        <td>2.0 ลิตร</td>
      </tr>
      <tr>
        <td>12 ก.ย. (เสาร์)</td>
        <td>วิ่ง</td>
        <td>50 นาที</td>
        <td>8.2 ชม.</td>
        <td>2.8 ลิตร</td>
      </tr>
      <tr>
        <td>13 ก.ย. (อาทิตย์)</td>
        <td>พักผ่อน (Rest Day)</td>
        <td>-</td>
        <td>7.0 ชม.</td>
        <td>2.1 ลิตร</td>
      </tr>
    </tbody>
  </table>

  <!-- 3. Trend Visual Bars -->
  <h2>แนวโน้มชั่วโมงการนอนและปริมาณน้ำดื่ม 7 วัน</h2>
  <table class="data-table">
    <thead>
      <tr>
        <th style="width: 15%;">วัน</th>
        <th style="width: 42.5%;">ชั่วโมงการนอน (เป้าหมาย 7-8 ชม.)</th>
        <th style="width: 42.5%;">ปริมาณน้ำดื่ม (เป้าหมาย 3.0 ลิตร)</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><strong>จันทร์</strong></td>
        <td>
          <div class="bar-container"><div class="bar-sleep" style="width: 72%;"></div></div>
          <span class="val-text">7.2 ชม.</span>
        </td>
        <td>
          <div class="bar-container"><div class="bar-water" style="width: 60%;"></div></div>
          <span class="val-text">1.8 ลิตร</span>
        </td>
      </tr>
      <tr>
        <td><strong>อังคาร</strong></td>
        <td>
          <div class="bar-container"><div class="bar-sleep" style="width: 65%;"></div></div>
          <span class="val-text">6.5 ชม.</span>
        </td>
        <td>
          <div class="bar-container"><div class="bar-water" style="width: 50%;"></div></div>
          <span class="val-text">1.5 ลิตร</span>
        </td>
      </tr>
      <tr>
        <td><strong>พุธ</strong></td>
        <td>
          <div class="bar-container"><div class="bar-sleep" style="width: 80%;"></div></div>
          <span class="val-text">8.0 ชม.</span>
        </td>
        <td>
          <div class="bar-container"><div class="bar-water" style="width: 83%;"></div></div>
          <span class="val-text">2.5 ลิตร</span>
        </td>
      </tr>
      <tr>
        <td><strong>พฤหัสบดี</strong></td>
        <td>
          <div class="bar-container"><div class="bar-sleep" style="width: 75%;"></div></div>
          <span class="val-text">7.5 ชม.</span>
        </td>
        <td>
          <div class="bar-container"><div class="bar-water" style="width: 73%;"></div></div>
          <span class="val-text">2.2 ลิตร</span>
        </td>
      </tr>
      <tr>
        <td><strong>ศุกร์</strong></td>
        <td>
          <div class="bar-container"><div class="bar-sleep" style="width: 68%;"></div></div>
          <span class="val-text">6.8 ชม.</span>
        </td>
        <td>
          <div class="bar-container"><div class="bar-water" style="width: 66%;"></div></div>
          <span class="val-text">2.0 ลิตร</span>
        </td>
      </tr>
      <tr>
        <td><strong>เสาร์</strong></td>
        <td>
          <div class="bar-container"><div class="bar-sleep" style="width: 82%;"></div></div>
          <span class="val-text">8.2 ชม.</span>
        </td>
        <td>
          <div class="bar-container"><div class="bar-water" style="width: 93%;"></div></div>
          <span class="val-text">2.8 ลิตร</span>
        </td>
      </tr>
      <tr>
        <td><strong>อาทิตย์</strong></td>
        <td>
          <div class="bar-container"><div class="bar-sleep" style="width: 70%;"></div></div>
          <span class="val-text">7.0 ชม.</span>
        </td>
        <td>
          <div class="bar-container"><div class="bar-water" style="width: 70%;"></div></div>
          <span class="val-text">2.1 ลิตร</span>
        </td>
      </tr>
    </tbody>
  </table>
</div>

</body>
</html>
# dashboard-