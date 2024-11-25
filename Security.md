# Security

## Policy Interpretation Deep Dive

![Security](images/Security.png)

**Steps in Interpreting Policies**

1. Identify the number of statements
2. Identify at a high level what each statement actually does or effect of each statement
3. Check the overlaps of each statement

* Effect Hierarchy: Explicit Deny > Explicit Allow > Implicit Deny

## Policy Evaluation Logic

### Components involved in evaluating policies

1. Organization Service Control Policies (SCP)
	- impact what identities inside Organization Member accounts can do.

1. Resource Policies
	- policies attached to resources which allows or denies specified principals.

1. IAM Identity Boundaries
2. Session Policies
3. Identity Policies

### Hierarchy of Evaluation for Same Account

![Security-1](images/Security-1.png)

1. Explicit Deny
2. Service Control Policies
3. Resource Policies
4. Permissions Boundaries
5. Session Policies
6. Identity Policies

* AWS first checks the whole list for Explicit Denies.

### Hierarchy of Evaluation for Different Accounts (Multi-Account or Cross Account Access)

![Security-2](images/Security-2.png)

* A successful access requires an applicable allow from both Account A and Account B.

