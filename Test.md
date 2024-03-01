# Database Documentation

## MongoDB

### Collection: users

- **Description**: Stores user information.
- **Sample Record**:
  ```json
  {
    "_id": ObjectId("5f5eb891ab7e1c1e85f10001"),
    "username": "john_doe",
    "email": "john@example.com",
    "created_at": ISODate("2020-09-14T12:30:00Z"),
    "is_active": true
  }
  ```

### Collection: posts

- **Description**: Contains user-created posts.
- **Sample Record**:
  ```json
  {
    "_id": ObjectId("5f5eb891ab7e1c1e85f10002"),
    "user_id": ObjectId("5f5eb891ab7e1c1e85f10001"),
    "content": "This is a sample post.",
    "created_at": ISODate("2020-09-15T10:45:00Z"),
    "likes": 10
  }
  ```

## MySQL

### Table: posts

- **Description**: Contains user-created posts.

| Column      | Type           | PK  | FK           | NN  | Unique | Sample Values |
|-------------|----------------|-----|--------------|-----|--------|---------------|
| post_id     | Integer        | Yes |              | Yes | Yes    | 1, 2          |
| user_id     | Integer        |     | References users | Yes | Yes | 1, 2          |
| content     | TEXT           |     |              | No  | No     | 'This is a sample post.', 'Another post example.' |
| created_at  | DATETIME       |     |              | No  | No     | '2020-09-15 10:45:00', '2020-09-16 09:15:00'     |
| likes       | Integer        |     |              | No  | No     | 10, 15         |
| contains_1  | [Type]         |     | [Specify]    | Yes | Yes    | [Sample Value]|
| contains_2  | [Type]         |     |              |     |        | [Sample Value]|

### Relationships

- **users.user_id -> posts.user_id**: One-to-Many relationship between users and their posts.

