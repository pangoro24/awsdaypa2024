# awsdaypa2024
Remediación de recursos en incumplimiento usando Aws Config y Systems Manager Automation

# Config rule
Description:
  Checks whether AWS S3 public access account settings match the assigned parameters.
Trigger:
  Configuration changes
Resource Type to report on:
  S3 AccountPublicAccessBlock
Feature:
  In order to: ensure that s3 account settings are being restricted to the appropriate level
           As: a Cloud Security Engineer
       I want: to verify that the configuration of s3 account public access settings is correct.
Scenarios:
  Scenario 1:
    Given: Given: All input parameters are valid
      And: At least 1 S3 config parameter does not match the corresponding value for the account
     then: Return NON_COMPLIANT
  Scenario 2:
    Given: Given: All input parameters are valid
      And: All S3 config parameters match the corresponding value for the account
     then: Return COMPLIANT
