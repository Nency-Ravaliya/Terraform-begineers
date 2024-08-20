# Terraform Commands and Workflow

## Command Reference

### Formatting

- **Command:** `terraform fmt`
- **Usage:** Format your Terraform configuration files to ensure consistent code style and readability.
- **When to Use:** Before starting any new work or after editing configuration files.

### Validation

- **Command:** `terraform validate`
- **Usage:** Check the syntax and validity of your Terraform configuration files.
- **When to Use:** After formatting and before applying changes, to ensure the configuration is correct.

### Initialization

- **Command:** `terraform init`
- **Usage:** Initialize the Terraform working directory, download provider plugins, and set up the backend.
- **When to Use:** When setting up a new Terraform project or after changing backend configurations.

### Refreshing

- **Command:** `terraform refresh`
- **Usage:** Update the state file with the latest information from the infrastructure.
- **When to Use:** Before planning or applying changes to ensure the state file reflects the current state of resources.

### Planning

- **Command:** `terraform plan`
- **Usage:** Preview the changes Terraform will make to the infrastructure based on the current configuration.
- **When to Use:** Before applying changes to review what will be altered, created, or destroyed.

### Applying

- **Command:** `terraform apply`
- **Usage:** Apply the changes required to reach the desired state of the configuration.
- **When to Use:** After reviewing the plan and when you are ready to make the changes to your infrastructure.

### State Management (as needed)

- **List Resources**
  - **Command:** `terraform state list`
  - **Usage:** List all resources managed by Terraform in the state file.

- **Show Resource Details**
  - **Command:** `terraform state show <resource>`
  - **Usage:** View detailed information about a specific resource.

- **Remove Resource from State**
  - **Command:** `terraform state rm <resource>`
  - **Usage:** Remove a resource from the state file without deleting the actual resource.

- **Move Resource in State**
  - **Command:** `terraform state mv <old_resource> <new_resource>`
  - **Usage:** Rename or move a resource in the state file.

### Destroying

- **Command:** `terraform destroy`
- **Usage:** Destroy all resources managed by Terraform, effectively cleaning up your environment.
- **When to Use:** When you need to remove all infrastructure managed by Terraform, such as during a teardown or cleanup process.

## Summary of the Workflow

1. **Format:** `terraform fmt`
2. **Validate:** `terraform validate`
3. **Initialize:** `terraform init`
4. **Refresh:** `terraform refresh`
5. **Plan:** `terraform plan`
6. **Apply:** `terraform apply`
7. **(Optional) State Management:**
   - `terraform state list`
   - `terraform state show <resource>`
   - `terraform state rm <resource>`
   - `terraform state mv <old_resource> <new_resource>`
8. **Destroy:** `terraform destroy`
