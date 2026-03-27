# Lucidchart Import Instructions for Recipe Deployment Flow

## Overview
This document provides instructions for importing the recipe deployment flow diagram into Lucidchart using the provided CSV file.

## Files Provided
1. `recipe-deployment-flow-lucidchart.csv` - CSV format for Lucidchart import
2. `recipe-deployment-flow.png` - Visual reference of the flow diagram

## Import Steps

### Method 1: CSV Import (Recommended)
1. **Open Lucidchart**
   - Go to [lucidchart.com](https://www.lucidchart.com)
   - Sign in to your account

2. **Create New Document**
   - Click "New" or "Create New Document"
   - Select "Blank Document" or "Flowchart"

3. **Import CSV Data**
   - Go to **File** → **Import Data**
   - Select **CSV** as the import format
   - Click "Choose File" and select `recipe-deployment-flow-lucidchart.csv`
   - Click "Import"

4. **Configure Import Settings**
   - Map the columns appropriately:
     - **Id**: Unique identifier for each shape
     - **Name**: Text displayed in the shape
     - **Shape**: Shape type (Process, Decision, Terminator, Database)
     - **Fill Color**: Background color of the shape
     - **Source**: Starting point of connector
     - **Target**: Ending point of connector
     - **Label**: Text on the connector line

5. **Auto-Layout**
   - After import, use Lucidchart's auto-layout feature
   - Go to **Arrange** → **Auto Layout**
   - Select "Flowchart" layout style
   - Adjust spacing and alignment as needed

### Method 2: Manual Recreation
If CSV import doesn't work as expected, you can manually recreate the diagram using the PNG as reference:

1. **Open the PNG Reference**
   - Open `recipe-deployment-flow.png` in a separate window

2. **Add Shapes**
   - Use the shape library on the left
   - Add shapes in this order:
     - **Terminator** (rounded rectangle): Start and End nodes
     - **Decision** (diamond): Decision points
     - **Process** (rectangle): Action steps
     - **Database** (cylinder): Data repositories

3. **Apply Colors**
   - **Green (#90EE90)**: Success states
   - **Red (#FFB6C1)**: Error/failure states
   - **Blue (#87CEEB)**: Database repositories
   - **White (#FFFFFF)**: Standard process steps

4. **Connect Shapes**
   - Use connectors to link shapes
   - Add labels to connectors (DEV, UAT, PROD, Valid, Invalid, Success, Failure)

5. **Arrange Layout**
   - Use top-to-bottom flow
   - Align shapes for clarity
   - Ensure proper spacing

## Diagram Structure

### Flow Sequence
1. **Start**: DevOps Team Initiates One-Click Script
2. **Decision**: Identify Target Stage
3. **Branch**: Three paths (DEV, UAT, PROD)
4. **Database**: Seed Data Repository (stage-specific)
5. **Process**: Fetch Recipe Collections
6. **Decision**: Validate Recipes
7. **Branch**: Valid or Invalid
8. **Process** (if valid): Transform to Tenant Format
9. **Process**: Upload to Target Tenant
10. **Decision**: Verify Upload
11. **Branch**: Success or Failure
12. **End**: Deployment Successful or Failed

### Shape Types and Colors

| Shape Type | Use Case | Color |
|------------|----------|-------|
| Terminator | Start/End points | Green (success) / Red (failure) |
| Decision | Choice points | White |
| Process | Action steps | White / Red (errors) |
| Database | Data storage | Blue |

### Connector Labels
- **DEV, UAT, PROD**: Stage selection
- **Valid, Invalid**: Validation results
- **Success, Failure**: Verification outcomes

## Tips for Best Results

1. **Spacing**: Maintain consistent spacing between shapes (50-100px)
2. **Alignment**: Use Lucidchart's alignment tools for clean layout
3. **Grouping**: Group related shapes for easier manipulation
4. **Layers**: Use layers to organize different stages if needed
5. **Text Size**: Use 12-14pt font for readability
6. **Line Style**: Use solid lines for main flow, dashed for alternative paths

## Customization Options

### Adding Swimlanes
To organize by stage (DEV/UAT/PROD):
1. Add horizontal swimlanes
2. Place stage-specific steps in respective lanes
3. Label lanes: "DEV Stage", "UAT Stage", "PROD Stage"

### Adding Icons
Enhance visual appeal:
1. Add icons for:
   - Script/automation (gear icon)
   - Database (database icon)
   - Success (checkmark)
   - Error (X or warning icon)

### Adding Notes
Include additional context:
1. Add text boxes with notes
2. Link to detailed documentation
3. Include version information

## Troubleshooting

### CSV Import Issues
- **Problem**: Shapes not connecting properly
  - **Solution**: Verify Source and Target IDs match shape IDs

- **Problem**: Colors not applying
  - **Solution**: Manually apply colors using the format panel

- **Problem**: Layout is messy
  - **Solution**: Use auto-layout feature or manually arrange

### Alternative Formats
If CSV doesn't work, Lucidchart also supports:
- **Visio files (.vsdx)**: Export from other tools
- **Draw.io files (.drawio)**: Convert Mermaid to Draw.io first
- **Image import**: Use PNG as background and trace over it

## Export Options from Lucidchart

Once created, you can export as:
- **PDF**: For documentation
- **PNG/JPG**: For presentations
- **SVG**: For web use
- **Visio**: For Microsoft compatibility

## Additional Resources

- [Lucidchart CSV Import Guide](https://lucid.app/documents/help/import-data)
- [Flowchart Best Practices](https://lucid.app/documents/help/flowchart-best-practices)
- [Shape Library Reference](https://lucid.app/documents/help/shape-libraries)

## Support

For issues or questions:
1. Check Lucidchart's help documentation
2. Contact Lucidchart support
3. Refer to the original Mermaid diagram in `recipe-deployment-flow.mmd`