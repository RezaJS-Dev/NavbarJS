# Navigation Bar Web Component

A customizable, responsive navigation bar web component built with modern web standards.

## Features

- 🎯 **Responsive Design** - Adapts to desktop, tablet, and mobile screens
- 📍 **Sticky Navigation** - Becomes fixed at the top when scrolling
- 🍔 **Side Menu** - Slide-out menu with accordion dropdown functionality
- 🎨 **Customizable Styling** - Uses CSS custom properties for easy theming
- 🌍 **RTL Support** - Built with right-to-left language support
- 🔍 **Search Functionality** - Integrated search box with toggle animation
- 📱 **Social Media Integration** - Built-in social media links
- ♿ **Accessibility** - Proper semantic markup and keyboard navigation support

## Installation

### Basic HTML Usage

```html
<!DOCTYPE html>
<html lang="fa">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Website</title>
</head>
<body>
    <nav-bar></nav-bar>
    
    <!-- Your content here -->
    
    <script src="path-to/nav-bar.js"></script>
</body>
</html>
```

### As ES6 Module

```javascript
import './nav-bar.js';

// Use in your HTML
// <nav-bar></nav-bar>
```

## Usage

### Basic Implementation

```html
<nav-bar></nav-bar>
```

### Customized Implementation

```html
    <nav-bar id="navbar1"
             style="
               --nav-bar-font: byekan;
               --nav-bar-font-size: 18px;
               --nav-bar-background-color: transparent;
               --nav-bar-menu-background-color: #e1e1e1;
               --nav-bar-links-color: #3030ef;
               --nav-bar-links-hover: #ef30c6;" 
             menu-button-label = '[{"text": "فروشگاه"}]'
             logo = '[{ "src": "./assets/images/logo.png", "href": "javascript:void(0)" }]'
             side-menu-logo = '[{ "src": "./assets/images/logo.png", "href": "javascript:void(0)" }]'
             side-menu-list = '[
               {
                 "text": "مبلمان راحتي",
                 "link": "javascript:void(0)",
                 "icon": "./assets/images/icon1.png", 
                 "accordion": "", 
                 "dropdown": ""
               },
               {
                 "text": "مبلمان اداري",
                 "link": "javascript:void(0)",
                 "icon": "./assets/images/icon2.png", 
                 "accordion": "", 
                 "dropdown": ""
               },
               {
                 "text": "انواع ميز",
                 "link": "javascript:void(0)",
                 "icon": "./assets/images/icon5.png", 
                 "accordion": "yes", 
                 "dropdown": [
                   { "text": "ميز ناهارخوري", "href": "javascript:void(0)" },
                   { "text": "ميز آشپزخانه", "href": "javascript:void(0)" },
                   { "text": "ميز پذيرايي", "href": "javascript:void(0)" },
                   { "text": "ميز تحرير", "href": "javascript:void(0)" }
                 ]
               },
               {
                 "text": "سرويس خواب",
                 "link": "javascript:void(0)",
                 "icon": "./assets/images/icon3.png", 
                 "accordion": "", 
                 "dropdown": ""
               },
               {
                 "text": "فرش و موكت",
                 "link": "javascript:void(0)",
                 "icon": "./assets/images/icon4.png", 
                 "accordion": "", 
                 "dropdown": ""
               }
             ]'
             social-links = '[
               { "instagram": "javascript:void(0)" },
               { "email": "somewhere@gmail.com" },
               { "telegram": "javascript:void(0)" },
               { "whatsapp": "989123456789" },
               { "phone": "02112345678" }
             ]'
             items = '[
               { "text": "درباره ما", "href": "/" },
               { "text": "تماس با ما", "href": "/guide" }
             ]'
    ></nav-bar>
	<script src="./nav-bar.js"></script>
```

## Styling Customization

The component uses CSS custom properties for easy theming:

```css
:root {
  /* Main navigation colors */
  --nav-bar-background-color: #ffffff;
  --nav-bar-links-color: #333333;
  --nav-bar-links-hover: #007bff;
  
  /* Typography */
  --nav-bar-font: 'Arial', sans-serif;
  --nav-bar-font-size: 16px;
  
  /* Side menu */
  --nav-bar-menu-background-color: #f8f9fa;
}
```

### Example Custom Theme

```css
:root {
  --nav-bar-background-color: #2c3e50;
  --nav-bar-links-color: #ecf0f1;
  --nav-bar-links-hover: #3498db;
  --nav-bar-font: 'Tahoma', 'Arial', sans-serif;
  --nav-bar-font-size: 14px;
  --nav-bar-menu-background-color: #34495e;
}
```

## Attributes

| Attribute | Type | Description | Default |
|-----------|------|-------------|---------|
| `logo` | JSON Array | Main logo image and link | `[{src: '', href: 'javascript:void(0)'}]` |
| `menu-button-label` | JSON Array | Menu button text | `[{text: 'محصولات'}]` |
| `side-menu-logo` | JSON Array | Side menu logo image and link | `[{src: '', href: 'javascript:void(0)'}]` |
| `side-menu-list` | JSON Array | Side menu items with nested structure | See example below |
| `social-links` | JSON Array | Social media links | See example below |
| `items` | JSON Array | Main navigation items | `[{text: 'درباره ما', href: 'javascript:void(0)'}]` |

### Side Menu List Structure

```json
[
  {
    "text": "آيتم اول",
    "link": "/item1",
    "icon": "/icon1.png",
    "accordion": "",
    "dropdown": []
  },
  {
    "text": "آيتم دوم", 
    "link": "/item2",
    "icon": "/icon2.png",
    "accordion": "yes",
    "dropdown": [
      { "text": "زیر آيتم اول", "href": "/subitem1" },
      { "text": "زیر آيتم دوم", "href": "/subitem2" }
    ]
  }
]
```

### Social Links Structure

```json
[
  { "email": "contact@example.com" },
  { "instagram": "https://instagram.com/username" },
  { "telegram": "https://t.me/username" },
  { "whatsapp": "1234567890" },
  { "phone": "1234567890" }
]
```

## Component Structure

### Navigation Elements
- **Logo** - Customizable logo with link
- **Menu Button** - Hamburger menu with animated toggle
- **Navigation Items** - Right-aligned navigation links
- **User Actions** - Shopping cart, user profile, and search functionality

### Side Menu Features
- **Logo Section** - Dedicated logo display
- **Accordion Menu** - Expandable/collapsible menu items with nested dropdowns
- **Social Media Links** - Email, Instagram, Telegram, WhatsApp, and phone links
- **Smooth Animations** - CSS transitions for opening/closing

## Browser Compatibility

- ✅ Chrome 67+
- ✅ Firefox 63+
- ✅ Safari 10.1+
- ✅ Edge 79+

## Dependencies

- [Line Awesome Icons](https://icons8.com/line-awesome) - Icon library (loaded via CDN)

## Technical Details

- **Shadow DOM**: Uses open Shadow DOM for encapsulation
- **CSS Reset**: Comprehensive CSS reset for consistent styling
- **Adopted StyleSheets**: Modern CSSStyleSheet API for efficient styling
- **Event Handling**: Comprehensive JavaScript for interactive functionality
- **Media Queries**: Responsive breakpoints for optimal display

## Development

### Building from Source

```bash
# Clone the repository
git clone https://github.com/your-username/nav-bar-component.git

# Navigate to project directory
cd nav-bar-component
```

### File Structure

```
nav-bar-component/
├── nav-bar.js          # Main component file
├── README.md           # Documentation
├── examples/           # Usage examples
│   ├── basic.html
│   └── advanced.html
└── demo/               # Demo files
    └── index.html
```

## License

MIT License - feel free to use this component in your projects.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Support

If you have any questions or issues, please open an issue on GitHub.

