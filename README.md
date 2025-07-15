# Tempo × myAbode User Onboarding Flow

## Overview
This document describes the user journey for myAbode users becoming Tempo customers through a partner organization&apos;s magic link system. The flow enables seamless transition from partner platforms to Tempo with automatic account creation, authentication, and partner benefits.

## User Flow Stages

### Stage 1: Starting Point (myAbode)
- Authenticated user is on myAbode hosted landing page
- Landing page displays myAbode branding with a prominent &quot;Get Started with Tempo&quot; call-to-action button

### Stage 2: API Request
- User clicks the CTA button, triggering a secure API call to Tempo
- System makes a POST request to Tempo partner API endpoint
- Request includes user&apos;s email, name, and partner secret
- Tempo API generates and returns a secure magic link URL (valid for 1 hour)

### Stage 3: Redirect
- User&apos;s browser is automatically redirected to the generated magic link
- URL changes from myAbode domain to Tempo domain
- Brief loading state as the redirect processes

### Stage 4: Account Creation & Auto-Login
- Tempo system automatically creates a new user account based on the verified magic link
- User is logged in without requiring password entry (session token cookie set. subsequent logins will require using Tempo magic link sign in at https://app.ontempo.io/login)
- Account is linked to the partner organization

### Stage 5: Site Creation
- User arrives at the Tempo dashboard on site creation form
- User can begin creating a new website using the &quot;Create New Site&quot; functionality
- Site begins in draft mode for development and customization
- Site cannot be published unless a subscription is purchased

### Stage 6: Publishing & Pricing
- User navigates to the plans and pricing page 
- Pricing table shows original prices with partner discount clearly highlighted
- Partner discount is automatically applied due to the partner organization connection
- Discount is prominently displayed with clear savings calculation
- User can proceed to checkout with discounted pricing already applied in checkout session

## Security Features

Throughout the entire flow, security is maintained through:
- **Encrypted Communication**: All data transfers use HTTPS and encrypted connections
- **Token Validation**: Magic links contain digitally signed tokens that are validated at each step
- **Time-Limited Access**: Magic links expire after 1 hour to prevent unauthorized access
- **Partner Verification**: Partner organization secrets are validated before account creation

## Key Benefits

This user flow provides several advantages:
1. **Seamless Transition**: Users move from myAbode to Tempo without friction
2. **Automatic Authentication**: No manual account creation or password setup required
3. **Instant Partner Benefits**: Discounts and partner perks are automatically applied
4. **Security**: Multi-layered security ensures safe data transfer and account creation
5. **User Experience**: Streamlined process reduces abandonment and increases conversion
