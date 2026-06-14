# Garmin GraphQL Schema

## Overview

This conceptual GraphQL schema models the Garmin Connect platform — covering health metrics, fitness activities, training, devices, social features, and user management. It draws from the Garmin Connect Health API, Activity API, Training API, Courses API, Health SDK, and FIT SDK data models. Garmin does not currently publish a public GraphQL endpoint; this schema represents the data surface as a GraphQL type system for integration and tooling purposes.

## Source APIs

- [Garmin Connect Health API](https://developer.garmin.com/gc-developer-program/health-api/)
- [Garmin Connect Activity API](https://developer.garmin.com/gc-developer-program/activity-api/)
- [Garmin Connect Training API](https://developer.garmin.com/gc-developer-program/training-api/)
- [Garmin Connect Courses API](https://developer.garmin.com/gc-developer-program/courses-api/)
- [Garmin Health SDK](https://developer.garmin.com/health-sdk/overview/)
- [Garmin FIT SDK](https://developer.garmin.com/fit/overview/)

## Root Types

### Query

- `userProfile(userId: ID!): UserProfile` — Fetch a user's Garmin Connect profile.
- `dailyActivities(userId: ID!, startDate: String!, endDate: String!): [DailyActivities]` — Retrieve daily wellness summaries for a date range.
- `steps(userId: ID!, date: String!): Steps` — Step count data for a specific day.
- `heartRate(userId: ID!, date: String!): HeartRate` — Resting and continuous heart rate readings.
- `sleep(userId: ID!, date: String!): Sleep` — Sleep session data including stages and score.
- `activities(userId: ID!, limit: Int, offset: Int): [Activity]` — Paginated list of recorded activities.
- `activity(activityId: ID!): Activity` — Single activity with full detail.
- `device(deviceId: ID!): Device` — Garmin device metadata and sensor info.
- `devices(userId: ID!): [Device]` — All devices registered to a user.
- `workouts(userId: ID!, limit: Int): [Workout]` — Structured workouts assigned to the user.
- `courses(userId: ID!): [Course]` — GPS courses available on the user's devices.
- `goals(userId: ID!): [Goal]` — Active user wellness goals.
- `leaderboard(challengeId: ID!): Leaderboard` — Challenge leaderboard entries.
- `achievements(userId: ID!): [Achievement]` — Earned badges and achievements.
- `trainingStatus(userId: ID!): TrainingStatus` — Current training load and readiness metrics.

### Mutation

- `pushWorkout(userId: ID!, workout: WorkoutInput!): Workout` — Push a structured workout to a user's Garmin device via the Training API.
- `pushCourse(userId: ID!, course: CourseInput!): Course` — Push a GPS course to the user's Garmin device.
- `updateUserSetting(userId: ID!, setting: UserSettingInput!): UserSetting` — Update a user preference.
- `logWeight(userId: ID!, weight: WeightInput!): Weight` — Log a manual body weight entry.

## Type Descriptions

### Health and Wellness

- **UserProfile** — Garmin Connect user identity including display name, join date, and locale. Links to settings and connected devices.
- **DailyActivities** — All-day summary for a calendar date: steps, distance, calories, floors, active minutes, and intensity minutes. Sourced from the Health API dailySummaries push.
- **Steps** — Step count broken down by epoch intervals within a day; includes goal and time-of-day offset.
- **Distance** — Cumulative distance in meters from device step/activity tracking.
- **Calories** — Active and resting calorie burn; distinguishes BMR calories from activity calories.
- **ActiveMinutes** — Intensity minutes (moderate and vigorous) accumulated toward weekly guidelines.
- **HRV** — Heart rate variability status and nightly average. Includes 5-minute overnight readings and a weekly average trend.
- **HeartRate** — Resting heart rate, daily minimum and maximum, and continuous intraday readings at specified sampling intervals.
- **HeartRateZone** — Named heart rate zone (e.g., Zone 1 Warm-Up through Zone 5 Max) with bpm range and time-in-zone.
- **BodyBattery** — Garmin's proprietary energy reserve metric (0–100) with intraday readings showing drain and recharge events.
- **StressLevel** — Stress score derived from HRV; rated low, medium, high, or rest. Includes rest-period detection.
- **Sleep** — Full sleep session record with start/end time, total duration, and overall sleep score. Contains nested stage breakdown and movement data.
- **SleepMovement** — Movement intensity readings captured during a sleep session at epoch intervals.
- **SleepScore** — Composite sleep quality score and component subscores (duration, quality, recovery).
- **SleepStage** — Classified sleep phase (deep, light, REM, awake) with start offset and duration.
- **SpO2** — Blood oxygen saturation pulse oximetry snapshot including reading, confidence, and device mode.
- **PulseOxData** — Continuous overnight or on-demand SpO2 series with sampling interval metadata.
- **BodyComposition** — Body composition measurement from a compatible Garmin scale or manual entry: weight, BMI, body fat, skeletal muscle, bone mass.
- **Weight** — Single scale or manual weight measurement in kilograms with timestamp and source.
- **BMI** — Calculated body mass index with categorization label.
- **BodyFat** — Body fat percentage reading with measurement method indicator.

### Activity and Performance

- **Activity** — Recorded sport session (30+ Garmin activity types). Contains summary metrics and links to laps, splits, route, and gear. FIT file reference included.
- **ActivityLap** — Auto-detected or manual lap within an activity: distance, duration, pace, cadence, heart rate average, and elevation change.
- **ActivitySplit** — Distance-based split (e.g., each kilometer or mile) with pace, elapsed time, and heart rate.
- **ActivityDevice** — The specific Garmin hardware unit that recorded the activity, with firmware version at record time.
- **Route** — GPS track associated with an activity or standalone course; contains ordered RoutePoints.
- **RoutePoint** — Individual trackpoint: latitude, longitude, altitude, timestamp, heart rate, cadence.
- **Course** — Pre-planned GPS route pushed to a device for navigation. Includes waypoints and course type.
- **SegmentResults** — Segment leaderboard result for a user on a defined route segment (Strava-style integration data).
- **TrainingStatus** — Aggregated training load summary: current load, optimal range, aerobic and anaerobic load contributions, and load focus.
- **TrainingReadiness** — Pre-session readiness score (0–100) derived from sleep quality, HRV status, recovery time, and training history.
- **Performance** — Composite performance metrics for an activity: training effect (aerobic and anaerobic), performance condition, and normalized power (cycling).
- **VO2Max** — Estimated maximal oxygen uptake value, trend direction, and fitness age.
- **FTPScore** — Functional threshold power estimate (cycling) in watts with date of last calculation.

### Devices and Gear

- **Gear** — Wearable or equipment item associated with the user (shoes, bike, etc.) with distance/time tracking for maintenance alerts.
- **Device** — Garmin wearable or unit registered to the user account with model name, product ID, and registration date.
- **DeviceInfo** — Technical device metadata: firmware version, battery status, software part numbers, and display resolution.
- **DeviceSensor** — Sensor capability declared by the device (e.g., optical HR, GPS, barometric altimeter, pulse ox).
- **SyncSession** — Record of a device-to-Garmin-Connect sync: timestamp, files transferred, and sync method (BLE, Wi-Fi, USB).

### Training and Workouts

- **Workout** — Structured workout definition with ordered steps delivered via the Training API. Includes sport type and estimated duration.
- **WorkoutExercise** — Individual exercise step within a workout: exercise name, target (pace, HR, power, cadence), repetitions or duration, and rest period.
- **WorkoutHistory** — Completed workout execution record linking the original Workout definition to the resulting Activity.
- **Calendar** — User training calendar with scheduled workout and race events.

### Social and Goals

- **Goal** — User-defined wellness or performance goal: type (steps, weight, distance), target value, start and end dates, and progress.
- **Challenge** — Community or partner challenge with participation window, goal metric, and participant count.
- **ChallengeStatus** — User's current standing in a Challenge: progress value, rank, and completion percentage.
- **Leaderboard** — Ranked list of LeaderboardEntry objects for a specific Challenge.
- **LeaderboardEntry** — Individual user rank entry within a Leaderboard with display name, avatar, progress value, and rank position.
- **Achievement** — Milestone or accomplishment earned by the user (e.g., first activity, annual distance goals).
- **Badge** — Visual award asset linked to an Achievement: badge name, image URL, earn date.

### User Settings

- **User** — Core account entity linking to UserProfile and all health, activity, and device data.
- **UserSetting** — Named preference value (unit system, privacy level, heart rate zone configuration, lactate threshold settings).

## Scalar Types

- `DateTime` — ISO 8601 datetime string.
- `Date` — Calendar date string in YYYY-MM-DD format.
- `Float` — IEEE 754 double-precision decimal for measurement values.
- `ID` — Opaque string identifier.

## Schema File

See `garmin-schema.graphql` for the full type definitions.
