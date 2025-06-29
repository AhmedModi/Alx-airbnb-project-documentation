# Booking Process Flowchart

## Overview
![Booking Flowchart](booking-flowchart.png)

## Key Steps
1. **Availability Check**:
   - Query database for selected dates
   - Cross-check with existing bookings

2. **Price Calculation**:
   - Base rate × nights
   - Add cleaning fee (15%)
   - Apply seasonal pricing

3. **Payment Processing**:
   - Stripe API integration
   - 3D Secure authentication
   - Error handling for declined cards

## Decision Points
| Step                  | Yes Path                 | No Path                |
|-----------------------|--------------------------|------------------------|
| Property Available?   | Proceed to booking       | Show similar listings  |
| Payment Successful?   | Confirm booking          | Display error          |

## Error Handling
- Credit card declines → Retry prompt
- Double booking attempts → Real-time inventory refresh
