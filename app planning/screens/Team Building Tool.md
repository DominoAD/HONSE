	•	Description: Helps users build teams by analyzing their available characters’ stats and roles.
	•	Features:
	•	Team Role Selection: Choose roles (Warrior, Support, Archer, Mage, Rogue) to fill.
	•	Team Composition Recommendation: Suggests characters based on roles, synergy, and stats.
	•	Artifact Assignment: Recommends artifacts for each character based on role and stats.
	•	Multiple Modes: Allow for different team compositions based on game modes, like PvE or PvP.
	
```kotlin
data class Character(
    val name: String,
    val role: Role,
    val stats: Stats
)

enum class Role {
    WARRIOR, SUPPORT, ARCHER, MAGE, ROGUE
}

data class Stats(
    val attack: Int,
    val defense: Int,
    val health: Int,
    val speed: Int
)

class TeamBuilder {

    fun selectRoles(roles: List<Role>): List<Character> {
        // Implementation for selecting characters based on roles
    }

    fun recommendTeamComposition(characters: List<Character>): List<Character> {
        // Implementation for recommending team composition based on synergy and stats
    }

    fun assignArtifacts(characters: List<Character>): Map<Character, Artifact> {
        // Implementation for recommending artifacts based on role and stats
    }

    fun getTeamForMode(mode: GameMode): List<Character> {
        // Implementation for different team compositions based on game modes
    }
}

enum class GameMode {
    PVE, PVP
}

data class Artifact(
    val name: String,
    val bonus: String
)
```