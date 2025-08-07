<h1 align="center">
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
      <img src="https://github.com/user-attachments/assets/1a342048-6738-411c-9153-357984a8722c" alt="Before Welcome Page" width="400"/>
      <p><i>Welcome Page</i></p>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/9437f745-fbc8-4a96-8044-4e3d3e73a536" alt="After Welcome Page" width="400"/>
      <p><i>Welcome Page</i></p>
    </td>
  </tr>

  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/58ee3417-96aa-4ea2-9bd9-6c1d075484de" alt="Before Mongo Db Connection" width="400"/>
      <p><i>Mongo Db Connection</i></p>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/2d04bc9c-196d-445c-8661-243fe172879e" alt="After Mongo Db Connection" width="400"/>
      <p><i>Mongo Db Connection</i></p>
    </td>
  </tr>

  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/d6a44012-ce05-4d48-8a95-c341eb93c357" alt="Before Restart View" width="400"/>
      <p><i>Restart View</i></p>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/63b13076-9ae9-4b6a-a96b-4dd665f7bdd8" alt="After Restart View" width="400"/>
      <p><i>Restart View</i></p>
    </td>
  </tr>

  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/0b90de72-45eb-49b1-87b4-363ec239a0ab" alt="Before Title & Favicon Area" width="400"/>
      <p><i>Title & Favicon Area</i></p>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/84792626-695c-42ab-b52d-9f316e1a9663" alt="After Title & Favicon Area" width="400"/>
      <p><i>Title & Favicon Area</i></p>
    </td>
  </tr>

  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/7defd689-4ecc-462a-85cf-edbd138dfbb2" alt="Before Login Page" width="400"/>
      <p><i>Login Page</i></p>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/27f753f7-a729-485b-b55e-36b59366f46d" alt="After Login Page" width="400"/>
      <p><i>Login Page</i></p>
    </td>
  </tr>

  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/bb0c3fcb-c157-40e8-920a-83cea19d632f" alt="Before Dashboard Page" width="400"/>
      <p><i>Dashboard Page</i></p>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/fa13cd83-2f01-4e19-8d46-d17dd4942c9d" alt="After Dashboard Page" width="400"/>
      <p><i>Dashboard Page</i></p>
    </td>
  </tr>

  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/95259be2-e81b-4a54-bb79-71020413b708" alt="Before Title & Favicon Area2" width="400"/>
      <p><i>Title & Favicon Area 2</i></p>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/89764071-8b87-4185-8197-dafc0d40b8d2" alt="After Title & Favicon Area2" width="400"/>
      <p><i>Title & Favicon Area 2</i></p>
    </td>
  </tr>

  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/e89d435a-2548-4a83-928d-e99a276edde0" alt="Before Settings View" width="400"/>
      <p><i>Settings View</i></p>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/5342cf43-68f8-43b3-b68c-688477bf4691" alt="After Settings View" width="400"/>
      <p><i>Settings View</i></p>
    </td>
  </tr>

  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/beb5d799-d8ce-4b04-b453-9cca2637b396" alt="Before About Page" width="400"/>
      <p><i>About Page</i></p>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/f4660422-5dbc-4889-baf7-7c2fcbcae72a" alt="After About Page" width="400"/>
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
### 🧑‍💻 3. Create MongoDB Admin and Application User
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
### 🚀 4. Start the App with PM2
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
