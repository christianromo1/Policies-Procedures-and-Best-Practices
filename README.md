# Cybersecurity Policies, Procedures & Best Practices

**Identity Management Policy: Password Reset Procedure** — a technical research project developed for a network security course (COMP 348), covering policy scope, standards research, a step-by-step procedure, and validation for a hybrid Active Directory password reset process.

## What I Did

I completed a technical research project that involved the preparation of a security policy, adoption of a best practice, and the development of a procedure. I created and documented a single technical operation for the following policy area: Comprehensive identity management - Password resets (self-service and service desk assisted).

## How I Did It

I researched and reviewed real examples of cybersecurity policies, procedures, and best practices. I found and based my documentation on NIST SP 800-63B and Microsoft Entra ID.

## Key Learning

I got hands-on experience in researching and understanding security policies, developing a scope for my procedure, reviewing and selecting an official standard/guideline/best-practice, implementing the procedure, and ensuring a proper way to validate it.

## Relevance

Password reset flows are one of the most commonly abused paths into an account, mainly because organizations have to balance making them usable enough that legitimate users don't get locked out, while ensuring they're resistant enough that an attacker can't just talk their way past verification.

#Project
## Issue

Lack of a comprehensive identity management - password reset (self-service and service desk assisted) feature for corporate Active Directory (AD) accounts. From what I researched, this is an important security concern, and attackers can easily abuse a password reset feature if it does not comply with the procedure below.

## Scope

The scope of the procedures includes corporate employee and contractor accounts in an enterprise AD environment. It includes hybrid identity systems that use a self-service password reset (SSPR) portal with a password writeback to an on-site AD. The scope does not include other types of accounts, including privileged or administrator accounts, as these require more secure practices. Procedure protection includes passwords, MFA methods, recovery information, reset tickets, and audit logs.

## Published Standard

I based my documentation on NIST SP 800-63B and Microsoft Entra ID, which gives lots of guidance on password handling, account recovery, and rate limiting. The main takeaway is that security questions are weaker in comparison to MFA, recovery codes, or controlled identity proofing.

## Procedure

1. Confirm the account is in scope and not a privileged or service account.
2. If self-service is available, direct the user to the approved SSPR portal first.
3. Require the user to verify identity via two different methods, such as an authenticator app and a phone or email.
4. No security questions as reset methods.
5. After identity is verified, allow the user to create a new password that follows the company password policy.
6. If self-service is not possible, the service desk must open a ticket before proceeding.
7. The service desk must verify the user's identity by using stronger methods, such as an MFA challenge to a registered device, a callback to a known phone number, or formal re-verification if the user lost access to their factors.
8. If verification fails or the request looks suspicious, the reset must be denied and escalated.
9. After a successful reset, the system should send a notification to the user and log the event in both AD and cloud audit logs.

## Validation

1. Logs and tickets must be reviewed and reset each month. The organization must confirm that password reset events are being recorded, and that service desk tickets document the verification method used.
2. Organization must test the process quarterly by attempting failed verifications, confirming lockout behavior, and checking that excluded accounts are denied or escalated properly.

## Source Documents

- [Original Submission (348-ROMO.pdf)](docs/348-ROMO-original-submission.pdf) — the complete project exactly as submitted, including full references.
- [Assignment Specifications (proj2-348.pdf)](docs/proj2-348-assignment-specifications.pdf) — the original project brief and grading rubric.

---

Written by [Christian Romo](https://github.com/christianromo1) — aspiring Cybersecurity Analyst. More projects at [github.com/christianromo1](https://github.com/christianromo1/christianromo1).
