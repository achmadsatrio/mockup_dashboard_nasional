# National/Regional Dashboard Wireframes

Medium-fidelity wireframes for the new National/Regional dashboard of Taraswin Sales Backend system.

## Overview

These wireframes demonstrate the user interface and functionality for a national-level dashboard that manages global master data and provides aggregated reporting across all areas. The dashboard supports a hierarchical structure: **National → Regional → Area**.

## System Architecture

```
National Level (This Dashboard)
    ├── Manages global master data
    ├── Assigns data to Regional/Area
    └── Provides national/regional reports
        
Regional Level
    ├── Consumes national master data
    ├── Assigns to areas
    └── Can have specific configurations
        
Area Level (Existing Dashboard)
    ├── Consumes master data
    ├── Area-specific configurations
    └── Operational activities
```

## Key Features

### Master Data Management (Global Level)
1. **3-Level Channel Hierarchy**
   - Channel (Modern, Traditional)
   - Outlet Category (Supermarket, Minimarket, Warung, etc.)
   - Classification (Gold, Silver, Bronze) - Auto-calculated with manual override

2. **Product Management with Area Assignment**
   - National base products
   - Area-specific pricing and configurations
   - Bulk import/export capabilities

3. **Roles & Permissions**
   - National roles (available in all areas)
   - Area-specific roles (only in assigned areas)
   - Granular permission management

4. **Area & Regional Management**
   - Hierarchical organization structure
   - Area assignment and configuration
   - Link to existing area dashboards

### Reports & Analytics
- Sales overview with multi-level filtering
- Product performance across areas
- Outlet analytics by classification
- Employee performance metrics

## Wireframe Files

### 01. Dashboard Layout
**File**: `01-dashboard-layout.html`

The base layout structure used across all pages.

**Components**:
- Fixed left sidebar with navigation menu
- Sticky top navigation bar
- Breadcrumb navigation
- User profile and notifications
- Main content area

**Navigation Menu**:
- Dashboard (Home)
- Master Data
  - Channels
  - Products
  - Roles & Permissions
  - Areas & Regions
- Reports
  - Sales Reports
  - Product Reports
  - Outlet Reports
  - Employee Reports
- Settings

### 02. Dashboard Home
**File**: `02-dashboard-home.html`

Landing page with KPIs and quick overview.

**Key Elements**:
- Welcome header with level indicator
- 4 KPI cards (Areas, Outlets, Products, Users)
- Sales trend chart (line/bar)
- Top performing areas chart
- Product category distribution (pie)
- Recent activities table
- Quick actions panel
- System status indicators

**Actions**:
- Export report
- Date range filtering
- Quick access to management pages

### 03. Channel Management
**File**: `03-channel-management.html`

3-level channel hierarchy management.

**Key Elements**:
- Hierarchical tree view table
- Level 1: Channels (Modern, Traditional)
- Level 2: Outlet Categories (Supermarket, Minimarket, Warung, etc.)
- Level 3: Classifications (Gold, Silver, Bronze)
- Classification settings modal
- Auto-calculation rules configuration

**Actions**:
- Add/Edit/Delete channels and categories
- Configure classification thresholds
- Set color codes for classifications

**Important Notes**:
- Classifications are auto-calculated based on average transaction value over last 3 months
- Manual override available per outlet
- Classification settings affect all outlets globally

### 04. Product Management
**File**: `04-product-management.html`

National product management with area assignments.

**Key Elements**:
- Product data table with search/filter
- Product code, name, category, base price
- Active areas badge count
- Area assignment modal
- Area-specific configuration panel

**Actions**:
- Add/Edit products
- Bulk import/export
- Assign products to areas
- Set area-specific prices and settings

**Area Assignment Features**:
- Multi-select areas
- Configure per-area pricing
- Set initial stock levels
- Area-specific notes/settings
- Status toggle per area

**Important Notes**:
- Base price set at national level
- Each area can override with custom pricing
- Product can be active in some areas and inactive in others
- Areas have independent stock management

### 05. Roles & Permissions
**File**: `05-roles-permissions.html`

Role-based access control management.

**Key Elements**:
- Scope selector tabs (National/Area/All)
- Roles data table
- Permission grouping by category
- Add/Edit role modals
- View role details modal

**Actions**:
- Create/Edit/Delete roles
- Assign permissions
- Set role scope (National/Area-specific)
- Assign areas for area-specific roles
- View assigned users

**Permission Categories**:
- Master Data Management
- Operational
- Reports & Analytics
- User Management

**Important Notes**:
- National roles automatically appear in all areas
- Area-specific roles only appear in assigned areas
- Permissions can be grouped and selected in bulk

### 06. Area & Regional Management
**File**: `06-area-regional.html`

Hierarchical area and regional organization.

**Key Elements**:
- Regional cards with summary stats
- Area cards in grid layout
- View toggle (Card/List view)
- Add/Edit area modal
- Link to existing area dashboard

**Regional Information**:
- Total areas count
- Total outlets count
- Active products count
- Edit regional details

**Area Card Information**:
- Area name and status
- Outlet count
- Active products count
- User count
- Quick actions (Edit, View Dashboard)

**Actions**:
- Add/Edit areas
- Assign to regional
- Activate/Deactivate areas
- View area dashboard (link to existing system)

### 07. Reports Dashboard
**File**: `07-reports.html`

Comprehensive national/regional reporting.

**Key Elements**:
- Advanced filter panel (Date, Regional, Area)
- 4 report tabs:
  1. Sales Overview
  2. Product Performance
  3. Outlet Analytics
  4. Employee Performance

**Sales Overview Tab**:
- Summary cards (Total Sales, Growth, Avg Transaction)
- Sales by Regional (bar chart)
- Sales by Channel (donut chart)
- Sales trend analysis (multi-line chart)
- Top 10 areas table with metrics

**Product Performance Tab**:
- Summary cards (Products Sold, Active Products, Avg Revenue)
- Product category comparison chart
- Stock movement analysis
- Top products table
- Area-wise product adoption heatmap

**Outlet Analytics Tab**:
- Classification summary cards (Gold/Silver/Bronze counts)
- New outlets trend chart
- Channel distribution chart
- Outlet distribution map
- Outlets by channel & classification table

**Employee Performance Tab**:
- Summary cards (Total Employees, Avg Visits, Compliance)
- Performance metrics by area chart
- Activity summary chart
- Top performers table
- Schedule compliance metrics

**Actions**:
- Export reports
- Schedule automated reports
- Apply multi-level filters
- Drill down into specific areas

## Technical Notes

### Technology Stack
- **HTML5**: Semantic markup
- **CSS3**: Custom styling (see `styles.css`)
- **No JavaScript framework**: Static wireframes for demonstration

### Styling
- **Color Scheme**:
  - Primary: Blue (#3B82F6)
  - Success: Green (#10B981)
  - Warning: Yellow (#F59E0B)
  - Danger: Red (#EF4444)
  - Gold: #FFD700
  - Silver: #C0C0C0
  - Bronze: #CD7F32

### Responsive Design
- Desktop-first approach (admin dashboard)
- Breakpoints:
  - Desktop: 1024px+
  - Tablet: 768px - 1023px
  - Mobile: < 768px
- Collapsible sidebar on smaller screens
- Stacked layouts for mobile

### Components Used
- Data tables with sorting/pagination
- Modal dialogs
- Form inputs and selects
- Dropdown menus
- Tree view components
- Chart placeholders
- Badge indicators
- Card layouts
- Tab navigation
- Breadcrumb navigation

## How to View

1. Open any HTML file in a web browser
2. Start with `01-dashboard-layout.html` to see the overall structure
3. Navigate using the sidebar menu or direct file links
4. All files are standalone and can be viewed independently

**Recommended viewing order**:
1. `01-dashboard-layout.html` - Layout structure
2. `02-dashboard-home.html` - Dashboard overview
3. `03-channel-management.html` - Channel hierarchy
4. `04-product-management.html` - Product & area assignment
5. `05-roles-permissions.html` - RBAC system
6. `06-area-regional.html` - Area organization
7. `07-reports.html` - Reporting dashboard

## Navigation Flow

```
Dashboard Home
├── Master Data
│   ├── Channels → Add/Edit/Configure Classifications
│   ├── Products → Add/Edit → Assign to Areas
│   ├── Roles & Permissions → Add/Edit Roles → Assign Permissions
│   └── Areas & Regions → Add/Edit Areas → View Area Dashboard (External)
└── Reports
    ├── Sales Overview → Filter → Export
    ├── Product Performance → Analyze → Export
    ├── Outlet Analytics → View Map → Export
    └── Employee Performance → View Metrics → Export
```

## User Interactions

### Modals
- Click overlay or "Cancel" button to close
- Click "X" button to close (if present)
- Form validation on submit

### Tables
- Click row to select (where applicable)
- Action buttons for Edit/Delete/View
- Sortable columns (indicated by headers)
- Pagination controls at bottom

### Forms
- Required fields marked with *
- Inline validation
- Dropdown selects for predefined options
- Multi-select for areas/permissions

### Charts
- Placeholder boxes show chart type and purpose
- Interactive tooltips (in production)
- Legend for multi-series charts
- Click to drill down (in production)

## Data Model Concepts

### Channel Hierarchy
```
Channel (Level 1)
└── Outlet Category (Level 2)
    └── Classification (Level 3)
        ├── Gold (> Rp 50M avg/3mo)
        ├── Silver (Rp 20M - 50M avg/3mo)
        └── Bronze (< Rp 20M avg/3mo)
```

### Product Assignment
```
Product (National)
├── Base Price
├── National Settings
└── Area Assignments
    ├── Area A: Custom Price, Stock, Settings
    ├── Area B: Custom Price, Stock, Settings
    └── ...
```

### Role Scope
```
Roles
├── National Roles → Available in ALL areas automatically
└── Area-Specific Roles → Only in assigned areas
```

## Implementation Notes

### For Frontend Developers

1. **Replace Chart Placeholders**: Use Chart.js, ApexCharts, or similar
2. **Add Real Data**: Connect to API endpoints
3. **Implement Interactions**: 
   - Table sorting and filtering
   - Modal open/close
   - Form validation
   - Tab switching
4. **Add State Management**: React Context, Redux, or Vuex
5. **API Integration**: Connect all CRUD operations
6. **Authentication**: Integrate with JWT auth system

### For Backend Developers

1. **New Tables Required**:
   - `channels` (3-level hierarchy)
   - `outlet_classifications` (Gold/Silver/Bronze with thresholds)
   - `product_area_assignments` (pivot with custom fields)
   - `role_scopes` (National vs Area-specific)

2. **API Endpoints Needed**:
   - Channel CRUD with hierarchy
   - Product area assignment
   - Role scope management
   - National/regional reporting aggregation

3. **Business Logic**:
   - Auto-classification calculation
   - National role propagation
   - Area-specific product pricing
   - Multi-level filtering for reports

### Database Schema Additions

```sql
-- Channels (3-level hierarchy)
channels
├── id
├── parent_id (nullable, self-reference)
├── level (1=Channel, 2=Category, 3=Classification)
├── code
├── name
├── description
└── status

-- Classification Settings
classification_settings
├── id
├── name (Gold/Silver/Bronze)
├── min_threshold
├── color_code
└── description

-- Product Area Assignments
product_area_assignments
├── id
├── product_id
├── area_id (company_id in current schema)
├── custom_price (nullable)
├── initial_stock
├── special_settings
├── status
└── timestamps

-- Role Scopes
role_scopes
├── id
├── role_id
├── scope_type (national/area)
├── area_ids (JSON array for area-specific)
└── timestamps
```

## Future Enhancements

1. **Real-time Updates**: WebSocket for live data
2. **Advanced Filtering**: Save filter presets
3. **Custom Dashboards**: Drag-and-drop widgets
4. **Export Scheduling**: Automated report generation
5. **Mobile App**: Native mobile experience
6. **Offline Mode**: Progressive Web App capabilities
7. **Advanced Analytics**: Predictive insights using ML
8. **Multi-language**: i18n support

## Support & Feedback

For questions or feedback regarding these wireframes:
- Review the plan document for detailed specifications
- Check component annotations in HTML files
- Refer to the architectural diagrams in plan

## Version History

- **v1.0** (February 2026) - Initial wireframe creation
  - 7 complete wireframes
  - Medium-fidelity design
  - All core features covered

---

**Created**: February 9, 2026  
**Purpose**: Development guide for National/Regional Dashboard  
**Status**: Ready for review and implementation
