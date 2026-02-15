# Discipline Tracker 

A professional, feature-rich task and sleep tracking web application built with vanilla HTML, CSS, and JavaScript. Track your productivity, monitor sleep patterns, and maintain daily discipline streaks - all in your browser with local data persistence.

## 🎯 Features

### ⏱️ Time Tracking
- **Real-time Stopwatch**: Precise task duration tracking
- **Start/Stop Controls**: Easy task logging with one click
- **Sleep Tracking**: Dedicated sleep session logging
- **Active Task Indicator**: Visual display of currently running tasks
- **Auto-Save**: All data persists in browser localStorage

### 📋 Task Management
- Log tasks with automatic timestamps
- Categorize activities as productive or sleep
- **Quick-Start Favorites**: Save and reuse frequent tasks
- **Task History**: View all today's activities with duration
- **Delete Functionality**: Remove tasks if needed
- **Color-Coded Display**: Green for productive, Purple for sleep

### 📊 Statistics Dashboard
- **Productive Time**: Hours spent on productive tasks today
- **Sleep Time**: Total sleep duration tracked
- **Total Tracked**: Combined productive + sleep time
- **Day Streak**: Consecutive days with logged activity
- Real-time updates as you log activities

### 🔥 Streak System
- Automatic consecutive day counter
- Beautiful popup notifications
- Customized messages for milestones:
  - Day 1: "Day one. This is where it begins."
  - Day 7: "One week! Discipline is becoming a habit."
  - Day 30: "One month of discipline. Elite status."
  - Day 365: "One year. You've mastered yourself."
- Never lose your streak data (persisted locally)

### 📈 Analytics & Reporting
- **Productivity Trend Graph**: Line chart with smooth curves
  - View 7 days, 30 days, 3 months, 6 months, or 1 year
  - Shaded area fill for visual clarity
- **Sleep Analysis Chart**: Bar chart showing sleep patterns
  - Same time range options as productivity
- **Performance Report**: Monthly detailed breakdown
  - Summary statistics (tasks, hours, streak)
  - Daily breakdown table
  - Print-ready formatting
- **Export Data**: Download all data as CSV file

### 💡 Motivation System
- 20 rotating inspirational quotes
- Discipline and comeback-focused messaging
- Auto-rotates every 15 seconds
- Smooth fade in/out transitions
- Keeps you mentally engaged and focused

## 🎨 Design & UI

- **Dark Professional Theme**: Modern gradient background with glassmorphism effects
- **Responsive Layout**: Optimized for desktop, tablet, and mobile devices
- **Smooth Animations**: Fade transitions, hover effects, pulse animations
- **Accessibility**: Font Awesome icons, high contrast text, semantic HTML
- **Zero Dependencies**: Pure vanilla HTML/CSS/JavaScript (except Chart.js)

### Responsive Breakpoints
- **Desktop** (1400px): Full featured layout with side graphs
- **Tablet** (768px): Single column with stacked components
- **Mobile** (480px): Optimized touch-friendly interface

## 🚀 Quick Start

### Installation
1. Clone or download this repository
2. Open `Discipline.html` in your web browser
3. No build process, no dependencies, no installation required!

### Usage

#### Starting a Task
1. Enter a task name in the input field
2. Click **Start** button (or press Enter)
3. Watch the stopwatch timer count up
4. Click **Stop** when finished
5. Task automatically saves with timestamp and duration

#### Logging Sleep
1. Click the **Sleep** button
2. Timer starts for sleep session
3. Click **Stop** when done
4. Sleep session logged separately (purple indicator)

#### Adding Favorites
1. Enter a frequently used task name
2. Click the **⭐ Star** button
3. Task saved to Quick Start Favorites
4. Click favorite card to instantly start that task

#### Viewing Reports
1. Click **Report** button in top right
2. View current month's performance summary
3. See daily breakdown table
4. Click **Print** to print report
5. Close modal to return to tracker

#### Exporting Data
1. Click **Export** button
2. CSV file automatically downloads
3. Open in Excel, Google Sheets, or any spreadsheet app
4. Analyze your data however you need

## 💾 Data Storage

All data is stored in browser's **localStorage**:
- `discipline_tracker_tasks`: All logged tasks with timestamps
- `discipline_tracker_favorites`: Quick-start favorite tasks
- `discipline_tracker_streak`: Current streak count
- `discipline_tracker_last_activity`: Last activity date
- `discipline_tracker_active_task`: Currently running task (survives page refresh)

**Note**: Data is stored locally in your browser. Clearing browser data/cache will delete saved tasks.

## 🔧 Technical Details

### Architecture
Built with class-based JavaScript architecture for clean, maintainable code:

- **DisciplineTracker**: Main application controller
- **StopwatchManager**: Timer logic and task recording
- **TaskManager**: Task CRUD operations and rendering
- **UIManager**: UI updates, reports, and motivation
- **GraphManager**: Chart.js integration for analytics
- **EventManager**: Event binding and user interactions

### Technologies
- **HTML5**: Semantic markup
- **CSS3**: Custom properties, gradients, animations, Grid/Flexbox
- **Vanilla JavaScript (ES6+)**: No frameworks, pure JS
- **Chart.js**: Data visualization library
- **Font Awesome 6.4.0**: Icon library

### Browser Compatibility
- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Any modern browser with ES6 support and localStorage

## 📱 Responsive Design

The application automatically adapts to different screen sizes:
