# cookie_session_auth (LAB: Security in NodeJS)

## How to run
```bash
npm install
node app.js
```
MongoDB phải chạy trước (local hoặc docker).

---

## Endpoints & How to test (POSTMAN)

### Register
POST `http://localhost:3000/auth/register`  
Body JSON:
```json
{ "username": "alice", "password": "12345" }
```
Expected: `User registered successfully!`  
![register](public/results/register.png)

---

### Login
POST `http://localhost:3000/auth/login`  
Body JSON:
```json
{ "username": "alice", "password": "12345" }
```
Expected: `Login successful!`  
![login](public/results/login.png)

---

### Profile
GET `http://localhost:3000/auth/profile`  
Expected: user info  
![profile](public/results/profile.png)

---

### Logout
GET `http://localhost:3000/auth/logout`  
Expected: `Logout successful!`  
![logout](public/results/logout.png)

---

### Session in DB
- Sau khi login:  
![session_in_db_login](public/results/session_in_db_login.png)

- Sau khi logout:  
![session_in_db_logout](public/results/session_in_db_logout.png)

---

## Commit & push lên GitHub
```bash
git init
git add .
git commit -m "Cookie session auth lab with screenshots"
git remote add origin https://github.com/<your-username>/cookie_session_auth
git branch -M main
git push -u origin main
```
