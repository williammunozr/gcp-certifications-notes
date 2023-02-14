# Organizations and IAM

## Google Cloud Resource Hierarchy

- Organization
- Folders
- Projects

### Organization

- An organization is the root of the resource hierarchy and typically corresponds to a company organization.
- Organization will have a quota of projects it can create.

### Folders

- Folders are the building blocks of multilayer organizational hierarchies. 
- Organizations contain folders. 
- Folders can contain other folders or projects. 
- Folders are optional and do not have to be used.

### Projects

- Projects are in some ways the most important part of the hierarchy. 
- It is in projects that we create resources.
- Anyone with the `resourcemanager.projects.create` IAM permission can create a project.

### Organization Policies

- Google Cloud provides an Organization Policy Service.
- This service controls access to an organization's resources.
- The Organization Policy Service complements the IAM service.
- IAM lets you assign permissions so that users or roles can perform specific operations in the cloud.
- The Organization Policy Service lets you specify limits on the ways resources can be used.
- IAM specifies `who` can do things, and the Organization Policy Service specifies `what` can be done with resources.

## Roles and Identities

- A `role` is a collection of permissions.
- Roles are granted to users by binding a user to a role.
- When we talk of `identities`, we mean the object we use to represent a human `user` or `service account` in Google Cloud.

### There are three types of roles in Google Cloud

- Basic Roles
- Predefined Roles
- Custom Roles

### Roles

- Formerly known as primitive roles.
- Include `Owner`, `Editor`, and `Viewer`.
- It is best practice to use predefined roles instead of basic roles when possible.
- Basic roles grant wide ranges of permissions that may not always be needed by a user.
- By using predefined roles, you can grant only the permissions a user needs to perform their function.
- This practice of only assigning permissions that are needed and no more is known as the `principle of least privilege`.
- Predefined roles provide granular access to resources in Google Cloud, and they are specific to Google Cloud products and managed and updated by Google.
- Custom roles allow cloud administrators to create and administer their own roles.
- You can use most permissions in a custom role, some, such as `iam.ServiceAccounts.getAccessToken`, are not available in custom roles.

### Granting Roles to Identities

- It is important that permissions cannot be assigned to users.
- Permissions can be assigned only to roles.
- Roles are assigned to users.

## Service Accounts

- A `service account` is a special kind of account used by an application or compute workload.
- A service account is identified by its email address, which is unique to the account.
- Service accounts do `not` have passwords, and cannot log in via browsers or cookies.
- You can let other users or service accounts impersonate a service account.
- Service accounts do `not` belong to your Google Workspace domain, unlike users accounts.
- Users can create up to 100 service accounts per project.

### Service Account Use Case

- You may have an application that neeeds to access a database but you do not want to allow users of the application to access the database directly.
- All user requests to the database should go through the application.
- You can create a service account that has access to the database.
- You can assign that service account to the application so that the application can execute queries on behald of users without having to grant database access to those users.

### Service Accounts as Resources or Identities

- Sometimes service accounts are treat them as resources and sometimes as identities. 
- When we assign a role to a service account, we are treating it as an identity.
- When we give users permissions to access a service account, we are treating it as a resource.

### Types of Service Accounts

- User-managed service accounts.
- Google-managed service accounts.


## Billing

- The Google Cloud Billing API provides a way for you to manage how to pay for resources used.

### Billing Accounts

- Billing accounts store information about how to pay charges for resources used.
- A billing account is associated with one or more projects.
- All projects must have a billing account unless they use only free services.
- Billing accounts can be matched to the way the company is paying their resources.

### Types of Billing Accounts

- Self-serve:
	- Self-serve accounts are paid by credit card or direct debit from a bank account.
	- The costs are charged automatically.
- Invoiced
	- Bills or invoices are sent to customers.
	- This type of account is commonly used by enterprises and other large customers.

### Roles Associated with Billing

- Billing Account Creator, which can create new self-service billing accounts.
- Billing Account Administrator, which manages billing accounts but cannot create them.
- Billing Account User, which enables a user to link projects to billing accounts.
- Billing Account Viewer, which enables a user to view billing account cost and transactions.

### Billing Budgets and Alerts

- Google Cloud Billing service includes an option for defining a budget and setting billing alerts.
- Budget is associated with a billing account, not a project.
- One or more projects can be linked to a billing account, so the budget and alerts you specify should be based on what you expect to spend for all projects linked to the billing account.
- You can specify a particular amount or specify that your budget is the amount spent in the previous month.

### Exporting Billing Data

- You can export billing data for later analysis or for compliance reasons.
- Billing data can be exported to BigQuery.
- You can set multiple alert percentages.
- By default, three percentages are set: 50 percent, 90 percent, and 100 percent.
- If you'd like more than three alerts, you can click `Add Item` in the `Set Budget Alerts` section to add additional alert thresholds.
- When that percentage of a budget has been spent, it will notify billing administrators and billing account users by email.
- To respond to alerts programmatically, you can have notifications sent to a `Pub/Sub` topic by checking the appropriate box in the `Manage Notification` sections.

