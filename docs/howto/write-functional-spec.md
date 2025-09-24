# How to Write a Functional Specification

This guide walks you through the steps to create a clear and useful functional specification for a software feature. Functional specs help align developers, designers, and stakeholders by describing exactly how a feature should work.

## Prerequisites

- A defined feature or problem to solve
- Access to product or technical documentation (if any)
- Collaboration with developers and/or designers

## Steps

1. **Define the Objective**

    Start by writing a short description of what the feature is and what problem it solves.

    ```text
    Example:
    Allow users to reset their password via email if they forget their login credentials.
    ```

2. **Describe the User Story**

    Include the primary user story and any relevant secondary stories using the standard format:

    ```text
    As a [type of user], I want to [perform some action] so that [achieve some goal].
    ```

    ```text
    Example:
    As a registered user, I want to reset my password via email so that I can regain access to my account without contacting support.
    ```

3. **List Requirements**

    Break down the feature into functional requirements. These are specific, testable statements of what the system must do.

    ```text
    - The login page must include a "Forgot Password?" link.
    - The link opens a form requesting the user’s email.
    - The system sends a reset email with a unique link.
    - The link is valid for 30 minutes and can only be used once.
    ```

4. **Specify Edge Cases and Constraints**

    Think through and document edge cases or limitations.

    ```text
    - If the email is not associated with an account, show a generic success message.
    - If the token is expired, display a message and allow the user to request a new one.
    ```

5. **Add Wireframes or UI References**

    If available, include wireframes, UI mocks, or even links to design systems.

    ```text
    [Include screenshot or design link here]
    ```

6. **Define Acceptance Criteria**

    Clearly state how the team will know the feature is complete and working as intended.

    ```text
    - Clicking “Forgot Password?” opens the reset form.
    - Submitting a valid email sends a reset link.
    - The reset link brings the user to a new password form.
    - The system rejects expired or reused links.
    ```

7. **Review with Stakeholders**

    Share the draft with developers, designers, and product stakeholders for feedback before development starts.

---

## Tips

- Use plain language. Avoid ambiguity.
- Be concise, but cover edge cases.
- Include only what’s necessary for implementation and testing.
- Avoid mixing design or implementation decisions unless required.

---

## Next Steps

Once approved, save the specification in your team’s documentation system (e.g. Git repo, Notion, Confluence) and link to it from the relevant Jira or task-tracking item.
