
### **Step-by-Step Guide for Your Friends to Fork Your Private Repository and Contribute**

#### **1. Forking Your Repository**

1. **Go to Your Repository**: Your friends should visit your private repository on GitHub. Since your repository is private, make sure that they have been **added as collaborators** to the repository. If they aren't collaborators yet, you'll need to add them (go to the **Settings** → **Manage access** → **Invite a collaborator**).

2. **Fork the Repository**:
   - In the top-right corner of the page, there will be a **Fork** button. Your friends need to click it.
   - This will create a **copy of your private repository** in their own GitHub account.

#### **2. Clone Their Fork Locally**

Once the repository has been forked, your friends need to clone it to their local machine.

1. On their forked repository page (in their own GitHub account), they need to click the **Clone or download** button and copy the **HTTPS URL**.

2. In their terminal, they should run this command:
   ```bash
   git clone https://github.com/their-username/repository-name.git
   ```
   Replace `their-username` with their GitHub username and `repository-name` with the name of the repository.

#### **3. Create a New Branch (Not `main`)**

To avoid pushing changes directly to the `main` branch, your friends should **always create a new branch** for each feature or bug fix they are working on.

1. **Navigate to their local repository**:
   ```bash
   cd repository-name
   ```

2. **Create a new branch**:
   ```bash
   git checkout -b feature-branch-name
   ```
   Replace `feature-branch-name` with a descriptive name for the feature they are working on (e.g., `feature-add-login`).

#### **4. Work on the Feature and Commit Changes**

They can now make their changes in the new branch. Once they’re done with their changes:

1. **Stage and commit the changes**:
   ```bash
   git add .
   git commit -m "Description of changes"
   ```

2. **Push the changes to their fork**:
   ```bash
   git push origin feature-branch-name
   ```

#### **5. Create a Pull Request (PR) to Your Repository**

Once the changes are pushed to their forked repository, they can create a **pull request (PR)** to propose their changes to your `main` branch.

1. **Go to Your GitHub Repository** (the original one).
2. Click on the **Pull Requests** tab.
3. Click **New Pull Request**.
4. Under **base**, select `main` (the branch in your repository).
5. Under **compare**, select their branch (`feature-branch-name`) from their forked repository.
6. Write a description for the pull request (optional).
7. Click **Create Pull Request**.

#### **6. Review and Merge the PR**

Once the pull request is created, you, as the repository owner, can review the changes and merge them into your `main` branch.

1. Go to the **Pull Requests** tab of your repository.
2. Review the pull request.
3. If everything looks good, click **Merge pull request** to merge the changes into `main`.

#### **7. Sync Their Fork (If Needed)**

If your `main` branch receives new updates and your friends want to keep their fork in sync with your repository, they can follow these steps to **sync their fork**:

1. **Add your repository as an upstream remote**:
   ```bash
   git remote add upstream https://github.com/your-username/repository-name.git
   ```

2. **Fetch the latest changes**:
   ```bash
   git fetch upstream
   ```

3. **Merge the changes into their local main branch**:
   ```bash
   git checkout main
   git merge upstream/main
   ```

4. **Push the changes** to their fork (if needed):
   ```bash
   git push origin main
   ```

---

### **Summary of the Workflow for Your Friends:**

1. **Fork** your private repository (ensure they're added as collaborators).
2. **Clone their fork** to their local machine.
3. **Create a new branch** (don't work directly on `main`).
4. **Make changes**, **commit**, and **push** to their fork.
5. **Create a pull request** to propose changes to your `main` branch.
6. You review and **merge the pull request** into `main`.
7. Optionally, **sync their fork** with the latest changes from your repository.

---

Steps for Your Friend to Set Up the Project: .zipFile

Extract the Project Files: After receiving the compressed file, your friend should extract it to their local development environment.

Set Up the Environment: Install Composer and Node.js (if not already installed). Run the following commands in the project root:

composer install

composer update

npm install

npm run dev

Set Up the Database: Import the SQL file into their local database. Update the .env file with their local database credentials.

Run Migrations and Seeders (if needed):

php artisan migrate

php artisan db:seed

Start the Development Server:

php artisan serve
