# 📘 Notes & Photo Gallery — Laravel Application

A full-stack Laravel application that allows users to:

 Create, Read, Update, Delete (CRUD) personal Notes  
 Upload, view, and delete Photos  
 Organize photos using Albums  
 Manage their profile  
 Use secure authentication  
 Store images safely inside Laravel storage  

This project follows MVC architecture and uses Laravel's built-in features for authentication, validation, file storage, and routing.

---

##  Features

###  **Notes**
- Create, Read, Update, Delete notes
- Each note belongs only to the logged-in user

### 📷 **Photo Gallery**
- Upload photos (JPG, PNG, JPEG, GIF)
- Each photo belongs to a user & optionally to an album
- Auto-stored inside `storage/app/public/photos`
- Accessible through `/storage/photos/...`

###  **Albums**
- Users can create albums
- Photos can be assigned to albums

###  **User Authentication**
- Login, Register, Logout
- Password hashing and user verification  
- Provided by Laravel Breeze

###  **User Profile**
- Update profile information  
- Update password  
- Delete account  

###  **Custom Frontend**
- Tailwind CSS  
- Blade Templates  
- Custom landing page  
- Custom login & register UI  

---

## 🛠️ Tools & Technologies Used

### **Backend**
| Tool / Technology | Purpose |
|------------------|---------|
| **Laravel 12** | Main backend framework |
| **PHP 8.2** | Server-side language |
| **MySQL** | Database |
| **Composer** | Dependency manager |
| **Laravel Breeze** | Authentication scaffolding |
| **MVC Architecture** | Separation of logic |

### **Frontend**
| Tool / Technology | Purpose |
|------------------|---------|
| **Blade Templates** | HTML templating |
| **Tailwind CSS** | Responsive styling |
| **Bootstrap (optional)** | Additional UI |
| **Custom CSS** | UI enhancements |

### **Storage / File Handling**
- Laravel Storage (`storage/app/public`)
- Symbolic link: `php artisan storage:link`
- Uploaded images stored in `public/storage/photos`

---

##  Project File Structure (Important Files Only)

```
notes-gallery/
│
├── app/
│   ├── Http/Controllers/
│   │      ├── NoteController.php
│   │      ├── PhotoController.php
│   │      ├── AlbumController.php
│   │      └── ProfileController.php
│   ├── Models/
│          ├── User.php
│          ├── Note.php
│          ├── Photo.php
│          └── Album.php
│
├── database/
│   ├── migrations/ (tables)
│   ├── sql/
│   │     └── notes_gallery.sql   <-- your full database export
│
├── resources/views/
│   ├── notes/
│   ├── photos/
│   ├── albums/
│   ├── profile/
│   ├── layouts/
│   └── landing.blade.php
│
├── public/
│   └── storage → storage/app/public (symlink)
│
└── routes/
    ├── web.php
    └── auth.php
```

---

##  Database Setup

###  Your database file is included in:
```
database/sql/notes_gallery.sql
```

###  **To import the database (for anyone using the project):**

1. Open **phpMyAdmin**
2. Create a database:
   ```
   notes_gallery
   ```
3. Go to **Import**
4. Choose:
   ```
   database/sql/notes_gallery.sql
   ```
5. Click **Go**

Database restored successfully 

---

## 🔧 Installation Guide (For Anyone Cloning the Project)

### 1️⃣ Clone the repository
```bash
git clone <your-repository-url>
cd notes-gallery
```

### 2️⃣ Install PHP dependencies
```bash
composer install
```

### 3️⃣ Install Node dependencies (optional)
```bash
npm install
npm run build
```

### 4️⃣ Configure `.env`
Copy the sample:
```bash
cp .env.example .env
```

Generate key:
```bash
php artisan key:generate
```

Update database values:
```
DB_DATABASE=notes_gallery
DB_USERNAME=root
DB_PASSWORD=
```

### 5️⃣ Import SQL Database
(Instruction above)

### 6️⃣ Run migrations (if needed)
```bash
php artisan migrate
```

### 7️⃣ Create storage link
```bash
php artisan storage:link
```

### 8️⃣ Start the server
```bash
php artisan serve
```

App will run at:
```
http://127.0.0.1:8000
```

---

##  Testing the App

### ✔ Add a Note  
Go to `/notes`

### ✔ Upload a Photo  
Go to `/photos`

### ✔ Create Album  
Go to `/albums/create`

### ✔ Update Profile  
Go to `/profile`

---

##  Contributing

If you want to contribute:

1. Fork the repository  
2. Create your feature branch  
3. Submit a pull request  

---

##  License

This project is open-source under the **MIT License**.

---

##  Author

Created by **Jyothishma Gondu**  
For academic project submission (CSCI 6000).

READY FOR GITHUB
If you want, I can ALSO:

✔ Create a PDF from this README
✔ Create a GitHub description
✔ Write a commit message
✔ Write instructions for your professor

Just tell me:

👉 “Make the PDF”







