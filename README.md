# Swift MVVM Architecture 🚀

A clean and scalable iOS application architecture using **MVVM (Model-View-ViewModel)** pattern in Swift.

---

## 📱 Overview

This project demonstrates how to structure an iOS application using the MVVM architecture pattern for better:

- Code organization
- Maintainability
- Testability
- Scalability
- Separation of concerns

---

# 🧱 Architecture

## MVVM Structure

```bash
Project/
│
├── Model/
├── View/
├── ViewModel/
├── Network/
├── Services/
├── Extensions/
├── Utilities/
└── Resources/
```

---

# 📂 Folder Description

## Model
Contains data structures and business models.

Example:
- User
- Product
- APIResponse

---

## View
Contains UI components.

Example:
- ViewController
- UITableViewCell
- UICollectionViewCell
- Custom Views

---

## ViewModel
Handles presentation logic and prepares data for the View.

Responsibilities:
- API Calls
- Data formatting
- State management
- Business logic

---

## Network
Responsible for API communication.

Example:
- APIManager
- Endpoint
- Request Builder

---

## Services
Reusable app services.

Example:
- Authentication
- Local Storage
- Analytics

---

## Extensions
Swift extensions for reusable helpers.

Example:
- UIColor+Extension
- UIView+Extension

---

## Utilities
Helper classes and common utilities.

Example:
- Constants
- Logger
- Validators

---

# 🔄 MVVM Flow

```text
View → ViewModel → Model
View ← ViewModel ← API/Data
```

The View never directly talks to the Model.

---

# ✨ Features

- Clean MVVM architecture
- Modular structure
- Reusable components
- Easy API integration
- Scalable project setup
- Beginner friendly

---

# 🛠 Technologies

- Swift
- UIKit / SwiftUI
- URLSession / Alamofire
- Combine / RxSwift (Optional)

---

# 🚀 Getting Started

## Requirements

- Xcode 15+
- iOS 15+
- Swift 5.9+

---

## Installation

```bash
git clone https://github.com/your-repository.git
```

Open:

```bash
YourProject.xcodeproj
```

Run the project using:

```bash
⌘ + R
```

---

# 📌 Example MVVM

## Model

```swift
struct User: Codable {
    let name: String
}
```

## ViewModel

```swift
final class UserViewModel {

    private let user: User

    init(user: User) {
        self.user = user
    }

    var username: String {
        user.name
    }
}
```

## ViewController

```swift
final class UserViewController: UIViewController {

    var viewModel: UserViewModel?

    override func viewDidLoad() {
        super.viewDidLoad()

        title = viewModel?.username
    }
}
```

---

# ✅ Best Practices

- Keep ViewController lightweight
- Avoid business logic inside Views
- Use dependency injection
- Write reusable ViewModels
- Separate networking layer

---

# 🧪 Testing

Recommended:
- Unit Test ViewModels
- Mock API Services
- Test business logic independently

---

# 📖 Resources

- Apple Developer Documentation
- Swift.org
- MVVM Design Pattern

---

# 👨‍💻 Author

Developed with ❤️ using Swift MVVM Architecture.

---

# 📄 License

MIT License
