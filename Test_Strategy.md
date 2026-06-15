# Test Strategy

## Objective

Validate the critical user journeys of the RNME Android application through end-to-end mobile automation from an end-user perspective.

## Approach

A risk-based approach was used to prioritize high-impact features. Tests were designed to be independent, maintainable, and include both positive and negative scenarios.

## Test Coverage

### Authentication

* Valid login
* Invalid login
* Authentication validation
* Logout

### Movie Discovery

* Search for a movie
* View movie details
* Search with no results

### Favorites

* Add movie to Favorites
* Remove movie from Favorites
* Watch trailer navigation

### Profile

* Access Profile
* Change application theme (Light, Dark, System)

### Session Management

* Verify user remains authenticated during app usage
* Verify session persists until explicit logout

### Offline Scenarios

* Validate login behavior without internet connectivity
* Verify application behavior when an logged in user goes offline

## Test Data


| Scenario            | Test Data                                                 |
| ------------------- | --------------------------------------------------------- |
| Valid Login         | Email: `test@rnme.com`
                        Password: `Test123$$`           
| Invalid Login       | Email: `invalid@rnme.com`
                        Password: `WrongPassword123` 
| Movie Search        | `Batman`                                                  |
| Search – No Results | `xyzabc123`                                               |
| Favorites           | `The Batman`                                              |
| Offline Scenarios   | Android Emulator network disabled                         |
| Theme Validation    | Light, Dark, and System themes                            |

## Automation Approach

* Framework: Maestro
* Platform: Android
* Device: Pixel 8 Emulator (Android 14)
* Test Format: YAML

## Preconditions

* The provided APK is stable and representative of the application.
* Test credentials remain valid.
* Internet connectivity is available for online scenarios.

## Reusability

The automation suite is designed to be reusable and executable by any team member with the documented prerequisites. Once the Android Emulator, Maestro, and the RNME APK are set up, the tests can be executed without additional configuration or source code changes.

## Preconditions

Maestro installed
Android Studio with an Android Emulator
RNME APK installed on the emulator/device
ADB configured and accessible from the command line
Internet connectivity for online scenarios
Execution

##Run an individual test:

maestro test maestro/login.yaml

Run the complete test suite:

maestro test maestro/

## Future Improvements

* Accessibility testing
* Cross-device validation
* Network recovery scenarios
* CI/CD integration and reporting
* Performance testing
