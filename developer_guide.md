# Git Workflow Guide: Branch Management & Safe Development

## Initial Setup
1. Clone repository
```bash
git clone https://github.com/Cybernetic-Controls/CCL_Timetracker.git
cd CCL_Timetracker
```

## Creating & Working with Branches
1. Create and switch to new branch
```bash
git checkout -b Changes
```

2. Check current branch (verify you're on correct branch)
```bash
git status
```

## Making Changes
1. Best practices for changes:
   - Make small, focused changes addressing single issues
   - Test changes thoroughly in isolation
   - Keep commits atomic and related to single functionality
   - Document changes clearly in commit messages

2. Stage changes
```bash
git add <specific-files>  # Stage specific files
git add .                 # Stage all changes
```

3. Commit changes
```bash
git commit -m "descriptive message about changes"
```

## Testing
1. Run all tests in branch
2. Verify functionality works as expected
3. Check for any conflicts with main branch
```bash
git checkout main
git pull origin main
git checkout Changes
git merge main
```

## Merging to Main
1. Update main branch
```bash
git checkout main
git pull origin main
```

2. Merge changes
```bash
git merge Changes
```

3. Push to remote
```bash
git push origin main
```

## Why Make Small Changes?

### Benefits
1. Easier to review and test
2. Simpler conflict resolution
3. Better version control
4. Faster rollback if issues occur
5. Clearer development history

### Best Practices
1. One feature/fix per branch
2. Regular commits with clear messages
3. Test before merging
4. Keep branches short-lived
5. Regular synchronization with main branch

## Common Issues & Solutions

### Merge Conflicts
```bash
# If conflicts occur during merge
git status                  # Check conflicting files
# Resolve conflicts manually
git add <resolved-files>
git commit -m "resolve merge conflicts"
```

### Undo Last Commit
```bash
git reset --soft HEAD~1    # Undo commit but keep changes
```

### Discard Changes
```bash
git checkout -- <file>     # Discard changes in specific file
git reset --hard          # Discard all changes (use carefully)
```


This guide provides a structured approach to managing code changes. Would you like me to explain any specific part in more detail?