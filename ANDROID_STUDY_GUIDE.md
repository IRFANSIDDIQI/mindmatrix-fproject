# Grama-Vaxi: Android Development Guide (Kotlin)

This document provides the core Kotlin code and setup instructions to build the **Grama-Vaxi** Android app in Android Studio.

## 1. Project Setup
1. Open **Android Studio**.
2. Create a **New Project** -> **Empty Views Activity**.
3. Language: **Kotlin**.
4. Minimum SDK: **API 26 (Oreo)** or higher (needed for Notification Channels).

## 2. Dependencies (build.gradle.kts)
Add these to your app-level `build.gradle.kts`:
```kotlin
dependencies {
    // Room DB
    val room_version = "2.6.1"
    implementation("androidx.room:room-runtime:$room_version")
    kapt("androidx.room:room-compiler:$room_version")
    implementation("androidx.room:room-ktx:$room_version")

    // WorkManager (for background alerts)
    implementation("androidx.work:work-runtime-ktx:2.9.0")

    // UI
    implementation("androidx.recyclerview:recyclerview:1.3.2")
    implementation("com.google.android.material:material:1.11.0")
}
```

## 3. Data Model (AnimalEntity.kt)
```kotlin
@Entity(tableName = "animals")
data class Animal(
    @PrimaryKey(autoGenerate = true) val id: Int = 0,
    val name: String,
    val breed: String,
    val age: Int,
    val type: String, // Sheep/Goat
    val lastVaccineDate: Long,
    val nextVaccineDate: Long
)
```

## 4. Background Notification (VaccineReminderWorker.kt)
This code ensures reminders trigger even if the app hasn't been opened.
```kotlin
class VaccineReminderWorker(context: Context, params: WorkerParameters) : Worker(context, params) {
    override fun doWork(): Result {
        val animalName = inputData.getString("animal_name") ?: "Livestock"
        showNotification(animalName)
        return Result.success()
    }

    private fun showNotification(name: String) {
        val channelId = "vaccine_alerts"
        val notification = NotificationCompat.Builder(applicationContext, channelId)
            .setSmallIcon(R.drawable.ic_notification)
            .setContentTitle("Vaccination Alert!")
            .setContentText("Reminder: $name is due for a vaccine in 3 days.")
            .setPriority(NotificationCompat.PRIORITY_HIGH)
            .build()
        
        val manager = applicationContext.getSystemService(Context.NOTIFICATION_SERVICE) as NotificationManager
        manager.notify(1, notification)
    }
}
```

## 5. Scheduling the Alert
Use this in your `Repository` or `ViewModel` when a new animal is registered:
```kotlin
val reminderRequest = OneTimeWorkRequestBuilder<VaccineReminderWorker>()
    .setInitialDelay(delayInDays, TimeUnit.DAYS)
    .setInputData(workDataOf("animal_name" to animalName))
    .build()

WorkManager.getInstance(context).enqueue(reminderRequest)
```

## 6. How to Run
1. Connect your Android device or start an Emulator.
2. Click the **Run** button (Green Triangle) in Android Studio.
3. To test the **Kannada** support:
   - Go to `Settings` > `Languages` on your device.
   - Add **Kannada** as a language.
   - Android will automatically use your `res/values-kn/strings.xml` file.
