# IVR Fallback System

## Overview
This module implements an **IVR-based fallback payment system** that allows users to confirm transactions via a phone call when internet is unavailable.
It is built using **Twilio Voice API** and **TwiML**, simulating a real-time voice-driven payment confirmation flow.

## How It Works
1. User selects **“Pay via Call”**
2. IVR call is triggered
3. System announces payment details
4. User is prompted to:
   * Press **1** → Confirm
   * Press **2** → Cancel
5. Based on input (conceptually), system processes the request
6. IVR provides final confirmation

## IVR Flow
```text id="flow2"
User
  ↓
Tap "Pay via Call"
  ↓
IVR Call Triggered
  ↓
Announce Payment Details
  ↓
User Input (1 / 2)
  ↓
(Backend Processing - Conceptual)
  ↓
Voice Confirmation
```

## IVR Logic
* **<Say>** → Voice instructions
* **<Gather>** → Captures user keypad input
* **Timeout Handling** → Handles no input case
* **Post-Gather Flow** → Simulated confirmation
> Note: Backend processing is conceptual in this prototype. In production, input would be handled via an API endpoint.

## IVR Script (Updated)
```xml id="ivrfinal"
<Response>
  <Say voice="alice">Welcome to Smart Pay offline payment system.</Say>
  <Say>You are about to pay 500 rupees to Merchant ABC.</Say>

  <Gather numDigits="1" timeout="5">
    <Say>Press 1 to confirm payment.</Say>
    <Say>Press 2 to cancel transaction.</Say>
  </Gather>

  <Say>Processing your request.</Say>
  <Say>Your payment has been successfully completed.</Say>
  <Say>Thank you for using Smart Pay.</Say>

</Response>
```

## Key Features

* Works without internet (GSM-based interaction)
* Real-time user input via keypad
* Simple and scalable fallback mechanism
* Designed for low-connectivity environments

## 📌 Notes

* This is a **prototype implementation**
* Payment confirmation is simulated
* Input handling is demonstrated conceptually
* Designed to showcase fallback reliability

---
