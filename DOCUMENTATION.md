# DonorCore - Complete Documentation

**Version:** 1.0.0  
**Author:** Lalit RajPurohit  
**License:** GPL-2.0+

---

## Table of Contents

1. [Introduction](#introduction)
2. [Requirements](#requirements)
3. [Installation](#installation)
4. [Quick Start Guide](#quick-start-guide)
5. [Features Overview](#features-overview)
6. [Campaign Management](#campaign-management)
7. [Donation Forms](#donation-forms)
8. [Shortcodes Reference](#shortcodes-reference)
9. [Gutenberg Blocks](#gutenberg-blocks)
10. [Donor Management](#donor-management)
11. [Settings & Configuration](#settings--configuration)
12. [Email Templates](#email-templates)
13. [PDF Receipt Templates](#pdf-receipt-templates)
14. [Styling Customization](#styling-customization)
15. [Troubleshooting](#troubleshooting)
16. [FAQ](#faq)
17. [Changelog](#changelog)

---

## Introduction

**DonorCore** is a professional donation management plugin that transforms WooCommerce into a powerful fundraising platform. Built with modern React technology and following WordPress.org coding standards, DonorCore provides nonprofits, NGOs, charities, and community organizations with a complete solution for managing donations, tracking donors, and generating automated receipts.

### Why Choose DonorCore?

- ✅ **WooCommerce Native** - Leverages WooCommerce's secure checkout system
- ✅ **Modern Admin Dashboard** - React-powered interface with real-time analytics
- ✅ **Complete Donor Management** - Track lifetime value, donation history, and contact information
- ✅ **Automated Receipts** - Generate and email PDF receipts automatically
- ✅ **Flexible Campaigns** - Create unlimited campaigns with goal tracking
- ✅ **Deep Customization** - Style every aspect without writing code
- ✅ **GDPR Compliant** - Integrates with WordPress privacy tools
- ✅ **Performance Optimized** - Database indexing, caching, and query optimization

---

## Requirements

### Minimum Requirements

| Requirement | Version |
|------------|---------|
| **WordPress** | 6.5 or higher |
| **PHP** | 7.4 or higher |
| **WooCommerce** | 8.0 or higher |
| **PHP Extensions** | mbstring (for PDF generation) |
| **Email** | SMTP configuration required for receipt emails |

### Recommended Requirements

| Requirement | Version |
|------------|---------|
| **WordPress** | 6.9+ |
| **PHP** | 8.0+ |
| **WooCommerce** | 8.5+ |
| **MySQL** | 5.7+ or MariaDB 10.3+ |

### Browser Support

- Chrome/Edge (latest 2 versions)
- Firefox (latest 2 versions)
- Safari (latest 2 versions)

---

## Installation

### Automatic Installation

1. Log in to your WordPress admin panel
2. Navigate to **Plugins → Add New**
3. Search for "DonorCore"
4. Click **Install Now** on the DonorCore plugin
5. After installation, click **Activate**

### Manual Installation

1. Download the plugin ZIP file
2. Log in to your WordPress admin panel
3. Navigate to **Plugins → Add New → Upload Plugin**
4. Choose the ZIP file and click **Install Now**
5. After installation, click **Activate**

### Via FTP

1. Download and extract the plugin ZIP file
2. Upload the `donorcore-premium-woocommerce-donation-plugin` folder to `/wp-content/plugins/`
3. Log in to your WordPress admin panel
4. Navigate to **Plugins** and activate **DonorCore**

> **Note:** DonorCore requires WooCommerce to be installed and activated. If WooCommerce is not detected, you'll see an admin notice with a link to install it.

---

## Quick Start Guide

Follow these steps to get started with DonorCore in under 10 minutes:

### Step 1: Verify Installation

After activation, you should see a new **DonorCore** menu in your WordPress admin sidebar.

### Step 2: Configure General Settings

1. Navigate to **DonorCore → Settings**
2. Go to the **General** tab
3. Set your minimum donation amount (default: $10)
4. Configure suggested donation amounts (e.g., 25, 50, 100, 250)
5. Click **Save Settings**

### Step 3: Configure SMTP for Email Receipts

> **⚠️ Important:** Email receipts require SMTP configuration to work properly.

**Recommended SMTP Plugin:**
Install **WP Mail SMTP** or **Easy WP SMTP**:

1. Go to **Plugins → Add New**
2. Search for "WP Mail SMTP"
3. Install and activate
4. Configure your SMTP settings:
   - SMTP Host (e.g., smtp.gmail.com)
   - SMTP Port (587 for TLS, 465 for SSL)
   - SMTP Username (your email)
   - SMTP Password
5. Send a test email to verify

**Alternative SMTP Services:**
- Gmail SMTP
- SendGrid
- Mailgun
- Amazon SES
- Any SMTP service

### Step 4: Create Your First Campaign

1. Navigate to **Campaigns → Add New** (standard WordPress post editor)
2. Enter a campaign title (e.g., "Emergency Relief Fund")
3. Set a fundraising goal (e.g., $10,000)
4. Configure suggested donation amounts (e.g., 25, 50, 100, 250)
5. Optionally set start date and end date
6. Write a campaign description
7. Click **Publish**

### Step 4: Add a Donation Form

**Using Gutenberg Block:**

1. Edit any page or post
2. Click the **+ Add Block** button
3. Search for "Donation Form"
4. Select the **Donation Form** block
5. In the block settings sidebar, select your campaign
6. Update the page

**Using Shortcode:**

Add this shortcode to any page or post:
```
[dc_donation_form campaign_id="123"]
```
Replace `123` with your actual campaign ID.

### Step 5: Test a Donation

1. Visit your donation form page
2. Select an amount or enter a custom amount
3. Fill in donor details
4. Complete the checkout process
5. Check that the email and PDF receipt were sent to Donor Email Address

> **Note:** If emails are not being sent, verify your SMTP configuration. See [Troubleshooting](#troubleshooting) section.

### Step 6: View Analytics

1. Navigate to **DonorCore → Dashboard**
2. View real-time donation statistics
3. Check the timeline chart to see donation trends
4. View the top donors leaderboard

🎉 **Congratulations!** Your donation system is now live.

---

## Features Overview

### 1. React Admin Dashboard

A modern, fast, and intuitive admin interface built with React and Material-UI.

**Features:**
- Real-time donation analytics
- Interactive timeline charts showing donation trends
- Quick stats cards (Total Raised, Donors, Campaigns, Monthly Revenue)
- Top 10 donors leaderboard
- Responsive design for mobile and tablet

**Access:** Navigate to **DonorCore → Dashboard**

### 2. Campaign Management

Create and manage unlimited fundraising campaigns with goal tracking.

**Features:**
- Set fundraising goals
- Track progress with visual progress bars
- Set campaign end dates
- Custom suggested amounts per campaign
- Campaign-specific analytics
- WooCommerce integration via custom product type

**Access:** **Campaigns → Add New** or **Campaigns → All Campaigns**

### 3. Donor Management

Complete donor database with detailed profiles and donation history.

**Features:**
- Searchable donor database
- Individual donor profiles showing:
  - Lifetime donation value
  - Total donation count
  - Contact information (email, phone)
  - Full donation history with campaign details
- Material-UI drawer interface for quick viewing
- Export donor data for email campaigns

**Access:** Navigate to **DonorCore → Donors**

### 4. Donation Forms

Flexible donation forms with two deployment methods:

**Gutenberg Block:**
- Live preview in editor
- Campaign selection
- Custom suggested amounts
- Mobile-responsive

**Shortcode:**
- Embed anywhere
- Template compatibility
- Widget support

### 5. Automated Email & PDF Receipts

Professional receipts sent automatically after every donation.

> **⚠️ SMTP Required:** Email functionality requires SMTP configuration. Install a plugin like WP Mail SMTP.

**Email Features:**
- HTML email templates
- Dynamic placeholders (donor name, amount, campaign, etc.)
- Custom subject lines
- Background processing via Action Scheduler
- Site logo embedding

**PDF Features:**
- Automatically generated PDF receipts
- HTML-based templates
- Same placeholder system as emails
- Attached to donation emails
- Secure download links

### 6. Complete Styling Control

Customize every visual aspect of your donation forms and progress bars from a central admin panel.

**Customizable Elements:**
- Colors (primary, secondary, background, text, borders)
- Typography (font family, sizes, weights, line height)
- Spacing (padding, margin, gap)
- Borders & shadows
- Button styles (radius, padding, hover effects)
- Progress bar styles (height, colors, text)
- Custom CSS support

---

## Campaign Management

### Creating a Campaign

1. Navigate to **Campaigns → Add New**
2. Enter campaign details:
   - **Title:** Campaign name (e.g., "Build a School")
   - **Goal Amount:** Fundraising target (e.g., 50000)
   - **End Date:** Optional campaign end date
   - **Description:** Campaign story and details
3. Set a featured image (recommended: 1200x630px)
4. Click **Publish**

### Campaign Settings

#### Goal Tracking

Set a fundraising goal to display progress bars:

```
Goal: $50,000
Raised: $23,450
Progress: 47%
```

Progress bars automatically update as donations come in.

#### End Dates

When a campaign reaches its end date:
- Donation forms automatically lock
- A "Campaign Ended" message displays
- No new donations are accepted
- Existing donations remain tracked

#### Custom Suggested Amounts

Override global suggested amounts per campaign:

**Global Settings:** 25, 50, 100, 250  
**Campaign Override:** 100, 250, 500, 1000

### Viewing Campaign Analytics

1. Navigate to **DonorCore → Campaigns**
2. View list of all campaigns with metrics:
   - Total raised
   - Number of donors
   - Progress percentage
   - Status (Active/Ended)

### Editing Campaigns

Campaigns are standard WordPress custom posts, so you can:
- Edit title, content, and featured image
- Change goal amounts
- Update end dates
- Modify suggested amounts
- Delete or trash campaigns

---

## Donation Forms

### Using the Donation Form Block

The Donation Form block is a Gutenberg block that provides a visual, customizable donation form.

#### Adding the Block

1. Edit any page or post
2. Click **+ Add Block**
3. Search for "Donation Form"
4. Click to insert the block

#### Block Settings

In the **Block Settings** sidebar (right panel):

| Setting | Description | Example |
|---------|-------------|---------|
| **Select Campaign** | Choose which campaign to link | "Emergency Relief" |
| **Suggested Amounts** | Override default amounts | 50, 100, 250, 500 |
| **Custom Amount Enabled** | Allow custom donation amounts | Yes (default) |

#### Live Preview

The block shows a live preview in the editor. Changes to styling in **Settings → Donation Form Styling** update immediately.

### Using the Donation Form Shortcode

For theme templates, widgets, or classic editor:

```php
[dc_donation_form campaign_id="123"]
```

#### Shortcode Attributes

| Attribute | Description | Default | Example |
|-----------|-------------|---------|---------|
| `campaign_id` | Campaign post ID | Required | `123` |


#### Finding Campaign ID

1. Go to **Campaigns → All Campaigns**
2. Hover over a campaign title
3. Look in the browser status bar: `post=123` (123 is the ID)

Or edit the campaign and check the URL:
```
.../wp-admin/post.php?post=123&action=edit
```

#### Shortcode Examples

**Basic Usage:**
```php
[dc_donation_form campaign_id="456"]
```

**Custom Amounts:**
```php
[dc_donation_form campaign_id="456" amounts="100,250,500,1000"]
```

**In PHP Templates:**
```php
<?php echo do_shortcode('[dc_donation_form campaign_id="456"]'); ?>
```

---

## Shortcodes Reference

### 1. Donation Form Shortcode

**Shortcode:** `[dc_donation_form]`

**Purpose:** Displays a fully functional donation form for a specific campaign.

**Required Attributes:**
- `campaign_id` - The ID of the campaign

**Example:**
```php
[dc_donation_form campaign_id="123"]
```

**Output:**
- Donation amount buttons
- Custom amount input field
- Donor information form (handled by WooCommerce)
- Submit button
- Campaign progress (if goal is set)

### 2. Campaign Progress Shortcode

**Shortcode:** `[dc_campaign_progress]`

**Purpose:** Displays a visual progress bar showing campaign fundraising progress.

**Required Attributes:**
- `id` - The campaign post ID

**Example:**
```php
[dc_campaign_progress id="123"]
```

**Output:**
- Visual progress bar
- Amount raised
- Goal amount
- Percentage complete
- Number of donors
- Campaign title

**Styling:** Progress bars inherit styles from **Settings → Progress Bar Styling**.

---

## Gutenberg Blocks

### 1. Donation Form Block

**Block Name:** `donor-core/donation-form`

**Description:** Interactive donation form with amount selection and custom amount input.

**Block Settings:**

| Setting | Type | Description |
|---------|------|-------------|
| Campaign | Dropdown | Select campaign to link donations |

> **Note:** Suggested amounts are configured in the campaign settings, not in the block editor.

**Features:**
- Live preview in editor
- Responsive layout
- Inherits global styling
- Mobile-optimized

**How to Add:**
1. Open the block inserter (+)
2. Search "Donation Form"
3. Click to insert
4. Configure in sidebar

### 2. Progress Bar Block

**Block Name:** `donor-core/progress-bar`

**Description:** Visual progress indicator showing campaign fundraising progress.

**Block Settings:**

| Setting | Type | Description |
|---------|------|-------------|
| Campaign | Dropdown | Select campaign to display progress |
| Show Goal | Toggle | Display goal amount |
| Show Raised | Toggle | Display amount raised |
| Show Donors | Toggle | Display donor count |

**Features:**
- Real-time progress updates
- Customizable via Settings panel
- Responsive design
- Animated progress fill

**How to Add:**
1. Open the block inserter (+)
2. Search "Progress Bar" or "Campaign Progress"
3. Click to insert
4. Select campaign in sidebar

---

## Donor Management

### Accessing the Donor Database

Navigate to **DonorCore → Donors**

### Donor List View

The donor table displays:

| Column | Description |
|--------|-------------|
| **Donor Name** | Full name from billing details |
| **Email** | Contact email address |
| **Lifetime Value** | Total amount donated |
| **Donations** | Number of separate donations |
| **Last Donation** | Date of most recent donation |
| **Actions** | View details button (eye icon) |

### Searching Donors

Use the search box to find donors by:
- Name (first or last)
- Email address

Results update in real-time as you type.

### Viewing Donor Details

Click the **eye icon** in the Actions column to open the donor details drawer.

**Drawer Contents:**

1. **Header Section:**
   - Donor name
   - Email address
   - Profile avatar

2. **Statistics Cards:**
   - **Lifetime Value:** Total amount donated
   - **Total Donations:** Number of donations made

3. **Contact Information:**
   - Email address (clickable mailto: link)
   - Phone number (clickable tel: link)

4. **Donation History:**
   - List of all donations including:
     - Campaign name
     - Donation amount
     - Donation date
     - Donation type (one-time/recurring)
   - Sorted by most recent first

### Donor Analytics

Donors are automatically tracked when they complete a donation through WooCommerce checkout.

**Data Stored:**
- Donor email (unique identifier)
- Customer ID (linked to WooCommerce user)
- Total lifetime value
- Total donation count
- First donation date
- Last donation date

**Database Table:** `wp_dc_donor_analytics`

---

## Settings & Configuration

Access all settings at **DonorCore → Settings**

Settings are organized into 5 tabs:

### 1. General Settings

**Minimum Donation Amount**
- Set the lowest acceptable donation amount
- Default: $10
- Used for form validation

**Suggested Amounts**
- Comma-separated list of preset donation amounts
- Default: 50, 100, 250, 500
- Displayed as buttons on donation forms
- Can be overridden per campaign

**Data Management**
- **Delete All Data** button: Truncates donation logs and analytics
- Use with caution - this action is irreversible
- Useful for testing or fresh starts

**How to Save:**
Click **Save Settings** at the bottom of the tab.

### 2. Email Template Settings

Customize the automated email receipts sent to donors.

**Email Subject**
- Default: "Your Donation Receipt from {site_name}"
- Supports placeholders (see [Email Templates](#email-templates))

**Email Template (HTML)**
- Full HTML editor with syntax highlighting
- Default template provided
- Supports all email placeholders

**Reset to Default**
- Restores default email subject and template
- Useful if customizations break formatting

**Email Placeholders Available:**

| Category | Placeholders |
|----------|-------------|
| **Donor Info** | `{donor_name}`, `{donor_first_name}`, `{donor_last_name}`, `{donor_email}` |
| **Donation Info** | `{amount}`, `{date}`, `{order_id}` |
| **Campaign Info** | `{campaign}`, `{campaign_name}` |
| **Site Info** | `{site_name}`, `{site_url}`, `{site_logo}` |

### 3. PDF Template Settings

Customize the PDF receipts attached to donation emails.

**PDF Body Template (HTML)**
- Full HTML editor
- Default template provided
- Supports all PDF placeholders

**PDF Placeholders Available:**

| Category | Placeholders |
|----------|-------------|
| **Donor Info** | `{donor_name}`, `{donor_email}`, `{donor_address}` |
| **Donation Info** | `{amount}`, `{currency}`, `{date}`, `{order_id}`, `{receipt_number}` |
| **Campaign Info** | `{campaign}` |
| **Organization Info** | `{org_name}`, `{org_address}`, `{site_logo}` |

**Receipt Number Format:** `DC-{order_id}-{year}`  
Example: `DC-1234-2026`

### 4. Donation Form Styling

Complete visual customization of donation forms.

**Typography**
- **Font Family:** System fonts or Google Fonts
- **Heading Size:** 14-32px
- **Body Size:** 12-24px
- **Button Font Size:** 12-24px
- **Font Weight:** 100-900
- **Line Height:** 1.0-2.0

**Colors**
- **Primary Color:** Main brand color
- **Secondary Color:** Hover states
- **Background Color:** Form container
- **Text Color:** Main text
- **Label Color:** Form labels
- **Border Color:** Input borders
- **Input Background:** Input fields
- **Input Focus Color:** Active input border

**Spacing & Layout**
- **Container Padding:** Internal spacing
- **Container Margin:** External spacing
- **Element Gap:** Space between form elements
- **Max Width:** Maximum form width
- **Amount Columns:** Button grid layout (1-4)

**Borders & Shadows**
- **Border Radius:** Container corners
- **Button Radius:** Button corners
- **Input Radius:** Input corners
- **Border Width:** Border thickness
- **Shadow:** None / Small / Medium / Large

**Buttons**
- **Padding Y:** Vertical button padding
- **Padding X:** Horizontal button padding
- **Hover Effect:** None / Lift / Glow / Scale

**Advanced**
- **Custom CSS:** Add custom styles
- **Amount Button Padding:** Suggested amount buttons

**Reset to Default:** Restores all styling to defaults.

### 5. Progress Bar Styling

Customize campaign progress bars.

**Typography**
- **Font Family**
- **Heading Size**
- **Body Size**
- **Font Weights** (heading, amount, label, percentage)

**Colors**
- **Primary Color:** Progress fill
- **Background Color:** Container background
- **Text Color:** General text
- **Fill Color:** Progress bar fill
- **Track Background:** Empty progress area
- **Percentage Text Color:** Completion percentage

**Layout**
- **Bar Height:** 10-60px
- **Container Padding**
- **Container Margin**
- **Max Width**
- **Border Radius**
- **Shadow**

**Custom CSS:** Override any default styles.

---

## Email Templates

### Default Email Template

DonorCore includes a professional default email template located at:
```
includes/Receipts/templates/email-default.html
```

### Customizing Email Templates

1. Navigate to **Settings → Email Template**
2. Edit the HTML in the editor
3. Use placeholders for dynamic content
4. Click **Save Settings**
5. Test by making a test donation

### Email Placeholder Reference

#### Donor Information

| Placeholder | Output Example | Description |
|------------|----------------|-------------|
| `{donor_name}` | John Doe | Full name (first + last) |
| `{donor_first_name}` | John | First name only |
| `{donor_last_name}` | Doe | Last name only |
| `{donor_email}` | john@example.com | Email address |

#### Donation Information

| Placeholder | Output Example | Description |
|------------|----------------|-------------|
| `{amount}` | $100.00 | Formatted donation amount with currency |
| `{date}` | January 22, 2026 | Donation date (formatted) |
| `{order_id}` | 1234 | WooCommerce order ID |

#### Campaign Information

| Placeholder | Output Example | Description |
|------------|----------------|-------------|
| `{campaign}` | Emergency Relief Fund | Campaign title |
| `{campaign_name}` | Emergency Relief Fund | Campaign title (alias) |

#### Site Information

| Placeholder | Output Example | Description |
|------------|----------------|-------------|
| `{site_name}` | My Charity | Site title from WordPress settings |
| `{site_url}` | https://example.com | Site homepage URL |
| `{site_logo}` | `<img src="...">` | Site logo as HTML image tag |

### Example Email Template

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Donation Receipt</title>
</head>
<body style="font-family: Arial, sans-serif; line-height: 1.6; color: #333;">
    <div style="max-width: 600px; margin: 0 auto; padding: 20px;">
        <!-- Logo -->
        <div style="text-align: center; margin-bottom: 30px;">
            {site_logo}
        </div>
        
        <!-- Header -->
        <h1 style="color: #0073aa; text-align: center;">
            Thank You for Your Donation!
        </h1>
        
        <!-- Greeting -->
        <p>Dear {donor_first_name},</p>
        
        <!-- Message -->
        <p>
            Thank you for your generous donation of <strong>{amount}</strong> 
            to {campaign} on {date}.
        </p>
        
        <p>
            Your contribution makes a real difference and helps us continue our mission.
        </p>
        
        <!-- Receipt Details -->
        <table style="width: 100%; border: 1px solid #ddd; border-collapse: collapse; margin: 20px 0;">
            <tr>
                <td style="padding: 10px; border: 1px solid #ddd; font-weight: bold;">
                    Donation Amount:
                </td>
                <td style="padding: 10px; border: 1px solid #ddd;">
                    {amount}
                </td>
            </tr>
            <tr>
                <td style="padding: 10px; border: 1px solid #ddd; font-weight: bold;">
                    Date:
                </td>
                <td style="padding: 10px; border: 1px solid #ddd;">
                    {date}
                </td>
            </tr>
            <tr>
                <td style="padding: 10px; border: 1px solid #ddd; font-weight: bold;">
                    Campaign:
                </td>
                <td style="padding: 10px; border: 1px solid #ddd;">
                    {campaign}
                </td>
            </tr>
            <tr>
                <td style="padding: 10px; border: 1px solid #ddd; font-weight: bold;">
                    Order ID:
                </td>
                <td style="padding: 10px; border: 1px solid #ddd;">
                    {order_id}
                </td>
            </tr>
        </table>
        
        <!-- Attached PDF Note -->
        <p style="background: #f9f9f9; padding: 15px; border-left: 4px solid #0073aa;">
            <strong>Note:</strong> A PDF receipt is attached to this email for your records.
        </p>
        
        <!-- Footer -->
        <p>
            Warm regards,<br>
            The {site_name} Team
        </p>
        
        <hr style="border: none; border-top: 1px solid #ddd; margin: 30px 0;">
        
        <p style="font-size: 12px; color: #666; text-align: center;">
            {site_name}<br>
            <a href="{site_url}" style="color: #0073aa;">{site_url}</a>
        </p>
    </div>
</body>
</html>
```

### Testing Email Templates

1. Make a test donation using WooCommerce's test mode
2. Check your email for the receipt
3. Verify all placeholders are replaced correctly
4. Check PDF attachment

---

## PDF Receipt Templates

### Default PDF Template

Located at:
```
includes/Receipts/templates/pdf-default.html
```

### Customizing PDF Templates

1. Navigate to **Settings → PDF Template**
2. Edit the HTML template
3. Use PDF-specific placeholders
4. Click **Save Settings**
5. Test with a donation

### PDF-Specific Placeholders

#### All Email Placeholders Plus:

| Placeholder | Output Example | Description |
|------------|----------------|-------------|
| `{receipt_number}` | DC-1234-2026 | Unique receipt number |
| `{currency}` | USD | Three-letter currency code |
| `{donor_address}` | 123 Main St... | Full formatted address |
| `{org_name}` | My Charity Org | Organization name |
| `{org_address}` | 456 Office Blvd... | Organization address |

### Example PDF Template

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Donation Receipt {receipt_number}</title>
    <style>
        body {
            font-family: 'DejaVu Sans', Arial, sans-serif;
            font-size: 12px;
            line-height: 1.6;
            color: #333;
        }
        .receipt-container {
            max-width: 800px;
            margin: 0 auto;
            padding: 40px;
        }
        .header {
            text-align: center;
            border-bottom: 3px solid #0073aa;
            padding-bottom: 20px;
            margin-bottom: 30px;
        }
        .receipt-title {
            font-size: 28px;
            color: #0073aa;
            margin: 0;
        }
        .receipt-number {
            font-size: 14px;
            color: #666;
            margin-top: 5px;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }
        table td {
            padding: 12px;
            border: 1px solid #ddd;
        }
        table td:first-child {
            font-weight: bold;
            background: #f9f9f9;
            width: 40%;
        }
        .footer {
            margin-top: 40px;
            padding-top: 20px;
            border-top: 2px solid #ddd;
            text-align: center;
            font-size: 10px;
            color: #666;
        }
    </style>
</head>
<body>
    <div class="receipt-container">
        <!-- Header with Logo -->
        <div class="header">
            {site_logo}
            <h1 class="receipt-title">Official Donation Receipt</h1>
            <p class="receipt-number">Receipt #: {receipt_number}</p>
        </div>
        
        <!-- Organization Info -->
        <h3>From:</h3>
        <p>
            <strong>{org_name}</strong><br>
            {org_address}
        </p>
        
        <!-- Donor Info -->
        <h3>To:</h3>
        <p>
            <strong>{donor_name}</strong><br>
            {donor_email}<br>
            {donor_address}
        </p>
        
        <!-- Donation Details -->
        <h3>Donation Details:</h3>
        <table>
            <tr>
                <td>Receipt Number</td>
                <td>{receipt_number}</td>
            </tr>
            <tr>
                <td>Date of Donation</td>
                <td>{date}</td>
            </tr>
            <tr>
                <td>Campaign</td>
                <td>{campaign}</td>
            </tr>
            <tr>
                <td>Amount Donated</td>
                <td><strong style="font-size: 16px;">{amount}</strong></td>
            </tr>
            <tr>
                <td>Currency</td>
                <td>{currency}</td>
            </tr>
            <tr>
                <td>Order ID</td>
                <td>{order_id}</td>
            </tr>
        </table>
        
        <!-- Tax Deductible Notice -->
        <p style="background: #f0f8ff; padding: 15px; border-left: 4px solid #0073aa;">
            <strong>Important:</strong> This receipt is for your records. 
            Please consult with your tax advisor regarding the deductibility of this donation.
        </p>
        
        <!-- Thank You Message -->
        <p style="text-align: center; font-size: 14px; margin: 30px 0;">
            Thank you for your generous support!
        </p>
        
        <!-- Footer -->
        <div class="footer">
            <p>{org_name}</p>
            <p>{site_url}</p>
            <p>This is an official receipt for your donation.</p>
        </div>
    </div>
</body>
</html>
```

### PDF Generation Library

DonorCore uses **Dompdf** for PDF generation:
- Supports most CSS 2.1 properties
- Handles images (including site logo)
- UTF-8 support for international characters
- A4 paper size, portrait orientation

---

## Styling Customization

### How to Update Styling

1. Go to **DonorCore → Settings**
2. Click on **Donation Form Styling** or **Progress Bar Styling** tab
3. Adjust the settings:
   - Typography (fonts, sizes, weights)
   - Colors (primary, secondary, backgrounds)
   - Spacing (padding, margins, gaps)
   - Borders & shadows
4. Click **Save Settings**
5. Clear your site cache if using a caching plugin
6. View your donation forms to see the changes

### Custom CSS

For advanced customizations, use the **Custom CSS** field in the Settings panel:

```css
/* Make donation buttons gradient */
.dc-amount-btn {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    border: none;
}

/* Customize amount button on hover */
.dc-amount-btn:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 20px rgba(102, 126, 234, 0.3);
}

/* Style the custom amount input */
.dc-custom-amount-input input {
    border: 2px solid var(--dc-df-primary);
}

/* Animate progress bar fill */
.dc-progress-fill {
    transition: width 1s ease-in-out;
}
```

### Targeting Specific Forms

Add custom classes via shortcode wrapper:

```html
<div class="emergency-fund-form">
    [dc_donation_form campaign_id="123"]
</div>
```

Then style specifically:

```css
.emergency-fund-form .dc-amount-btn {
    background: #ff4444;
}
```

---

## Developer API & Hooks

> **For Developer Use Only**  
> **Contact:** Lalit Rajpurohit (lalitraj881@gmail.com)

DonorCore provides REST API endpoints and WordPress hooks for advanced customization. For complete API documentation, developer hooks, and integration examples, please contact the developer directly.

---

## Troubleshooting

### Common Issues

#### 1. WooCommerce Not Detected

**Symptoms:**
- DonorCore shows "WooCommerce required" notice
- Plugin won't activate

**Solutions:**
1. Install WooCommerce from **Plugins → Add New**
2. Activate WooCommerce before activating DonorCore
3. Check if WooCommerce is a MU plugin (must-use)
4. Verify WooCommerce version is 8.0+

#### 2. PDF Generation Fails

**Symptoms:**
- No PDF attached to emails
- "mbstring extension required" error

**Solutions:**
1. **Enable mbstring extension:**
   - Contact your hosting provider
   - Or add to `php.ini`: `extension=mbstring`
   - Restart web server

2. **Check permissions:**
   ```
   chmod 755 wp-content/uploads/donor-core-receipts/
   ```

3. **Check Dompdf library:**
   - Verify `vendor/dompdf/` folder exists
   - Run `composer install` if missing

#### 3. Email Receipts Not Sending

**Symptoms:**
- Donors don't receive email receipts
- No email notifications

**Solutions:**

1. **⚠️ Configure SMTP (Most Common Issue):**

   WordPress default mail function often fails. You MUST configure SMTP:
   
   **Install WP Mail SMTP Plugin:**
   ```
   Plugins → Add New → Search "WP Mail SMTP" → Install → Activate
   ```
   
   **Configure SMTP Settings:**
   - Go to **WP Mail SMTP → Settings**
   - Choose mailer (Gmail, SendGrid, Mailgun, etc.)
   - Enter SMTP credentials:
     - SMTP Host: smtp.gmail.com (for Gmail)
     - SMTP Port: 587 (TLS) or 465 (SSL)
     - Username: your email
     - Password: app-specific password
   - Click **Save Settings**
   - Send test email to verify

2. **Test WordPress email:**
   - In WP Mail SMTP, go to **Email Test** tab
   - Send test email
   - Check inbox and spam folder

3. **Check Action Scheduler:**
   - Go to **WooCommerce → Status → Scheduled Actions**
   - Look for `dc_send_receipt` actions
   - Check if they completed or failed

3. **Check spam folder**

4. **Debug email sending:**
   ```php
   // Add to wp-config.php
   define('WP_DEBUG', true);
   define('WP_DEBUG_LOG', true);
   ```
   Check `wp-content/debug.log` for email errors

#### 4. Donation Forms Not Displaying

**Symptoms:**
- Shortcode shows raw text
- Block shows blank

**Solutions:**
1. **Check campaign ID:**
   - Verify campaign exists and is published
   - Confirm ID is correct number

2. **Clear caches:**
   - WordPress object cache
   - Page cache (if using caching plugin)
   - Browser cache

3. **Check JavaScript errors:**
   - Open browser console (F12)
   - Look for errors
   - Report to support if found

4. **Verify block registration:**
   - In block editor, search for "Donation Form"
   - If not found, deactivate and reactivate plugin

#### 5. Styling Not Applied

**Symptoms:**
- Forms look unstyled
- Settings changes don't appear

**Solutions:**
1. **Clear all caches**

2. **Check for CSS conflicts:**
   - Inspect element in browser
   - Look for overriding styles
   - Use `!important` in Custom CSS if needed

3. **Verify settings saved:**
   - Check **Settings → Donation Form Styling**
   - Click **Save Settings** again

4. **Check CSS variables:**
   - View page source
   - Look for `<style id="dc-dynamic-styles">`
   - Verify CSS variables are present

#### 6. Dashboard Shows No Data

**Symptoms:**
- Empty charts
- Zero stats despite donations

**Solutions:**
1. **Check database tables:**
   ```sql
   SELECT COUNT(*) FROM wp_dc_donation_logs;
   SELECT COUNT(*) FROM wp_dc_donor_analytics;
   ```

2. **Make a test donation:**
   - Use WooCommerce test mode
   - Complete checkout
   - Check if data appears

3. **Rebuild analytics:**
   - Go to **Settings → General**
   - Note: Currently no rebuild button (feature request)

4. **Clear query cache:**
   ```php
   // Add to functions.php temporarily
   delete_transient('dc_dashboard_overview');
   delete_transient('dc_dashboard_timeline');
   ```

### Debug Mode

Enable WordPress debug mode for detailed error logging:

```php
// wp-config.php
define('WP_DEBUG', true);
define('WP_DEBUG_LOG', true);
define('WP_DEBUG_DISPLAY', false);
define('SCRIPT_DEBUG', true);
```

Check logs at: `wp-content/debug.log`

### Browser Console Debugging

For React admin issues:

1. Open browser DevTools (F12)
2. Go to **Console** tab
3. Look for errors
4. Check **Network** tab for failed API requests

### Database Issues

Check table creation:

```sql
SHOW TABLES LIKE 'wp_dc_%';
```

Expected tables:
- `wp_dc_donation_logs`
- `wp_dc_donor_analytics`

If missing, deactivate and reactivate the plugin.

### Performance Issues

If the admin dashboard is slow:

1. **Increase PHP memory:**
   ```php
   // wp-config.php
   define('WP_MEMORY_LIMIT', '256M');
   define('WP_MAX_MEMORY_LIMIT', '512M');
   ```

2. **Enable caching:**
   - DonorCore caches queries for 30 minutes
   - Use object caching (Redis/Memcached)

3. **Limit data queries:**
   - Archive old campaigns
   - Export and delete old donation logs

### Getting Help

If you encounter issues not covered here:

1. Check DonorCore [GitHub Issues](mailto:lalitraj881@gmail.com)
2. Read WordPress.org support forum
3. Contact support with:
   - WordPress version
   - WooCommerce version
   - PHP version
   - Error messages from debug.log
   - Steps to reproduce

---

## FAQ

### General Questions

**Q: Is DonorCore free?**  
A: DonorCore is open-source and released under GPL-2.0+ license. It's free to use and modify.

**Q: Do I need WooCommerce Subscriptions for recurring donations?**  
A: No. DonorCore works with standard WooCommerce. Recurring donations may be added in future versions.

**Q: Can I accept international donations?**  
A: Yes. WooCommerce supports multiple currencies and payment gateways. Configure in **WooCommerce → Settings**.

**Q: Is DonorCore GDPR compliant?**  
A: Yes. DonorCore integrates with WordPress privacy tools for data export and erasure. Check **Settings → Privacy** in WordPress.

**Q: Can I migrate from another donation plugin?**  
A: Manual migration is required. Export data from your current plugin and import into WooCommerce orders.

### Features

**Q: How many campaigns can I create?**  
A: Unlimited campaigns.

**Q: Can I set campaign end dates?**  
A: Yes. Set an end date when creating/editing a campaign. Forms automatically lock when the date passes.

**Q: Can donors choose which campaign to support?**  
A: Each donation form is linked to a specific campaign. Create multiple forms for multiple campaigns.

**Q: Can I accept anonymous donations?**  
A: WooCommerce requires billing details for order processing. However, you can allow guest checkout so donors don't need accounts.

**Q: Do donation receipts go to the donor or admin?**  
A: Receipts are sent to the donor's billing email address, not the site admin.

### Customization

**Q: Can I change the donation form layout?**  
A: Yes. Use the Styling panel to adjust colors, fonts, spacing, and more. For advanced changes, add Custom CSS.

**Q: Can I translate DonorCore?**  
A: Yes. DonorCore is translation-ready with text domain `donor-core`. Use Loco Translate or Poedit.

**Q: Can I add my logo to receipts?**  
A: Yes. Upload a custom logo in **Appearance → Customize → Site Identity**. It automatically appears in emails and PDFs via the `{site_logo}` placeholder.

**Q: Can I customize the "Thank You" page after donation?**  
A: Yes. Configure in **WooCommerce → Settings → Advanced → Checkout**. Set a custom "Checkout" page.

### Technical

**Q: Does DonorCore work with HPOS (High-Performance Order Storage)?**  
A: Yes. DonorCore is fully compatible with WooCommerce HPOS.

**Q: Does DonorCore work with page builders?**  
A: Yes. Use shortcodes in Elementor, Divi, or any page builder that supports WordPress shortcodes.

**Q: Can I use DonorCore with a multisite network?**  
A: Each site in the network needs DonorCore installed separately. Shared data across sites is not currently supported.

**Q: Does DonorCore work with caching plugins?**  
A: Yes. DonorCore is compatible with WP Super Cache, W3 Total Cache, and other caching plugins.


### Donations & Payments

**Q: Which payment gateways are supported?**  
A: DonorCore uses WooCommerce checkout, so any WooCommerce-compatible payment gateway works (Stripe, PayPal, Square, etc.).

**Q: Can I offer payment plans for large donations?**  
A: Not currently. Each donation is a one-time WooCommerce order.

**Q: Can donors get tax receipts?**  
A: PDF receipts are automatically generated. However, you should consult legal/tax professionals to ensure receipts meet local regulations for tax deductibility.

**Q: Can I offer donation incentives (rewards)?**  
A: Not built-in, but you can manually send rewards or use WooCommerce extensions.

**Q: Can I set a maximum donation amount?**  
A: Not built-in. WooCommerce doesn't limit order totals by default.

---

## Changelog

### Version 1.0.0 (2026-01-22)

**Initial Release**

- ✅ React-based admin dashboard with real-time analytics
- ✅ Campaign custom post type with goal tracking
- ✅ Gutenberg blocks: Donation Form & Progress Bar
- ✅ Shortcodes: `[dc_donation_form]` and `[dc_campaign_progress]`
- ✅ Automated email receipts with customizable HTML templates
- ✅ Automated PDF receipt generation using Dompdf
- ✅ Donor management with searchable database
- ✅ Donor analytics: lifetime value, donation count, history
- ✅ Complete styling control panel for forms and progress bars
- ✅ Email & PDF template editor with placeholder system
- ✅ REST API for programmatic data access
- ✅ GDPR compliance via WordPress privacy tools
- ✅ WooCommerce HPOS compatibility
- ✅ Performance optimizations: indexing, caching, lazy loading
- ✅ Security: nonce validation, capability checks, prepared queries
- ✅ WordPress.org coding standards compliance

**Database:**
- `wp_dc_donation_logs` - Immutable donation ledger
- `wp_dc_donor_analytics` - Pre-calculated donor metrics

**Developer Features:**
- Action hooks: `donor_core_after_donation_saved`, `donor_core_receipt_generated`, `donor_core_email_sent`
- Filter hooks: `donor_core_minimum_donation_amount`, `donor_core_suggested_amounts`, `donor_core_email_subject`

---

## Credits

**Development Team:**
- Lead Developer: Lalit Rajpurohit
- Email: lalitraj881@gmail.com

**Libraries & Dependencies:**
- [React](https://reactjs.org/) - UI framework
- [Material-UI](https://mui.com/) - React component library
- [Dompdf](https://github.com/dompdf/dompdf) - PDF generation
- [WooCommerce](https://woocommerce.com/) - E-commerce platform

**Special Thanks:**
- WordPress.org plugin review team
- Beta testers and early adopters

---

## License

DonorCore is licensed under the **GNU General Public License v2.0 or later**.

```
Copyright (C) 2026 DonorCore Team

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 2 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
```

---

## Support

- **Developer Contact:** lalitraj881@gmail.com
- **Documentation:** This file (DOCUMENTATION.md) is publicly available
- **Support:** For plugin support, contact the developer directly

---

**Made with ❤️ for nonprofits worldwide**
