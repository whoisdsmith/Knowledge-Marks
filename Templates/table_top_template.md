tags: #templates 

1. Think of a scenario specific to the org (ask employees if a scenario is relevant)
2. Invite IR & SOC teams, and other affected teams
3. Look at older findings as a table top scenario

"It's okay to not know the answer"

### Scenario 1 (example)

> A disgruntled employee writes a quick script to brute force all LDAP accounts. Now all accounts, including service accounts and super users are locked out. This affects production systems and the code that relies on those service accounts to run. The platform is now offline. What happens next?

#### "Interject" (providing more context information to the scenario)

> This scenario is taking place at 2PM on a Wednesday.

#### Expected Reaction

- Alerts
- Flood of employee complaints to helpdesk

### Scenario 2 (example)

> All of a sudden, your phishing alias goes bonkers, the pager is pinging like crazy. Hundreds of employees are forwarding the same email to the IR team. We do initial analysis and determine the email contains a malicious payload. What would we do next?

#### "Interject"

> More employees continue to forward the same email to the IR team, and now IR employee's cannot access their inboxes. What happens next?

#### Expected Reaction

What happens to the people who haven't clicked on it?
What happens to the people who HAVE clicked on it?

#### Considerations

1. Retract e-mails
2. Reset accounts
3. Enroll in MFA
