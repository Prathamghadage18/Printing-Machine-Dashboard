# Industrial Print Monitor Dashboard

A comprehensive real-time monitoring dashboard for industrial printing machines, providing insights into operational efficiency, energy consumption, and production metrics.

## 🚀 Features

### Real-Time Monitoring
- **Live Data Updates**: Automatic refresh every 30 seconds with real-time machine status
- **Multi-Machine Support**: Monitor up to 2 printing machines simultaneously
- **Interactive Charts**: Dynamic visualizations using Chart.js with smooth animations

### Key Metrics Tracked

#### 📊 Running Hours Analysis
- Total running hours (24-hour view)
- Average running rate per hour
- Uptime percentage and downtime tracking
- Hourly and shift-wise breakdowns
- Weekly and monthly historical trends

#### 📏 Production Metrics
- Total running length in meters
- Average production rate (meters/hour)
- Current speed monitoring
- Target progress tracking
- Production output trends

#### ⚡ Electrical Parameters
- Active energy consumption (kWh)
- Active power monitoring (kW)
- Current draw tracking (Amperes)
- Power factor analysis
- Real-time status indicators with color-coded alerts
- 24-hour min/max/average statistics
- Trend sparklines for quick visual analysis

#### 🔋 Energy & Production Correlation
- Energy per running hour efficiency metrics
- Energy per meter cost analysis
- Total energy consumption tracking
- Production vs energy correlation analysis (R²)
- Scatter plots showing efficiency relationships
- Shift-wise consumption comparisons

### 🎨 User Interface
- **Dark Theme**: Professional dark interface optimized for industrial environments
- **Responsive Design**: Fully responsive layout for desktop, tablet, and mobile devices
- **Interactive Elements**: Clickable metric cards with drill-down capabilities
- **Color-Coded Status**: Visual indicators for normal, warning, and critical states
- **Machine Tabs**: Easy switching between different machine views

### 📈 Data Visualization
- **Line Charts**: Time-series data for hourly trends
- **Bar Charts**: Shift-wise and weekly comparisons
- **Scatter Plots**: Correlation analysis between energy and production
- **Sparklines**: Mini trend charts in data tables
- **Dual-Axis Charts**: Multiple metrics on single visualizations

### 🛠️ Functional Features
- **Time Range Filtering**: Hour, Shift, Day, Week, and Month views
- **Machine Filtering**: View all machines or focus on specific equipment
- **Export Capabilities**: CSV export for all data and individual tables
- **Drill-Down Modal**: Detailed analysis for any metric
- **Actionable Insights**: Automated recommendations based on data patterns

## 🏗️ Technical Architecture

### Frontend Technologies
- **HTML5**: Semantic markup with accessibility considerations
- **CSS3**: Custom CSS with CSS variables for theming
- **JavaScript ES6+**: Modern JavaScript with Chart.js integration
- **Bootstrap 5**: Responsive grid system and components
- **TailwindCSS**: Utility-first CSS framework

### Data Visualization
- **Chart.js 4.4.1**: Interactive charting library
- **Real-time Updates**: Automatic data refresh with smooth animations
- **Responsive Charts**: Charts that adapt to screen size
- **Custom Themes**: Dark-optimized chart styling

### Integration Capabilities
- **Elements SDK**: Configurable dashboard parameters
- **Data SDK**: External data source integration
- **Customizable Settings**: Machine names, colors, and display options

## 📋 System Requirements

### Browser Compatibility
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

### Performance Requirements
- Minimum 4GB RAM recommended
- Modern JavaScript engine required
- Stable internet connection for real-time updates

## 🚀 Installation & Setup

### Quick Start
1. Clone or download the project files
2. Open `dashboard.html` in a modern web browser
3. The dashboard will initialize with sample data

### Configuration
The dashboard supports runtime configuration through the Elements SDK:

```javascript
const config = {
    dashboard_title: 'Industrial Print Monitor',
    machine_1_name: 'Machine 1',
    machine_2_name: 'Machine 2',
    background_color: '#0a0e14',
    card_color: '#1a2230',
    text_color: '#e8ecf0',
    accent_color: '#00d4ff',
    secondary_accent: '#ff6b35'
};
```

### Data Integration
To integrate with real data sources:
1. Replace the sample data generation functions
2. Connect to your API endpoints
3. Update the `updateCharts()` function with real data fetching

## 📊 Data Structure

### Machine Data Format
```javascript
{
    timestamp: "2024-01-01T12:00:00Z",
    machine_id: "m1",
    running_hours: 0.75,
    running_length: 1875,
    energy_consumption: 38.7,
    current_draw: 58.2,
    power_factor: 0.94,
    status: "running"
}
```

### API Endpoints Expected
- `/api/machines/status` - Current machine status
- `/api/metrics/hours` - Running hours data
- `/api/metrics/production` - Production metrics
- `/api/metrics/energy` - Energy consumption data
- `/api/metrics/electrical` - Electrical parameters

## 🎯 Usage Guide

### Navigation
- **Machine Tabs**: Click to switch between machine views
- **Time Range Buttons**: Select different time periods for analysis
- **Metric Cards**: Click any card to see detailed drill-down analysis
- **Export Button**: Download data as CSV for external analysis

### Understanding Indicators
- 🟢 **Green**: Normal operating range
- 🟡 **Yellow**: Warning/attention required
- 🔴 **Red**: Critical/alert condition
- ⚪ **Gray**: Offline/no data

### Filtering Data
1. Use the machine dropdown to focus on specific equipment
2. Select time range buttons to change analysis period
3. Charts and metrics update automatically

## 🔧 Customization

### Styling
Modify CSS variables in the `<style>` section:
```css
:root {
    --bg-primary: #0a0e14;
    --accent-cyan: #00d4ff;
    --accent-orange: #ff6b35;
    /* ... other variables */
}
```

### Adding New Metrics
1. Add metric cards to the HTML structure
2. Update chart configurations in `initCharts()`
3. Modify data generation functions
4. Add export functionality if needed

### Branding
- Update the logo SVG in the header
- Modify color scheme through CSS variables
- Customize machine names through configuration

## 📈 Performance Optimization

### Chart Performance
- Charts use `update('none')` for smooth animations
- Data refresh rate optimized at 30 seconds
- Efficient DOM manipulation for updates

### Memory Management
- Chart instances properly destroyed on modal close
- Event listeners properly managed
- No memory leaks in long-running sessions

## 🐛 Troubleshooting

### Common Issues
1. **Charts not loading**: Check Chart.js CDN connection
2. **Data not updating**: Verify JavaScript console for errors
3. **Responsive issues**: Test on different screen sizes
4. **Export not working**: Ensure browser supports blob downloads

### Debug Mode
Enable browser developer tools to monitor:
- Console errors and warnings
- Network requests (if using real data)
- Performance metrics


### Development Guidelines
1. Follow existing code style and patterns
2. Test responsive behavior on multiple devices
3. Ensure accessibility standards are met
4. Update documentation for new features

### Code Structure
- **HTML**: Semantic structure with Bootstrap grid
- **CSS**: Component-based styling with CSS variables
- **JavaScript**: Modular functions with clear separation of concerns

## 📞 Support

For technical support or questions:
- Review the troubleshooting section
- Check browser console for error messages
- Verify all CDN dependencies are accessible

## 📄 License

This project is provided as-is for industrial monitoring purposes. Please ensure compliance with your organization's data security and privacy policies when deploying in production environments.

---

**Version**: 1.0.0  
**Last Updated**: 2024  
**Framework**: Vanilla JavaScript with Chart.js  
**Compatibility**: Modern browsers with ES6+ support
