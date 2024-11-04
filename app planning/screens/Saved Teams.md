	•	Description: Database of saved teams for future reference.
	•	Features:
	•	Save Team: Save optimized teams for future access.
	•	Edit Team: Update team members based on new character unlocks or strategy changes.
	•	Team Comparison: Compare two or more saved teams for quick decision-making.
	•	Performance Insights: Track performance metrics (if available) for each team in different game modes.
	
```kotlin
	data class Team(
					val name: String,
					val members: List<String>,
					val performanceMetrics: Map<String, Any>? = null
	)

	class TeamDatabase {
					private val teams = mutableListOf<Team>()

					fun saveTeam(team: Team) {
									teams.add(team)
					}

					fun editTeam(teamName: String, newMembers: List<String>) {
									val team = teams.find { it.name == teamName }
									team?.let {
													teams[teams.indexOf(it)] = it.copy(members = newMembers)
									}
					}

					fun compareTeams(teamNames: List<String>): List<Team> {
									return teams.filter { it.name in teamNames }
					}

					fun getPerformanceInsights(teamName: String): Map<String, Any>? {
									return teams.find { it.name == teamName }?.performanceMetrics
					}
	}
```