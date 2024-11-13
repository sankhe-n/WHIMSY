# Assignment 8

## Project Title: 
 # Whimsy: Your Virtual Pet & Self-Care Companion 
 *For a whimsical journey to wellness!*
 -
 
 **Team Members:**
 
 Neha Bhushan Sankhe
 (email: sankhe.n@northeastern.edu)
 
 Vishal Babu Mahesh Babu
 (email: maheshbabu.v@northeastern.edu)
 
 ---
## APIs Assigned to Neha

 ### **User Management API**
- **/register**: Register a new user
- **/login**: User login
- **/logout**: User logout
- **/updateSettings**: Update user preferences (theme, notification preferences, etc.)
- **/getUserSettings**: Retrieve current user settings
- **/changePassword**: Update password securely

### **Journey and Task Management API**
- **/createJourney**: Create a new journey
- **/getJourneys**: Retrieve all journeys for a user
- **/updateJourney**: Update journey details
- **/deleteJourney**: Delete a journey
- **/addTask**: Add a task to a specific journey or individually
- **/updateTask**: Update task details (due date, status, etc.)
- **/deleteTask**: Remove a task
- **/getTasksByJourney**: Get tasks for a specific journey
- **/completeTask**: Mark a task as completed and award rainbow stones

### **Progress & Reward System API**
- **/getProgress**: Retrieve user progress summary (task completion rate, streaks, etc.)
- **/getRainbowStones**: Fetch current balance of rainbow stones
- **/earnRainbowStones**: Award stones for completed tasks
- **/purchaseRainbowStones**: Buy rainbow stones with digital wallets (PayPal, Google Pay)
- **/transactionHistory**: View purchase and earning history for rainbow stones

### **Reminder and Notification API**
- **/createReminder**: Create a reminder for a specific task or journey
- **/getReminders**: Fetch all reminders for a user
- **/updateReminder**: Update reminder details
- **/deleteReminder**: Remove a reminder
- **/notificationSettings**: Update notification preferences (sound, frequency)

---

## APIs Assigned to Vishal

### **Virtual Pet Management API**
- **/selectPet**: Choose a pet type (cat, dog, etc.)
- **/getPetStatus**: Get pet’s current mood and health status
- **/updatePetMood**: Modify pet mood based on user progress
- **/updatePetHealth**: Change pet health status
- **/getPetGrowthStage**: Retrieve pet’s growth stage
- **/customizePet**: Apply customizations to pet

### **Mood and Wellness Tracking API**
- **/logMood**: Record a mood entry
- **/getMoodHistory**: Fetch user’s past mood entries
- **/calculateWellnessScore**: Generate wellness score based on mood and task data
- **/getMoodInsights**: Retrieve trends and insights for user moods

### **Self-Care Techniques API**
- **/getSelfCareTechniques**: Fetch available self-care resources
- **/breathingExercise**: Provide animated guide for breathing
- **/groundingExercise**: Offer grounding exercises
- **/dailyAffirmation**: Send daily affirmations

### **Customization Store API**
- **/getAvailableAccessories**: List purchasable accessories
- **/getAvailableBackgrounds**: List available backgrounds for pet customization
- **/purchaseAccessory**: Buy a specific accessory using rainbow stones
- **/purchaseBackground**: Buy a background using rainbow stones
- **/getCustomizationOptions**: Fetch all available customizations for the pet
---

## **Ideology**

### **Aim**
Whimsy is an interactive self-care app where users adopt a virtual pet and take care of their mental health and well-being. By engaging in self-care routines, users help their pet grow and develop, unlocking fun new features and personalized care. The app serves as a fun way to keep track of self-care, mood, productivity, and mental health with weekly and monthly reports.

### **Motivation**
Life moves fast, and keeping track of self-care can get lost in the shuffle. Whimsy makes self-care easy, fun, and engaging with a virtual pet that grows alongside your mental health journey. Track your mood, productivity, self-care habits, and streaks with an intuitive interface. The app also offers quick fixes for mental health, such as breathing exercises, reflections, and grounding techniques.

### **Inspiration**
Whimsy draws inspiration from Finch and similar apps, combining interactive virtual pet care with mental health and well-being. The idea is to create a space where users are motivated to care for themselves, just like they care for their virtual pet.

---

## **Technology**

### **Overview of Whimsy**
Whimsy is a self-care app that combines mental health tracking with the fun of taking care of a virtual pet. The app’s primary features include mood tracking, habit logging, pet development, and mental health support tools. Each pet's development is tied to the user's self-care activities, which include things like journaling, exercise, mindfulness, and more.

---

## **Screen & Functionality Breakdown**

### **Onboarding Screen**
- **Function**: Introduces users to Whimsy’s features and virtual pet concept.
- **Elements**:
  - Animated welcome and pet selection screen where users pick their virtual animal companion (e.g., cat, dog, rabbit).
  - Introduction to main functionalities: habit tracking, mood monitoring, and self-care tasks.

### **Home/Dashboard Screen**
- **Function**: Central hub displaying user’s progress, pet status, and navigation.
- **Elements**:
  - **Virtual Pet**: Visual of the pet’s current health and mood, linked to user progress.
  - **Daily Tasks**: List of tasks for mood check-ins, self-care, and habits.
  - **Progress Overview**: Summarizes streaks, mood trends, and task completion rate.

### **Pet Growth & Customization Screen**
- **Function**: Allows users to customize and evolve their pet with app engagement.
- **Elements**:
  - **Growth Stages**: Pets evolve from baby to adult, gaining new physical features.
  - **Customization Options**: Unlockable accessories, backgrounds, and visual changes.

### **Habit & Goal Tracker Screen**
- **Function**: Enables users to set, track, and monitor daily self-care habits.
- **Elements**:
  - **Habit List**: Users add and check off daily habits.
  - **Progress Graphs**: Simple charts display habit consistency.
  - **Reminders & Streaks**: Notifications for milestone achievements.

### **Mood & Wellness Tracking Screen**
- **Function**: Monitors mood and facilitates daily self-reflection.
- **Elements**:
  - **Mood Check-Ins**: Slider or emojis for recording daily moods.
  - **Journal Section**: Short text entries for reflection.
  - **Weekly/Monthly Graphs**: Tracks mood trends and emotional states.

### **Quick Self-Care Techniques Screen**
- **Function**: Provides quick exercises for stress relief and grounding.
- **Elements**:
  - **Breathing Exercises**: Animated guides for calm breathing.
  - **Grounding Techniques**: Exercises like the 3-3-3 rule and 5-to-1 senses.
  - **Daily Affirmations**: Positive messages for mood boost.

### **Reports & Insights Screen**
- **Function**: Offers visual summaries of self-care and wellness progress.
- **Elements**:
  - **Monthly Summaries**: Overview of habits, mood, and streaks.
  - **Progress Graphs**: Productivity, self-care consistency, and mood charts.
  - **Achievements**: Badges or rewards for milestones.

### **Settings & Notifications Screen**
- **Function**: Customizable notifications and reminders for user preferences.
- **Elements**:
  - **Reminder Scheduling**: Preferred times for daily task reminders.
  - **Sound & Notification Settings**: Manage sound, frequency, and visual themes.
  - **Pet Preferences**: Change pets or update pet visuals as per user choice.

---

### **Functional Components & REST APIs**

1. **User Registration & Authentication**
   - **Endpoint**: `POST /signup`, `POST /login`
   - **Purpose**: Users create an account and log in.
   - **Example**:  
     - Request body: `{ "username": "john_doe", "password": "strongpassword123" }`
     - Response: `{ "token": "xyz123" }`

2. **Pet Adoption & Customization**
   - **Endpoint**: `POST /pet/adopt`, `PUT /pet/customize`
   - **Purpose**: Users adopt a virtual pet and customize its appearance and personality.
   - **Example**:
     - Request body: `{ "petType": "cat", "name": "Fluffy", "appearance": { "color": "white", "size": "small" } }`
     - Response: `{ "message": "Pet adopted successfully" }`

3. **Self-Care Activity Logging**
   - **Endpoint**: `POST /habit/log`
   - **Purpose**: Log daily self-care activities like journaling, exercise, etc.
   - **Example**:  
     - Request body: `{ "activity": "journaling", "status": "completed", "timestamp": "2024-11-12T10:00:00Z" }`
     - Response: `{ "message": "Activity logged successfully" }`

4. **Mood & Mental Health Tracking**
   - **Endpoint**: `POST /mood/track`, `GET /mood/summary`
   - **Purpose**: Track daily moods and get a summary of mood patterns.
   - **Example**:
     - Request body: `{ "mood": "happy", "comment": "Had a productive day!" }`
     - Response: `{ "message": "Mood tracked successfully" }`

5. **Pet Development**
   - **Endpoint**: `GET /pet/status`
   - **Purpose**: Shows the pet’s growth and development based on self-care activities.
   - **Example**:  
     - Response: `{ "petName": "Fluffy", "growthStage": "Teen", "appearance": { "color": "gray", "size": "medium" } }`

6. **User Progress Reports & Analytics**
   - **Endpoint**: `GET /reports/weekly`, `GET /reports/monthly`
   - **Purpose**: Get weekly/monthly summaries of self-care activities, mood, and productivity.
   - **Example**:  
     - Response: `{ "week": "Week 1", "moodGraph": [ "happy", "sad", "neutral" ], "streaks": 5 }`

7. **Mental Health Support Tools**
   - **Endpoint**: `GET /tools/breathing`, `GET /tools/reflection`
   - **Purpose**: Provide users with mental health exercises like breathing techniques and reflection prompts.
   - **Example**:  
     - Response: `{ "exercise": "breathe in for 4 counts, hold for 4, exhale for 4" }`

---

## **Technical Details**

#### **Object Model & Domain Driven Design (DDD)**

- **Entities**: `User`, `Pet`, `Activity`, `Mood`, `Habit`, `Report`
- **Relationships**:
  - One `User` can adopt one `Pet` (one-to-one relationship)
  - One `User` can log multiple `Activities` and track multiple `Moods` (one-to-many relationships)
  - One `User` can have multiple `Reports` (one-to-many relationship)
- **Value Objects**: `PetAppearance`, `HabitType`, `MoodIndicator`

---
## **Scalability Considerations**

To ensure that Whimsy can scale with growing user demand, the following approaches are considered:

1. **Cloud Infrastructure**:
   - Utilize cloud services (e.g., **Azure** and **MongoDB Atlas**) for storage and computing, allowing the app to handle an increase in data and user load efficiently.
   - Automatic scaling to handle large spikes in app usage, especially during high-demand periods (e.g., mental health awareness campaigns, app updates).

2. **Database Design**:
   - Implementing **MongoDB Atlas** allows for scalable, flexible database management, accommodating millions of users and their data (e.g., pet records, self-care habits, mood data) without performance degradation.
   - Use of **sharded clusters** to distribute the database load across multiple servers, enhancing scalability and performance.

3. **Microservices Architecture**:
   - Each feature (e.g., pet adoption, habit logging, mood tracking) is designed as an independent service. This allows the system to scale each service independently based on user demand.
   - REST APIs and **OpenAPI specifications** ensure that services are loosely coupled and can be scaled individually, making future updates and additions easier.

4. **Load Balancing & Caching**:
   - Use **load balancers** to distribute incoming traffic across multiple servers to ensure responsiveness under heavy load.
   - Implement **Redis caching** to optimize API performance, especially for frequently accessed data (e.g., mood summaries, pet status).

5. **User Notifications & Real-time Updates**:
   - Implement **push notifications** to notify users about pet status changes, habit tracking reminders, and mental health check-ins without overloading the server.
   - **WebSockets** or **real-time APIs** could be used to send instant updates to users about pet development or progress.

6. **Performance Optimization**:
   - Monitor and optimize API endpoints, ensuring they can handle high traffic efficiently.  
   - Implement **lazy loading** for pet customization features and media content to prevent delays
   - 
   
---
## **Scalability Considerations**

### **1. Additional Functionalities**
- **Expanded Self-Care Modules**: New wellness features, such as sleep tracking, diet management, and guided meditations, can be added.
- **Personalized Pet Behavior**: Pet behaviors can evolve based on the user's engagement, creating a more personalized experience.
- **Social Features**: Community challenges and virtual pet competitions can be introduced to encourage user interaction.
- **AI-powered Mood Analysis**: AI can provide deeper insights into mood trends, offering personalized recommendations based on historical data.
- **Subscription-Based Premium Features**: Premium features like exclusive pet customizations and detailed progress reports could be introduced.

### **2. Customizations**
- **More Pet Types & Accessories**: Expand pet options and visual customizations, providing users with more personalized experiences.
- **User-defined Goals**: Allow users to create and track their own self-care goals.
- **Pet Evolution Paths**: Offer different evolution paths for pets to reflect each user's unique self-care journey.

### **3. User-Specific Concerns**
- **User-Specific Recommendations**: Based on mood and self-care activity, personalized recommendations for tasks or techniques can be provided.
- **Mental Health Resource Integration**: Users could access real-time counseling services and other professional mental health support.
- **Data Privacy & Security**: Implement enhanced security measures, like encryption and two-factor authentication.
- **Accessibility Features**: Introduce text-to-speech, voice commands, and customizable visual settings for users with specific needs.

---

## Entities and Attributes

### **User**

The `User` represents the person using the app, interacting with tasks, mood check-ins, progress tracking, and their virtual pet.

- **Attributes:**
  - `UserID`: String
  - `Name`: String
  - `Email`: String
  - `Password`: String (Encrypted)
  - `Settings`: Settings
  - `Pet`: Pet (One-to-One relationship with Pet)
  - `Journeys`: List<Journey> (One-to-Many relationship with Journey)
  - `Tasks`: List<Task> (One-to-Many relationship with Task)

### **Pet**

The `Pet` represents the virtual pet that the user owns and cares for.

- **Attributes:**
  - `PetID`: String
  - `PetType`: Enum (Cat, Dog, Rabbit, etc.)
  - `PetMood`: Enum (Happy, Sad, Neutral)
  - `PetHealth`: Enum (Healthy, Sick, Needs Attention)
  - `GrowthStage`: Enum (Baby, Adolescent, Adult)
  - `Customization`: Customization (One-to-One relationship with Customization)
  - `User`: User (Many-to-One relationship with User)

### **Journey**

A `Journey` represents a specific goal or path that the user follows to achieve personal growth or self-care. Each journey has associated tasks.

- **Attributes:**
  - `JourneyID`: String
  - `Name`: String
  - `Description`: String
  - `StartDate`: DateTime
  - `EndDate`: DateTime
  - `Tasks`: List<Task> (One-to-Many relationship with Task)
  - `User`: User (Many-to-One relationship with User)

### **Task**

A `Task` is a specific action that the user performs. It could belong to a journey or be independently added by the user.

- **Attributes:**
  - `TaskID`: String
  - `Title`: String
  - `Description`: String
  - `Category`: Enum (Mood Check-In, Self-Care, Habit, Custom)
  - `DueDate`: DateTime
  - `Frequency`: Enum (Once, Daily, Weekly, Custom)
  - `CustomFrequency`: Integer (For custom frequency tasks, e.g., tasks per day)
  - `Status`: Enum (Pending, Completed, Overdue)
  - `Journey`: Journey (Many-to-One relationship with Journey)
  - `User`: User (Many-to-One relationship with User)

### **Mood**

The `Mood` entity stores the user's emotional state at specific points in time.

- **Attributes:**
  - `MoodID`: String
  - `MoodType`: Enum (Happy, Sad, Neutral, Anxious, Angry)
  - `MoodScore`: Integer (Scale 1-10)
  - `DateTime`: DateTime
  - `User`: User (Many-to-One relationship with User)

### **Progress**

`Progress` tracks the user's overall journey, task completion rate, and wellness scores.

- **Attributes:**
  - `ProgressID`: String
  - `MoodHistory`: List<Mood> (One-to-Many relationship with Mood)
  - `TaskCompletionRate`: Decimal (Percentage of tasks completed)
  - `Streak`: Integer
  - `WellnessScore`: Integer
  - `User`: User (One-to-One relationship with User)

### **Customization**

Represents the customization options for the user's virtual pet, including accessories and backgrounds.

- **Attributes:**
  - `CustomizationID`: String
  - `Accessories`: List<Accessory> (One-to-Many relationship with Accessory)
  - `Backgrounds`: List<Background> (One-to-Many relationship with Background)
  - `User`: User (Many-to-One relationship with User)

### **Accessory**

Represents an accessory that can be applied to the user's virtual pet.

- **Attributes:**
  - `AccessoryID`: String
  - `Type`: Enum (Hat, Glasses, Collar, etc.)
  - `Name`: String
  - `Price`: Decimal
  - `Availability`: Boolean (whether the accessory is available for customization)
  - `Customization`: Customization (Many-to-One relationship with Customization)

### **Background**

Represents a background theme for the user's pet or pet screen.

- **Attributes:**
  - `BackgroundID`: String
  - `Name`: String
  - `Price`: Decimal
  - `Availability`: Boolean (whether the background is available for customization)
  - `Customization`: Customization (Many-to-One relationship with Customization)

### **Reminder**

Reminders allow users to set specific times for self-care tasks.

- **Attributes:**
  - `ReminderID`: String
  - `Title`: String
  - `Time`: DateTime
  - `Message`: String
  - `Status`: Enum (Active, Inactive, Completed)
  - `User`: User (Many-to-One relationship with User)

### **SelfCare**

`SelfCare` stores self-care techniques that users can follow.

- **Attributes:**
  - `SelfCareID`: String
  - `Category`: Enum (Breathing Exercise, Grounding, Affirmations, etc.)
  - `Description`: String
  - `Frequency`: Enum (Daily, Weekly, As Needed)
  - `User`: User (Many-to-One relationship with User)

## Value Objects

### **Settings**

Represents user preferences regarding app appearance and notifications.

- **Attributes:**
  - `Theme`: Enum (Light, Dark)
  - `NotificationPreferences`: NotificationPreferences
  - `Language`: Enum (English, Spanish, etc.)

### **NotificationPreferences**

Defines notification settings.

- **Attributes:**
  - `Frequency`: Enum (Daily, Weekly, Immediate)
  - `Sound`: Boolean (Enabled/Disabled)
  - `Vibration`: Boolean (Enabled/Disabled)

### **Customization Options**

Defines all possible customization options available to the user for their virtual pet.

- **Attributes:**
  - `Accessories`: List<Accessory>
  - `Backgrounds`: List<Background>

### **DateTime** (For Task and Mood)

Represents the specific date and time for task completion and mood tracking.

- **Attributes:**
  - `Date`: Date
  - `Time`: Time

### **Wellness Score**

Tracks the user’s overall wellness score.

- **Attributes:**
  - `Score`: Integer (1-100)
  - `Date`: DateTime

## Relationships and Cardinality

### **User to Pet**
- **Relationship**: One-to-One
- **Description**: Each user can have one pet, and each pet is linked to one user.

### **User to Journey**
- **Relationship**: One-to-Many
- **Description**: Each user can have multiple journeys.

### **User to Task**
- **Relationship**: One-to-Many
- **Description**: A user can create multiple tasks (either through journeys or individually).

### **Journey to Task**
- **Relationship**: One-to-Many
- **Description**: A journey can have multiple tasks associated with it.

### **User to Mood**
- **Relationship**: One-to-Many
- **Description**: A user can have multiple mood check-ins.

### **User to Progress**
- **Relationship**: One-to-One
- **Description**: Each user has one progress object tracking their overall self-care journey.

### **User to Customization**
- **Relationship**: One-to-One
- **Description**: Each user can have one set of customizations for their virtual pet.

### **Customization to Accessory**
- **Relationship**: One-to-Many
- **Description**: A customization can have multiple accessories.

### **Customization to Background**
- **Relationship**: One-to-Many
- **Description**: A customization can have multiple backgrounds.

### **User to Reminder**
- **Relationship**: One-to-Many
- **Description**: A user can set multiple reminders for self-care tasks.

### **User to SelfCare**
- **Relationship**: One-to-Many
- **Description**: A user can have multiple self-care techniques assigned to them.

---

**Memaid code:**
#Domain MOdel for WHIMSY
 
```mermaid
---
title: WHIMSY
---



classDiagram
    User --> Pet : owns
    User --> Journey : participates
    User --> Task : creates
    User --> Mood : tracks
    User --> Progress : tracks
    User --> Customization : customizes
    User --> Reminder : sets
    User --> SelfCare : follows
    User --> RainbowStone : earns
    User --> Wallet : uses for purchases

    Pet --> Customization : has
    Journey --> Task : has
    Customization --> Accessory : includes
    Customization --> Background : includes
    Progress --> Mood : tracks
    Reminder --> User : notifies
    SelfCare --> User : assigned
    Wallet --> RainbowStone : purchases

    class User {
        +String UserID
        +String Name
        +String Email
        +String Password
        +Settings Settings
        +List<Journey> Journeys
        +List<Task> Tasks
        +Integer RainbowStones  // Currency earned or purchased for customizations
    }
    
    class Pet {
        +String PetID
        +Enum PetType
        +Enum PetMood
        +Enum PetHealth
        +Enum GrowthStage
        +Customization Customization
    }
    
    class Journey {
        +String JourneyID
        +String Name
        +String Description
        +DateTime StartDate
        +DateTime EndDate
    }
    
    class Task {
        +String TaskID
        +String Title
        +String Description
        +Enum Category
        +DateTime DueDate
        +Enum Frequency
        +Integer CustomFrequency
        +Enum Status
        +Integer RainbowStoneValue  // Amount of Rainbow Stones awarded upon completion
    }
    
    class Mood {
        +String MoodID
        +Enum MoodType
        +Integer MoodScore
        +DateTime DateTime
    }

    class Progress {
        +String ProgressID
        +Decimal TaskCompletionRate
        +Integer Streak
        +Integer WellnessScore
    }

    class Customization {
        +String CustomizationID
        +List<Accessory> Accessories
        +List<Background> Backgrounds
        +Integer TotalRainbowStoneCost  // Cost of current customizations in Rainbow Stones
    }

    class Accessory {
        +String AccessoryID
        +Enum Type
        +String Name
        +Decimal Price
        +Boolean Availability
        +Integer RainbowStoneCost  // Cost in Rainbow Stones
    }

    class Background {
        +String BackgroundID
        +String Name
        +Decimal Price
        +Boolean Availability
        +Integer RainbowStoneCost  // Cost in Rainbow Stones
    }

    class Reminder {
        +String ReminderID
        +String Title
        +DateTime Time
        +String Message
        +Enum Status
    }

    class SelfCare {
        +String SelfCareID
        +Enum Category
        +String Description
        +Enum Frequency
    }

    class Settings {
        +Enum Theme
        +NotificationPreferences NotificationPreferences
        +Enum Language
    }

    class NotificationPreferences {
        +Enum Frequency
        +Boolean Sound
        +Boolean Vibration
    }

    class Wallet {
        +String WalletID
        +Enum PaymentMethod  // Enum for payment options like PayPal, Google Pay
        +Decimal Balance
        +purchaseRainbowStones(int amount) : Boolean  // Method for purchasing Rainbow Stones
    }