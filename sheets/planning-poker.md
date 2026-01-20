## PLANNING POKER

### 1-2 points (Simple):
* The task is **well known** by the team, they've done something similar before
* Has **few or no technical doubts**
* Involves **few files/components** of the system
* **Low risk** of blockers or dependencies
* Example: Fix a text, adjust CSS, create a simple CRUD endpoint

### 3-5 points (Moderate):
* The task has **some uncertainty** or novelty
* Involves **multiple components** or integrations
* May have **dependencies** on other areas/people
* Requires **some investigation** or technical decisions during execution
* **Moderate risk** of unforeseen complexity
* Example: Implement a new feature with validations, integrate with external API, refactor medium-sized module

### 8 points (High/Complex):
* The task has **high technical or requirements uncertainty**
* Involves **multiple systems/modules** with complex integrations
* Requires **research/proof of concept** before final implementation
* Has **critical dependencies** on other teams or external systems
* **High risk** of discovering unforeseen complexities during development
* May involve **new technologies** for the team or unfamiliar architecture
* Touches **critical parts** of the system that require extra care
* Example: Database migration, implement new authentication system, create new microservice architecture, complex integration with legacy system

### Warning sign:
If a task receives 8 points, you should **immediately question**:
* "Can we break this into smaller tasks?"
* "Which specific part is generating this complexity?"
* "Do we need to do a spike (investigation) first?"

### Practical rule:
* 8 points generally indicates the story **is not ready** to enter the sprint
* Should go back to **refinement** and be divided into 1-5 point pieces
* Or create a separate **spike** to resolve uncertainties first

### Remember:
If the team frequently estimates 8 points, it may be a sign that:
1. Stories are arriving too "raw" at planning
2. Refinement needs to be more detailed
3. The definition of "done" is not clear

**Ideally, most tasks should be between 2-5 points in sprint planning!**

---

## Important tip:
Encourage the team to use **discussion** during Planning Poker. If there's a large divergence (someone votes 2 and another votes 5), ask both to explain their reasoning. This usually reveals risks or simplifications that weren't clear to everyone.
