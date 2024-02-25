# User service authentication

## 0. User model

**File:** `user.py`

- Create a SQLAlchemy model named `User` for a database table named `users`.
- The model should have the following attributes:
  - `id` (integer primary key)
  - `email` (non-nullable string)
  - `hashed_password` (non-nullable string)
  - `session_id` (nullable string)
  - `reset_token` (nullable string)

## 1. Create user

**File:** `db.py`

- Implement the `add_user` method in the `DB` class.
- The method should take `email` and `hashed_password` as arguments and return a `User` object.

## 2. Find user

**File:** `db.py`

- Implement the `find_user_by` method in the `DB` class.
- The method should take arbitrary keyword arguments and return the first row found in the users table.

## 3. Update user

**File:** `db.py`

- Implement the `update_user` method in the `DB` class.
- The method should take a `user_id` and arbitrary keyword arguments.

## 4. Hash password

**File:** `auth.py`

- Define a `_hash_password` method that takes a password string and returns bytes.

## 5. Register user

**File:** `auth.py`

- Implement the `register_user` method in the `Auth` class.
- The method should take `email` and `password` as arguments and return a `User` object.

## 6. Basic Flask app

**File:** `app.py`

- Set up a basic Flask app with a single GET route ("/").

## 7. Register user

**File:** `app.py`

- Implement the POST `/users` route to register a user.

## 8. Credentials validation

**File:** `auth.py`

- Implement the `valid_login` method in the `Auth` class.
- The method should take `email` and `password` as arguments and return a boolean.

## 9. Generate UUIDs

**File:** `auth.py`

- Implement a `_generate_uuid` function that returns a string representation of a new UUID.

## 10. Get session ID

**File:** `auth.py`

- Implement the `create_session` method in the `Auth` class.
- The method should take an `email` as an argument and return the session ID.

## 11. Log in

**File:** `app.py`

- Implement the POST `/sessions` route for user login.

## 12. Find user by session ID

**File:** `auth.py`

- Implement the `get_user_from_session_id` method in the `Auth` class.

## 13. Destroy session

**File:** `auth.py`

- Implement the `destroy_session` method in the `Auth` class.

## 14. Log out

**File:** `app.py`

- Implement the DELETE `/sessions` route for user logout.

## 15. User profile

**File:** `app.py`

- Implement the GET `/profile` route to display the user profile.

## 16. Generate reset password token

**File:** `auth.py`

- Implement the `get_reset_password_token` method in the `Auth` class.

## 17. Get reset password token

**File:** `app.py`

- Implement the POST `/reset_password` route.

## 18. Update password

**File:** `auth.py`

- Implement the `update_password` method in the `Auth` class.

## 19. Update password end-point

**File:** `app.py`

- Implement the PUT `/reset_password` route.

## 20. End-to-end integration test

**File:** `main.py`

- Create a module called `main.py` for end-to-end integration testing using the `requests` module.

