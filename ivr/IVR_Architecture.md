# IVR System Architecture

## Components

- User Device (Mobile App)
- Twilio Voice API
- IVR Logic (TwiML)
- Backend Server (Conceptual)
- Payment System (UPI/Wallet - Simulated)

## Flow

1. User initiates "Pay via Call"
2. App triggers IVR call via Twilio
3. Twilio executes TwiML script
4. User input captured via keypad
5. Backend processes request (conceptual)
6. Confirmation response delivered

## Key Insight

The system ensures **payment confirmation even without internet** using GSM voice network.
