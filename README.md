Joseph Nmaawie Beresie 

this web app consists of 4 main pages a store where public can view books,a download page where books can be downloaded,a login page for the writers dashboard ,a dashboard where a user can add ,delete and edit books

to run the app

start server
npm i
npm run dev

start backend server
cd backend/BookStore.API
dotnet restore
dotnet run

if you run into trouble connecting with the database because of ip if running on ipv6
backend/BookStore.API/appsettings.json
replace connectionstring
{
  "ConnectionStrings": {
    "DefaultConnection": "Host=db.pwbpbsyagyoytniidoah.supabase.co;Database=postgres;Username=postgres;Password=[YOUR-PASSWORD];SSL Mode=Require;Trust Server Certificate=true"
  }
}

password is in appsettings.json

dotnet run

technologies used 

React Router for navigation
Bootstrap 5 with custom CSS for responsive design
Lucide React for modern icons
Vite for fast development and building
Axios for HTTP requests to the backend API

JWT-based authentication via .NET Core API
for api calls authentication and user authentication

Entity Framework Core
to simplify database migrations and access

.NET Core Web API
for backend api controllers

React + TypeScript

for modern frontend 

Backend structure

BookStore.API/
├── Controllers/
│   ├── AuthController.cs      # Authentication endpoints
│   └── BooksController.cs     # Book CRUD endpoints
├── Data/
│   └── BookStoreContext.cs    # Entity Framework DbContext
├── DTOs/
│   ├── AuthDTOs.cs           # Authentication data transfer objects
│   └── BookDTOs.cs           # Book data transfer objects
├── Models/
│   ├── User.cs               # User entity model
│   └── Book.cs               # Book entity model
├── Repositories/
│   ├── IUserRepository.cs    # User repository interface
│   ├── UserRepository.cs     # User repository implementation
│   ├── IBookRepository.cs    # Book repository interface
│   └── BookRepository.cs     # Book repository implementation
├── Services/
│   ├── ITokenService.cs      # JWT token service interface
│   └── TokenService.cs       # JWT token service implementation
├── Program.cs                # Application startup and configuration
├── appsettings.json          # Production configuration
└── appsettings.Development.json # Development configuration
