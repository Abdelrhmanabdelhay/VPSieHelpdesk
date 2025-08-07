[<h1 align="center">
<a href=""><img src="https://vpsie.com/wp-content/uploads/2021/08/white-logo-web-save.png" width="300" /></a>
</h1>

Customized version of [Trudesk](https://github.com/polonel/trudesk) with VPSie branding and reporting logic.

## 🎨 Branding Before vs. After

Below are the UI changes made as part of VPSie branding.

<table>
  <tr>
    <th style="text-align:center">Before</th>
    <th style="text-align:center">After</th>
  </tr>

  <tr>
    <td align="center">
        <img src="https://github.com/user-attachments/assets/31b0e162-5fa0-41eb-a991-6b24b9e40ff9" alt="Before Welcome Page" width="400"/>
      <p><i>Welcome Page</i></p>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/00014f11-1125-4195-a220-a822be762b5e" alt="After Welcome Page" width="400"/>
      <p><i>Welcome Page</i></p>
    </td>
  </tr>

  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/30414fef-73d4-4ab5-bd57-94bfec086ae8" alt="Before Mongo Db Connection" width="400"/>
      <p><i>Mongo Db Connection</i></p>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/b73af7f9-9066-48d1-b912-aa32d45be7e2" alt="After Mongo Db Connection" width="400"/>
      <p><i>Mongo Db Connection</i></p>
    </td>
  </tr>

  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/9c2fa280-2c24-46ec-a568-0783a8a1b80a" alt="Before Restart View" width="400"/>
      <p><i>Restart View</i></p>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/51f98cc1-6fbf-4b7b-aad1-bfe813869b66" alt="After Restart View" width="400"/>
      <p><i>Restart View</i></p>
    </td>
  </tr>
    <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/71b03179-6a74-46a4-89aa-1e16a5537833" alt="Before Title & Favicon Area" width="400"/>
      <p><i>Title & Favicon Area</i></p>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/9945782e-4de6-46bd-ac6b-2af06ecbb456" alt="After Title & Favicon Area" width="400"/>
      <p><i>Title & Favicon Area</i></p>
    </td>
  </tr>
      <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/20fedf65-def4-4d18-8766-e5a25393d9ef" alt="Before Login Page" width="400"/>
      <p><i>Login Page</i></p>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/b6f802d7-7271-42f0-8ff1-61c1896db097" alt="After Login Page" width="400"/>
      <p><i>Login Page</i></p>
    </td>
  </tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/aa128957-d31b-4f46-985d-552a93e4990c" alt="Before Dashboard Page" width="400"/>
      <p><i>Dashboard Page</i></p>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/2819b8e0-50d4-4b24-946a-820ae5333fef" alt="After Dashboard Page" width="400"/>
      <p><i>Dashboard Page</i></p>
    </td>
    <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/b7c4aad8-748a-4bfe-8427-0f0c913d6201" alt="Before Title & Favicon Area2" width="400"/>
      <p><i>Title & Favicon Area 2</i></p>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/9daced58-9e6d-4e35-bb67-2a96bcf9cadb" alt="After Title & Favicon Area2" width="400"/>
      <p><i>Title & Favicon Area 2</i></p>
    </td>
  </tr>
      <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/1786bd93-a179-4f34-a626-ecc0a97f25ac" alt="Before Settings View" width="400"/>
      <p><i>Settings View</i></p>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/07448735-806b-4651-a028-88dfa4274238" alt="After Settings View" width="400"/>
      <p><i>Settings View</i></p>
    </td>
  </tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/11f197fb-cf05-4bce-a658-87b410819b9d" alt="Before About Page" width="400"/>
      <p><i>About Page</i></p>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/2f860aa1-d978-4077-8a43-df60daa5f281" alt="After About Page" width="400"/>
      <p><i>About Page</i></p>
    </td>
  </tr>
</table>

#### Requirements
- NodeJS 16
- MongoDB 5.0+
- Elasticsearch 8 (optional to enable search)

## 🚀 How to Run Locally

### 📦 1. Install Node.js v16 using NVM

```bash
nvm install 16
nvm use 16
```


### 📂 2. Install Dependencies
```bash
npm install --legacy-peer-deps
```
###🧑‍💻 3. Create MongoDB Admin and Application User
```bash
use trudesk
db.createUser({
  user: "trudeskuser",
  pwd: "yourTrudeskPassword",
  roles: [
    { role: "readWrite", db: "trudesk" }
  ]
})
```
### 🚀 5. Start the App with PM2
```bash
npm install -g pm2
pm2 start app.js --name trudesk
pm2 save
pm2 logs

Visit the app at:
http://localhost:8118
```
## 📊 Reporting Features:
### 📁 1.Attachments per Month
### ✅ What It Does:
- Attachments per Month
- Count how many file attachments were uploaded per month
- Display this data either as a table or API response (or chart if ambitious)

### 📁 Location:
```bash
src\controllers\api\v1\reports.js
```
### Code:
```bash
/**
 * @api {get} /api/v1/reports/attachments-per-month Attachments Per Month
 * @apiName attachmentsPerMonth
 * @apiDescription Get the count of file attachments uploaded per month
 * @apiVersion 1.0.0
 * @apiGroup Reports
 * @apiHeader {string} accesstoken The access token for the logged in user
 *
 * @apiSuccess {object[]} months Array of objects with { month, year, count }
 */
 apiReports.generate.attachmentsPerMonth = async function (req, res) {
  try {
    const Ticket = require('../../../models/ticket.js')
    // Aggregate all attachments from all tickets
    const pipeline = [
      { $unwind: '$attachments' },
      { $match: { 'attachments.date': { $exists: true } } },
      {
        $group: {
          _id: {
            year: { $year: '$attachments.date' },
            month: { $month: '$attachments.date' }
          },
          count: { $sum: 1 }
        }
      },
      { $sort: { '_id.year': 1, '_id.month': 1 } }
    ];
    const result =await  Ticket.aggregate(pipeline)
    // Format result
    const months = result.map(r => ({
      year: r._id.year,
      month: r._id.month,
      count: r.count
    }))
    return res.json({ success: true, months })
  } catch (err) {
    return res.status(500).json({ success: false, error: err.message })
  }
}
```
### 🧪 Available Endpoints:
```bash
{get} /api/v1/reports/attachments-per-month
```
### Results
```bash
{
    "success": true,
    "months": [
        {
            "year": 2025,
            "month": 8,
            "count": 5
        }
    ]
}
```
### 📁 2. Average Time to Close a Ticket

### ✅ What It Does:
For each month: 
- Calculate the average time (in hours/days) between ticket created and closed
### 📁 Location:
```bash
src\controllers\api\v1\tickets.js
```
### Code:
```bash
/**
 * @api {get} /api/v1/tickets/getaverageclosetimebymonth
 * @apiName getAverageCloseTime
 * @apiDescription Calculates the average time (in hours) to close tickets, grouped by month. 
 * Tickets that are still open (no closedDate) are excluded.
 * @apiGroup Ticket
 * @apiSuccess {Boolean} success Indicates if the request was successful
 * @apiSuccess {Object[]} data Array of results grouped by month
 * @apiSuccess {String} data.month Month in format YYYY-MM
 * @apiSuccess {String} data.averageTimeInHours Average close time in hours (rounded to 2 decimals)
 * @apiSuccess {Number} data.ticketCount Number of tickets closed that month
 */

apiTickets.getAverageCloseTimeByMonth = async function (req,res)  {
  const Ticket = require('../../../models/ticket');
  try {
    const results = await Ticket.aggregate([
      // Only include tickets that are closed
      {
        $match: {
          closedDate: { $ne: null }
        }
      },
      // Project year, month, and duration in hours
      {
        $project: {
          year: { $year: "$closedDate" },
          month: { $month: "$closedDate" },
          durationInHours: {
            $divide: [{ $subtract: ["$closedDate", "$date"] }, 1000 * 60 * 60]
          }
        }
      },
      // Group by year/month and calculate average close time
      {
        $group: {
          _id: {
            year: "$year",
            month: "$month"
          },
          avgCloseTimeInHours: { $avg: "$durationInHours" },
          count: { $sum: 1 }
        }
      },
      // Sort by year and month
      {
        $sort: {
          "_id.year": 1,
          "_id.month": 1
        }
      }
    ]);

    // Format output
    const formatted = results.map(item => ({
      month: `${item._id.year}-${String(item._id.month).padStart(2, '0')}`,
      averageTimeInHours: item.avgCloseTimeInHours.toFixed(2),
      ticketCount: item.count
    }));

    console.log(formatted);
   return res.json({ success: true, data: formatted });

  } catch (err) {
    console.error('Error calculating average close time:', err);
    throw err;
  }
};
```
### 🧪 Available Endpoints:
```bash
@{get} /api/v1/tickets/getaverageclosetimebymonth
```
### Results
```bash
{
    "success": true,
    "data": [
        {
            "month": "2025-08", //Month in format YYYY-MM
            "averageTimeInHours": "0.07",//Average close time in hours (rounded to 2 decimals)
            "ticketCount": 1 //Number of tickets closed that month
        }
    ]
}

```
](https://github.com/Abdelrhmanabdelhay/VpsieHelpdesk)
