# Activity Tracker Changelog

## v1.0.4 - November 12, 2024

### Changed
- **Redesigned activity layout** for better information hierarchy:
  - Top line shows: **Card Name** [labels] on **Board Name** with time badge in top-right
  - Time badge: dark background (#5e6c84), white bold text, bottom-left corner rounded (flag effect)
  - Removed user initials avatar from right side
  - Activity icon and username now left-aligned in second row
- **Enhanced label display**:
  - Shows maximum 2 labels inline after card name
  - Additional labels indicated with "+N" badge showing count
  - Tooltip on "+N" badge shows remaining label names
- **Improved comment display**:
  - Comments shown as blockquote with gray left border and light background
  - First line visible by default with "[Show more]" link
  - Expandable to show full comment text with "[Show less]" link
  - No truncation of comment text
- **Performance improvement**: TrelloPowerUp retry attempts reduced from 50 to 10

### Technical
- Added `toggleComment()` function for expanding/collapsing comment text
- Restructured activity item HTML with header/content separation
- Time badge uses `border-radius: 0 0 0 6px` for flag corner effect
- Labels limited to 2 visible with overflow counter

---

## v1.0.3 - November 12, 2024

### Added
- **Parse "Card Updated" activities**: Now shows specific changes instead of generic "updated card"
  - Detects name changes, description edits, due date changes, completion status
  - Shows archived/unarchived, reordered, cover image changes
  - Example: "changed due date from Nov 10 to Nov 12" instead of "updated card"
- **Enhanced label display**: Proper Trello color mapping with hex values
  - Supports all Trello label colors (green, yellow, orange, red, purple, blue, sky, lime, pink, black)
  - Includes dark variants for accurate color representation
  - Empty labels show as colored dots

### Improved
- **Compact layout**: Activity items now more space-efficient
  - Reduced padding (16px → 12px)
  - Smaller spacing between items (12px → 8px)
  - Colored left border indicates activity type (card=green, comment=yellow, etc.)
  - Border expands on hover for better visual feedback
- **Better visual hierarchy**:
  - User names in darker text (full name only, no @ prefix)
  - Description in lighter gray for better readability
  - Smaller, cleaner badges and metadata
  - Improved user avatar styling with gradient background
- **Refined typography**:
  - Activity text: 13px (was 14px)
  - Metadata: 11px (was 12px)
  - Tighter line height (1.3) for compact feel
  - Labels now 10px with bolder text

### Technical
- Added `parseUpdateCardActivity()` function to detect specific card changes
- Added `getTrelloLabelColor()` for accurate Trello color mapping
- Activity type color indicators via left border styling
- Enhanced hover states with smooth transitions

---

## v1.0.2 - November 12, 2024

### Fixed
- **API 400 Error**: Removed `member=me` parameter that was causing "invalid value for member" error
  - Now fetches all board activities without member filter
  - Slightly slower but more reliable

### Enhanced
- **Improved Automation Detection**: Added multiple new detection methods for Butler activities
  - Checks for Butler-specific display properties
  - Detects batch field updates (due dates, labels, list changes)
  - Identifies automated field updates (subscribed, dueComplete)
  - Detects multiple automated fields changed at once
- **Debug Logging**: Added detailed activity structure logging when Hide Automation is enabled
  - Shows sample activities with their data structure
  - Helps identify automation patterns
  - Console shows memberCreator, display properties, and data keys

### Technical
- Simplified API call logic (removed fallback approach)
- Better error handling for fetch operations
- Enhanced isAutomationActivity function with 7 detection methods

---

## v1.0.1 - November 12, 2024

### Fixed
- **Arrow icons** now display correctly (â–¶ â–¼ instead of Ã¢â€“Â¶ Ã¢â€“Â¼)
- **Search icon** in loading state now shows correct refresh icon (ðŸ”„ instead of ðŸ”â€¢)
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
