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

### Service Account Use Case

- You may have an application that neeeds to access a database but you do not want to allow users of the application to access the database directly.
- All user requests to the database should go through the application.
- You can create a service account that has access to the database.
- You can assign that service account to the application so that the application can execute queries on behald of users without having to grant database access to those users.

### Services Accounts as Resources or Identities

- Sometimes service accounts are treat them as resources and sometimes as identities. 
- When we assign a role to a service account, we are treating it as an identity.
- When we give users permissions to access a service account, we are treating it as a resource.
