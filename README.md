# Hintro-Task
 Building a functional Task Board application with a static login flow. The focus is on frontend engineering quality, state management, and usability.
 Link for the extended link which are of more size :- https://drive.google.com/file/d/1nzsNcyUGjceGkZfBkN_UPIXB4YBmNC-e/view?usp=sharing
Bash to run the app :-
Open your terminal to run the application :- quick deploy :-
# Make sure you're in the project folder
cd task-board-app
# Install dependencies (if not done already)
npm install
# Deploy to Vercel
npx vercel --prod
# do this to get the link of the product. 
https://task-board-app.netlify.app
This application is developed as a comprehensive solution for personal and team task management. It showcases:
Professional frontend engineering practices
Modern React patterns and best practices
Type-safe development with TypeScript
Client-side state management and data persistence
Responsive design and accessible UI components
Test-driven development approach
Key Features
Authentication System
Secure Login Flow: Static authentication with hardcoded credentials for demo purposes
Session Management: "Remember me" functionality with persistent login state
Route Protection: Automatic redirection to login page for unauthenticated users
Clean Logout: Secure session termination with state cleanup
Task Management
Full CRUD Operations: Create, read, update, and delete tasks with ease
Rich Task Data Model:
Title (required field with validation)
Description (multi-line text support)
Priority levels (Low, Medium, High with visual indicators)
Due dates with calendar picker
Custom tags for categorization
Automatic timestamp tracking
Status Tracking: Three-column Kanban board (Todo, Doing, Done)
Interactive User Interface
Drag & Drop: Smooth, intuitive task movement between columns using @hello-pangea/dnd
Real-time Search: Instant filtering by task title as you type
Multi-level Filtering: Filter tasks by priority level
Smart Sorting: Sort by due date with empty dates automatically placed last
Responsive Design: Fully functional on desktop, tablet, and mobile devices
Activity Tracking
Comprehensive Logging: Automatic tracking of all task operations
Action Types: Created, edited, moved, and deleted events
Timestamp Display: Human-readable timestamps for each action
Recent Activity View: Sidebar panel showing the latest 20 activities
Visual Indicators: Emoji icons for different action types
Data Persistence
LocalStorage Integration: All data persists across browser sessions
Error Handling: Safe operations with fallback for storage failures
Data Integrity: Validation before saving to prevent corruption
Reset Functionality: Option to clear all data with confirmation dialog
Architecture & Design Decisions
Technology Stack Rationale
Next.js 14: Chosen for its excellent developer experience, built-in routing, and optimization features. The App Router provides a modern, intuitive file-based routing system.
TypeScript: Ensures type safety throughout the application, reducing runtime errors and improving code maintainability. All components, contexts, and utilities are fully typed.
React Context API: Lightweight state management solution perfect for this application's scope. Provides global state without the complexity of external libraries like Redux.
Framer Motion: Professional animation library that enhances user experience with smooth, performant animations without sacrificing bundle size.
@hello-pangea/dnd: Modern, maintained fork of react-beautiful-dnd providing accessible, smooth drag-and-drop functionality.
Project Structure
src
├── app                   # Next.js App Router pages
│   ├── board            # Main task board interface
│   ├── login             # Authentication page
│   └── layout.tsx         # Root layout with providers
├── components            # Reusable UI components
│   ├── ProtectedRoute    # Authentication wrapper
│   ├── TaskCard         # Individual task display
│   └── TaskModal        # Task creation/editing form
├── contexts              # React Context providers
│   ├── AuthContext.tsx    # Authentication state
│   └── TaskContext.tsx    # Task management state
├── types                # TypeScript type definitions
├── utils                # Utility functions
│   └── storage.ts         # LocalStorage operations
├── styles                # Global CSS and design tokens
└── __tests__           # Test suites
Design Philosophy
User-Centric: Every feature prioritizes ease of use and clear visual feedback. Users should never wonder what an action will do or whether it succeeded.
Performance-First: Optimized re-renders, code splitting, and efficient data structures ensure smooth performance even with hundreds of tasks.
Accessibility: ARIA labels, keyboard navigation, and semantic HTML ensure the application is usable by everyone.
Maintainability: Clean code, consistent patterns, and comprehensive documentation make the codebase easy to understand and extend.
Technical Highlights
State Management Pattern :- The application uses a clean separation of concerns with two primary contexts:
AuthContext: Manages authentication state, login/logout operations, and session persistence
TaskContext: Handles all task CRUD operations, filtering, searching, and sorting
This pattern provides:
Clear data flow
Easy testing
Scalable architecture
Type-safe operations
Form Validation
Client-side validation ensures data integrity:
Required field validation
Real-time error messages
Input sanitization
Type checking
Error Handling
Comprehensive error handling throughout:
Try-catch blocks for storage operations
Fallback values for missing data
User-friendly error messages
Console logging for debugging
Performance Optimizations
useMemo: Expensive computations (filtering, sorting) are memoized
useEffect dependencies: Carefully managed to prevent unnecessary re-renders
Code splitting: Next.js automatic code splitting for optimal load times
Lazy loading: Components loaded only when needed
# This project is created as a frontend internship assignment and is available for educational and portfolio purposes.
# Created as part of the Hintro Frontend Internship Assignment, demonstrating modern web development skills and best practices.
