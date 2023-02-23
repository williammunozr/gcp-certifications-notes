# Compute Service Options

## Options

- Complete control and flexibility.
- Flexible container technology.
- Managed application platform.
- Serverless environments.

## Compute Engine

- Virtual machines (VMs) called `instances`.
- Instances run images, which contain operating systems, libraries, and other code.
- Choose `region` and `zone` to deploy.
- You decide the `operating system` and the `software` you decide to put on it.
- Use `public` or `private images` to create instances.
- You can create a custom image from a boot disk or by starting with another image.
- Pre-configured images and software packages available in `Google Cloud Marketplace`.
- Manage multiple instances using `instance groups`.
- Add/remove capacity using `autoscaling with instance groups`.
- Attach/detach `disks` as needed.
- Can be used with `Google Cloud Storage`.
- Use `SSH` to connect directly.
- All data in Google Cloud is encrypted when stored (known as `encryption at rest`) in persistent storage.
- We do not have the option to persistently store data without encryption.
- Disk can be attached as read/write disks or as read-only disk.
- A disk by default is kept when an instance is deleted, but you can choose to have the disk deleted when the instance is deleted.

### Public Images

- CentOS.
- Container-Optimized OS from Google.
- Debian.
- Red Hat Enterprise Linux.
- SUSE Enterprise Linux Server.
- Ubuntu.
- Windows Server.

### How Encryption Keys are Managed

- With `Google-managed` encryption keys, Google creates and manages keys.
- With `customer-managed` encryption keys, customers create their own keys but Google manages them.
- When we use `customer-supplied` encryption keys, the customers create and managed keys outside of Google cloud.

### Virtual Trusted Platform Module (vTPM)

- Validates boot integrity and provides additional protections for key generation and protection.
- When vTPM is enabled, you have the option of enabling `Integrity Monitoring`, which verifies the runtime integrity of the virtual machine.

## Google Kubernetes Engine (GKE)

- `Container-orchestration` system for automating, deploying, scaling, and `managing containers`.
- Built on `open-source Kubernetes`.
- Flexibility to `integrate` with on-premise Kubernetes.
- Uses `Compute Engine` instances as `nodes` in a cluster.
- A `cluster` is a `group of nodes` or `Compute Engine Instances`.
- Considered `CaaS`.

## App Engine

- `Fully managed`, `serverless platform` for developing and hosting web applications at scale (`PaaS`).
- Provisions servers and `scales your app` instances based `on demand`.
- Build your app in `Go`, `Java`, `.NET`, `Node.js`, `PHP`, `Python`, or `Ruby`.
- `Connect` with other Google services `seamlessly`.
- `Integrates` with `Web Security Scanner` to identify threats.

## Cloud Funtions

- `Serverless execution environment` for building and connecting cloud services.
- Simple, `single-purpose functions` that are attached to events.
- Triggered when an event being watched is fired.
- Your code executes in a fully managed environment.
- No need to provision any infrastructure.
- `Cloud Functions` can be written using `JavaScript`, `Python`, `Go`, or `Java` runtimes.
- Use cases:
    - Data processing or ETL operations (video transcoding).
    - Webhooks to respond to HTTP triggers.
    - APIs that compose loosely coupled logic.
    - Mobile backend functions.
- `FaaS`.

## Cloud Run

- `Fully managed compute platform for` deploying and scaling `containerized applications` quickly and securely.
- Built upon an open standard `Knative`.
- `Abstracts` away all `infrastructure` management.
- Known as `serverless for containers`.
- `Flexibility`. Any language, any library, any binary.
- Considered `FaaS`.
