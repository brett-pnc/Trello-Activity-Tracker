# 📊 Trello Activity Tracker Power-Up - Enhanced Edition

A comprehensive Trello Power-Up for tracking, filtering, and analyzing board activities with advanced features.

![Version](https://img.shields.io/badge/Version-2.0-blue?style=flat-square)
![Status](https://img.shields.io/badge/Status-Enhanced-green?style=flat-square)

## 🚀 What's New in Version 2.0

### ✨ 10 Major Enhancements Added:

1. **📅 Date Shortcuts** - Quick buttons for Today, Yesterday, Last 7/14/30/31 days
2. **⬆️ Sort Direction** - Toggle between oldest-first (default) and newest-first
3. **📋 View Modes** - Switch between Expanded and Compact display
4. **🏷️ Card Labels** - Colored label pills displayed on activities
5. **🔍 Parsed Updates** - Specific change descriptions (not just "updated")
6. **📆 Date Headers** - Activities grouped by day with counts
7. **🤖 Hide Automation** - Filter out Butler automation activities
8. **☑️ Better Checkboxes** - Entire activity type box is clickable
9. **💾 Filter Presets** - Save and load your favorite filter configurations
10. **🎨 Layout Improvements** - Cleaner design with tooltips

## 📦 Installation

### Quick Setup

1. **Install from GitHub**:
   - Your Power-Up is hosted at: `https://yourusername.github.io/Trello-Activity-Tracker/`
   - Enable GitHub Pages in repository settings

2. **Configure in Trello**:
   - Go to https://trello.com/power-ups/admin
   - Create new Power-Up (OAuth 2.0 Integration)
   - Set all capabilities to your GitHub Pages URL

3. **Add to Board**:
   - Open any Trello board
   - Power-Ups menu → Add Power-Up
   - Find your Activity Tracker
   - Click "Add" and authorize

## 🎯 Features

### Core Functionality

- **📅 Flexible Date Ranges** (up to 31 days)
  - Manual date selection
  - Quick shortcuts (Today, Yesterday, Last 7/14/30/31 days)
  
- **🎯 Advanced Filtering**
  - Filter by specific boards
  - Filter by users
  - Filter by activity types (14+ types tracked)
  - Hide automation activities
  
- **📊 Real-Time Statistics**
  - Total activities
  - Card actions count
  - Comments count
  - Boards affected

- **🏷️ Visual Enhancements**
  - Card labels displayed as colored pills
  - Activity type icons with color coding
  - User avatars with initials
  - Clean date headers grouping activities by day

### Display Modes

#### 📋 Expanded View (Default)
- Full activity details with descriptions
- Large icons (32px) and avatars
- Labels as colored pills with text
- More spacing for easy reading
- Shows board name and precise time

#### 📄 Compact View
- Single-line activity display
- Smaller icons (24px) for density
- Labels as tiny colored bars
- Less spacing to see more activities
- Board name on second line

### Activity Types Tracked

- ✅ **Card Operations**: Create, Update, Move, Delete, Copy
- 💬 **Communications**: Comments and Replies
- 📎 **Attachments**: File additions
- ☑️ **Checklists**: Creation and item updates
- 👤 **Members**: Assignments and removals
- 🏷️ **Labels**: Additions and removals
- 📝 **Lists**: Creation, updates, moves
- 🔄 **Conversions**: Checklist items to cards
- 🏢 **Organization**: Board additions/removals

### Parsed Update Intelligence

Instead of generic "updated card" descriptions, see exactly what changed:

- **List Moves**: "moved from 'To Do' to 'In Progress'"
- **Due Dates**: "set due date to 11/15/2025" or "changed due date" or "removed due date"
- **Renaming**: "renamed from 'Old Name' to 'New Name'"
- **Descriptions**: "added description", "updated description", or "removed description"
- **Status**: "archived" or "unarchived"
- **Multiple Changes**: Combined into one description

### Filter Presets

Save your frequently-used filter combinations:

- **Save**: Current filters, sort direction, view mode, and options
- **Load**: Restore saved configurations instantly
- **Manage**: Delete unused presets
- **Storage**: Saved in browser localStorage (persists across sessions)

### Data Export

**CSV Export** with comprehensive data:
- Date and time
- User (full name and username)
- Activity type
- Detailed description
- Board name
- Card name
- List transitions (for moves)
- Comment text (for comments)

## 🎨 User Interface

### Header Controls
```
📊 Activity Tracker    [📋 Expanded ▼] [Load Activities]
```

### Quick Date Selection
```
[Today] [Yesterday] [Last 7] [Last 14] [Last 30] [Last 31]
```

### Filter Section
```
Start Date    End Date      Board Filter
[______]      [______]      [All Boards ▼]

User Filter    Sort Direction    Options
[All Users▼]   [⬆️ Oldest▼]     [☑] Hide Automation
```

### Action Buttons
```
[📥 Export CSV]  [💾 Save Preset]  [📂 Load Preset]
```

### Activity Display with Date Headers
```
══════════════════════════════════════════════
Monday, November 11, 2025        (15 activities)
══════════════════════════════════════════════

[💬] @user commented on "Card" 🏷️ Bug    3:26 PM  [U]
     Product Board

[✏️] @user updated "Card": moved from       2:15 PM  [U]
     "To Do" to "Done" 🏷️ Feature
     Dev Board
```

## 🔧 Technical Details

### Architecture
- **Client-Side Power-Up**: Runs entirely in browser, no server needed
- **Trello API Integration**: Official REST API with OAuth 2.0
- **Storage**: LocalStorage for presets (browser-based, not synced)
- **Hosting**: GitHub Pages (static files)

### API Endpoints Used
- `GET /1/members/me/boards` - User's accessible boards
- `GET /1/boards/{id}/actions` - Board activity history

### Permissions Required
- ✅ **Read access** to boards and activities
- ❌ **No write access** to boards
- ❌ **No access** to personal information

### Browser Compatibility
- Chrome/Chromium 80+
- Firefox 75+
- Safari 13+
- Edge 80+

### Performance
- Handles 1000+ activities efficiently
- Date grouping optimized for large result sets
- Compact view recommended for 100+ activities
- 31-day maximum range enforced

## 📋 Usage Guide

### Basic Workflow

1. **Open Activity Tracker**
   - Click the 📊 button in your board's menu

2. **Select Date Range**
   - Use quick shortcuts OR
   - Manually select start and end dates

3. **Apply Filters** (optional)
   - Choose specific board
   - Select user
   - Check activity types to include
   - Toggle "Hide Automation" if desired

4. **Choose Display Options**
   - Select sort direction (oldest or newest first)
   - Toggle between Expanded and Compact view

5. **Load Activities**
   - Click "Load Activities" button
   - Wait for activities to load
   - Review grouped activities with date headers

6. **Export or Save** (optional)
   - Export to CSV for external analysis
   - Save current filters as preset for reuse

### Pro Tips

1. **Default to Oldest-First** - Better for reviewing chronological work
2. **Use Compact View** - When scanning many activities
3. **Save Common Presets** - For your typical filter combinations
4. **Hide Automation** - Focus on human activities
5. **Quick Shortcuts** - Faster than manual date entry
6. **Filter by Type** - Focus on specific activity categories

## 🎯 Use Cases

### Team Management
- Daily standup reviews (use "Yesterday" shortcut)
- Weekly sprint reviews (use "Last 7 Days")
- Individual contributor tracking (filter by user)
- Automation audit (show only automation with filter OFF)

### Project Tracking
- Card progression monitoring (filter Move activities)
- Comment history review (filter Comments only)
- Label usage analysis (visible in activity descriptions)
- Board activity comparison (filter by specific boards)

### Reporting
- Export activities to CSV for analysis
- Share activity summaries with stakeholders
- Track team velocity over time
- Document project history

## 🔍 Activity Examples

### Expanded View Example:
```
[✏️]  @jane_smith updated "Database Migration": moved from 
32px  "In Progress" to "Review", set due date to 11/15/2025
      🏷️ Feature  🏷️ Database  🏷️ High Priority
      
      📋 Development Board | 🕒 2:15 PM            [JS]
```

### Compact View Example:
```
[✏️] @jane_smith "DB Migration": moved... ▌▌▌  2:15 PM [JS]
     Development Board
```
(▌ = tiny colored label bars)

## 🐛 Troubleshooting

### Button doesn't appear
- Verify Power-Up is installed on the board
- Check GitHub Pages is working and deployed
- Try refreshing the Trello board
- Check browser console for errors

### Authorization fails
- Ensure API key is correct in index.html
- Verify scope is set to 'read'
- Try in incognito mode
- Check Trello account has board access

### No activities load
- Check date range has activity in it
- Try broader date range (e.g., Last 30 Days)
- Verify board filter allows your boards
- Check user has permissions on selected boards
- Try "All Users" filter instead of specific user

### Labels not showing
- Ensure cards have labels assigned in Trello
- Labels only show on activities with labeled cards
- Try expanded view (compact shows tiny bars)
- Check that activity type is not filtered out

### Automation not hiding
- Butler activities detected by username pattern
- May need to add specific Butler user IDs
- Check browser console for detection logs
- Try manually filtering to test

### Presets won't save
- Check browser allows localStorage
- Try in different browser
- Ensure you're not in private/incognito mode
- Check storage isn't full

### Display issues
- Try different view mode (Expanded vs Compact)
- Check browser zoom level (100% recommended)
- Clear browser cache
- Try different browser

## 🔐 Privacy & Security

### Data Handling
- ✅ **Read-Only**: Only reads your activities, never writes
- ✅ **Client-Side**: All processing done in your browser
- ✅ **No Storage**: Activity data not stored on external servers
- ✅ **Local Presets**: Filter presets stored in browser only

### What We Access
- Board names and IDs you have access to
- Activity history from your boards
- Card names, lists, and metadata
- User names performing activities

### What We Don't Access
- Card descriptions or detailed content
- Attachments or file contents
- Personal messages or private data
- Data from boards you can't access

## 📊 Statistics

### Tracked Metrics
- **Total Activities**: All matching activities in date range
- **Card Actions**: Creates, updates, moves, deletes
- **Comments**: All comment activities
- **Boards Affected**: Unique boards with activity

### Activity Counts
- Per-day counts in date headers
- Per-type counts in filter checkboxes
- Total count in statistics bar
- Filtered count updates in real-time

## 🚀 Advanced Features

### Keyboard Shortcuts
*(Future enhancement planned)*

### Search Functionality  
*(Future enhancement planned)*

### Direct Card Links
*(Future enhancement planned)*

### Activity Charts
*(Future enhancement planned)*

## 📞 Support

### Getting Help
1. Check browser console (F12) for error messages
2. Review this README's troubleshooting section
3. Verify all capability URLs are correct
4. Test in incognito mode to rule out extensions
5. Try with a fresh Power-Up installation

### Common Error Messages

**"No authorization token available"**
- Click the activity tracker button again
- Authorize when prompted
- Check that authorization popup wasn't blocked

**"Failed to load boards"**
- Check internet connection
- Verify Trello account is logged in
- Try refreshing the page

**"Date range cannot exceed 31 days"**
- Select a shorter date range
- Use the "Last 31 Days" quick shortcut for maximum range

## 🎨 Customization

### Label Colors
The Power-Up supports all 10 standard Trello label colors:
- Green, Yellow, Orange, Red, Purple
- Blue, Sky, Lime, Pink, Black

### Activity Type Icons
Each activity type has a unique icon:
- 📋 Card operations
- 💬 Comments
- 📎 Attachments
- ☑️ Checklists
- 👤 Members
- 🏷️ Labels
- And more...

### View Preferences
- Default view mode: Expanded
- Default sort: Oldest-first
- Default date range: Last 7 days
- All configurable through UI

## 📈 Roadmap

### Planned Enhancements
- 🔍 Text search across activities
- 📊 Activity charts and visualizations
- 🔗 Direct links to cards from activities
- 📅 Calendar view of activities
- 🔔 Activity notifications
- 📱 Mobile optimization improvements
- 🎨 Custom themes
- 🌐 Multi-language support
- 📥 Additional export formats (JSON, PDF)
- 🔄 Auto-refresh option

## 📄 License

Open source - free to use and modify for your needs.

## 🙏 Acknowledgments

Built with:
- [Trello Power-Up Framework](https://developers.trello.com/)
- [Trello REST API](https://developers.trello.com/reference)
- Modern web technologies (HTML5, CSS3, ES6+)

## 📝 Changelog

### Version 2.0 (Current)
- ✨ Added date shortcuts for quick selection
- ✨ Added sort direction control (oldest/newest first)
- ✨ Added view mode toggle (expanded/compact)
- ✨ Added card labels display
- ✨ Added parsed update intelligence
- ✨ Added date headers with activity grouping
- ✨ Added hide automation option
- ✨ Fixed checkbox click areas (entire box clickable)
- ✨ Added filter presets (save/load)
- 🎨 Improved layout with tooltips
- 🔧 Enhanced user experience throughout

### Version 1.0
- 🎉 Initial release
- 📅 Basic date range filtering
- 🎯 Board and user filtering
- ☑️ Activity type filtering
- 📊 Real-time statistics
- 📥 CSV export functionality

---

**Made with ❤️ for better Trello productivity**

Need help? Check the troubleshooting section or inspect your browser console for detailed error messages.
