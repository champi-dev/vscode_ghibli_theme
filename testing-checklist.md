# Studio Ghibli Theme Testing Checklist

## Installation Testing
- [ ] Theme installs correctly from VSIX file
- [ ] Both theme variants appear in theme picker
- [ ] Theme activates without errors
- [ ] Theme switches smoothly between variants

## Color Contrast Testing
- [ ] All text is readable on backgrounds (WCAG AA compliance)
- [ ] Selected text is clearly visible
- [ ] Hover states are distinguishable
- [ ] Error/warning colors are noticeable but not jarring

## Language Testing

### JavaScript/TypeScript
- [ ] Keywords (const, let, function, class) use correct colors
- [ ] String literals and template literals are colored
- [ ] Comments are styled with italic gray-green
- [ ] Function names are sky blue
- [ ] Class names are purple
- [ ] Numbers and booleans are pink
- [ ] Import/export statements are distinct

### Python
- [ ] def and class keywords are styled
- [ ] Decorators are visible
- [ ] String literals (including f-strings) are colored
- [ ] Built-in functions are highlighted
- [ ] Self parameter has appropriate styling

### HTML
- [ ] Tags are forest green (light) or soft green (dark)
- [ ] Attributes are sky blue
- [ ] Attribute values are orange
- [ ] Comments are gray-green

### CSS/SCSS
- [ ] Selectors are properly colored
- [ ] Properties are sky blue
- [ ] Values are orange
- [ ] Variables are distinct
- [ ] Media queries are readable

### JSON
- [ ] Property names are colored appropriately
- [ ] String values are orange
- [ ] Numbers are pink
- [ ] Booleans and null are styled

### Markdown
- [ ] Headers are bold and colored
- [ ] Links are blue and underlined
- [ ] Code blocks have distinct background
- [ ] Bold and italic text work correctly
- [ ] Lists are readable

### YAML
- [ ] Keys are properly colored
- [ ] Values are distinct
- [ ] Indentation is clear
- [ ] Comments are gray-green

## UI Element Testing

### Editor
- [ ] Background color is comfortable for extended use
- [ ] Line numbers are visible but not distracting
- [ ] Current line highlight is subtle
- [ ] Selection color provides good contrast
- [ ] Find/replace highlights are visible
- [ ] Bracket matching is clear

### Sidebar
- [ ] File tree is readable
- [ ] Selected files are highlighted
- [ ] Git status colors are correct
- [ ] Icons (if any) are visible

### Activity Bar
- [ ] Active icon is clearly indicated
- [ ] Inactive icons are visible but subdued
- [ ] Badges are noticeable

### Status Bar
- [ ] Text is readable
- [ ] Different states (normal, debugging) are distinct
- [ ] Git branch info is visible

### Terminal
- [ ] All ANSI colors are visible
- [ ] Text is readable on background
- [ ] Cursor is visible
- [ ] Selection works properly

### Tabs
- [ ] Active tab is clearly distinguished
- [ ] Inactive tabs are readable
- [ ] Modified indicator is visible
- [ ] Tab borders are appropriate

## Special Features

### Bracket Pair Colorization
- [ ] Each bracket level has distinct color
- [ ] Colors cycle appropriately
- [ ] Mismatched brackets are indicated

### Git Integration
- [ ] Modified files show orange indicator
- [ ] Added files show green indicator
- [ ] Deleted files show red indicator
- [ ] Gutter indicators are visible

### Diff Editor
- [ ] Added lines have green background
- [ ] Removed lines have red background
- [ ] Inline changes are highlighted

### Minimap
- [ ] Code structure is visible
- [ ] Current viewport is indicated
- [ ] Colors provide useful overview

## Error States
- [ ] Error squiggles are red and visible
- [ ] Warning squiggles are orange and visible
- [ ] Info squiggles are blue and visible
- [ ] Problem panel shows appropriate colors

## Performance
- [ ] Theme loads quickly
- [ ] No noticeable lag when switching themes
- [ ] Scrolling remains smooth
- [ ] Syntax highlighting is responsive

## Edge Cases
- [ ] Very long lines display correctly
- [ ] Unicode characters are handled properly
- [ ] Mixed language files work (e.g., HTML with embedded JS)
- [ ] Large files maintain performance

## Accessibility
- [ ] Screen reader users can distinguish elements
- [ ] High contrast mode doesn't break theme
- [ ] Colorblind users can use theme effectively

## Final Checks
- [ ] README has accurate information
- [ ] CHANGELOG is up to date
- [ ] Package.json has correct metadata
- [ ] Icon displays properly in marketplace
- [ ] No console errors in developer tools