# 🤖 What is an Agent in AI?

An **Agent** in Artificial Intelligence is an entity that:
- **Perceives** its environment through sensors,
- **Acts** upon the environment through actuators,
- And performs actions to achieve goals.

In simple words:

> **Agent = Anything that senses + thinks + acts**

Examples of agents:
- Self-driving car  
- ChatGPT  
- Robot vacuum cleaner  
- Google Maps navigation  

---

# 🎯 Role of an Agent in AI

AI Agents play a central role because they:
1. **Sense the environment** (collect information).
2. **Process information** (think, plan, learn).
3. **Take actions** that maximize performance.
4. **Interact continuously** with the environment.
5. **Learn from experience** to improve decisions.

Agents are the **decision-makers** in AI systems.

---

# 🧠 Five Main Types of AI Agents (Explained)

AI agents differ in their intelligence and how they make decisions.  
These are the **five major types**:

---

# 1️⃣ Simple Reflex Agent

### ✔ How it works:
- Acts ONLY on the **current percept**.
- Follows simple **IF condition → THEN action** rules.
- No memory of past events.

### ✔ Example:
A vacuum cleaner:
- If floor is dirty → CLEAN  
- If clean → MOVE  

### ✔ Limitations:
- Cannot handle complex or partially observable environments.

---

# 2️⃣ Model-Based Reflex Agent

### ✔ How it works:
- Maintains an **internal state** (memory).
- Uses **current percept + stored information**.
- Can operate in partially observable environments.

### ✔ Example:
A smart vacuum:
- Remembers which rooms are already cleaned.
- Knows obstacle positions even if not currently visible.

### ✔ Advantage:
- More intelligent than simple reflex agents.

---

# 3️⃣ Goal-Based Agent

### ✔ How it works:
- Uses **goals** to decide actions.
- Performs **search and planning**.
- Chooses actions that move closer to achieving the goal.

### ✔ Example:
Google Maps:
- Goal: Reach destination.
- Plans the shortest or fastest route.

### ✔ Key Feature:
- Considers **future consequences** of actions.

---

# 4️⃣ Utility-Based Agent

### ✔ How it works:
- Chooses actions based on **maximum utility (happiness/value)**.
- Handles trade-offs (speed, comfort, safety, cost).
- More advanced than goal-based agents.

### ✔ Example:
Self-driving car:
- Chooses route with best combination of:
  - Safety  
  - Time  
  - Fuel efficiency  
  - Comfort  

### ✔ Key Feature:
- Uses a **utility function** to measure performance.

---

# 5️⃣ Learning Agent

### ✔ How it works:
- Learns from **past experiences**.
- Improves performance over time.
- Can adapt even without explicit programming.

### ✔ Components:
- **Learning element** → improves agent behavior  
- **Performance element** → selects actions  
- **Critic** → evaluates performance  
- **Problem generator** → suggests new actions  

### ✔ Example:
ChatGPT  
- Learns patterns from huge datasets.
- Improves responses based on training.

### ✔ Advantage:
- Best suited for dynamic and uncertain environments.

---

# 📝 Short Exam Answer

An **agent** in AI is an entity that perceives its environment through sensors and acts upon it using actuators.  
Its role is to make intelligent decisions to achieve goals.

The **five main types of AI agents** are:

1. **Simple Reflex Agent** – Uses condition-action rules, no memory.  
2. **Model-Based Reflex Agent** – Uses memory + percepts to act.  
3. **Goal-Based Agent** – Chooses actions to achieve goals using planning.  
4. **Utility-Based Agent** – Selects actions that maximize utility.  
5. **Learning Agent** – Learns from experience and improves over time.

