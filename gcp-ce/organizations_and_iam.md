# Organizations and IAM

## Google Cloud Resource Hierarchy

- Organizations
- Folders
- Projects

### Organization

- An organization is the root of the resource hierarchy and typically corresponds to a company organization.
- Organization will have a quota of projects it can create.

### Folder

- Folders are the building blocks of multilayer organizational hierarchies. 
- Organizations contain folders. 
- Folders can contain other folders or projects. 
- Folders are optional and do not have to be used.

### Project

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

## There are three types of roles in Google Cloud

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

