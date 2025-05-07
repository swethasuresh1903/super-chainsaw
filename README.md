{
  "name": "devops-dashboard-backend",
  "version": "1.0.0",
  "main": "server.js",
  "scripts": {
    "start": "node server.js"
  },
  "dependencies": {
    "express": "^4.17.1"
  }
}
const express = require('express');
const app = express();
const port = 5000;

app.get('/api/status', (req, res) => {
    res.json({ message: 'Deployment data fetched successfully', status: 'Active' });
});

app.listen(port, () => {
    console.log(`Backend running on http://localhost:${port}`);
});
