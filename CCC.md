# Sport Club App 🏆

A modern Flutter application for sports community connection, venue booking, and club management. Built with Flutter 3.x, this app provides a seamless experience for sports enthusiasts to discover clubs, book venues, create meets, and connect with teammates.

## ✨ Features

### 🏠 Core Features

- **Home Dashboard**: Personalized greeting, location-based sports & classes, quick actions
- **Club Discovery**: Browse and search sports clubs with filters, ratings, and detailed views
- **Venue Booking**: Find and book sports venues with real-time availability
- **Payment System**: Integrated payment flow with QR code confirmation
- **Messaging**: Direct and group chat for team communication
- **Premium Membership**: One Pass subscription for unlimited access

### 👥 Club Management

- **Create Club**: Multi-step flow to create and customize your sports club
- **Member Management**: Admin and member roles with circular avatar grids
- **Activities Feed**: Post events, two-way matches, and updates
- **Media Gallery**: Share and browse club photos in grid layout

### 🎯 Meet & Match

- **Create Meets**: Organize pickup games and tournaments
- **Discover Meets**: Find nearby sports activities
- **Join & RSVP**: Easy registration for events

### 👤 User Profile

- **Profile Customization**: Edit profile, settings, and preferences
- **My Bookings**: View and manage venue reservations
- **Notification Center**: Stay updated with app activities

## 🛠️ Tech Stack

### Framework & Language

- **Flutter**: 3.4.3+
- **Dart**: SDK >=3.4.3 <4.0.0

### State Management & Architecture

- **Provider**: State management and dependency injection
- **GetIt**: Service locator for dependency injection

### Navigation

- **GoRouter**: Declarative routing with nested navigation and deep linking

### UI & Design

- **flutter_screenutil**: Responsive sizing across devices
- **google_fonts**: Geist font family
- **lottie**: Smooth animations
- **flutter_animate**: Advanced UI animations
- **animated_text_kit**: Text animations
- **shimmer**: Loading placeholders

### Backend & Services

- **Firebase Core**: App initialization
- **Firebase Auth**: Authentication (email/password, Google Sign-In)
- **Cloud Firestore**: Real-time database
- **Firebase Messaging**: Push notifications
- **flutter_local_notifications**: Local notification handling

### Maps & Location

- **google_maps_flutter**: Interactive maps for venue locations
- **geolocator**: Location services and distance calculations

### Media & Assets

- **cached_network_image**: Optimized image loading and caching
- **image_picker**: Camera and gallery access
- **flutter_svg**: SVG asset support

### Storage & Data

- **Hive**: Local NoSQL database
- **shared_preferences**: Key-value storage
- **path_provider**: File system access

### Networking

- **Dio**: HTTP client with interceptors
- **connectivity_plus**: Network status monitoring
- **pretty_dio_logger**: API request/response logging

### Utilities

- **url_launcher**: Open external links
- **qr_flutter**: QR code generation for payments

## 📁 Project Structure

```
lib/
├── core/
│   ├── config/
│   │   ├── app_router.dart          # GoRouter configuration
│   │   └── app_constants.dart       # App-wide constants
│   └── utils/
│       └── theme_extensions.dart    # Theme helper extensions
├── data/
│   └── models/
│       └── create_club_data.dart    # Club creation data model
├── providers/
│   └── auth_provider.dart           # Authentication state management
├── screens/
│   ├── auth/                        # Authentication screens
│   ├── booking/                     # Venue booking flow
│   ├── create_club/                 # Club creation flow
│   ├── discover/                    # Club discovery & details
│   ├── main/                        # Main navigation screens
│   ├── meets/                       # Meet creation & listing
│   ├── messages/                    # Chat & messaging
│   ├── profile/                     # User profile & settings
│   └── splash/                      # Splash screen
├── widgets/
│   ├── common/                      # Reusable widgets
│   └── custom_navigation_bar.dart   # Bottom navigation bar
├── firebase_options.dart            # Firebase configuration
└── main.dart                        # App entry point

assets/
├── fonts/                           # Geist font family
├── png/                             # PNG images
└── svg/                             # SVG icons
```

## 🚀 Getting Started

### Prerequisites

- Flutter SDK (3.4.3 or higher)
- Dart SDK (3.4.3 or higher)
- Android Studio / VS Code with Flutter extensions
- Firebase account and project setup

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/sniren210/sport_club_app.git
   cd sport_club_app
   ```

2. **Install dependencies**

   ```bash
   flutter pub get
   ```

3. **Firebase Setup**

   - Create a Firebase project at [Firebase Console](https://console.firebase.google.com/)
   - Add Android and iOS apps to your Firebase project
   - Download `google-services.json` (Android) and `GoogleService-Info.plist` (iOS)
   - Place them in the respective platform directories
   - Run FlutterFire CLI to configure:
     ```bash
     flutterfire configure
     ```

4. **Google Maps Setup**

   - Get API keys from [Google Cloud Console](https://console.cloud.google.com/)
   - Enable Maps SDK for Android/iOS
   - Add your API key to:
     - Android: `android/app/src/main/AndroidManifest.xml`
     - iOS: `ios/Runner/AppDelegate.swift`

5. **Run the app**
   ```bash
   flutter run
   ```

### Build Commands

**Development build**

```bash
flutter run --debug
```

**Release build (Android)**

```bash
flutter build apk --release
flutter build appbundle --release
```

**Release build (iOS)**

```bash
flutter build ios --release
```

## 🎨 Design System

### Theme

- **Primary Color**: Custom sport-themed primary
- **Secondary Color**: Accent yellow
- **Tertiary Color**: Supporting accent
- **Typography**: Geist font family (Thin to Black weights)
- **Spacing**: Consistent ScreenUtil-based responsive sizing

### Navigation

- **Bottom Navigation**: Custom glass-styled navigation bar
- **Routing**: Declarative GoRouter with nested routes
- **Deep Linking**: Support for `/discover/club/:id`, `/booking/venue/:id`, etc.

## 🔐 Authentication

The app supports multiple authentication methods:

- Email/Password with email verification
- Google Sign-In
- Password reset via OTP
- Onboarding flow for new users

## 📱 Key Screens

### Home

- Personalized greeting and location
- "One Pass" premium CTA cards
- Sports & classes near you
- Promotional banners

### Club Details

- Club information with avatar and badges
- Three tabs: Members, Activities, Media
- Admin and member sections
- Activity feed with like/comment
- Media gallery with full-screen preview

### Venue Details

- Image carousel with indicators
- Venue information (hours, phone, location)
- Google Maps integration
- Price and booking CTA

### Payment Flow

1. Venue selection → Details
2. Payment details with booking summary
3. Payment success with QR code
4. Back to home

### Create Club Flow

1. Introduction
2. Name your club
3. Select sport
4. Select skill level
5. Select location

## 🧪 Testing

Run tests:

```bash
flutter test
```

Run with coverage:

```bash
flutter test --coverage
```

## 🏗️ Build & Release

### Android

1. Update version in `pubspec.yaml`
2. Update `android/app/build.gradle` version codes
3. Build release:
   ```bash
   flutter build appbundle --release
   ```
4. Upload to Play Console

### iOS

1. Update version in `pubspec.yaml`
2. Update Xcode project version
3. Build release:
   ```bash
   flutter build ios --release
   ```
4. Archive and upload via Xcode

## 📄 License

This project is private and proprietary.

## 👨‍💻 Author

**sniren210**

- GitHub: [@sniren210](https://github.com/sniren210)

## 🤝 Contributing

This is a private project. For collaboration inquiries, please contact the repository owner.

## 📞 Support

For issues and feature requests, please open an issue in the GitHub repository.

---

Built with ❤️ using Flutter
