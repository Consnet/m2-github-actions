
# GitHub Actions for Magento

## Usage 
To use the actions, a yaml file needs to be created in the `.github/workflows` directory and use the usage directions under the respective action.

## Categories
The actions included in here are meant for use with Magento projects. The following categories are included here. 

### Static Analyses

The static analysis actions are for performing PHP analyses that assist in eradicating all the issues that are raised. 

The following are all the analyses that are performed. For more details and usage details, check the README file in each action's folder

#### 1. Coding Standard 

The coding standard check uses PHPCS.

#### 2. Mess Detection 

This test checks for code smells and errors using PHPMD.

#### 3. Copy/Paste Detection 

This action tests for code duplication using PHPCPD. 

#### 4. Bug Checks 

This action tests for bugs and errors in static code using PHPStan.
