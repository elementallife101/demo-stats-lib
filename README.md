# GitHub Practical - Statistics Library

A simple Python statistics library for practicing GitHub workflows, team collaboration, automated testing (to implement), and continuous integration. The library provides fundamental statistical operations:

- `mean(data)` - Returns the arithmetic mean (average) of a list of numbers
- `variance(data)` - Returns the variance of a list of numbers


## Project Files

- `stats_demo.py` - A demo script that uses the statistics library
- `stats_lib.py` - A library containing basic statistical functions
- `test_stats_lib.py` - Pytest test suite for the statistics library


## Getting Started

#### Prerequisites

- Python 3.8 or higher
- A package manager: pip, conda, or uv

#### Dependencies installation

Install dependencies using your preferred package manager:

```bash
# Using pip (built-in with Python)
pip install pytest pytest-cov pandas

# Using conda (recommended for data science)
conda install pytest pytest-cov pandas

# Using uv (fast, modern alternative)
uv pip install pytest pytest-cov pandas
```


#### Usage

Run the demo script:

```bash
python stats_demo.py data/temp2005.csv

# This data file contains NAs
python stats_demo.py data/temp1995.csv

```

Or import the statistics library in your own code:

```python
from statistics import mean, variance

data = [1, 2, 3, 4, 5]

print(f"Mean: {mean(data)}")            # Output: Mean: 3.0
print(f"Variance: {variance(data)}")    # Output: Variance: 2.0
```


## Testing

This project includes a simple set of pytest tests to demonstrate good testing practices.

To run all tests locally:

```bash
pytest -v

# Coverage report
pytest --cov=statistics --cov-report=term
```


## Practice Exercise

Here is an exercise for practicing Git and GitHub workflows. Add a new function `stdev(data)` that calculates the standard deviation ($\sigma = \sqrt{\text{variance}}$) and new tests for it.

Add a workflow for GitHub Actions to watch the tests run automatically.
<https://github.com/Bristol-Training/demo-calc-lib>


#### 1. Fork and Clone

You cannot create a branch directly in someone else's repository if you're not a collaborator. Click the "Fork" button on GitHub to copy this repo to your account first. Then clone your fork:

```bash
git clone https://github.com/YOUR_USERNAME/demo-stats-lib.git
cd demo-stats-lib
```

#### 2. Create a Feature Branch

```bash
git checkout -b feature/add-function-stdev
```

This creates the branch and switches to it in one command.

#### 3. Make Changes and Commit

Edit the files using your text editor, then:

```bash
git status                      # See what files you changed
git add .                       # Stage all changed files
git commit -m "Add standard deviation function"
```

#### 4. Run Tests Locally

Before pushing, make sure all tests pass:

```bash
pytest -v
```

#### 5. Push and Create Pull Request

```bash
git push origin feature/add-function-stdev
```

- Go to GitHub and click "Compare & pull request"
- Add description and request review
- Watch the automated tests run in the PR
- Merge via the web interface once tests pass

#### 6. Add Continuous Integration

This repository uses **GitHub Actions** to automatically run tests on every push and pull request. The CI workflow:

- Tests against multiple Python versions (3.8, 3.9, 3.10, 3.11)
- Runs the full pytest suite with coverage reporting
- Verifies the demo script executes successfully

You can view the test results in the **Actions** tab of the GitHub repository.

- `.github/workflows/pytest.yml` - GitHub Actions CI workflow

<br>
© 2025 Pau Erola, Jean Golding Institute, University of Bristol
