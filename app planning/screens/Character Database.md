	•	Description: Database of all characters with detailed attributes and stats.
	•	Features:
	•	Character Profiles:
	•	Basic Stats: HP, ATK, Phys DEF, Magic DEF
	•	Offensive Stats: ATK SPD, Crit, Haste, DEF Penetration, Execution, Crit DMG Boost
	•	Defensive Stats: Vitality, Life Drain, Crit Resist, Ranged DEF, Crit DMG DEF
	•	Other Stats: Healing, Assistance, Energy on Hit, Debuff Focus, Resilience, Proficiency, Skill Power, Ultimate’s Power
	•	Search and Filter Options: Filter characters by class, stats, rarity, etc.
	•	Add/Edit/Delete: Allows players to update their character list based on unlocked characters.
	
	•	How to Tackle This in Android Studio:
		1.	Setup Project:
			•	Create a new project in Android Studio.
			•	Choose an appropriate project template (e.g., Empty Activity).
			•	Configure project settings such as name, package name, and save location.
		2.	Design Database Schema:
			•	Define tables for characters and their attributes.
			•	Use Room Database for local storage.
			•	Create Entity classes for each table.
		3.	Implement UI:
			•	Design layouts for character profiles, stats display, and search/filter options using XML.
			•	Use RecyclerView for displaying lists of characters.
			•	Implement necessary adapters and view holders.
		4.	Develop Features:
			•	Character Profiles: Create activities/fragments to display character details.
			•	Search and Filter Options: Implement search functionality using SearchView and filter logic.
			•	Add/Edit/Delete: Create forms for adding/editing characters and implement delete functionality.
		5.	Connect UI with Database:
			•	Use ViewModel and LiveData to observe data changes.
			•	Bind data to UI components.
		6.	Test and Debug:
			•	Test each feature thoroughly.
			•	Debug any issues and ensure smooth functionality.
		7.	Optimize and Refine:
			•	Optimize database queries.
			•	Refine UI for better user experience.
		8.	Deploy:
			•	Build APK and test on various devices.
			•	Prepare for release on Google Play Store.