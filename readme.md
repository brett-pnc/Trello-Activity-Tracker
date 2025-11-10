# 📊 Trello Activity Tracker Power-Up

A powerful Trello Power-Up that provides comprehensive activity tracking, filtering, and reporting capabilities for your Trello boards.

![Trello Activity Tracker](https://img.shields.io/badge/Trello-Power--Up-blue?style=for-the-badge&logo=trello)
![Status](https://img.shields.io/badge/Status-Active-green?style=for-the-badge)
![Version](https://img.shields.io/badge/Version-1.0-blue?style=for-the-badge)

## 🚀 Features

### 📅 **Advanced Filtering**
- **Date Range Selection**: Filter activities by custom date ranges (up to 31 days)
- **Board Filtering**: View activities from all boards or focus on specific boards
- **User Filtering**: See activities by specific team members
- **Activity Type Filtering**: Focus on specific types of activities with intuitive checkboxes

### 👥 **User Tracking**
- **User Attribution**: See exactly who performed each activity with `@username` display
- **User Avatars**: Visual user identification with initials avatars
- **Team Analytics**: Filter and analyze individual team member contributions

### 📊 **Real-Time Statistics**
- **Activity Counts**: Total activities, card actions, comments, and boards affected
- **Live Updates**: Statistics update automatically as you change filters
- **Visual Dashboards**: Color-coded statistics cards for quick insights

### 📁 **Data Export**
- **CSV Export**: Export filtered results to CSV with comprehensive data
- **Detailed Information**: Includes dates, users, activity types, descriptions, boards, and more
- **Automatic Naming**: Files named with date ranges for easy organization

### 🎨 **Modern Interface**
- **Responsive Design**: Optimized for Trello's modal constraints (680px width)
- **Intuitive Filters**: Easy-to-use checkboxes and dropdowns
- **Real-Time Filtering**: No page reloads needed when changing filters
- **Activity Type Icons**: Color-coded icons for different activity types

## 📋 Activity Types Tracked

### 🔵 **Card Activities** (Common)
- ✅ Card Creation
- ✅ Card Updates  
- ✅ Card Moves
- ✅ Card Deletion

### 💬 **Communication** (Common)
- ✅ Comments and Replies

### 🔧 **Advanced Activities**
- 📎 Attachment Management
- ☑️ Checklist Operations
- 👤 Member Assignments
- 🏷️ Label Management
- 📝 List Operations
- 🔄 Card Conversions
- 🏢 Organization Changes

## 🛠️ Installation

### Prerequisites
- Trello account with board access
- Modern web browser
- Trello Power-Up permissions

### Quick Start
1. **Get the Power-Up**: Install from your Trello board's Power-Up menu
2. **Authorize Access**: Grant read permissions when prompted
3. **Start Tracking**: Click the Activity Tracker button in your board menu

### Manual Installation (Developers)
1. Clone this repository
2. Enable GitHub Pages
3. Create Trello Power-Up with your GitHub Pages URL
4. Configure capabilities and install on boards

## 📖 Usage

### Basic Usage
1. **Open Activity Tracker**: Click the 📊 button in your board menu
2. **Select Date Range**: Choose start and end dates (max 31 days)
3. **Apply Filters**: Select boards, users, and activity types
4. **Load Activities**: Click "Load Activities" to fetch data
5. **Analyze Results**: View statistics and detailed activity lists

### Advanced Features
- **User Filtering**: Select specific team members from the dropdown
- **Activity Type Selection**: Use checkboxes to focus on specific activities
- **Quick Filters**: Use "All", "None", or "Common" buttons for activity types
- **Export Data**: Click "Export CSV" to download filtered results

### CSV Export Fields
- Date & Time
- User (Full Name & Username)
- Activity Type
- Description
- Board Name
- Card Name (when applicable)
- List From/To (for moves)
- Comment Text (for comments)

## 🔧 Technical Details

### Architecture
- **Client-Side Power-Up**: Runs entirely in browser
- **Trello API Integration**: Uses official Trello REST API
- **OAuth Authentication**: Secure token-based authentication
- **Real-Time Processing**: No server required

### Browser Compatibility
- Chrome/Chromium 80+
- Firefox 75+
- Safari 13+
- Edge 80+

### API Endpoints Used
- `GET /1/members/me/boards` - User's boards
- `GET /1/boards/{id}/actions` - Board activities

## 🔒 Privacy & Security

### Data Handling
- ✅ **Read-Only Access**: Only requests 'read' permissions
- ✅ **No Data Storage**: No activity data stored on external servers
- ✅ **Client-Side Processing**: All filtering and processing done locally
- ✅ **Secure Authentication**: Uses Trello's OAuth system

### Permissions Required
- **Read access** to your boards and activities
- **No write access** to your boards
- **No access** to personal information

## 🎨 Customization

### Activity Types
Add or modify activity types in the `activityTypes` configuration:
```javascript
const activityTypes = {
    customType: { 
        icon: '🔥', 
        name: 'Custom Activity', 
        class: 'type-custom', 
        common: false 
    }
};
```

### Styling
Modify CSS classes for custom appearance:
- `.type-card` - Card activities
- `.type-comment` - Comments
- `.type-attachment` - Attachments
- `.type-checklist` - Checklists
- `.type-member` - Member activities
- `.type-label` - Labels
- `.type-other` - Other activities

## 📊 Statistics

### What You Can Track
- **Team Productivity**: See who's most active
- **Activity Patterns**: Understand workflow patterns  
- **Board Usage**: Identify most/least active boards
- **Time Analysis**: Track activity over time periods
- **Project Insights**: Analyze specific project activities

### Export Analysis
Use exported CSV data for:
- **Excel Pivot Tables**: Advanced analytics
- **Team Reports**: Share activity summaries
- **Time Tracking**: Calculate time spent on activities
- **Project Documentation**: Record project progress

## 🤝 Contributing

### Development Setup
1. Fork the repository
2. Enable GitHub Pages on your fork
3. Create test Trello Power-Up pointing to your fork
4. Make changes and test

### Contribution Guidelines
- Test all features before submitting
- Follow existing code style
- Update documentation for new features
- Ensure responsive design compatibility

## 📄 License

This project is open source. Feel free to use, modify, and distribute according to your needs.

## 🆘 Support

### Common Issues

**Button doesn't appear:**
- Verify Power-Up is installed on your board
- Check that you have proper board permissions
- Try refreshing the page

**Authorization fails:**
- Clear browser cache and cookies
- Ensure you have Trello account access
- Try in incognito/private browsing mode

**No activities loading:**
- Check selected date range has activity
- Verify you have access to the selected boards
- Try expanding the date range

**Export issues:**
- Ensure you have activities selected
- Check browser's download settings
- Try a different browser

### Getting Help
- Check browser console (F12) for error messages
- Verify all filters are properly configured
- Try with a broader date range first

## 📈 Roadmap

### Planned Features
- 📊 **Advanced Analytics**: Charts and graphs
- 🔄 **Auto-Refresh**: Real-time activity updates
- 📱 **Mobile Optimization**: Better mobile experience
- 🎯 **Custom Filters**: User-defined filter combinations
- 📧 **Scheduled Reports**: Automated activity reports
- 🔍 **Search Functionality**: Text-based activity search

### Version History
- **v1.0** - Initial release with core functionality
  - Date range filtering
  - User and activity type filtering
  - CSV export capabilities
  - Responsive design

---

## 🙏 Acknowledgments

Built with:
- [Trello Power-Up Framework](https://developers.trello.com/)
- [Trello REST API](https://developers.trello.com/reference)
- Modern web technologies (HTML5, CSS3, ES6+)

---

**Made with ❤️ for better Trello productivity**