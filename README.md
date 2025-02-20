# Flutter In-App Subscription Implementation

A Flutter application demonstrating in-app subscription implementation with a clean architecture approach and modern UI design. This project showcases how to handle in-app purchases for both iOS and Android platforms.

<div align="center">
  <img src="https://i.imgur.com/YourScreenshotURL.png" alt="Subscription Plans" width="300"/>
</div>

## 🌟 Features

- ✅ In-App Purchase integration
- 🔄 Multiple subscription plans (3, 6, and 12 months)
- 💳 Secure purchase handling
- 🎨 Modern UI design with Material 3
- ⚡ Real-time status updates
- 🔒 Error handling and validation
- 📱 Cross-platform (iOS & Android)
- 🔄 Purchase restoration support

## 🏗 Project Structure

lib/
├── features/
│   └── store/
│       ├── domain/          # State management models
│       │   ├── product_state.dart
│       │   └── purchase_state.dart
│       ├── providers/       # Riverpod providers
│       │   └── subscription_provider.dart
│       └── presentation/│           ├── screens/
│           │   └── subscription_screen.dart
│           └── widgets/
│               ├── subscription_card.dart
│               └── current_plan_card.dart
├── utils/
│   └── app_messages.dart
└── main.dart

## 🚀 Getting Started

### Prerequisites

- Flutter SDK (2.0 or higher)
- Xcode (for iOS)
- Android Studio (for Android)
- Paid Apple Developer account (for iOS)
- Google Play Developer account (for Android)

<div align="center">
  <table>
    <tr>
      <th colspan="2">⚡ Quick Installation Guide</th>
    </tr>
    <tr>
      <td>
        <h4>1. Clone Repository</h4>
        <pre style="background-color: #f6f8fa; padding: 10px; border-radius: 6px;">
git clone https://github.com/yourusername/flutter_iap_store.git</pre>
      </td>
    </tr>
    <tr>
      <td>
        <h4>2. Install Dependencies</h4>
        <pre style="background-color: #f6f8fa; padding: 10px; border-radius: 6px;">
cd flutter_iap_store
flutter pub get</pre>
      </td>
    </tr>
    <tr>
      <td>
        <h4>3. Run Application</h4>
        <pre style="background-color: #f6f8fa; padding: 10px; border-radius: 6px;">
flutter run</pre>
      </td>
    </tr>
    <tr>
      <td>
        <div style="background-color: #fff3cd; padding: 10px; border-radius: 6px; margin-top: 10px;">
          <strong>Note:</strong> Make sure you have Flutter and necessary tools installed on your system.
          <ul>
            <li>Flutter SDK</li>
            <li>Android Studio / Xcode</li>
            <li>A connected device or emulator</li>
          </ul>
        </div>
      </td>
    </tr>
  </table>
</div>

## 📱 Store Configuration

<div align="center">
  <table>
    <tr>
      <th width="50%">iOS Configuration</th>
      <th width="50%">Android Configuration</th>
    </tr>
    <tr>
      <td>
        <h4>Steps:</h4>
        <ol>
          <li>Open App Store Connect</li>
          <li>Go to Features > In-App Purchases</li>
          <li>Create Products with IDs:</li>
        </ol>
        <pre>
ios_3months_sub
ios_6months_sub
ios_12months_sub</pre>
        <h4>Required in Info.plist:</h4>
        <pre>&lt;key&gt;SKPaymentQueue&lt;/key&gt;
&lt;true/&gt;</pre>
        <h4>Requirements:</h4>
        <ul>
          <li>Paid Apple Developer Account</li>
          <li>App Store Connect Setup</li>
          <li>Valid Bundle ID</li>
        </ul>
      </td>
      <td>
        <h4>Steps:</h4>
        <ol>
          <li>Open Google Play Console</li>
          <li>Go to Monetization setup</li>
          <li>Create Products with IDs:</li>
        </ol>
        <pre>
android_3months_sub
android_6months_sub
android_12months_sub</pre>
        <h4>Required in AndroidManifest.xml:</h4>
        <pre>&lt;uses-permission 
android:name="com.android.vending.BILLING" /&gt;</pre>
        <h4>Requirements:</h4>
        <ul>
          <li>Google Play Console Account</li>
          <li>One-time Registration Fee</li>
          <li>Valid Package Name</li>
        </ul>
      </td>
    </tr>
  </table>
</div>

<div align="center">
  <table>
    <tr>
      <th colspan="2">Testing Instructions</th>
    </tr>
    <tr>
      <td width="50%">
        <h4>iOS Testing</h4>
        <ul>
          <li>Create Sandbox Accounts</li>
          <li>Use TestFlight for testing</li>
          <li>Test on real iOS devices</li>
        </ul>
      </td>
      <td width="50%">
        <h4>Android Testing</h4>
        <ul>
          <li>Set up License Testing</li>
          <li>Use Internal Testing Track</li>
          <li>Test on real Android devices</li>
        </ul>
      </td>
    </tr>
  </table>
</div>

<div align="center">
  <table>
    <tr>
      <th>⚠️ Important Notes</th>
    </tr>
    <tr>
      <td>
        <ul>
          <li>Always implement server-side receipt validation</li>
          <li>Test purchases in sandbox environment first</li>
          <li>Handle network errors and edge cases</li>
          <li>Store subscription status securely</li>
          <li>Implement restore purchases functionality</li>
        </ul>
      </td>
    </tr>
  </table>
</div>
