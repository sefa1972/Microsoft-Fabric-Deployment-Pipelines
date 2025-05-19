# Microsoft Fabric Deployment Pipelines 

This lab demonstrates how to implement deployment pipelines in Microsoft Fabric to automate content deployment across development, test, and production environments.

## Lab Objectives

- Create multiple workspaces for different deployment stages
- Set up a deployment pipeline
- Deploy content (Lakehouse) between stages
- Validate successful deployments

## Prerequisites

- Microsoft Fabric account with admin privileges
- Fabric capacity (Trial, Premium, or Fabric license)
- Basic understanding of Microsoft Fabric concepts

## Lab Steps

### 1. Create Workspaces

1. Navigate to https://app.fabric.microsoft.com
2. Create three workspaces:
   - Development
   - Test
   - Production
3. Verify all three workspaces appear in your workspace list

### 2 Create Deployment Pipeline

1. Go to Workspaces > Deployment Pipelines
2. Select "New pipeline"
3. Name your pipeline (e.g., "LabPipeline")
4. Select "Create and continue"

### 3. Assign Workspaces to Pipeline Stages

1. Open your newly created pipeline
2. For each stage (Development, Test, Production):
   - Select "Assign a workspace"
   - Choose the corresponding workspace
   - Confirm assignment with checkmark

### 4. Create Content in Development

1. Open the Development workspace
2. Create new Lakehouse named "LabLakehouse"
3. Select "Start with sample data" > "NYCTaxi" to populate

### 5. Deploy Between Stages

1. In your pipeline:
   - Deploy from Development to Test
   - Then deploy from Test to Production
2. Verify green check marks appear between all stages

### 6. Validate Deployment

1. Check Test and Production workspaces
2. Confirm "LabLakehouse" appears in both
3. Verify sample data is present

### Cleanup

1. For each workspace:
   - Go to Workspace settings
   - Select "Remove this workspace"
2. Delete your deployment pipeline
   
