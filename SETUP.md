# Setup Instructions

## Backend Setup

1. **Install Dependencies**
```bash
cd server
npm install
```

2. **Create PostgreSQL Database**
```bash
psql -U postgres
CREATE DATABASE financial_planner;
\q
```

3. **Run Database Schema**
```bash
psql -U postgres -d financial_planner -f database/schema.sql
```

4. **Setup Environment Variables**
```bash
cp .env.example .env
# Edit .env with your PostgreSQL password and Finnhub API key
```

Get free Finnhub API key: https://finnhub.io/register

5. **Start Backend Server**
```bash
npm run dev
```

Backend will run on: http://localhost:5000

## Frontend Setup

1. **Install Dependencies**
```bash
cd client
npm install
```

2. **Start React App**
```bash
npm start
```

Frontend will open at: http://localhost:3000

## Using the Application

1. **Register** - Create your account
2. **Dashboard** - View your portfolio overview
3. **Portfolio** - Add/manage stocks
4. **Stocks** - Search NSE stocks and view real-time prices
5. **Calculations** - Use financial calculators

## Features

✅ User Authentication (JWT)
✅ Real-time NSE Stock Prices (Finnhub API)
✅ Portfolio Management
✅ 4 Financial Calculators
✅ Responsive Design
✅ Calculation History

## Available Calculators

- **Compound Interest** - Calculate investment growth
- **EMI** - Calculate loan EMI
- **SIP** - Calculate Systematic Investment Plan returns
- **Future Value** - Calculate future value of investment

## Supported NSE Stocks

TCS, INFY, RELIANCE, WIPRO, HCLTECH, TECHM, LT, MARUTI, HDFC, SBIN, ICICIBANK, BAJAJFINSV, ADANIGREEN, ASIANPAINT, DRREDDY

## Troubleshooting

### Port Already in Use
```bash
# Kill process on port 5000
lsof -ti:5000 | xargs kill -9
```

### Database Connection Error
- Verify PostgreSQL is running
- Check DATABASE_URL in .env
- Ensure database exists: `psql -l`

### CORS Issues
- Verify backend CORS is enabled
- Check CLIENT_URL in backend .env
- Restart both servers

## Deployment

### Frontend (Vercel)
```bash
cd client
npm run build
# Deploy to Vercel
```

### Backend (Railway)
```bash
# Deploy to Railway
# Set environment variables in Railway dashboard
```

## Support

For issues, create a GitHub issue or contact support.

**Happy Financial Planning! 💰📈**
