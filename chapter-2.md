# Chapter 2 - Understanding Identity and Access Management 

Security Objectives - 1.2, 2.4, 2.5, 4.5, 4.6

### Exploring Authentication Management

Identification (users making a claim about their identity) vs Authentication (proving an identity)

#### Comparing Identification and AAA 

Authentication, Authorization, and Accounting (AAA)
- Authorization: What resources a proven identity can access 
- Accounting: Tracking activity and recording it in logs, creating an audit trail

#### Comparing Authentication Factors

Something you know: A shared secret (least secure form of authentication)
- Password expiration is not a best practice (assuming MFA)
- Password history remembers past passwords to prevent users from reusing them; usually used in conjuntion with a minimum password age setting
- Knowledge-Based Authentication (KBA)
    - Static KBA: Used to verify an identity when the password is forgotten
    - Dynamic KBA: Identifies individuals without an account
    - Identity proofing: Confirming a new user's identity
- Lockout policies
    - Account lockout threshold: Max number of times a user can enter the wrong password 
    - Account lockout duration: How long an account remains locked 

Something you have: Something you can physically hold
- Smart Card Authentication
    - Embedded Certificate: Holds a user's private key
    - Public Key Infrastructure (PKI): Supposrts issuing and managing certificates
    - Often used with 2FA combining something a user has and something they know (like a pin)
- Security Key: Contains cryptographic information that completes the authentication process
- Hard Token: Small electronic device that provides a OTP
- Soft Token: Application that provides a OTP
- How do tokens remain in sync with authentication servers?
    - HMAC-based One-Time Password (HOTP): Algorithm to change the code based on a moving counter
        - Token and authentication server have the same shared secret
        - User presses a button to generate next password
    - Time-based One-Time Password (TOTP): Algorithm that changes the code based on the current time
        - Code changes automatically in time intervals
- Short Message Service (SMS)
- Push Notifications

Something you are: Uses biometrics for authentication (strongest form of authentication)
- Biometric methods: fingerprints, vein matching, retina imaging, iris scanners, facial recognition, voice recognition, gait analysis
    - Strongest are iris and retina scans; facial and gait can bypass the enrollment process when used for identification
- Biometric Efficacy Rate: Performance of the system under ideal conditions
    - False acceptance, false rejection, true acceptance, true rejection
    - A lower Crossover Error Rate (CER) indicates a more accurate biometric system

Somewhere you are: Identifies a user's location using geolocation (IP is often used)
- Can be used to identify impossible travel time

Two-Factor & Multifactor Authentication: Uses two different authentication factors
- Using two methods of authentication in the same factor is **not** 2FA

Passwordless Authentication

#### Authentication Log Files

Authentication log files track both successful and unsuccessful login attempts

### Managing Accounts