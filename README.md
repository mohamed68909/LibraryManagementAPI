<div align="center">

# Library Management API

![.NET](https://img.shields.io/badge/.NET_Web_API-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=csharp&logoColor=white)
![EF Core](https://img.shields.io/badge/EF_Core-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
[![Stars](https://img.shields.io/github/stars/mohamed68909/LibraryManagementAPI?style=for-the-badge&color=yellow)](https://github.com/mohamed68909/LibraryManagementAPI/stargazers)

A RESTful API for managing library resources â€” books, members, and borrowing records â€” built with ASP.NET Core Web API and Entity Framework Core.

</div>

---

## Overview

The Library Management API provides a complete backend solution for library operations including book catalog management, member registration, and borrowing tracking with due date enforcement.

---

## Tech Stack

| Technology | Version |
|-----------|---------|
| ASP.NET Core Web API | 8.0 |
| Entity Framework Core | 8.0 |
| SQL Server | 2019+ |
| Swagger / OpenAPI | 6.0 |
| C# | 12 |

---

## Key Features

- **Book Management** â€” Full CRUD for books with category and author tracking
- **Member Management** â€” Register and manage library members
- **Borrowing System** â€” Issue, return, and track borrowed books
- **Due Date Tracking** â€” Automatic overdue detection
- **Swagger UI** â€” Interactive API documentation
- **Pagination** â€” Efficient data retrieval for large collections
- **Validation** â€” Input validation using Data Annotations

---

## Getting Started

### Prerequisites
- .NET 8 SDK
- SQL Server

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/mohamed68909/LibraryManagementAPI.git
cd LibraryManagementAPI

# 2. Restore packages
dotnet restore

# 3. Set connection string in appsettings.json

# 4. Run migrations
dotnet ef database update

# 5. Start the API
dotnet run
```

Open Swagger UI at: `https://localhost:5001/swagger`

---

## API Endpoints

### Books
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | /api/books | Get all books (paginated) |
| GET | /api/books/{id} | Get book by ID |
| POST | /api/books | Add new book |
| PUT | /api/books/{id} | Update book info |
| DELETE | /api/books/{id} | Remove book |

### Members
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | /api/members | Get all members |
| POST | /api/members | Register new member |
| GET | /api/members/{id} | Get member details |

### Borrowing
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | /api/borrow | Issue a book |
| PUT | /api/borrow/{id}/return | Return a book |
| GET | /api/borrow/overdue | Get overdue books |

---

## License

MIT License â€” see [LICENSE](LICENSE) for details.

---

<div align="center">
  Built by <a href="https://github.com/mohamed68909">Mohamed Ashraf</a>
</div>