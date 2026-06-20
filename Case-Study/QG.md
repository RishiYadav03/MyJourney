# Case Study: Building a Custom Quotation Management System for the Interior Design Industry

## Overview

Over the past few months, I worked on designing and developing a custom Quotation Management System for the modular furniture and interior design industry. What started as a simple quotation tool evolved into a comprehensive business application capable of handling complex pricing calculations, multi-company operations, role-based access control, and automated PDF generation.

The objective was to eliminate manual Excel-based quotation processes and create a centralized platform that could streamline quotation creation, pricing management, user access control, and reporting.

---

# The Business Problem

The organization was generating quotations manually, which created several challenges:

* Time-consuming quotation preparation
* Inconsistent pricing calculations
* Difficulty managing multiple projects
* Lack of centralized quotation records
* No role-based access control
* Limited visibility across teams
* Manual PDF creation process
* Difficulty scaling operations across multiple business entities

The goal was to create a scalable web-based system capable of handling complex quotation workflows while maintaining accuracy and performance.

---

# Technology Stack

### Frontend

* HTML5
* CSS3
* Bootstrap
* JavaScript
* AJAX

### Backend

* PHP 8

### Database

* MySQL

### Additional Libraries

* DomPDF
* Composer

---

# Understanding the Business Workflow

Unlike a standard quotation system, this project required handling multiple layers of hierarchy.

A quotation could contain:

Quotation
→ Elevations
→ Units
→ Drawers
→ Shelves
→ Accessories
→ Materials
→ Pricing Components

For example:

Kitchen Quotation

* Elevation A

  * Tall Unit
  * Upper Unit
  * Bottom Unit

* Elevation B

  * Loft Unit
  * Tall Unit

Each unit had its own dimensions, material selections, accessories, pricing calculations, and storage components.

Managing this hierarchy became one of the most important architectural challenges of the project.

---

# Database Architecture Design

One of the earliest challenges was designing a database structure that could support future scalability.

Major tables included:

* users
* roles
* permissions
* role_permissions
* entities
* clients
* quotations
* elevations
* units
* drawers
* shelves
* accessories
* carcass_materials
* shutter_categories
* shutter_materials

The database was designed using relational principles while ensuring flexibility for future feature additions.

Key focus areas included:

* Proper foreign key relationships
* Data normalization
* Future scalability
* Multi-entity support
* Performance optimization

---

# Dynamic Unit Generation System

A major requirement was allowing users to create different furniture units dynamically.

Supported unit types:

* Tall Units
* Upper Units
* Bottom Units
* Loft Units

Each unit could have:

* Custom dimensions
* Material selection
* Drawers
* Shelves
* Cost calculations

The frontend dynamically generated units using JavaScript while maintaining synchronization with backend data structures.

This significantly reduced manual data entry.

---

# Automated Pricing Engine

One of the most complex components was the pricing engine.

The system automatically calculated:

### Unit Area

Using dimension-based square-foot calculations.

### Material Cost

Based on:

* Carcass Category
* Carcass Material
* Shutter Category
* Shutter Material

### Additional Costs

* Accessories
* Packing & Forwarding
* Transport
* Installation Charges

### Commercial Adjustments

* Discounts
* Final Customer Pricing

The result was a fully automated pricing workflow that eliminated manual calculations and reduced human errors.

---

# Drawer & Shelf Management

The project required support for multiple drawers and shelves per unit.

Features included:

* Dynamic drawer creation
* Dynamic shelf creation
* Unit assignment tracking
* Automatic cost calculation
* Unit-wise display

Instead of grouping all drawers and shelves together, the system was redesigned to display them beneath their respective units, improving readability and user experience.

---

# Multi-Entity Architecture

A major business requirement was supporting multiple brands under the same platform.

Entities implemented:

* F&R Kitchens and Wardrobes Pvt Ltd
* Craftred

Requirements included:

* Shared application
* Separate data visibility
* Entity-specific dashboards
* Entity-specific quotation management

The system was redesigned to support entity-based segregation while maintaining a single codebase.

---

# Role-Based Access Control (RBAC)

As the project grew, access control became essential.

Implemented tables:

* Roles
* Permissions
* Role Permissions

Supported user types:

* Super Admin
* Entity Admin
* Sales Team
* Other operational users

The RBAC system allowed:

* Permission-based page access
* Entity-level data restrictions
* Dashboard-level control
* Feature-level authorization

This created a secure and scalable user management structure.

---

# Dashboard Development

Multiple dashboards were created for different business entities.

Dashboard features included:

* Total Quotations
* Revenue Tracking
* User Performance
* Recent Quotations
* Monthly Statistics

The dashboards provided management-level visibility into quotation activity and business performance.

---

# PDF Generation System

One of the most requested features was automated quotation generation.

Using DomPDF, the system generated professional quotation documents containing:

* Client Information
* Project Details
* Elevations
* Unit Breakdown
* Material Information
* Pricing Summary
* Terms & Conditions

Several formatting challenges were solved including:

* Page breaks
* Font rendering
* Layout consistency
* Dynamic content handling

The result was a printable and shareable quotation document generated directly from system data.

---

# Performance Optimization Challenges

As data volume increased, performance issues started appearing.

Major challenges included:

### Excessive Queries

Quotation pages were executing too many database calls.

### N+1 Query Problems

Units, drawers, shelves, and accessories were being loaded inefficiently.

### Missing Indexes

Frequently filtered columns lacked indexing.

### Heavy Dashboard Queries

Reporting pages required optimization.

Solutions included:

* Query restructuring
* Database indexing
* Optimized joins
* Reduced database round trips
* Session-based permission caching

These improvements significantly improved application responsiveness.

---

# Key Technical Challenges Solved

During development, several real-world issues had to be addressed:

### Database Design Challenges

Creating relationships between deeply nested quotation structures.

### Dynamic Form Management

Handling multiple elevations and units generated on the fly.

### Pricing Consistency

Ensuring calculations remained accurate across different modules.

### Data Security

Implementing entity-level and role-level access restrictions.

### PDF Rendering Issues

Managing complex layouts and dynamic content inside generated documents.

### Scalability Planning

Designing the architecture to support future growth without requiring major redesigns.

---

# Business Impact

The completed system delivered significant operational improvements.

### Benefits Achieved

✅ Faster quotation creation

✅ Reduced manual calculations

✅ Improved pricing accuracy

✅ Centralized quotation management

✅ Multi-company support

✅ Automated PDF generation

✅ Secure role-based access

✅ Better reporting and visibility

✅ Scalable database architecture

✅ Improved user productivity

---

# Key Learnings

This project reinforced several important software engineering principles:

* Good database design is critical for long-term scalability.
* Business requirements often evolve during development.
* Role-based access control should be planned early.
* Query optimization becomes increasingly important as data grows.
* Real-world applications require balancing technical design with business usability.
* Building custom business software provides insights that go far beyond tutorials and academic projects.

---

# Conclusion

What began as a quotation generation tool ultimately evolved into a complete business management platform tailored for the interior and modular furniture industry.

The project provided hands-on experience in database architecture, backend development, frontend engineering, performance optimization, role-based access control, reporting systems, and document automation.

More importantly, it demonstrated how technology can transform manual business processes into scalable, efficient, and data-driven workflows.

This project remains one of the most valuable learning experiences in understanding how real-world software is designed, optimized, and delivered to solve business problems.
