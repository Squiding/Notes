# Git Commands and SSH Configuration

## Basic Git Commands

### Repository Operations
```bash
# Initialize a new repository
git init

# Clone a repository
git clone <repository-url>

# Check repository status
git status

# View commit history
git log
```

### Making Changes
```bash
# Stage changes
git add <file>          # Stage specific file
git add .              # Stage all changes

# Commit changes
git commit -m "Your commit message"

# Push changes to remote
git push origin main    # Push to main branch
```

### Updating Local Repository
```bash
# Pull latest changes
git pull origin main

# Fetch changes without merging
git fetch origin
```

## SSH vs HTTPS

### Why SSH is Faster
- SSH uses a persistent connection
- No need to enter credentials repeatedly
- Better performance for large repositories
- More secure authentication method

### Setting Up SSH
1. Generate SSH key:
```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

2. Add SSH key to GitHub:
   - Copy public key: `cat ~/.ssh/id_rsa.pub`
   - Add to GitHub: Settings → SSH and GPG keys → New SSH key

3. Configure Git to use SSH:
```bash
git remote set-url origin git@github.com:username/repository.git
```

### Switching from HTTPS to SSH
```bash
# Check current remote URL
git remote -v

# Change to SSH URL
git remote set-url origin git@github.com:username/repository.git
```

## Common Workflow
1. Make changes to files
2. Stage changes: `git add .`
3. Commit changes: `git commit -m "message"`
4. Push to remote: `git push origin main`
5. Pull updates: `git pull origin main`

## Troubleshooting
- If push fails: `git push -f origin main` (use with caution)
- If pull has conflicts: resolve conflicts then commit
- If SSH connection fails: check SSH key configuration 