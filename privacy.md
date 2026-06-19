# Privacy Policy - ArgusApps

**Effective date:** 2026-05-11.
**Last updated:** 2026-06-19.
**Apps:** This policy covers all apps published under the ArgusApps brand, including:
- Argus Scan (package `dev.appengine.app_001_document_scanner`) - document scanner with OCR
- Argus Edit (package `dev.appengine.app_002_photo_editor`) - photo editor with background removal

**Developer:** ArgusApps, sole trader, United Kingdom.
**Contact:** sirreignbatt3@gmail.com

---

## Summary

ArgusApps are designed to keep your content on your phone. We do not have a server. We do not sync your files. We do not have your account. The only personal data leaving your device goes to (1) Google AdMob, which serves the optional rewarded video ads, and (2) Google Firebase Crashlytics, which receives sanitized crash reports so we can fix bugs.

If you accept the rewarded-ad consent on first launch (EU and UK users), Google AdMob may collect your advertising identifier, an IP-derived approximate location, and your device model and OS version to serve and measure ads. You can revoke consent at any time via Settings -> Privacy.

If you buy the lifetime ad-removal in-app purchase, advertising data collection stops entirely for that device. Google Play handles the purchase; we never see your payment details.

You can use our apps fully without granting any storage permission beyond the per-file picker (Storage Access Framework). Camera permission is requested only for capture screens (scanning documents or taking photos to edit); you can always fall back to picking existing photos from your gallery instead.

## 1. Who we are

ArgusApps is a portfolio of mobile utility apps operated by a UK-based sole trader. For the purpose of UK GDPR and the EU GDPR (where applicable), the data controller is:

```
George Alexander, trading as ArgusApps
United Kingdom
Email: sirreignbatt3@gmail.com
```

If you need to send formal correspondence by post, contact us at the email above and we will provide a postal address on request.

## 2. What data we collect

### 2.1 Your content - we do not collect it

All content you create or import stays on your device:

- **Argus Scan:** Document images and any text recognized from them (OCR) are processed entirely on your device using on-device machine learning (Google ML Kit). We never receive, transmit, or store your document contents.
- **Argus Edit:** Photos you edit, crop, annotate, or enhance stay on your device. Background removal and other image processing use on-device machine learning models that run locally - your photos are never sent to any server.

Content is stored in app-managed storage or where you choose to save it via the Android Storage Access Framework.

### 2.2 Crash diagnostics - sanitized, via Firebase Crashlytics

When the app crashes, a sanitized error report is sent to Google Firebase Crashlytics so we can diagnose and fix the bug. Before sending, our internal sanitizer (`CrashSanitizer`) removes or truncates:

- Absolute file paths beyond filename
- Long string blobs that may contain document text
- Metadata keys known to contain document contents (e.g. `ocrText`, `pageContent`)

Crashlytics still receives the following operational data: app version, device model, OS version, the stack trace, and a Crashlytics-assigned installation ID (not linked to your Google account). File contents (documents, photos) are never included in crash reports.

Legal basis (UK GDPR / EU GDPR): legitimate interest in maintaining a working app. You can disable Crashlytics from Settings -> Privacy.

### 2.3 Advertising - Google AdMob

If you watch a rewarded video ad, or if you have not bought the ad-removal IAP, Google AdMob runs in your app session. AdMob may collect:

- Advertising identifier (Android Advertising ID; resettable in your device settings)
- Approximate location derived from IP address
- Device model, OS version, app version
- Ad interaction events (ad load, ad shown, ad click, reward grant)

Where required by law (EU and UK), we present a Google User Messaging Platform (UMP) consent form before AdMob initializes. Without consent, AdMob serves non-personalized ads only.

Legal basis (UK GDPR / EU GDPR):
- Consent for personalized advertising and for any non-essential cookies/identifiers via the UMP consent form.
- Legitimate interest for non-personalized advertising where consent was not granted but the app is funded via ads.

You can:
- Revoke consent at any time via Settings -> Privacy -> Reset advertising consent.
- Buy the lifetime ad-removal IAP to disable ad collection entirely on this device.
- Reset your Android Advertising ID via Android system settings.

Google AdMob is operated by Google LLC and (in the UK) Google Ireland Limited. Their privacy policy is at https://policies.google.com/privacy and their advertising policies at https://policies.google.com/technologies/ads.

### 2.4 In-app purchase

If you buy the lifetime ad-removal, the purchase is processed by Google Play. We receive only a token from Google Play confirming entitlement; we do not see your payment method, billing address, or Google account email. Google Play's privacy policy applies: https://policies.google.com/privacy.

### 2.5 On-device machine learning

Some features use machine learning models that run entirely on your device:

- **OCR** (Argus Scan): Google ML Kit Text Recognition processes document images locally to extract text. No images or text are sent to Google's servers.
- **Background removal** (Argus Edit): Google ML Kit Selfie/Subject Segmentation processes photos locally to separate foreground from background. No images are sent to Google's servers.

These models are bundled with the app or downloaded once via Google Play Services. The ML processing itself is fully offline and local.

### 2.6 Permissions we ask for

- **Camera:** used for capturing documents (Scan) or photos to edit (Edit). If denied, you can use the gallery-picker fallback in both apps.
- **Storage Access Framework:** you choose the file when you import or export. We do not request `MANAGE_EXTERNAL_STORAGE` and we do not browse your storage.
- **Internet:** required for serving ads and for the optional crash-report transmission.

We do not request: location services, contacts, microphone, calendar, SMS, call log, or biometrics.

## 3. Children's privacy

ArgusApps are not directed to children under 13. We do not knowingly collect personal data from anyone under 13. If you believe a child has used one of our apps and we hold their data via the AdMob pipeline, contact us at the email below and we will assist with deletion requests passed to Google.

## 4. International transfers

Data sent to Google AdMob and Firebase Crashlytics may be processed in the United States or other countries outside the UK / EEA. Google relies on Standard Contractual Clauses (SCCs) and the UK International Data Transfer Addendum to safeguard such transfers. See Google's policy at https://privacy.google.com/businesses/processorterms/.

## 5. Your rights under UK and EU GDPR

You have the right to:
- **Access** the personal data we hold about you (DSAR).
- **Rectify** inaccurate data.
- **Erase** your data ("right to be forgotten").
- **Restrict** processing.
- **Object** to processing based on legitimate interest.
- **Portability** of data you provided.
- **Withdraw consent** at any time (does not affect the lawfulness of prior consent-based processing).

To exercise any of these rights, email us. We respond within 30 days.

You also have the right to complain to:
- UK: Information Commissioner's Office (https://ico.org.uk), tel 0303 123 1113.
- EU: your national data protection authority.

## 6. Data retention

- **Crash reports:** Firebase Crashlytics retains data for 90 days by default.
- **Advertising identifiers:** Google AdMob retains as described in their policy. You can reset the Advertising ID at any time in Android Settings.
- **On-device files (documents, photos, edits):** retained until you delete them or uninstall the app.
- **IAP entitlement:** retained by Google Play until you uninstall the app or revoke the purchase.

We do not hold any personal data on our own servers. We have no servers.

## 7. Security

- All third-party transmissions (AdMob, Crashlytics) use HTTPS / TLS.
- The app does not include a debug logging endpoint accessible after install.
- Your content (documents, photos, edits) never leaves your device, so is not subject to transmission-layer risk.
- All machine learning processing (OCR, background removal) runs on-device with no network calls.
- Release builds are signed using Play App Signing.

## 8. Changes to this policy

We may update this policy when we add features or third parties. Material changes will be flagged in the in-app About screen. The "Last updated" line above will reflect the change date.

## 9. Contact

For privacy questions, DSAR requests, or complaints:

```
Email: sirreignbatt3@gmail.com
```

For app support and bugs, use the same email.
