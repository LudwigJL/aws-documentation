##AWS Lambda x Terraform: Apply issue - Result from Link:
### `{"message":"Missing Authentication Token"}`

### Steps:

1. **Wipe All Files Associated with Terraform**

   - Remove the data file (e.g., `backend.zip`):
     ```bash
     $ rm -rf backend.zip
     ```

   - Remove all Terraform-related files:
     ```bash
     $ rm -rf terraform.tfstate .terraform terraform.tfstate.backup .terraform.lock.hcl
     ```
     
   - Check if any terraform files remains, if there are, rm them.
      ```bash
     $ ls
     ```

   - Clean the Gradle build:
     ```bash
     $ ./gradlew clean build
     ```

1. **Rebuild Everything from Scratch**  
   Ensure that the `main.tf` file is 100% correct before running `terraform init` and `terraform apply`.

2. **Fix All Collisions with AWS IAM Users and Lambda Functions**

3. **Run the Generated Link Again and Check the Results**
