	•	Description: Manage app settings, preferences, and customization options.
	•	Features:
	•	Theme Options: Light, dark, and custom themes.
	•	Notification Settings: Alerts for team recommendations or new character additions.
	•	Data Backup and Restore: Option to back up the character and team data and restore as needed.
	
```kotlin
	data class AppSettings(
					val themeOptions: ThemeOptions,
					val notificationSettings: NotificationSettings,
					val dataBackupAndRestore: DataBackupAndRestore
	)

	data class ThemeOptions(
					val lightTheme: Boolean,
					val darkTheme: Boolean,
					val customTheme: String?
	)

	data class NotificationSettings(
					val teamRecommendations: Boolean,
					val newCharacterAdditions: Boolean
	)

	data class DataBackupAndRestore(
					val backupEnabled: Boolean,
					val restoreEnabled: Boolean
	)
```	