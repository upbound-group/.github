![Upbound Logo](https://upbound.com/assets/images/Upbound-logo.png?v=Mar-16-v1)
# Upbound Group GitHub Organization

Welcome to the Upbound Group GitHub Organization! Part of the [Upbound Group](https://upbound.com/) 

This organization is dedicated to managing and collaborating on projects related to Upbound Group's software development efforts. 

This README provides an overview of how the organization is structured, including details on team management, repository organization and other information that all members should be aware of.

<details>
<summary><h2>How the Upbound Group Organization is managed</h2></summary>
The Upbound Group GitHub Organization is managed strictly through Infrastructure as Code (IaC) using Terraform. This approach ensures that all configurations are version-controlled, auditable, and reproducible. 

### Key Points:
- **Organization Settings**: Terraform scripts define the organization's settings, including billing, security policies, and member privileges. Those files can be found [here](https://github.com/upbound-group/devops_terraform/tree/main/applications/vcs/github/upbound-group).

- **Audit and Compliance**: All changes to the organization are tracked through version control, providing a clear audit trail and facilitating compliance with internal and external policies. All changes to an Organization are tracked, and streamed through an Audit Log to our Security Operations Center.

By leveraging Terraform, the Upbound Group ensures a scalable and maintainable approach to managing its GitHub organization.

</details>

--- 

<details>
<summary><h2>How Teams are organized and managed</h2></summary>

Teams within the Upbound Group GitHub Organization are structured to promote collaboration and efficient project management. Teams are also managed through Terraform, ensuring consistent configuration and access controls. The code for Team management can be found [here](https://github.com/upbound-group/upbound-cloud-directory/blob/main/directory/teams/rac.yml).

### Key Points:
- **Team Creation**: New teams are created via Terraform scripts, specifying team names, descriptions, and membership. In some cases, the membership of a team is manually defined through Terraform. In other cases, a team is synchronized with Entra ID. This way Entra ID becomes the source of truth for a team.

- **Access Control**: Teams are granted repository access based on their roles and responsibilities. Access levels (read, write, admin) are defined in the Terraform configurations to maintain security and proper permissions. A zero-trust approach is followed to ensure that teams or team members do not have more access than they need. 

- **Membership Management**: Team memberships are regularly reviewed and updated through version-controlled Terraform files. Changes in team composition are tracked to maintain an accurate record of access rights. In the case that a Team is synchronized with Entra ID, usually changes made in Entra ID are shown in GitHub in approximately 1 hour.

</details>

--- 

<details>
<summary><h2>How Repositories are organized and managed</h2></summary>

Repositories within the Upbound Group GitHub Organization are organized to support clarity, security, and efficient collaboration. Repository management is also handled through Terraform to ensure consistent settings across all projects. The code for Repository management can be found [here](https://github.com/upbound-group/upbound-cloud-directory/blob/main/directory/repositories/upbound.yml)

### Key Points:
- **Repository Naming Conventions**: All repositories follow a standardized naming convention to make them easily identifiable and searchable.

- **Repository Visibility**: By default all repositories are to be Private, and shared with users or Teams that need access. 

    - In some cases, it is benneficial for a repository to be shared with all GitHub users. In this case, a repository may be configured with Internal priviledges. 
    - In the rarest of cases, a Public repository may be created. 
    - In either case, Internal or Public, these kinds of repositories should only be created by a DevOps team member, and reviewed through a pull request.

- **Access Control**: Repository access is managed through team permissions defined in Terraform. This ensures that only authorized team members can access, modify, or administer repositories. Changes to the access of repository must be approved by the owners of the repository.

- **Security and Compliance**: Security settings such as default branch protection,required pull request reviews, passing status checks and code scanning are enforced through Terraform. Repositories are regularly audited to ensure compliance with organizational policies.

- **Archiving and Deletion**: Inactive or deprecated repositories are archived. If a repository can be deleted, it is done with the oversight of the DevOps team, and completed through Terraform. This ensures a clean and organized environment.

</details>

---

## How do I reach out for help?

For further asisstance, you may reach out to the DevOps team in [Slack](https://simple-it.slack.com/archives/C0W019B0C) or [Teams](https://teams.microsoft.com/l/team/19%3AkMnmudqzDaLnw-w1ip36TR-_6l05guveDliM376qhBU1%40thread.tacv2/conversations?groupId=71830294-83d1-4cb2-8ab0-383698f5e994&tenantId=b2df5bc5-70df-4b7e-be09-6ffb2f11d0e9). In addition, you may reach out to the Cyber Security team in [Slack](https://simple-it.slack.com/archives/C04LK3WAMD1).




