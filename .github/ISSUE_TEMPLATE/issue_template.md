---
name: issue_template
about: a template for issue/bug tracking in github
title: issue_template
labels: termplate
assignees: rmv-admin-01

---

name: 🐞 Bug Report
description: File a bug report
title: "[Bug]: <title>"
labels: ["bug", "triage"]
assignees:
  - rmvhomes
body:
  - type: markdown
    attributes:
      value: |
        Thanks for taking the time to fill out this bug report!
  - type: input
    id: contact
    attributes:
      label: Contact Details
      description: How can we get in touch with you if we need more info?
      placeholder: ex. email@example.com
    validations:
      required: false
  - type: textarea
    id: description
    attributes:
      label: Description
      description:  |
        Also tell us, what did you expect to happen?
      placeholder: Tell us what you see!
      value: "A bug happened!"
    validations:
      required: true
  - type: dropdown
    id: version
    attributes:
      label: Version
      description: What version of our software are you running?
      options:
        - 1.0.2 (Default)
        - 1.0.3 (Edge)
    validations:
      required: true
  - type: dropdown
    id: browsers
    attributes:
      label: What browsers are you seeing the problem on?
      multiple: true
      options:
        - Firefox
        - Chrome
        - Safari
        - Microsoft Edge
  - type: textarea
    id: logs
    attributes:
      label: Relevant log output
      description: Please copy and paste any relevant log output. This will be automatically formatted into code, so no need for backticks.
      render: shell
  - type: checkboxes
    id: terms
    attributes:
      label: Code of Conduct
      description: By submitting this issue, you agree to follow our [Code of Conduct](https://example.com)
      options:
        - label: I agree to follow this project's Code of Conduct
          required: true
- type: dropdown
  id: priority
  attributes:
    label: Priority
    description: assign a priority for this bug/issue.
    multiple: false
    options:
      - Normal
      - Elevated
      - High
      - Show-Stopper!
  validations:
    required: true
- type: dropdown
  id: impact
  attributes:
    label: Impact
    description: Defines the effect of the risk on the project.
    multiple: false
    options:
      - Unknown
      - Low
      - Medium
      - High
  validations:
    required: true
- type: dropdown
  id: urgency
  attributes:
    label: Urgency
    description: Defines how critical the incident is, based on business needs.
    multiple: false
    options:
      - Unknown
      - Low
      - Medium
      - High
  validations:
    required: true
- type: input
  id: alternateid
  attributes:
    label: Alternate ID
    description: "Defines a reporter defined tracking number for this bug. Good for external id, set."
    placeholder: "No Placeholder"
  validations:
    required: false
- type: input
  id: next-step
  attributes:
    label: Next Step?
    description: "add the full name of the person that reported this bug."
    placeholder: "No Placeholder"
  validations:
    required: true
- type: input
  id: reporter
  attributes:
    label: Reporter
    description: "Input constructive answer to question here."
    placeholder: ""
  validations:
    required: true
blank_issues_enabled: false
contact_links:
  - name: GitHub Community Support
    url: https://github.community/
    about: Please ask and answer questions here.
  - name: GitHub Security Bug Bounty
    url: https://bounty.github.com/
    about: Please report security vulnerabilities here.
