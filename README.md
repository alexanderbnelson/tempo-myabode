# Tempo × myAbode User Onboarding Flow

## Overview
This document describes the user journey for myAbode users becoming Tempo customers through a partner organization&apos;s magic link system. The flow enables seamless transition from partner platforms to Tempo with automatic account creation, authentication, and partner benefits.

## User Flow Stages

### Stage 1: Starting Point (myAbode)
- **Location**: myAbode hosted landing page
- **User State**: Authenticated myAbode user
- **Interface**: Landing page displays myAbode branding with a prominent &quot;Get Started with Tempo&quot; call-to-action button
- **Security**: User is already authenticated within the myAbode system

### Stage 2: API Request
- **Action**: User clicks the CTA button, triggering a secure API call to Tempo
- **Process**: System makes a POST request to Tempo partner API endpoint
- **Data Transfer**: Request includes user&apos;s email, name, organization ID, and encrypted partner secret
- **Response**: Tempo API generates and returns a secure magic link URL (valid for 1 hour)

### Stage 3: Redirect
- **Action**: User&apos;s browser is automatically redirected to the generated magic link
- **Transition**: URL changes from myAbode domain to Tempo domain
- **User Experience**: Brief loading state as the redirect processes

### Stage 4: Account Creation & Auto-Login
- **Process**: Tempo system automatically creates a new user account based on the verified magic link
- **Authentication**: User is logged in without requiring password entry
- **Verification**: Email address is automatically verified through the partner authentication
- **Partner Benefits**: 
  - Account is linked to the partner organization
  - Partner discount is automatically applied
  - User profile displays partner affiliation
- **User Experience**: Seamless login without manual account creation steps

### Stage 5: Site Creation
- **Location**: User arrives at the Tempo dashboard
- **Interface**: Dashboard displays Tempo branding and site management options
- **Action**: User can begin creating a new website using the &quot;Create New Site&quot; functionality
- **Tools**: Access to site builder interface and website creation tools
- **Status**: Site begins in draft mode for development and customization

### Stage 6: Publishing & Pricing
- **Location**: User navigates to the plans and pricing page
- **Pricing Display**: Pricing table shows original prices with partner discount clearly highlighted
- **Discount Application**: Partner discount is automatically applied due to the partner organization connection
- **User Experience**: Discount is prominently displayed with clear savings calculation
- **Next Steps**: User can proceed to checkout with discounted pricing already applied

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
