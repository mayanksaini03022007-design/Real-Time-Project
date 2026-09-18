# Deeya Invest backend

1. Install Node.js 20+ and run MongoDB locally (or use an Atlas connection string).
2. Copy `.env.example` to `.env` and set `MONGODB_URI`, `JWT_SECRET`, and secure admin credentials.
3. For MongoDB Atlas, click **Connect > Drivers**, copy the complete URI, replace the username and password, and replace any special password characters with URL-encoded values (for example, `@` becomes `%40`). Also add your current IP address under **Network Access**.
4. For a local MongoDB server, use `MONGODB_URI=mongodb://127.0.0.1:27017/deeya-invest`.
5. Run `npm install`, then `npm start`.
6. Open `http://localhost:3000/index5.html`.

## OTP handling

Each OTP is generated on the server, hashed, expires after 10 minutes, and is limited to five verification attempts. The OTP is printed only in the server terminal with an `[ADMIN ONLY]` label; it is never sent to the employee or included in an API response. The admin must provide the OTP to the employee.
