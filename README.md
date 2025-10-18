Pak Charity is a mobile app that links people in need with verified donors. It adds an admin review step, push notifications, and a donation progress bar to keep each request on track. Built with Flutter and Firebase as part of a BSCS thesis.
# At a glance

Roles: Recipient, Donor, Admin. 
Core flows: sign-up/login, post request (recipient), admin approval, donate (donor), progress tracking.
Tech stack: Flutter (Dart), Android Studio, Firebase (Auth/DB), push notifications, card payment gateway. 
Target platforms: Android (API 16+) and iOS 9+. 
Process: Incremental model with defined milestones, test cases, and UI/UML design assets. 

# Features

Recipient posts a donation request with title, description, amount, type, and image. 
Admin verifies and accepts/declines requests before they go live. 
Donor browses events and pays by card; progress bar updates after each donation. 
Push notifications for approvals and status updates. 
Donor/recipient profiles and basic history stored in Firebase. 

# Screens

Splash, Onboarding, Sign-up/Sign-in, Donor Dashboard, Admin portal, Recipient Request, Donations.

Architecture and design

Event-driven flow: user actions trigger notifications and state changes across roles. 

UML: use cases, activity, sequence, class, state, data-flow, and component diagrams included in the thesis.

# Test coverage

Black-box test cases for: Log in, Update profile, Sign up, Post request, Donate, Admin decision; each with normal/abnormal inputs and expected results. Bsc_Thesis_Faheem.pdf chapter 6 for full tables and screenshots.

# Prerequisites

Flutter SDK and Android Studio (or Xcode for iOS). 
Firebase project (enable Auth and a database). 
Card payment gateway credentials (test mode is fine for dev). 

# Setup

Clone the repo and open the app/ folder.
Run flutter pub get.
Add google-services.json (Android) and/or GoogleService-Info.plist (iOS).
Configure your payment keys in the app’s config.
flutter run to launch on a device or emulator.
Notes: Minimum Android API 16; iOS 9+. Performance depends on device and network. 

# Security and data

Authenticated access for both donors and recipients; personal data not shared with third parties.
Use HTTPS, platform keystore, and Firebase security rules. The thesis targets end-to-end protection of personal info. Review and harden rules before production.

# Known limitations

Platform/version dependency, possible app crashes, and device variability; reliance on network speed. Monitor, log, and test across devices.

