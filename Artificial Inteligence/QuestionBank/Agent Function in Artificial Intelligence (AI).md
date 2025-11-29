🤖 Agent Function in Artificial Intelligence (AI)

## 📌 What is an Agent Function?

An **agent function** is a mapping from **percepts** (inputs received from the environment) to **actions** (outputs performed by the agent).

In simple words:

> **Agent Function = Perception → Action**

It tells the agent **what action to take** based on **what it perceives** from the environment.

---

# 📘 Simple Formula

Agent Function: f(percept) = action

yaml
Copy code

Where:
- **Percept:** What the agent senses  
- **Action:** What the agent does next  

---

# 📊 Simple Diagram of an Agent Function

sql
Copy code
      +------------------------+
      |    Environment         |
      +-----------+------------+
                  |
           (Percept)
                  |
            +-----v------+
            |   Agent    |
            |  Function  |
            +-----+------+
                  |
             (Action)
                  |
      +-----------v------------+
      |    Environment         |
      +------------------------+
pgsql
Copy code

This cycle repeats continuously.

---

# 🧠 Example: Vacuum Cleaner Agent

### **Percept:**
- Current location  
- Whether the location is dirty or clean  

### **Agent Function Example**

If location is DIRTY → action = CLEAN
If location is CLEAN → action = MOVE to next location

yaml
Copy code

### **Simple Mapping Example**

| Percept                | Action |
|------------------------|--------|
| (A, Dirty)             | Clean  |
| (A, Clean)             | Move   |
| (B, Dirty)             | Clean  |
| (B, Clean)             | Move   |

---

# 📌 Example Explained

If the agent senses:  
(A, Dirty)

bash
Copy code
→ The agent function outputs:  
Clean

yaml
Copy code

If the agent senses:  
(B, Clean)

bash
Copy code
→ The agent function outputs:  
Move

pgsql
Copy code

The function continues this mapping throughout the environment.

---
