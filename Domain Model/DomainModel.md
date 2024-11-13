classDiagram
    User --> Pet : owns
    User --> Journey : participates
    User --> Task : creates
    User --> Mood : tracks
    User --> Progress : tracks
    User --> Customization : customizes
    User --> Reminder : sets
    User --> SelfCare : follows
    
    Pet --> Customization : has
    Journey --> Task : has
    Customization --> Accessory : includes
    Customization --> Background : includes
    Progress --> Mood : tracks
    Reminder --> User : notifies
    SelfCare --> User : assigned

    class User {
        +String UserID
        +String Name
        +String Email
        +String Password
        +Settings Settings
        +List<Journey> Journeys
        +List<Task> Tasks
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
    }

    class Accessory {
        +String AccessoryID
        +Enum Type
        +String Name
        +Decimal Price
        +Boolean Availability
    }

    class Background {
        +String BackgroundID
        +String Name
        +Decimal Price
        +Boolean Availability
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
