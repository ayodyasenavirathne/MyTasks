# 11316 - CA3

## 1. App Description
MyTaskApp is a simple and efficient Android application designed for personal task management. Users can create new tasks with titles and descriptions, view them in a list, and manage them effectively. The app ensures data persistence, meaning all your notes remain saved even if you restart the application.

## 2. Key Features
* Create Tasks: Add a title and detailed description for each task.
* View Tasks: A clean list view (RecyclerView) to see all saved items.
* Data Persistence: Uses Room Database to store data locally on the device.
* State Management: Handles screen rotations properly using ViewModel.

## 3. Design Choices & Architecture
* Architecture (MVVM): I used the Model-View-ViewModel pattern to separate the UI logic from the data handling. This makes the app easier to maintain and test.
* UI Design: Built using Material Design guidelines to ensure a modern, user-friendly interface with consistent spacing and colors.
* Data Persistence: Room Database was chosen over SharedPreferences because it provides a more robust structure for managing task objects and allows for future scalability.

## 4. Secure Coding Practices
* Input Validation: The app checks if the task title is empty before saving, preventing database errors and ensuring data integrity.
* No Hard-coded Secrets: All configurations and sensitive data handling (if any) are managed through proper Android resources rather than being hard-coded in the source logic.
