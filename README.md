# NestAway - Property Rental Platform

## 📖 Overview

**NestAway** is a comprehensive web-based property rental management system built with ASP.NET Core MVC. The platform provides an end-to-end solution for property rental operations, enabling users to discover, book, and manage rental accommodations while offering property owners a streamlined listing and booking management system.

## ✨ Features

### 🔐 User Management
- **Secure Registration & Login**: BCrypt password hashing and session management
- **User Profiles**: Personalized user experience with booking history
- **Session Security**: Auto-logout and secure cookie handling

### 🏠 Property Management
- **Property Listings**: Browse 8+ pre-seeded properties across India
- **Advanced Search**: Filter by location, dates, and guest capacity
- **Property Details**: Comprehensive information with images and pricing

### 📅 Booking System (CRUD Operations)
- **Create Bookings**: Real-time availability checking and price calculation
- **View Bookings**: Complete booking history with status tracking
- **Update Bookings**: Modify booking details and status
- **Cancel Bookings**: Soft delete with status updates

### ⭐ Additional Features
- **Wishlist Management**: Save favorite properties for later
- **Reviews & Ratings**: Post-stay feedback system
- **Responsive Design**: Mobile-friendly Bootstrap UI
- **Indian Localization**: Date format (dd/MM/yyyy) and Indian properties

## 🛠️ Technology Stack

- **Backend**: ASP.NET Core MVC, C#
- **Database**: SQL Server / LocalDB
- **ORM**: Entity Framework Core
- **Frontend**: Razor Views, Bootstrap 4/5, HTML5, CSS3, JavaScript
- **Authentication**: Custom implementation with BCrypt
- **Session Management**: ASP.NET Core Session

## 📁 Project Structure

```
NestAway/
├── Controllers/          # MVC Controllers (Account, Booking, Property, etc.)
├── Models/              # Data models (User, Property, Booking, Review, Wishlist)
├── Views/               # Razor views organized by controller
│   ├── Account/         # Login, Register pages
│   ├── Booking/         # Booking management pages
│   ├── Home/            # Homepage and search
│   └── Shared/          # Layout and common views
├── Data/                # Database context and configuration
├── Migrations/          # EF Core database migrations
├── wwwroot/             # Static files (CSS, JS, images)
├── appsettings.json     # Configuration file
└── Program.cs           # Application entry point
```

## 🚀 Getting Started

### Prerequisites
- Visual Studio 2022 or later
- .NET 6.0 or later
- SQL Server or LocalDB

### Installation & Setup

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/nestaway.git
   cd nestaway
   ```

2. **Restore Dependencies**
   ```bash
   dotnet restore
   ```

3. **Update Connection String**
   - Open `appsettings.json`
   - Modify the connection string if needed

4. **Create Database**
   ```bash
   dotnet ef database update
   ```

5. **Run the Application**
   ```bash
   dotnet run
   ```

6. **Access the Application**
   - Open browser and navigate to `https://localhost:7233`

## 💾 Database Schema

### Core Entities
- **User**: Authentication and profile information
- **Property**: Rental property details and pricing
- **Booking**: Reservation records with dates and status
- **Review**: User feedback and ratings
- **Wishlist**: Saved properties for users

### Key Relationships
- User ↔ Booking (1:Many)
- Property ↔ Booking (1:Many)
- User ↔ Review (1:Many)
- Property ↔ Review (1:Many)
- User ↔ Wishlist (1:Many)

## 🎯 Usage Examples

### Creating a Booking
1. Register/Login to the platform
2. Browse available properties
3. Select dates and guest count
4. Complete booking with automatic price calculation
5. View booking confirmation and manage reservations

### Managing Properties (Admin)
1. Access admin panel
2. Add new property listings
3. Update existing property details
4. Monitor booking statistics

## 🔧 Configuration

### Database Configuration
```csharp
// Program.cs
builder.Services.AddDbContext<ApplicationDbContext>(options =>
    options.UseSqlServer(builder.Configuration.GetConnectionString("DefaultConnection")));
```

### Culture Configuration
```csharp
// Indian date format support
var cultureInfo = new CultureInfo("en-IN");
CultureInfo.DefaultThreadCurrentCulture = cultureInfo;
```

## 📸 Screenshots

- **Homepage**: Property listings with search functionality![WhatsApp Image 2025-10-13 at 9 27 21 PM](https://github.com/user-attachments/assets/13efd89f-f2da-4a1c-913a-1a6e95ffbe6b)

- **Login/Register**: Secure authentication system![WhatsApp Image 2025-10-13 at 9 27 24 PM](https://github.com/user-attachments/assets/acca3454-5bff-45e8-82b0-db0004be8ab6) ![WhatsApp Image 2025-09-20 at 6 46 52 PM](https://github.com/user-attachments/assets/a30457ce-9ee9-444c-9809-3618bbbfa6ba)

- **Booking Management**: Complete CRUD operations![WhatsApp Image 2025-10-13 at 9 27 25 PM](https://github.com/user-attachments/assets/14b853d8-941c-430c-8f5d-a12c9d562550) ![WhatsApp Image 2025-09-20 at 6 45 32 PM](https://github.com/user-attachments/assets/06d20e2d-0a84-45ec-9245-aa5753a7a119)

- **Property Details**: Comprehensive property information ![WhatsApp Image 2025-10-13 at 9 27 23 PM (1)](https://github.com/user-attachments/assets/bbf3dbdc-b9ac-416a-b04d-8587961f2f58) ![WhatsApp Image 2025-10-13 at 9 27 22 PM](https://github.com/user-attachments/assets/ddf9694a-a778-403d-b744-7481b92fe109)

- **User Dashboard**: Booking history and wishlist management ![WhatsApp Image 2025-10-13 at 9 27 26 PM](https://github.com/user-attachments/assets/fed6f510-e081-4342-8e6c-a7f61d28940d)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 👨‍💻 Author

**DEEKSHITHA.N**
- GitHub: [@Deeksha765](https://github.com/Deeksha765)
- Email: 12deekshitha@gmail.com

## 🙏 Acknowledgments

- Built as part of Web Development coursework
- Inspired by real-world rental platforms
- Bootstrap for responsive UI components
- Entity Framework team for excellent ORM tools

***

⭐ **Star this repository if it helped you learn ASP.NET Core MVC development!**
