## ExpenseManager
The ExpenseManager is an expense management system built to streamline employee expense claims. This application provides a structured workflow for submitting and approving expenses with role-based permissions, ensuring that only employees can submit claims and managers can review and approve or reject them.

## Table of Contents
Overview

Features

Setup

Usage

Permissions

Workflow

# Overview
The ExpenseManager application enables employees to submit expense claims, which are then reviewed and approved or rejected by managers. The app includes:
  Role-based Access Control: Only employees can submit expense claims, and only managers can approve/reject claims.
  Expense Approval Workflow: A clear and structured workflow for submitting, reviewing, and finalizing expense claims.
  Expense Types: Customizable expense types such as travel, meals, lodging, etc.
# Features
  Employee Expense Claims: Employees can submit expenses for approval.
  Manager Review and Approval: Managers review submitted claims and either approve or reject them.
  Expense Types: Track multiple types of expenses (e.g., travel, meals, lodging).
  Role-based Permissions: Access to features is controlled by user roles.

# Setup
  Clone the Repository:
  git clone https://github.com/MadhuNishad23/expense-manager
  cd expense-manager
  Install Dependencies: Follow your development framework’s guidelines for installing dependencies.

  Setup Database: Initialize the required database tables by running migrations:
  bench migrate
  
  Assign Roles: Assign the "Employee" role to employees and the "Manager" role to users who will review and approve claims.
  Start the Server:
  bench start

# Usage
  Submitting an Expense Claim:
  Go to the "Expense Claim" form.
  Fill out the required fields:
  Employee: Your name (linked to Employee DocType).
  Expense Type: Select from available options (e.g., Travel, Meals).
  Date: The date of the expense.
  Amount: The total amount of the expense.
  Submit the claim (Status will change to "Submitted").
  Reviewing a Claim (Manager):
  Go to the "Expense Claim" list.
  Select a claim with "Submitted" status.
  Change the status to "Under Review."
  Approve or Reject the claim (Status will change to "Approved" or "Rejected").

# Permissions
  Employees:
  Can submit new expense claims.
  Cannot approve or reject claims.
  Managers:
  Can review submitted claims.
  Can approve or reject claims.

# Workflow
  Submitted: The employee submits a new expense claim.
  Under Review: The manager begins reviewing the claim.
  Approved: The manager approves the claim.
  Rejected: The manager rejects the claim.
  The current status of each claim can be viewed by both the employee and manager, with appropriate permissions.
