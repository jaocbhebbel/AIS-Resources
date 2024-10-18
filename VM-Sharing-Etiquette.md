
# Proper Etiquette for Sharing a Virtual Machine (VM)

Sharing a virtual machine with others, especially in a professional or collaborative environment, requires careful attention to etiquette. VMs often have limited resources, and collaboration on them can lead to confusion or inefficiency if best practices are not followed. This guide outlines the key points for VM-sharing etiquette and provides answers to common questions to ensure smooth cooperation.

## Table of Contents

1. [General Guidelines](#general-guidelines)
2. [Communication](#communication)
3. [Resource Management](#resource-management)
4. [File Organization](#file-organization)
5. [Security Best Practices](#security-best-practices)
6. [Environment Management](#environment-management)
7. [Frequent FAQs: Do's and Don'ts](#frequent-faqs-dos-and-donts)
8. [Example AI Training File Structure](#example-ai-training-file-structure)

---

## General Guidelines

### 1. Respect System Resources
- Always be mindful of CPU, memory, and disk usage.
- If your task is computationally heavy (e.g., training a large AI model), ensure others are aware and not affected by slowdowns or crashes.
- Don't run long, resource-intensive processes without notifying others.

### 2. Clean Up After Yourself
- Once you finish a task, ensure that you clean up unused files, shut down processes, and remove any environment-specific configurations that are no longer needed.
- Avoid leaving personal temporary files or unused VMs/data lying around, cluttering shared space.

### 3. Consistency in Naming
- Use clear, consistent naming conventions for directories, scripts, virtual environments, and files.
- Prefix your files or directories with your username or project name, e.g., `john_model_training/`.

---

## Communication

### 1. Notify Others of Your Activity
- If you're about to perform tasks that may take up significant resources, notify the team.
- Use a shared messaging platform (Slack, email, etc.) to communicate when you're starting, and when you've completed heavy tasks.

## Resource Management

### 1. Monitor System Load
- Regularly monitor CPU, memory, and disk usage using tools like `htop`, `nvidia-smi` (for GPU), or `df -h` for disk space.
- If resources are scarce, consult others before starting additional processes.

### 2. Use Virtual Environments
- Use virtual environments (venv, conda, etc.) for your Python projects or any language-specific environments.
- Ensure that everyone works in isolated environments to avoid dependency conflicts.

---

## File Organization

### 1. Follow Agreed-upon File Structures
- Agree on a common file structure for storing datasets, scripts, results, and logs.
- Keep your files well-organized by creating clear directories for each project or task.

### 2. Limit the Use of Home Directories
- Avoid using personal home directories (`/home/yourname`) to store shared project files. Instead, use project-specific directories located in common spaces like `/projects/` or `/data/`.

### 3. Delete Obsolete Files
- Regularly remove unused or obsolete files to avoid clutter. If unsure, communicate with the team before deleting shared files.

---
## Security Best Practices

### 1. Use SSH Keys
- If accessing the VM remotely, use secure methods like SSH keys rather than plain passwords.
- Avoid sharing your SSH key or credentials with others. If others need access, ensure they generate and use their own keys.

### 2. Monitor Permissions
- Be mindful of file permissions. Use `chmod` to set appropriate access permissions on your files.
- Don’t open your directories to everyone unless it's necessary (`chmod 777` should be avoided in most cases).

### 3. Update and Patch
- Regularly update your software to ensure it's patched against vulnerabilities. Coordinate these updates with the team.

---

