# Interactive Photo Collage

An interactive web application that allows users to explore a house through clickable images and hover effects.

## Features

- **Landing Page**: Side-by-side display of New York map and house exterior
- **House Overview**: Interior view with clickable room entrances
- **Room Views**: Individual room views with interactive objects
- **Hover Effects**: Tooltips with images and descriptions for objects
- **Responsive Design**: Works on desktop and mobile devices
- **Smooth Transitions**: Animated navigation between views

## Image Placeholders

Replace the following placeholder images with your own content:

### Landing Page Images
- `images/ny_map.jpg` - New York map image (recommended: 800x400px)
- `images/house_exterior.jpg` - House exterior image (recommended: 800x400px)

### House Overview
- `images/house_interior_overview.jpg` - Interior overview with visible room entrances (recommended: 1000x600px)

### Room Images
- `images/living_room.jpg` - Living room view (recommended: 1000x600px)
- `images/kitchen.jpg` - Kitchen view (recommended: 1000x600px)
- `images/bedroom.jpg` - Bedroom view (recommended: 1000x600px)

### Interactive Object Detail Images
#### Living Room Objects
- `images/sofa_detail.jpg` - Close-up of sofa
- `images/painting_detail.jpg` - Close-up of painting
- `images/books_detail.jpg` - Close-up of bookshelf

#### Kitchen Objects
- `images/stove_detail.jpg` - Close-up of stove
- `images/spices_detail.jpg` - Close-up of spice rack
- `images/fruits_detail.jpg` - Close-up of fruits

#### Bedroom Objects
- `images/bed_detail.jpg` - Close-up of bed
- `images/window_view.jpg` - View from window
- `images/dresser_detail.jpg` - Close-up of dresser

## Customization

### Adding New Interactive Objects

1. Add a new div with class `interactive-object` in the appropriate room view
2. Position it using CSS `top`, `left`, `width`, and `height` properties
3. Add a tooltip div with class `object-tooltip` containing:
   - An image with class `tooltip-image`
   - A paragraph with description text

Example:
```html
<div class="interactive-object" id="newObject" 
     style="top: 40%; left: 50%; width: 15%; height: 20%;">
    <div class="object-tooltip">
        <img src="images/new_object_detail.jpg" alt="New Object" class="tooltip-image">
        <p>Description of the new object</p>
    </div>
</div>
```

### Modifying Room Entrances

1. Locate the clickable area in the house overview
2. Adjust the `top`, `left`, `width`, and `height` CSS properties to match your image
3. Update the room label text if needed

### Changing Text Content

- Room labels: Edit the text inside `.room-label` divs
- Object descriptions: Edit the paragraph text inside `.object-tooltip` divs
- Navigation title: Edit the `.nav-title` content in the HTML

## File Structure

```
interactive-photo-collage/
├── index.html          # Main HTML file
├── css/
│   └── styles.css      # All CSS styles
├── js/
│   └── script.js       # Interactive functionality
├── images/             # Image assets (add your images here)
└── README.md          # This documentation
```

## Usage Instructions

1. Replace all placeholder images in the `images/` folder with your own content
2. Open `index.html` in a web browser
3. Click on the house image to enter the house overview
4. Click on room entrances to navigate to specific rooms
5. Hover over objects in rooms to see detailed tooltips
6. Click objects for a larger modal view
7. Use the back button or press Escape to navigate back

## Browser Compatibility

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## Mobile Support

The application is fully responsive and supports touch interactions on mobile devices.

