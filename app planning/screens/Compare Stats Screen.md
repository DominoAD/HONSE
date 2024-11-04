	•	Description: Direct comparison of stats between two or more characters.
	•	Features:
	•	Select Characters: Dropdown or multi-select list to choose characters for comparison.
	•	Stat Comparison Table: Side-by-side comparison of all key stats.
	•	Comparison Metrics: Highlight strengths, weaknesses, and similarities.
	•	Best Fit Suggestions: Highlight characters with stats fitting the desired role (e.g., Tank, DPS).
	
```kotlin
fun main() {
    // Description: Direct comparison of stats between two or more characters.

    // Features:
    // Select Characters: Dropdown or multi-select list to choose characters for comparison.
    val characters = listOf("Character1", "Character2", "Character3")

    // Stat Comparison Table: Side-by-side comparison of all key stats.
    val stats = mapOf(
        "Character1" to mapOf("Health" to 100, "Attack" to 50, "Defense" to 30),
        "Character2" to mapOf("Health" to 120, "Attack" to 40, "Defense" to 35),
        "Character3" to mapOf("Health" to 90, "Attack" to 60, "Defense" to 25)
    )

    // Comparison Metrics: Highlight strengths, weaknesses, and similarities.
    fun compareStats(char1: String, char2: String) {
        val char1Stats = stats[char1]
        val char2Stats = stats[char2]

        if (char1Stats != null && char2Stats != null) {
            println("Comparison between $char1 and $char2:")
            char1Stats.keys.forEach { stat ->
                val char1Value = char1Stats[stat]
                val char2Value = char2Stats[stat]
                println("$stat: $char1 -> $char1Value, $char2 -> $char2Value")
            }
        } else {
            println("Invalid characters selected.")
        }
    }

    // Best Fit Suggestions: Highlight characters with stats fitting the desired role (e.g., Tank, DPS).
    fun suggestBestFit(role: String) {
        when (role) {
            "Tank" -> println("Best Tank: Character2")
            "DPS" -> println("Best DPS: Character3")
            else -> println("Role not recognized.")
        }
    }

    // Example usage
    compareStats("Character1", "Character2")
    suggestBestFit("Tank")
}
```