# EyeRadar

EyeRadar is an iOS research utility designed to capture eye-tracking information while a user reads text. It uses Apple’s ARKit and the TrueDepth front-facing camera to collect derived gaze signals and support the analysis of reading behavior.

The application is intended for research and experimental use.

## Features

- Sign in with Apple authentication
- Text-based reading sessions
- ARKit eye-tracking calibration
- Gaze position and timestamp recording
- Reading-session management
- ZIP export through the iOS share sheet
- Local storage of session data
- In-app account and data deletion

## Requirements

- iPhone with a TrueDepth front camera
- Face ID–supported device
- iOS 18 or later
- Sign in with Apple

## How EyeRadar Works

1. Sign in using Apple.
2. Select a text from the available reading materials.
3. Follow the instructions to begin a reading session.
4. Complete the AR calibration process.
5. Read the selected text while EyeRadar records derived gaze information.
6. Open the **Explorer** tab to review completed sessions.
7. Select one or more sessions and export them as ZIP files.

Personal information can be managed from:

```text
Settings → Personal Info
```

## Collected Data

During an active reading session, EyeRadar may process and save derived eye-tracking information such as:

- Gaze vectors
- ARKit `lookAtPoint` values
- Left and right eye transforms
- Blink openness estimates
- Frame timestamps
- Calibration parameters
- Device and session metadata

These signals may be used to calculate reading-related measurements such as fixation duration, dwell time, fixation count, and gaze movement.

## Privacy

EyeRadar processes eye-tracking signals locally on the device.

The application does not store:

- Raw RGB camera images
- Raw TrueDepth data
- Depth maps
- Full facial geometry or face meshes

Per-frame ARKit information is processed in memory and discarded after use. Saved reading-session data remains on the device unless the user explicitly exports it through the iOS share sheet.

Eye-tracking data is not used for:

- Facial identification
- Authentication
- Advertising
- Marketing
- User profiling

EyeRadar does not automatically upload session data and does not operate a non-Apple backend server.

Read the complete [Privacy Policy](https://nikossmyrnakis.github.io/eyeRadar/privacy.html).

## Account and Data Deletion

Users can delete their account directly from the application:

```text
Settings → Personal Info → Delete Account
```

Deleting an account:

- Removes personal information stored by the application
- Deletes locally stored reading sessions
- Signs the user out on the current device

Uninstalling the application also removes its locally stored data.

## Repository Contents

This repository includes the public support and privacy pages for EyeRadar.

```text
.
├── index.html       # EyeRadar support page
├── privacy.html     # EyeRadar privacy policy
└── README.md        # Project documentation
```

## Running the Website Locally

The support pages are static HTML files and can be opened directly in a browser.

Alternatively, start a local web server from the repository directory:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Deployment

The public pages can be hosted using GitHub Pages.

1. Open the repository’s **Settings**.
2. Select **Pages**.
3. Choose the branch containing the HTML files.
4. Select the repository root as the publishing directory.
5. Save the configuration.

The current pages are available at:

- [EyeRadar Support](https://nikossmyrnakis.github.io/eyeRadar/)
- [Privacy Policy](https://nikossmyrnakis.github.io/eyeRadar/privacy.html)

## Troubleshooting

### Camera or AR session does not start

Confirm that camera access is enabled:

```text
Settings → Privacy & Security → Camera
```

### Face tracking is unstable

Use EyeRadar in a well-lit environment and keep the iPhone approximately at arm’s length from your face.

### Export applications do not appear

Save the exported ZIP file to the Files application first, then attach or share it from there.

## Support

For questions, bug reports, or technical support:

- Email: [nick8smirn@gmail.com](mailto:nick8smirn@gmail.com)
- GitHub: [Open an issue](https://github.com/NikosSmyrnakis/eyeRadar/issues)

## Release Notes

### Version 1.0

- Initial EyeRadar release
- Reading-session capture
- ARKit calibration
- Eye-tracking data recording
- Session exploration
- ZIP export

## Planned Improvements

- Additional reading-text collections
- Configurable session parameters
- Additional export formats
- Extended reading metrics

## Author

**Nikolaos Smyrnakis**

## Copyright

Copyright © 2025 Nikolaos Smyrnakis. All rights reserved.
