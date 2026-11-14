# Privacy Policy for Element EQ

**Effective Date:** November 14, 2026  
**Last Updated:** November 14, 2026

**Element EQ** ("we", "our", or "us"), developed and operated by **Anugrah Korambeth** ("Service Provider"), is committed to protecting your privacy.

This Privacy Policy explains how Element EQ (Application ID: `com.elementeq.app`) collects, accesses, processes, stores, and protects information when you use our Android application.

Element EQ is an audio equalizer application that provides audio customization, real-time audio processing, equalizer presets, audio visualization, and automated equalizer profile switching.

Our approach prioritizes on-device processing and minimizes the transmission of personal information.

---

## 1. Summary of Privacy Principles

- **No audio recording or uploading:** Audio captured for real-time processing is processed locally in memory. The Application does not intentionally record or upload captured microphone audio to external servers.
- **No selling of personal information:** We do not sell, rent, or trade your personal information.
- **Local-first architecture:** Your custom equalizer presets, configurations, automation rules, and preferences are stored locally on your device.
- **Optional cloud backup:** Google Drive integration is optional and requires you to explicitly connect your Google account.
- **Minimal third-party services:** We use Firebase Crashlytics for application diagnostics and Google services where required for application functionality and optional backups.

---

## 2. Information We Access and Process

### A. Real-Time Audio Data (Microphone and Audio Processing)

**What we access:**

Element EQ may access real-time audio input through Android audio APIs, including `AudioRecord`, where microphone-based functionality is used.

The Application also uses Android audio processing capabilities, including `DynamicsProcessing`, where supported by the device and Android version.

**Why we need it:**

- To provide the Live Listen feature, which allows real-time microphone audio processing through equalizer settings.
- To power real-time frequency spectrum visualization.
- To display audio levels, peak measurements, and related visual feedback.

**Privacy practices:**

Audio captured for real-time processing is processed locally in volatile memory (RAM).

The Application does not intentionally:

- Record microphone audio into permanent audio files.
- Store captured microphone recordings on disk.
- Upload captured microphone audio to the Service Provider's servers.
- Transmit captured microphone recordings to third-party analytics or advertising services.

These practices apply to audio capture and processing performed by Element EQ itself. Other applications or Android system services may independently process audio according to their own functionality and privacy policies.

### B. Media Playback and Notification Information

**What we access:**

Element EQ uses Android's `NotificationListenerService` when the user explicitly enables Notification Access.

This allows the Application to receive information about active media notifications.

**Why we need it:**

- To identify the currently active media application.
- To support automated per-app equalizer profile switching.
- To associate playback activity with user-configured equalizer rules.

**Privacy practices:**

Element EQ is designed to extract only the application package identifier needed for identifying the active media application.

The Application does not intentionally collect or store notification message content, private conversations, sender names, or other personal notification information for its equalizer functionality.

Notification Access is an optional Android permission that must be enabled by the user through Android system settings.

### C. Bluetooth and Connected Audio Devices

**What we access:**

Depending on the Android version and functionality used, Element EQ may request:

- `BLUETOOTH_CONNECT`
- `BLUETOOTH_SCAN`

**Why we need it:**

- To detect connected Bluetooth audio devices.
- To identify audio device connection and disconnection events.
- To support automatic switching between device-specific equalizer profiles.

**Privacy practices:**

Bluetooth device information, such as device names, types, and identifiers, may be accessed to provide these features.

This information is used for local audio-device detection and equalizer profile management.

Element EQ does not intentionally use Bluetooth information to determine, track, or infer your physical location.

Where supported, the Application uses Android's `neverForLocation` permission flag for Bluetooth scanning.

### D. Installed Applications Information

**What we access:**

Element EQ may use Android package visibility capabilities, including `QUERY_ALL_PACKAGES`, where required by the implemented functionality.

**Why we need it:**

- To display compatible installed media applications.
- To allow users to select applications for per-app equalizer configurations.
- To configure application-specific audio automation rules.

**Privacy practices:**

Installed application information is accessed locally for the relevant functionality.

The Application does not intentionally upload the installed application list to the Service Provider's servers or use it for advertising or user profiling.

### E. Equalizer Settings, Presets and Preferences

Element EQ stores application settings and user configurations locally on your device.

These may include:

- Equalizer frequency gains and configurations.
- Parametric equalizer settings.
- Bass, treble, balance, and other audio adjustments.
- Custom equalizer presets and names.
- Per-app equalizer rules.
- Bluetooth device-specific profiles.
- Automation settings and timers.
- Application preferences and visual themes.

This information is stored using Android's private application storage mechanisms, including `SharedPreferences` and the local database used by the Application.

This information is not transmitted to external servers unless you explicitly use a feature that requires such transmission, such as Google Drive backup.

---

## 3. Optional Google Drive Backup

Element EQ provides an optional Google Drive backup feature to allow users to back up and restore their equalizer presets and configurations.

**User consent:**

- Google Drive backup is optional.
- Connecting a Google account requires an explicit user action.
- Backup operations are initiated through the Application's backup functionality.

**Scope of access:**

Element EQ uses the following Google Drive OAuth scope:

`https://www.googleapis.com/auth/drive.appdata`

This scope provides access to the application's dedicated Google Drive application data area.

It does not grant general access to browse the user's personal Google Drive files and folders.

**Information backed up:**

Depending on the backup implementation, the Application may upload:

- Custom equalizer presets.
- Equalizer configurations.
- Application-specific preferences.
- Supported automation rules and settings.

Microphone recordings, personal conversations, and unrelated personal files are not included in the Application's intended backup data.

**Backup deletion:**

Users can delete their application backup through the available backup functionality, where supported, or manage the Application's Google account access through their Google Account settings.

Disconnecting Google Drive access does not necessarily delete previously created backup files. Existing backup files may need to be deleted separately.

Google Privacy Policy:

https://policies.google.com/privacy

---

## 4. Third-Party Services and Diagnostics

Element EQ uses third-party services to support application stability and functionality.

### Firebase Crashlytics

**Provider:** Google LLC

**Purpose:**

Firebase Crashlytics is used to identify application crashes, diagnose technical problems, and improve application stability.

**Information that may be collected includes:**

- Crash reports and diagnostic stack traces.
- Device model and manufacturer.
- Android operating system version.
- Application version.
- Application installation identifiers.
- Technical information associated with application crashes.

This information helps identify and resolve software issues.

Crash diagnostic information may be processed by Google in accordance with its privacy practices and retention policies.

Firebase Privacy and Security Information:

https://firebase.google.com/support/privacy

### Google Play Services

Element EQ may use Google Play Services to support Android application functionality and integration with Google services.

Google Play Services may process technical information according to Google's applicable privacy policies.

Google Privacy Policy:

https://policies.google.com/privacy

The Service Provider does not control the independent data processing practices of these third-party providers.

---

## 5. Android Permissions and Their Purposes

Element EQ may request the following Android permissions depending on the features implemented and supported by the device.

| Permission | Technical Name | Purpose |
|---|---|---|
| Microphone | `RECORD_AUDIO` | Enables microphone-based Live Listen and real-time audio analysis. |
| Modify Audio Settings | `MODIFY_AUDIO_SETTINGS` | Allows interaction with Android audio settings and audio routing. |
| Foreground Service | `FOREGROUND_SERVICE` | Supports eligible long-running application operations. |
| Media Playback Foreground Service | `FOREGROUND_SERVICE_MEDIA_PLAYBACK` | Supports foreground media playback functionality where implemented. |
| Microphone Foreground Service | `FOREGROUND_SERVICE_MICROPHONE` | Supports eligible microphone operations in a foreground service. |
| Bluetooth Connect | `BLUETOOTH_CONNECT` | Detects and interacts with connected Bluetooth audio devices. |
| Bluetooth Scan | `BLUETOOTH_SCAN` | Detects nearby Bluetooth devices for audio-device profile functionality. |
| Notifications | `POST_NOTIFICATIONS` | Displays application notifications, service status, and timer alerts. |
| Notification Listener | `BIND_NOTIFICATION_LISTENER_SERVICE` | Allows the user-enabled notification listener service to identify active media applications. |
| Installed Applications Visibility | `QUERY_ALL_PACKAGES` | Supports installed media application selection and per-app equalizer configuration, where required. |
| Device Boot | `RECEIVE_BOOT_COMPLETED` | Supports restoration of eligible application services or scheduled functionality after device restart. |

Some permissions require explicit user approval through Android system settings.

Users can manage or revoke permissions through their device settings. Revoking certain permissions may affect the corresponding application features.

---

## 6. Data Retention and Deletion

### Locally Stored Information

Equalizer presets, custom configurations, application preferences, and supported automation settings remain stored locally on your device until they are deleted by the user or the Application's local storage is cleared.

You can remove locally stored information by:

- Using available deletion options within Element EQ.
- Clearing the Application's storage through Android settings.
- Uninstalling the Application.

Uninstalling the Application generally removes its locally stored private application data.

### Google Drive Backup Data

If you use Google Drive backup, backup files may remain in your Google Drive until you explicitly delete them.

You can manage or delete these files using the Application's backup functionality, where supported, or through the relevant Google account controls.

### Diagnostic Information

Information collected by Firebase Crashlytics and other third-party services is retained according to their respective retention policies.

The Service Provider does not independently control the retention periods of information held by these providers.

For privacy-related requests, contact:

**Email:** hello@elementeq.app

---

## 7. Data Sharing and Disclosure

The Service Provider does not sell, rent, or trade personal information.

Information may be processed or disclosed in the following circumstances:

- **Third-party service providers:** To support application functionality, crash diagnostics, and optional cloud backup.
- **Legal obligations:** When disclosure is required by applicable laws, regulations, court orders, or legal processes.
- **Security and protection:** When reasonably necessary to protect the rights, safety, or security of users, the Service Provider, or others.
- **Business transfers:** In connection with a merger, acquisition, restructuring, or transfer of business assets, subject to applicable privacy requirements.

The Application is not designed to share microphone recordings, private conversations, or personal audio content with advertising networks.

---

## 8. International Data Transfers

Certain third-party service providers, including Google, may process technical or diagnostic information on servers located outside your country of residence.

Where applicable, such transfers will be subject to the safeguards and transfer mechanisms required by relevant data protection laws.

Users are encouraged to review the privacy policies of the relevant third-party providers for additional information.

---

## 9. Children's Privacy

Element EQ is a general-purpose audio utility application and is not specifically directed toward children.

The Service Provider does not knowingly collect personal information from children under the age of 13 in violation of applicable privacy laws.

Where local laws establish a higher minimum age or require parental or guardian consent, those requirements will apply.

If the Service Provider becomes aware that personal information has been collected from a child in violation of applicable law, appropriate steps will be taken to address and delete such information where required.

Parents or legal guardians who have concerns regarding their child's information may contact the Service Provider.

**Email:** hello@elementeq.app

---

## 10. Security

The Service Provider takes reasonable measures to protect information processed by the Application.

These measures include:

- Using Android's application sandbox and private application storage mechanisms.
- Minimizing the collection and transmission of personal information.
- Processing supported audio functionality locally on the device.
- Using established third-party services for diagnostics and cloud functionality.
- Using encrypted HTTPS/TLS connections for supported communications with external services.

However, no method of electronic storage or transmission can be guaranteed to be completely secure.

Users should also take reasonable precautions to protect their devices and Google accounts.

---

## 11. Your Privacy Rights

Depending on your location and applicable data protection laws, you may have rights regarding your personal information.

These may include:

- Requesting access to personal information.
- Requesting correction of inaccurate information.
- Requesting deletion of personal information.
- Withdrawing consent where processing is based on consent.
- Objecting to certain processing activities.
- Requesting information about how personal information is processed or shared.

To exercise applicable rights, contact:

**Email:** hello@elementeq.app

The Service Provider will handle requests in accordance with applicable privacy laws.

Please note that certain technical or diagnostic information may be independently controlled by third-party service providers.

---

## 12. California Privacy Rights

California residents may have additional rights under applicable California privacy laws, including the California Consumer Privacy Act (CCPA), as amended by the California Privacy Rights Act (CPRA).

Where applicable, these rights may include:

- The right to know what personal information is collected.
- The right to request deletion of personal information.
- The right to request correction of inaccurate personal information.
- The right to opt out of the sale or sharing of personal information.
- The right to non-discrimination for exercising privacy rights.

The Service Provider does not sell personal information.

To submit a privacy-related request, contact:

**Email:** hello@elementeq.app

---

## 13. Changes to This Privacy Policy

The Service Provider may update this Privacy Policy from time to time to reflect changes in the Application, its features, third-party services, or applicable legal requirements.

Any updates will be published on this page with a revised "Last Updated" date.

Users are encouraged to review this Privacy Policy periodically.

Where required by applicable law, the Service Provider will obtain consent or provide additional notice before implementing changes that require it.

---

## 14. Contact Us

If you have questions, concerns, or requests regarding this Privacy Policy or the handling of information by Element EQ, please contact:

**Application:** Element EQ  
**Application ID:** `com.elementeq.app`  
**Developer:** Anugrah Korambeth  
**Email:** hello@elementeq.app  
**Alternative Email:** kdevproject14@gmail.com  
**Website:** https://elementeq.app

We will make reasonable efforts to respond to privacy-related inquiries.
