# Box Bar Events Website Guide

## Project Overview

**Original website reference:** https://www.boxbarevents.com

We want to create a new website for our business **"Box Bar Events"** - a mobile trailer bar that can be hired out for big events and weddings. The goal is to add interactive features that make it easier for customers to learn about our business and services.

### Key Objectives

- Create **two dedicated sections**: **Weddings** and **Corporate Events** with tailored experiences
- Enable **quick quote generation** for customers
- Maintain a **classy and elegant** feel that's **simple to use**
- Keep **consistent design language** across both sections while adapting messaging

---

## Site Structure: Two Dedicated Sections

### Wedding Section

**Target Audience:** Couples planning their special day

**Design Approach:**

- Emphasize **romantic elements** from our style guide (Blush Pink accents, script fonts for quotes)
- Hero imagery featuring elegant wedding setups
- Soft, romantic language: _"Celebrate your perfect day"_, _"Raise a glass to forever"_

**Content Focus:**

- Wedding package options (_"Classic Wedding Bar"_, _"Premium Romance Package"_)
- Signature cocktail menus and welcome drink options
- Testimonials from happy couples
- Wedding-specific add-ons (custom napkins, late-night treats, sparkler sendoff drinks)

### Corporate Events Section

**Target Audience:** Event planners, HR managers, business owners

**Design Approach:**

- Emphasize **professional elements** from our style guide (Deep Charcoal, Sage Green accents)
- Hero imagery featuring corporate events and networking
- Professional, confident language: _"Impress your clients"_, _"Professional bar service"_

**Content Focus:**

- Corporate package options (_"Professional Networking Bar"_, _"Executive Event Package"_)
- Efficient service and dietary accommodation options
- Testimonials from corporate clients and event planners
- Business-specific add-ons (branded glassware, coffee service, breakfast bar options)

### Shared Design Elements

Both sections will maintain **visual consistency** using:

- Same **color palette** (Champagne Gold, Light Dove Grey, Warm White as base)
- Same **typography hierarchy** (Playfair Display headings, Lato body text)
- Same **layout structure** and navigation
- Same **booking flow** and quote tool functionality
- Same **mobile-first responsive design**

### Navigation Strategy

- **Main homepage** introduces both services with clear section entry points
- **Dedicated landing pages** for each section with tailored messaging
- **Shared booking tool** that adapts packages based on event type selection
- **Cross-promotion** where appropriate (corporate clients planning office holiday parties might want wedding-style service)

---

## New Feature Ideas

### 1. Interactive Event Booking & Quote Tool

#### Date & Location Availability Checker

Customers can instantly check if you're available for their wedding/event date.

#### Build-Your-Own-Bar Package

A step-by-step form where users select:

- Number of guests
- Drink preferences (cocktails, beer, wine, mocktails)
- Additional services (glassware, custom menu, extra bartenders)

This gives them a **live estimated quote** and lets them request a booking.

#### Package Data Structure

**Wedding Packages:** Referenced from `booking-packages.json` containing Bronze, Silver, and Gold tiers with drink libraries and add-ons
**Corporate Packages:** Will be stored in `corporate-packages.json` with business-focused tiers and professional service options

---

## Step-by-Step User Flow

### Step 1 – Event Basics

**Form fields:**

- **Event date** (calendar picker with blocked-out unavailable dates)
- **Location** (postcode + venue name)
- **Event type** (Wedding, Corporate, Birthday, Festival, Other) _- This selection determines which packages are shown_
- **Number of guests** (dropdown or slider)

**Availability check:** After they choose a date & location, the tool pings your availability API (or Google Calendar integration) and gives instant feedback:

> ✅ _"We're available for your date!"_
>
> ❌ _"Sorry, that date is already booked — here are our next available weekends."_

### Step 2 – Choose Your Package _(Adapts based on Event Type)_

**For Weddings:**
Show wedding-focused packages from `booking-packages.json`:

- _"Bronze"_ (£2,500 minimum spend)
- _"Silver"_ (£3,250 minimum spend)
- _"Gold"_ (£4,250 minimum spend)

**For Corporate Events:**
Show business-focused packages from `corporate-packages.json`:

- _"Essential Business Bar"_
- _"Professional Networking Package"_
- _"Executive Event Experience"_

**Each card has:**

- Price per guest or base hire price
- A "What's included" list tailored to event type
- Option to customise (see Step 3)

### Step 3 – Customisation _(Event-Type Specific Add-ons)_

**Wedding Add-ons:**

- Extra bartender
- Signature wedding cocktails
- Welcome drinks for ceremony
- Elegant glassware rental
- Custom bar branding with couple's names
- Late-night snack pairings
- Champagne toast service

**Corporate Add-ons:**

- Professional bartender staff
- Coffee and tea service
- Branded glassware with company logo
- Dietary accommodation options
- Extended service hours
- Premium liquor upgrades
- Networking mixer packages

Each selection instantly updates the running total in a **sticky sidebar**.

### Step 4 – Summary & Enquiry

**Show a beautifully formatted summary:**

- Date & time
- Location
- Selected package
- Add-ons chosen
- **Estimated total price**

**Below that:**

- A short contact form for their name, email, and phone number
- **CTA:** _"Request to Book"_ or _"Save This Quote"_ (email it to them and to you)

### 2. Dedicated Landing Pages

#### Wedding Landing Page

A romantic **"Weddings"** section with:

- Elegant wedding photography showcasing your bar setup
- Testimonials from happy couples with their wedding photos
- Sample signature cocktail menus for weddings
- Wedding-specific package highlights
- _"Book for Your Perfect Day"_ CTA buttons
- Soft, romantic design elements (blush pink accents, script fonts for special quotes)

#### Corporate Events Landing Page

A professional **"Corporate Events"** section with:

- Clean, sophisticated imagery of business events and networking
- Testimonials from event planners and corporate clients
- Professional service highlights and efficiency focus
- Corporate package options and team-building elements
- _"Book Professional Bar Service"_ CTA buttons
- Professional design elements (sage green accents, clean typography)

**Shared Design Foundation:**
Both pages maintain the same overall layout structure, color palette base, and navigation while adapting messaging and accent colors to their target audience.

### 3. Interactive Gallery & Video Tours

- **Before & After Event Transformations** (drag slider to see the setup before guests arrive vs. in full swing)
- **360° Virtual Bar Tour** so customers can explore the inside of the trailer bar online
- **Short event highlight videos** showing your bar in action at weddings, festivals, and corporate events

### 4. Drink Menu Visualizer _(Section-Specific Menus)_

#### Wedding Menu Focus

An **interactive cocktail/mocktail menu** featuring:

- Romantic signature cocktails (_"Love Potion Martini"_, _"Blushing Bride"_)
- Seasonal wedding-themed drinks
- Welcome cocktail options for ceremonies
- Late-night coffee cocktails for reception

#### Corporate Menu Focus

An **interactive menu** featuring:

- Professional networking-appropriate cocktails
- Coffee and tea service options
- Light breakfast and lunch pairings
- Non-alcoholic sophisticated options for daytime events

**For both sections, customers can click to see:**

- Ingredients and allergen information
- Presentation style and glassware
- Serving suggestions and pairing options

### 5. Custom Quote & Instant Chat Support

- Add a **chatbot or live chat** for quick event queries
- Pre-programmed to answer FAQs like pricing, bar sizes, and booking steps

### 6. Social Proof & FOMO Triggers _(Tailored by Section)_

#### Wedding Section

- **Real-time booking ticker** (_"5 couples booked their dream wedding bar this week"_)
- **Instagram feed integration** showcasing recent weddings and romantic setups
- **Couple testimonials** displayed in elegant carousel with wedding photos
- **Pinterest-style inspiration board** with cocktail and setup ideas

#### Corporate Section

- **Professional booking updates** (_"12 corporate events successfully served this month"_)
- **LinkedIn integration** showcasing professional events and client partnerships
- **Corporate client testimonials** with professional event photos
- **Case studies** of successful corporate events and networking functions

**Shared Elements:**
Both sections use the same carousel and testimonial layout structure, maintaining visual consistency while adapting content.

### 7. Seamless Contact & Follow-up

- After someone enquires, send them a **beautiful PDF brochure** automatically with package details and event inspiration
- Let them **schedule a call or Zoom** directly from the site to discuss their event

### 8. Mobile-First, Scroll-Friendly Design

Many couples will browse on their phone while planning, so make sure:

- **Buttons are large and tap-friendly**
- **Forms are simple and short**
- **Photos are optimised for quick loading**

---

## Additional Core Features for Launch

### 9. Smart Recommendations & Upselling

- **Weather-based suggestions:** Hot cocktails for winter events, refreshing options for summer
- **Event-type recommendations:** Corporate events get different suggestions than weddings
- **"Popular with similar events" section** to increase average order value

### 10. Enhanced Quote Management

- **Save & Share quotes:** Customers can email quotes to partners/planners
- **Quote expiration dates** to create urgency
- **Price comparison tool** between different package options
- **Payment plan options:** Deposit + installments clearly displayed

### 11. Essential Business Features

- **Dynamic pricing indicators:** Show peak season pricing and early bird discounts
- **Venue compatibility checker:** Basic requirements (power, space, access)
- **Dietary requirements section:** Prominent non-alcoholic options and allergen info
- **Basic inventory tracking:** Real-time equipment availability

### 12. Customer Communication

- **Automated email sequences:** Booking confirmations, pre-event reminders, follow-ups
- **SMS notifications:** Day-before reminders and important updates
- **Customer portal:** View booking details, make final adjustments, upload venue info

---

## Future Improvements & Advanced Features

_These features can be implemented in Phase 2+ after the core application is established:_

### Progressive Web App (PWA) Features

- Offline browsing capabilities
- Push notifications for booking updates
- "Add to Home Screen" functionality

### Advanced Analytics & Optimization

- Customer behavior tracking and conversion optimization
- A/B testing for pricing and packages
- Seasonal demand pattern analysis

### Partnership & Integration Features

- Wedding planning app integrations
- Venue partnership directory
- Photographer/catering company referral system
- Wedding planner collaboration tools

### Enhanced Customer Experience

- Multi-event booking management (engagement + wedding)
- Interactive planning timeline with milestones
- Digital guestbook and photo sharing post-event
- Referral rewards program

### Advanced Business Operations

- Staff scheduling and skill-based recommendations
- Automated supply ordering based on bookings
- Delivery route optimization
- Integration with accounting software

### Marketing & Content Features

- Blog section with cocktail recipes and event tips
- Seasonal cocktail trend recommendations
- Content marketing hub for customer retention
- Anniversary and birthday follow-up campaigns

### Accessibility & Inclusivity

- Multiple language support
- Screen reader compatibility and high contrast modes
- Cultural/religious event considerations

### Emergency & Contingency Planning

- Weather contingency planning tools
- Last-minute guest count adjustments
- Backup equipment availability tracking
- Comprehensive cancellation/rescheduling system
