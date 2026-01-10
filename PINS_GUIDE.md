# 📍 Map Pins Management Guide

## Quick Start

All your map pins are located in **`index.html`** starting at **line 1548**.

Look for this section:
```javascript
// 📍 MAP PINS - ADD OR REMOVE LOCATIONS HERE
```

---

## How to Add a New Pin

### Step 1: Copy the Template
```javascript
{
    name: 'Short Name*',              // Required: Short display name
    place: 'Location Name*',          // Required: Main location name
    fullName: 'Full Official Name*',  // Required: Full location name
    address: 'Full Address*',         // Required: Street address
    coords: [latitude, longitude],    // Required: [40.7128, -74.0060]
    description: 'Your description',  // Optional: Main description text
    quote1: 'First quote',            // Optional: First quote
    quote2: 'Second quote',           // Optional: Second quote
    timeOfDay: 'day',                 // Required: 'day', 'night', or 'both'
    umbrellaCategory: 'Category*',    // Required: See category list below
    subCategory: 'Subcategory*'       // Required: Must match umbrella category
},
```

### Step 2: Fill in Your Details
- **name**: Short name displayed on the pin
- **place**: Location neighborhood/area
- **fullName**: Official full name of the place
- **address**: Complete street address
- **coords**: [latitude, longitude] - Get from Google Maps
- **description**: What makes this place special
- **quote1, quote2**: (Optional) Personal quotes about the place
- **timeOfDay**: Choose 'day', 'night', or 'both'
- **umbrellaCategory**: Choose from the 5 main categories (see below)
- **subCategory**: Must match your umbrella category (see combinations below)

### Step 3: Find the Right Section
Place your new pin in the appropriate category section:
- **Blossoming Love** - Parks, Nature & Romantic Spots
- **Golden Hour** - Sunsets, Views & Photography
- **Sweet Moments** - Cafés, Desserts & Cozy Spots
- **Adventure Together** - Activities, Exploration & Day Trips
- **Just for Us** - Museums, Cultural Spots & Intimate Places

### Step 4: Paste and Save
Paste your new pin object into the array, making sure to add a comma after the closing brace `},`

---

## Valid Category Combinations

### 🌸 Blossoming Love
- Parks & Gardens
- Walks / Scenic Routes
- Quiet Cafés
- Viewpoints

### 🌅 Golden Hour
- Rooftops
- Waterfront Spots
- Scenic Walks
- Photography Locations

### 🍰 Sweet Moments
- Dessert Spots
- Cozy Cafés
- Late-Night Food
- Bookstores

### 🎒 Adventure Together
- Day Trips
- Physical Activities
- Neighborhood Exploration
- Ferries / Water

### 💜 Just for Us
- Hidden Spots
- Quiet Museums
- Intimate Bars
- No-Plan Walks
- Special Places

---

## How to Remove a Pin

1. Find the pin you want to remove in `index.html`
2. Delete the entire pin object (from opening `{` to closing `},`)
3. Save the file

**Tip**: Make sure not to leave an extra comma at the end!

---

## How to Hide a Pin (Without Deleting It)

Want to temporarily hide a pin but keep it in your code for later? Just add `hidden: true` to the pin:

```javascript
{
    name: 'Cherry Blossoms',
    place: 'Roosevelt Island',
    fullName: 'Franklin D. Roosevelt Four Freedoms Park',
    address: '1 FDR Four Freedoms Park, New York, NY 10044',
    coords: [40.749864, -73.961200],
    description: 'Beautiful cherry blossoms in spring',
    timeOfDay: 'day',
    umbrellaCategory: 'Blossoming Love',
    subCategory: 'Parks & Gardens',
    hidden: true  // ← Add this line to hide the pin
},
```

**To show it again**: Just remove the `hidden: true` line or change it to `hidden: false`

---

## How to Get Coordinates

1. Go to [Google Maps](https://maps.google.com)
2. Right-click on the location
3. Click on the coordinates (they'll be copied automatically)
4. Paste in format: `[latitude, longitude]`

Example: `[40.7580, -73.9855]`

---

## File Structure

```
index.html (lines 1548-1920)
├── PIN TEMPLATE & GUIDE (lines 1503-1548)
├── HOME LOCATIONS (lines 1550-1575)
├── BLOSSOMING LOVE (lines 1577-1630)
├── GOLDEN HOUR (lines 1632-1690)
├── SWEET MOMENTS (lines 1692-1720)
├── ADVENTURE TOGETHER (lines 1722-1800)
└── JUST FOR US (lines 1802-1920)
```

---

## Tips

✅ **DO**:
- Use the template provided in the code
- Match subCategory with umbrellaCategory
- Add commas after each pin object
- Test after adding/removing pins

❌ **DON'T**:
- Mix up category combinations
- Forget the comma after your pin object
- Delete the home locations (Bhavi Home, Bel Home)
- Remove the closing `];` after the last pin

---

## Need Help?

If something breaks:
1. Check the browser console for errors (F12)
2. Make sure all brackets `{}` and commas are in place
3. Verify your category combinations are valid
4. Check that coordinates are in the right format

---

**Happy Pin Adding! 🗺️✨**
