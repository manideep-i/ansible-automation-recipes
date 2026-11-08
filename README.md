# Ansible Automation Recipes & Playbook Examples

![Ansible](https://img.shields.io/badge/Ansible-E00000?style=for-the-badge&logo=ansible&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![DevOps](https://img.shields.io/badge/DevOps-000000?style=for-the-badge&logo=devops&logoColor=white)

A comprehensive hands-on repository of **Ansible playbooks**, **configuration patterns**, **control flow techniques**, and **system administration recipes**. Designed as a practical reference for automation engineers and DevOps professionals.

---

## 📚 Topics & Playbooks Covered

### 1. Server Provisioning & Service Management
- **`firstplaybook.yml`**: Practical introduction to playbooks covering package installation (`yum`), handler triggers, custom prompts, and variable files.
- **`apacheweb.yml`**: Automated installation, configuration, and service management for Apache Web Server (`httpd`).
- **`appserver.yml`**: Application server package deployment and service configuration.

### 2. Control Flow & Advanced Playbook Logic
- **`loop.yml`**: Demonstrates iteration constructs (`with_items`) for batch user creation and multi-package management.
- **`when.yml`**: Conditional task execution targeting specific OS families (`RedHat`, `Debian`) and host facts.
- **`until.yml`**: Asynchronous task polling and retries until specific output conditions are satisfied.
- **`failure.yml`**: Error handling strategies using `ignore_errors`, custom failure conditions (`failed_when`), and graceful degradation.

### 3. Data Integration & External Lookups
- **`lookup.yml` & `lookup.csv`**: Ingesting and parsing external CSV datasets dynamically during playbook runtime using Ansible lookup plugins.

### 4. Execution Scoping & Modular Playbooks
- **`include.yml`**: Code reuse and playbook modularity using task inclusion techniques.
- **`tag.yml`**: Strategic task tagging (`tags`) for granular, targeted playbook execution.
- **`runonce.yml`**: Execution throttling (`run_once: true`) across host inventories.
- **`accounts.yml`**: Automated user account provisioning and rights management.
- **`local.yml`**: Localhost execution and task delegation patterns.

---

## 📂 Repository Structure

```
.
├── Playbooks/                  # Organized repository of playbooks & configs
│   ├── conf/                   # Modular variable files (copyright.yml, webdefaults.yml)
│   └── plays/                  # Reusable task plays (packages.yml)
├── Outline/                    # Web server setup drafts and configuration blueprints
├── apacheweb.yml                # Apache HTTP Server automation
├── appserver.yml               # Application server installation playbooks
├── accounts.yml                # Account management automation
├── failure.yml                 # Error handling & exception management examples
├── firstplaybook.yml           # Starter playbook template
├── include.yml                 # Playbook modularity & include patterns
├── local.yml                   # Local execution & delegation
├── loop.yml                    # Iteration and looping patterns
├── lookup.yml                  # CSV data lookup integration
├── runonce.yml                 # Throttling & run-once tasks
├── tag.yml                     # Task tagging examples
├── until.yml                   # Retries and status polling
└── when.yml                    # Conditional task execution
```

---

## 🚀 How to Use

### Run a Specific Playbook

Execute any playbook against your target inventory:

```bash
ansible-playbook -i hosts apacheweb.yml
```

### Run Tasks with Specific Tags

```bash
ansible-playbook -i hosts tag.yml --tags "packages"
```

### Dry-run (Check Mode)

```bash
ansible-playbook -i hosts firstplaybook.yml --check
```

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
