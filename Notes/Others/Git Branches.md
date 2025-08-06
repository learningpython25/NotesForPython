### Initial Setup

1. Create a folder and initialize Git:

```bash
mkdir git-maths-project
cd git-maths-project
git init
```

2. Create `maths.py`:

```bash
touch maths.py
```

3. Create your first commit on `main` branch:

```bash
git add maths.py
git commit -m "Initial empty maths.py"
```

---

### 1. Create `branch-one` for addition

```bash
git checkout -b branch-one
```

Now edit `maths.py` to add:

```python
def addition(a, b):
    return a + b
```

Then:

```bash
git add maths.py
git commit -m "Add addition function"
```

---

### 2. Create `branch-two` for subtraction

We want this **branch to start from main**, not from `branch-one`:

```bash
git checkout main
git checkout -b branch-two
```

Edit `maths.py`:

```python
def subtraction(a, b):
    return a - b
```

Then commit:

```bash
git add maths.py
git commit -m "Add subtraction function"
```

---

### 3. Switching Between Branches

To see the code in different branches:

```bash
git checkout branch-one
cat maths.py  # shows only addition

git checkout branch-two
cat maths.py  # shows only subtraction
```

---

### 4. Merge into `main`

Now merge both branches into `main`.

```bash
git checkout main
```

#### Merge `branch-one`:

```bash
git merge branch-one
# Now maths.py has addition()
```

#### Merge `branch-two`:

```bash
git merge branch-two
# Now maths.py has both addition() and subtraction()
```

Check final file:

```bash
cat maths.py
```

Output:

```python
def addition(a, b):
    return a + b

def subtraction(a, b):
    return a - b
```

---

### 5. Clean Up (Delete Merged Branches)

Once branches are merged, you can safely delete them:

```bash
git branch -d branch-one
git branch -d branch-two
```

---

### Summary of Commands

```bash
# Initialize
git init

# Create branch-one
git checkout -b branch-one
# add addition() in maths.py
git add maths.py
git commit -m "Add addition function"

# Create branch-two from main
git checkout main
git checkout -b branch-two
# add subtraction() in maths.py
git add maths.py
git commit -m "Add subtraction function"

# Merge both into main
git checkout main
git merge branch-one
git merge branch-two

# Delete branches
git branch -d branch-one
git branch -d branch-two
```
