# Activity Tracker Changelog

## v1.0.1 - November 12, 2024

### Fixed
- **Arrow icons** now display correctly (▶ ▼ instead of â–¶ â–¼)
- **Search icon** in loading state now shows correct refresh icon (🔄 instead of 🔍•)
- All emoji and Unicode symbols validated and corrected

### Changed
- **UI Reorganization**: Moved "Activity Types" filter into Filters section as a collapsible subsection
- **Default collapsed state**: Date Selection, Filters, Quick Date Selection, and Activity Types now collapsed on load for cleaner UI
- **Improved UX**: Users can expand sections as needed, reducing initial visual clutter

### Technical
- Fixed 10 icon corruptions using byte-level replacements
- Updated toggleSection function to handle flex display for quickDateContent
- Simplified showActivityTypeFilter function to work with new nested structure

---

## v1.0.0 - November 12, 2024

### Fixed
- **Hide Automation functionality** - Improved automation detection with multiple methods:
  - Detects null/undefined memberCreator (Butler activities often have no creator)
  - Checks for 'butler', 'automation', 'bot' in username/fullName
  - Added known Butler user ID to detection list
  - Checks for null idMemberCreator in activity data
  - Detects automation keywords in comment text
  - Added detailed console logging for debugging filter behavior

### Added
- **Version number** displayed in title header (v1.0.0)
  - Shows in light grey text next to Activity Tracker title
  - Will increment with each update

### Enhanced
- Better console logging for Hide Automation toggle
- Detailed filtering statistics in console
- Shows count of filtered automation activities

### Technical Details
- All emoji encoding issues resolved (107 fixes applied)
- File validated as proper UTF-8 with 76 emojis
- Automation filter applies after type and user filters
- Filter properly triggers re-display of activities
