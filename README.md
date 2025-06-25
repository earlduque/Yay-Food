# Yay Food - Restaurant Food Rating & Review App

## Overview

**Yay Food** is a ServiceNow-based application designed for users to record ratings and notes for individual food items at restaurants. The app provides a collaborative platform where groups of users can share their dining experiences, track their favorite dishes, and discover new culinary recommendations.

## Purpose

The primary purpose of Yay Food is to help users:
- **Track food experiences** - Record ratings and personal notes for specific dishes
- **Collaborate with groups** - Share restaurant and food recommendations within organized groups
- **Discover new favorites** - Browse ratings and reviews from other group members
- **Organize dining data** - Maintain structured records of restaurants, food items, and member preferences

## Key Features

### 🏪 Restaurant Management
- Add and manage restaurant information including name, location, and notes
- Organize restaurants by groups for better collaboration
- Track restaurant details with encrypted notes for privacy

### 🍽️ Food Item Tracking
- Record individual food items with ratings (decimal scale)
- Add personal notes and observations for each dish
- Link food items to specific restaurants
- Associate food items with group members who have tried them

### 👥 Group Collaboration
- Create password-protected groups for organized sharing
- Add members to groups for collaborative rating
- Customizable sorting preferences for viewing food items:
  - Average Rating (High to Low / Low to High)
  - Single Rating (High to Low / Low to High)
  - Alphabetical (A-Z / Z-A)
  - Review Date (Latest / Oldest)

### 🔐 Access Control
- Group-based access control for restaurants and food items
- Password protection for group membership
- Encrypted notes for sensitive information

## Data Model

The application consists of four main data tables:

### 1. Groups (`x_snc_yay_food_groups`)
- **Name**: Group identifier
- **Password**: Secure access control
- **Sort Preference**: Customizable viewing options
- **Number**: Auto-generated identifier

### 2. Members (`x_snc_yay_food_members`)
- **Name**: Member identifier
- **Group**: Reference to group membership
- **Number**: Auto-generated identifier

### 3. Restaurants (`x_snc_yay_food_restaurants`)
- **Name**: Restaurant name
- **Location**: Physical address or location
- **Group**: Associated group for access control
- **Note**: Encrypted notes about the restaurant
- **Number**: Auto-generated identifier

### 4. Food (`x_snc_yay_food_food`)
- **Food**: Name of the dish
- **Restaurant**: Reference to the restaurant
- **Rating**: Decimal rating for the dish
- **Note**: Personal notes about the food item
- **Members**: List of group members who have tried this dish
- **Number**: Auto-generated identifier

## User Interface

The app provides a ServiceNow Service Portal interface accessible at `/yayfood` with:
- Modern, responsive design
- Custom CSS styling for optimal user experience
- Public access for easy sharing
- Role-based access control

## Technical Details

- **Platform**: ServiceNow
- **Scope**: `x_snc_yay_food`
- **Version**: 1.0.0
- **License**: None (internal use)
- **Runtime Access Tracking**: Permissive
- **Scoped Administration**: False

## Usage

1. **Create or Join a Group**: Set up a group with a password for collaborative sharing
2. **Add Restaurants**: Enter restaurant information including name, location, and notes
3. **Record Food Items**: Add individual dishes with ratings and personal notes
4. **Share with Members**: Invite group members to view and contribute ratings
5. **Browse and Sort**: Use customizable sorting options to find the best-rated dishes

## Installation

This is a ServiceNow application that should be imported into a ServiceNow instance. The repository contains all necessary XML files for:
- Database tables and relationships
- UI components and pages
- Security configurations
- Application metadata

## Development Notes

⚠️ **Important**: This repository contains generated ServiceNow files. Do not edit these files outside of a ServiceNow instance to maintain data integrity and checksum validation.

For development and customization, always work within the ServiceNow platform to ensure proper version control and data consistency.

---

*Yay Food - Making restaurant experiences more delicious through shared knowledge! 🍕🍜🍔*
