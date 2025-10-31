# Health & Wellness Articles Website

## Files Overview

This website consists of three main files:

1. **index.html** - The main webpage
2. **articles.csv** - Contains all article data
3. **filters.csv** - Contains filter categories and subcategories

## How to Modify Filters (filters.csv)

The `filters.csv` file controls what filter options appear in the sidebar.

### CSV Format:
```csv
category,subcategory,value,label
```

### Columns Explained:
- **category**: The main category header (e.g., "Nutrition", "Fitness", "Mental Health")
- **subcategory**: Description of the filter option (currently same as label)
- **value**: The tag value that must match tags in articles.csv (e.g., "diet", "cardio")
- **label**: The text displayed to users in the filter checkbox

### Example:
```csv
Nutrition,Diet & Meal Planning,diet,Diet & Meal Planning
Fitness,Cardio,cardio,Cardio
Mental Health,Sleep Health,sleep,Sleep Health
```

### To Add a New Filter Category:

1. **Add a new category** (e.g., "Lifestyle"):
```csv
Lifestyle,Time Management,time-management,Time Management
Lifestyle,Work-Life Balance,work-life-balance,Work-Life Balance
```

2. **Add a new subcategory to existing category**:
```csv
Nutrition,Superfoods,superfoods,Superfoods
```

### Important Notes:
- The **value** field must exactly match the tags used in `articles.csv`
- Keep the header row intact: `category,subcategory,value,label`
- No empty lines between rows
- Use hyphens instead of spaces in the value field (e.g., "work-life-balance")

## How to Modify Articles (articles.csv)

### CSV Format:
```csv
title,author,date,excerpt,tags,categories
```

### Columns Explained:
- **title**: Article headline
- **author**: Author name
- **date**: Publication date
- **excerpt**: Article preview/description
- **tags**: Multiple tags separated by pipes `|` (must match filter values)
- **categories**: Additional categorization (separated by pipes)

### Example:
```csv
"Your Article Title","Author Name","October 31, 2025","This is the article description...","diet|nutrition|health","nutrition|wellness"
```

### Tag Guidelines:
- Tags should match the **value** field in `filters.csv`
- Separate multiple tags with `|` (pipe character)
- Example: `"sleep|mindfulness|stress"`

### To Add a New Article:

```csv
"Morning Meditation Guide","Jane Doe","November 1, 2025","Learn simple meditation techniques to start your day with clarity and focus.","mindfulness|stress","mental-health"
```

## Common Modifications

### Adding a New Topic Area:

1. **Update filters.csv**:
```csv
Wellness,Relationships,relationships,Relationships
Wellness,Community,community,Community
```

2. **Update articles.csv** with matching tags:
```csv
"Building Strong Relationships","John Smith","Nov 1, 2025","Tips for nurturing meaningful connections.","relationships|wellness","wellness"
```

### Tips:
- ✅ Always use quotes around fields containing commas
- ✅ Keep the header row in both CSV files
- ✅ Ensure tag values in articles.csv match filter values in filters.csv
- ✅ Use consistent date formatting
- ❌ Don't use line breaks inside CSV fields
- ❌ Don't leave empty lines in the CSV

## Testing Your Changes

1. Save your CSV files
2. Refresh the webpage in your browser
3. Check that new filters appear in the sidebar
4. Verify that articles are properly filtered by the new tags

## Troubleshooting

**Filters not appearing?**
- Check that `filters.csv` is in the same folder as `index.html`
- Verify the CSV format is correct (no extra quotes or commas)
- Check browser console for errors (F12)

**Articles not showing?**
- Ensure `articles.csv` is in the same folder
- Verify tags match filter values exactly
- Check that quotes are properly closed in the CSV

**Filtering not working?**
- Make sure the tag values in articles.csv exactly match the value field in filters.csv
- Tag matching is case-sensitive
