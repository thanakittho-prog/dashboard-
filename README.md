<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Dashboard สุขภาพประจำสัปดาห์</title>

    <style>
        * {
            box-sizing: border-box;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
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
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
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

        /* KPI */
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

        /* Health cards */
        .health-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 15px;
        }

        .health-card {
            border: 1px solid #e2e8f0;
            border-radius: 10px;
            padding: 18px;
            background-color: #ffffff;
        }

        .health-card h3 {
            margin-top: 0;
            color: #2b6cb0;
            font-size: 16px;
        }

        .health-card p {
            margin: 8px 0;
        }

        /* Progress bar */
        .progress {
            width: 100%;
            height: 10px;
            background: #edf2f7;
            border-radius: 10px;
            overflow: hidden;
            margin-top: 8px;
        }

        .progress-bar {
            height: 100%;
            background: #4299e1;
            border-radius: 10px;
        }

        /* Status */
        .status {
            display: inline-block;
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: bold;
        }

        .good {
            background: #c6f6d5;
            color: #276749;
        }

        .normal {
            background: #bee3f8;
            color: #2c5282;
        }

        .warning {
            background: #feebc8;
            color: #9c4221;
        }

        /* Table */
        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 10px;
        }

        th,
        td {
            border-bottom: 1px solid #e2e8f0;
            padding: 10px;
            text-align: left;
        }

        th {
            background-color: #f7fafc;
            color: #2d3748;
        }

        /* Recommendation */
        .recommendation {
            background-color: #ebf8ff;
            border-left: 4px solid #3182ce;
            padding: 15px;
            margin-top: 20px;
            border-radius: 5px;
        }

        .recommendation ul {
            margin-bottom: 0;
        }

        /* Mobile */
        @media (max-width: 600px) {
            body {
                padding: 10px;
            }

            .container {
                padding: 18px;
            }

            h1 {
                font-size: 21px;
            }

            .kpi-value {
                font-size: 21px;
            }
        }
    </style>
</head>

<body>

    <div class="container">

        <h1>Dashboard สุขภาพประจำสัปดาห์</h1>

        <!-- KPI -->
        <h2>ภาพรวมสุขภาพ</h2>

        <div class="kpi-grid">

            <div class="kpi-card">
                <div class="kpi-title">น้ำหนัก</div>
                <div class="kpi-value">
                    68 <span class="kpi-unit">kg</span>
                </div>
            </div>

            <div class="kpi-card">
                <div class="kpi-title">การนอน</div>
                <div class="kpi-value">
                    7.5 <span class="kpi-unit">ชม.</span>
                </div>
            </div>

            <div class="kpi-card">
                <div class="kpi-title">การออกกำลังกาย</div>
                <div class="kpi-value">
                    3 <span class="kpi-unit">ครั้ง</span>
                </div>
            </div>

            <div class="kpi-card">
                <div class="kpi-title">ดื่มน้ำ</div>
                <div class="kpi-value">
                    2.1 <span class="kpi-unit">ลิตร/วัน</span>
                </div>
            </div>

        </div>

        <!-- Health status -->
        <h2>สถานะสุขภาพ</h2>

        <div class="health-grid">

            <div class="health-card">
                <h3>การนอนหลับ</h3>

                <p>
                    ค่าเฉลี่ย 7.5 ชั่วโมง/วัน
                </p>

                <span class="status good">
                    ดี
                </span>

                <div class="progress">
                    <div class="progress-bar" style="width: 85%;"></div>
                </div>
            </div>

            <div class="health-card">
                <h3>การออกกำลังกาย</h3>

                <p>
                    ออกกำลังกาย 3 ครั้ง/สัปดาห์
                </p>

                <span class="status normal">
                    ปกติ
                </span>

                <div class="progress">
                    <div class="progress-bar" style="width: 60%;"></div>
                </div>
            </div>

            <div class="health-card">
                <h3>การดื่มน้ำ</h3>

                <p>
                    เฉลี่ย 2.1 ลิตร/วัน
                </p>

                <span class="status good">
                    ดี
                </span>

                <div class="progress">
                    <div class="progress-bar" style="width: 90%;"></div>
                </div>
            </div>

            <div class="health-card">
                <h3>อาหาร</h3>

                <p>
                    รับประทานอาหารครบ 3 มื้อ
                </p>

                <span class="status normal">
                    ปกติ
                </span>

                <div class="progress">
                    <div class="progress-bar" style="width: 70%;"></div>
                </div>
            </div>

        </div>

        <!-- Weekly record -->
        <h2>บันทึกประจำสัปดาห์</h2>

        <table>
            <thead>
                <tr>
                    <th>วัน</th>
                    <th>การนอน</th>
                    <th>ออกกำลังกาย</th>
                    <th>ดื่มน้ำ</th>
                </tr>
            </thead>

            <tbody>
                <tr>
                    <td>จันทร์</td>
                    <td>7 ชม.</td>
                    <td>เดิน 30 นาที</td>
                    <td>2 ลิตร</td>
                </tr>

                <tr>
                    <td>อังคาร</td>
                    <td>8 ชม.</td>
                    <td>วิ่ง 30 นาที</td>
                    <td>2.2 ลิตร</td>
                </tr>

                <tr>
                    <td>พุธ</td>
                    <td>7 ชม.</td>
                    <td>พัก</td>
                    <td>2 ลิตร</td>
                </tr>

                <tr>
                    <td>พฤหัสบดี</td>
                    <td>7.5 ชม.</td>
                    <td>เวทเทรนนิ่ง</td>
                    <td>2.3 ลิตร</td>
                </tr>

                <tr>
                    <td>ศุกร์</td>
                    <td>8 ชม.</td>
                    <td>พัก</td>
                    <td>2.1 ลิตร</td>
                </tr>

                <tr>
                    <td>เสาร์</td>
                    <td>7 ชม.</td>
                    <td>วิ่ง 40 นาที</td>
                    <td>2.2 ลิตร</td>
                </tr>

                <tr>
                    <td>อาทิตย์</td>
                    <td>8 ชม.</td>
                    <td>พัก</td>
                    <td>2 ลิตร</td>
                </tr>
            </tbody>
        </table>

        <!-- Recommendation -->
        <h2>คำแนะนำประจำสัปดาห์</h2>

        <div class="recommendation">
            <ul>
                <li>ควรนอนให้ได้ประมาณ 7–9 ชั่วโมงต่อวัน</li>
                <li>ออกกำลังกายอย่างน้อย 3–5 วันต่อสัปดาห์</li>
                <li>ดื่มน้ำให้เพียงพอตลอดทั้งวัน</li>
                <li>รับประทานผักและผลไม้เพิ่มขึ้น</li>
                <li>ลดอาหารหวาน มัน และเค็ม</li>
            </ul>
        </div>

    </div>

</body>
</html>