##  Database Schema

### Users Table
- `id`: Primary key
- `username`: Unique username
- `email`: User email
- `password`: Hashed password
- `balance`: Current wallet balance
- `created_at`: Registration timestamp

### Transactions Table
- `id`: Transaction ID
- `sender_id`: User ID of sender
- `receiver_id`: User ID of receiver
- `amount`: Transaction amount
- `transaction_type`: Type (send/receive)
- `status`: Transaction status
- `created_at`: Transaction timestamp

### Money Requests Table
- `id`: Request ID
- `sender_id`: User requesting money
- `receiver_id`: User receiving request
- `amount`: Requested amount
- `status`: pending/approved/rejected
- `created_at`: Request timestamp

## 💡 Usage Guide

### For Regular Users

1. **Register an Account**
   - Visit registration page
   - Fill in username, email, and password
   - Initial balance: PKR 1000

2. **Send Money**
   - Login to dashboard
   - Click "Send Money"
   - Enter recipient username and amount
   - Confirm transaction

3. **Request Money**
   - Navigate to "Request Money"
   - Enter username and amount
   - Wait for approval

4. **View Transactions**
   - Access transaction history
   - Filter by date or type
   - Download statements

# Security Features

- Password hashing using PHP's `password_hash()`
- Session-based authentication
- SQL injection prevention with prepared statements
- Input validation and sanitization
- Protected routes (login required)
- 
