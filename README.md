## Competitor Workflow

### Creating a Repository

1. **Access Gitea:**  
   Open your Git server (e.g., `https://git.local.skill17.com`) and log in using your credentials.

2. **Choose a Framework Template:**  
   Go to `organization -> frameworks` to pick a framework or the vanilla base for your repository. The templates include the necessary Docker and Gitea files with GitHub Actions ready to use. Check the [Frameworks Documentation](./frameworks.md) for details.  
   **Tip:** Keep frontend and backend in separate repositories for better organization.

3. **Use the Template:**  
   Click **"Use this template"** to create your repository. Name the repository to match the module name defined in the configuration file.  
   **Example:** If your module is `module-a`, name the repository `module-a`.

4. **Set Up Action Secrets:**  
   Go to **Settings → Actions → Secrets** in your new repository and add:  
   - **`USER`**: Your username (e.g., `comp01`)  
   - **`PASS`**: Your password (e.g., `test123`)

5. **Test the Setup:**  
   Make a commit to verify that GitHub Actions are working correctly.

### Cloning and using the Repository

1. Use the repository URL to clone it:  
   ```bash
   git clone https://git.local.skill17.com/<username>/<module_name>.git
   ```  
   **Example:**  
   ```bash
   git clone https://git.local.skill17.com/comp01/module-a.git
   ```

2. Edit, commit, and develop your code. Frequent commits help keep your work organized, and using branches allows you to work on features or fixes without affecting the main deployment. If competition organizers allow it, you can use third-party packages to support frameworks and enhance your project. Always keep your project README up to date with essential information about the repository, such as setup instructions and dependencies.

3. Every push automatically deploys to the competition URL (e.g., `https://<subdomain>-<module_name>.local.skill17.com`).  
   Be mindful of the number of pushes to avoid unnecessary deployments. Check your changes at the competition URL after each push.
