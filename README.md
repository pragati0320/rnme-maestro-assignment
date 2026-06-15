# RNME Mobile Automation Testing

## Application Setup

I used the pre-built APK provided in the repository (Option A) to test the application as a black-box Android application.

The APK was installed on an Android Emulator using:

adb install rnme/rnme.apk

`No source code modifications or environment configuration were required.
`

## Overview

This project contains UI automation tests for the RNME (Movie Explorer) Android application using Maestro.

### Covered Scenarios

Positive Scenarios

* Login with valid credentials
* Search Movie
* View Movie Details
* Add to Favorites
* Remove from Favorites
* Watch Trailer
* Logout
* Theme Change (Light/Dark Mode)

Negative Scenarios

* Login with invalid credentials
* Validation of authentication error messages
* Session Management
* Verify user session persists after navigation
* Verify authenticated user remains logged in until logout
---

## Framework

* Tool: Maestro
* Platform: Android
* Device: Pixel 8 Emulator (Android 14)
* Language: YAML

---

## Project Structure


maestro/
├── login.yaml
├── search-movie.yaml
├── movie-detail.yaml
├── add-favorite.yaml
└──search-no-result.yaml
├── search-movie.yaml
├── movie-detail.yaml
├── add-favorite.yaml
├── invalid-login.yaml
└── logout.yaml

---

## Test Credentials

**Email:** [test@rnme.com](mailto:test@rnme.com)

**Password:** Test123$$

---

## Run Tests

Run a single test:

```bash
maestro test maestro/login.yaml
```

Run all tests:

```bash
maestro test maestro/
```

---

## Preconditions

* Android emulator is running
* RNME APK is installed
* Internet connection is available
* Test account remains active

---
## Use of AI Tools

ChatGPT was used as an assistant for brainstorming test coverage, reviewing the test strategy, and refining documentation. All test scenarios, implementationwas done using Maestro Studio emulator and also validated manually over physical device.
---

## Author

Pragati Sapkota

QA Automation Engineer Assignment Submission
