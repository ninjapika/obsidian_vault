---
cssclass: cyberpunk-container
---

# 🎮 GAME OF LIFE DASHBOARD

## 📊 Current Stats
- Level: 1
- XP: 0/100
- Gold: 0
- Current Streak: 0 days

## 🎯 Active Quests

```dataviewjs
dv.table(["Quest", "Status", "Difficulty", "Reward"],
  dv.pages('"Quests"')
    .where(p => p.status == "active")
    .sort(p => p.difficulty, 'desc')
    .map(p => [p.file.link, p.status, p.difficulty, p.reward])
)
```

## 🏆 Daily Objectives

- [ ]  Complete 3 JEE practice problems
- [ ]  20 minutes Python coding
- [ ]  10-minute workout
- [ ]  Read 10 pages of Dune
- [ ]  Practice quantum computing concepts

## 💪 Current Streaks

```dataviewjs
dv.table(["Habit", "Current Streak", "Best Streak"],
  dv.pages('"Habits"')
    .where(p => p.streak > 0)
    .sort(p => p.streak, 'desc')
    .map(p => [p.file.link, p.streak, p["max-streak"]])
)
```

## 🎪 Side Quests Available

```dataviewjs
dv.table(["Side Quest", "Difficulty", "Reward", "Deadline"],
  dv.pages('"Side Quests"')
    .where(p => p.status == "available")
    .map(p => [p.file.link, p.difficulty, p.reward, p.deadline])
)
```

## 🏃‍♂️ Progress Tracking

### JEE Prep

- Physics: [=========>] 45%
- Chemistry: [=======>] 35%
- Mathematics: [==========>] 50%

### Coding Skills

- Python: [=======>] 35%
- Quantum Computing: [===>] 20%

## 🏪 Reward Shop

- 🎮 30min Gaming Session (50 gold)
- 📺 1 Episode of Favorite Show (30 gold)
- 🏍️ 1hr Motorcycle Ride (100 gold)