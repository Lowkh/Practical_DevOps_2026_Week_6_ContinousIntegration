# Continuous Integration Practical
## Automated Testing with GitHub Actions

Welcome to this guided, self-directed practical on continuous integration (CI).

You will create a small Python calculator, automate its tests, investigate a deliberate defect, repair a pull request and integrate a small feature.

You will work on Windows using a web browser. GitHub Actions executes the code on a hosted Windows runner. No local Git, Python, Docker or IDE installation is required for the required activities.

AI use is optional. If you choose to use an AI/LLM tool, evaluate its suggestions, verify results and acknowledge its assistance.

> Educational use
>
> Use your own disposable learning repository and follow the school’s policies. These examples are for learning, not production deployment. No personal access token, secret, payment details, cloud subscription or self-hosted runner is required by these instructions.

---

## Contents

- [1. Learning Outcomes](#1-learning-outcomes)
- [2. Practical Overview](#2-practical-overview)
- [3. Submission Requirements](#3-submission-requirements)
- [4. Working Safely](#4-working-safely)
- [5. Optional AI Use and Your Responsibilities](#5-optional-ai-use-and-your-responsibilities)
- [Guided Activities](#guided-activities)
- [6. G1 — Prepare Your Repository](#6-g1--prepare-your-repository)
- [7. G2 — Create the Application and Tests](#7-g2--create-the-application-and-tests)
- [8. G3 — Create the CI Workflow](#8-g3--create-the-ci-workflow)
- [9. G4 — Observe a Deliberate Failure](#9-g4--observe-a-deliberate-failure)
- [10. G5 — Repair and Merge](#10-g5--repair-and-merge)
- [11. G6 — Inspect Run Identity and History](#11-g6--inspect-run-identity-and-history)
- [12. Small Applied Practical Assessment](#12-small-applied-practical-assessment)
- [13. Reflection](#13-reflection)
- [14. AI/LLM Usage Declaration](#14-aillm-usage-declaration)
- [15. Assessment Criteria](#15-assessment-criteria)
- [16. Troubleshooting and Using AI Effectively](#16-troubleshooting-and-using-ai-effectively)
- [17. Final Submission Checklist](#17-final-submission-checklist)
- [18. After Capturing Your Evidence](#18-after-capturing-your-evidence)
- [Official Documentation](#official-documentation)

---

## 1. Learning Outcomes

By the end of this practical, you should be able to:

1. Explain how CI provides automated feedback when changes are proposed or integrated.
2. Identify a workflow, event, job, step, runner and action.
3. Create application code, automated tests and a GitHub Actions workflow.
4. Interpret a failing test and repair the implementation without weakening the test.
5. Use a branch and pull request to integrate a verified change.
6. Relate a result to the correct repository, event and commit.
7. Add a small feature and preserve the existing test suite.

If you choose to use AI, you should also be able to:

8. Ask a focused technical question.
9. Evaluate the response for accuracy, suitability and safety.
10. Verify suggestions through documentation and your own execution.
11. Acknowledge the assistance accurately.

---

## 2. Practical Overview

| Item | Details |
| :--- | :--- |
| Format | Guided self-learning followed by a small applied assessment |
| Student environment | Windows, web browser and Microsoft Word |
| Account | GitHub account permitted by the school |
| Execution environment | GitHub-hosted Windows runner with Python 3.xx |
| Testing framework | Python’s built-in `unittest` module |
| Local installation | None required for this route |
| Guided activities | G1–G6 |
| Applied assessment | Parts A and B form one feature task and one pull request |
| Optional tool | An AI/LLM tool permitted by the school |
| Submission | One Word document |

### Readiness Conditions

You need to be able to sign in to GitHub, create a repository and use GitHub Actions. Complete any account registration or verification required by the school.

If access is blocked, capture the restriction and document the unfinished activity. Do not bypass the school’s policies or enable paid usage.

### Required Route

```text
Create repository and Word document
                ↓
Add calculator and five tests
                ↓
Create workflow → verify five passing tests
                ↓
Open practice pull request → observe one failure
                ↓
Repair same pull request → verify → merge
                ↓
Inspect post-merge run and identity
                ↓
Add multiplication and two tests in a new pull request
                ↓
Verify seven tests → merge → complete submission
```

Capture evidence as you work, especially the deliberate failure. Organise it under the relevant Word document headings before continuing.

---

## 3. Submission Requirements

Submit one Word document containing:

1. Your name, student ID, class and learning repository URL.
2. Screenshot evidence under headings G1–G6.
3. Screenshot evidence for assessment Parts A and B.
4. A reflection of approximately 100–150 words.
5. A brief AI/LLM usage declaration stating whether you used AI.

No separate report, source-code upload, ZIP file, artifact, video or AI conversation transcript is required. The code remains in your learning repository.

### Prepare Your Document

Use these headings:

```text
Continuous Integration Practical

Student Details and Repository URL
G1 — Repository
G2 — Application and Tests
G3 — Successful Baseline
G4 — Deliberate Failure
G5 — Repair and Merge
G6 — Run Identity and History
Assessment Part A — Feature and Tests
Assessment Part B — Verification and Integration
Reflection
AI/LLM Usage Declaration
```

Save using the school’s naming convention. If none is specified, use:

```text
StudentID_CI_Practical.docx
```

Save your work regularly. Screenshots already used under G5 may also support G6; reference the existing evidence instead of taking an unnecessary duplicate.

### Screenshot Expectations

Each screenshot must include your initials or another identifier that demonstrates the work is your own, alongside the relevant technical work.

- Keep your repository owner/name, personalised README, initials-labelled run title or identity output visible.
- Keep relevant branch names, checks, test output and commit information readable.
- For a log screenshot, retain the run identity on screen or place a second browser window showing the same run’s identity beside the result.
- Capture the deliberate failure before repairing it.
- Use more than one screenshot if necessary; do not shrink text until it becomes unreadable.
- Do not add identification afterwards using an image editor.
- Do not submit generated, reconstructed or misleadingly edited output.
- Exclude passwords, tokens, full student IDs and unrelated private information from screenshots unless required by the school.

Visible identification supports attribution; it does not replace evidence of the work. Short captions are optional.

---

## 4. Working Safely

- Follow the school’s account, repository, security and AI-use policies.
- Use your own learning repository, not the teaching repository or another student’s repository.
- Use initials rather than full student details in repository content.
- Select the repository visibility required by the school. Public repositories are visible to others.
- Check Actions access and account usage limits. Stop if payment details or unauthorised access changes are required.
- Do not create secrets, access tokens, deployment credentials or self-hosted runners.
- Keep the workflow’s read-only repository permissions.
- Put deliberate defects only in the named practice branch.
- Check the latest successful run before merging; do not bypass existing school rules.
- Preserve runs and pull requests until evidence is complete and any retention instructions issued by the school have been met.

---

## 5. Optional AI Use and Your Responsibilities

You may complete every required activity using this guide and official documentation without AI. No explanation for not using AI is required.

If you choose to use AI:

```text
Identify a question → ask clearly → evaluate → verify → acknowledge
```

| Responsibility | What to do |
| :--- | :--- |
| Ask clearly | Include the relevant file, branch, workflow step and exact message. |
| Protect information | Remove credentials, student details and unrelated private content. |
| Evaluate | Compare the response with the actual code, YAML and intended behaviour. |
| Preserve tests | Do not delete tests, change correct expected values or ignore failures just to obtain a successful status. |
| Verify | Consult official documentation and inspect your own run. |
| Acknowledge | State the tool, purpose and how its advice was checked. |

No AI conversation screenshots or transcripts are required.

---

## Guided Activities

Complete G1–G6 in order. All required code is supplied below.

| Activity | Expected Outcome |
| :--- | :--- |
| G1 | Personalised repository with a `main` branch |
| G2 | Calculator and five tests at the repository root |
| G3 | Successful CI baseline |
| G4 | Pull-request check detects the deliberate subtraction defect |
| G5 | Same pull request passes after repair and is merged |
| G6 | Correctly identifies the post-merge run, event and commit |

### Key Concepts

| Term | Meaning in this practical |
| :--- | :--- |
| Continuous integration | Integrating changes regularly with automated checks to detect problems early. |
| Commit | A recorded version of changes, identified by a SHA. |
| Branch | A separate line of work. |
| Pull request | A proposal to integrate a branch into a base branch, with changes and checks available for review. |
| Workflow | Automation defined in a YAML file under `.github/workflows/`. |
| Event | The activity that triggers automation. |
| Runner | The machine executing a job. |
| Job | A group of steps executed on a runner. |
| Step | A command or reusable action within a job. |
| Action | A reusable automation component. |
| Assertion | A check comparing actual behaviour with expected behaviour. |

This practical runs automated tests. It does not package, release or deploy the calculator. Passing tests show that the configured checks passed—not that every possible defect has been excluded.

### Before You Begin

- [ ] I can sign in and create a learning repository.
- [ ] I have prepared my Word document.
- [ ] I understand the screenshot identification requirements.
- [ ] I understand that AI is optional.

---

## 6. G1 — Prepare Your Repository

### 6.1 Create the Repository

1. Open [GitHub](https://github.com/) and sign in using the account permitted by the school.
2. Select the `+` menu and choose New repository.
3. Name it `ci-practical-ab`, replacing `ab` with your initials. If that name already exists, use another suitable name such as `ci-practical-ab-actions`.
4. Use the description:

   ```text
   A guided CI practical using Python and GitHub Actions.
   ```

5. Choose the visibility required by the school.
6. Select the option to add a README and create the repository.
7. Confirm that the default branch is named `main`. If it is not, rename it through the repository’s branch settings if permitted before continuing.

Use a new repository rather than a fork for this route.

### 6.2 Personalise the README

1. Open `README.md` and select the pencil/edit control.
2. Paste the following and replace `AB` with your initials:

```markdown
# CI Practical — AB

Student initials: AB

This repository demonstrates automated testing with GitHub Actions.

Starting version: five calculator tests.
Final required version: seven calculator tests, including multiplication.
```

3. Select Commit changes.
4. Use the message `Personalise CI practical` and commit directly to `main`.
5. Add the repository URL to your Word document.

### Evidence for G1

Capture the repository home page with the owner/name, `main` branch and personalised README visible.

### Readiness Checkpoint

Confirm you can create and edit files. If account or Actions restrictions prevent progress, use Section 16 and record the limitation honestly.

---

## 7. G2 — Create the Application and Tests

### 7.1 Create a File in GitHub

For each file below:

1. Open the repository’s Code page and select `main`.
2. Select Add file → Create new file.
3. Enter the exact filename.
4. Paste the supplied content without the Markdown fence lines.
5. Select Commit changes and commit directly to `main` with the suggested message.

No workflow exists yet, so these starting commits will not run CI.

### 7.2 Create `calculator.py`

Replace `AB` with your initials. Keep the functions unchanged.

```python
STUDENT_INITIALS = "AB"


def add(a, b):
    return a + b


def subtract(a, b):
    return a - b


def divide(a, b):
    if b == 0:
        raise ValueError("Cannot divide by zero")
    return a / b
```

Commit message:

```text
Add calculator functions
```

### 7.3 Create `test_calculator.py`

```python
import unittest

from calculator import add, subtract, divide


class TestCalculator(unittest.TestCase):
    def test_add_positive_numbers(self):
        self.assertEqual(add(2, 3), 5)

    def test_add_negative_numbers(self):
        self.assertEqual(add(-2, -3), -5)

    def test_subtract(self):
        self.assertEqual(subtract(9, 4), 5)

    def test_divide(self):
        self.assertEqual(divide(8, 2), 4)

    def test_divide_by_zero(self):
        with self.assertRaisesRegex(ValueError, "Cannot divide by zero"):
            divide(8, 0)


if __name__ == "__main__":
    unittest.main()
```

Commit message:

```text
Add five calculator tests
```

### 7.4 Understand the Tests

| Test | Expected Behaviour |
| :--- | :--- |
| Positive addition | `add(2, 3)` returns `5`. |
| Negative addition | `add(-2, -3)` returns `-5`. |
| Subtraction | `subtract(9, 4)` returns `5`. |
| Division | `divide(8, 2)` returns `4`. |
| Division by zero | `divide(8, 0)` raises the expected `ValueError`. |

Each method whose name starts with `test_` is a test.

- `assertEqual` compares the actual result with the expected result.
- `assertRaisesRegex` verifies the exception type and message.
- The division-by-zero test passes when the expected exception occurs.

### Expected Files

```text
ci-practical-ab/
├── README.md
├── calculator.py
└── test_calculator.py
```

### Evidence for G2

Capture the file listing and the five test methods, keeping repository identification visible. No local Python execution is required.

---

## 8. G3 — Create the CI Workflow

### 8.1 Add the Workflow

1. On `main`, select Add file → Create new file.
2. Enter the full filename:

   ```text
   .github/workflows/ci.yml
   ```

   The slashes create the folders.

3. Paste the workflow below.
4. Replace both occurrences of `AB` with your initials: in `run-name` and `STUDENT_INITIALS`.
5. Preserve spaces and indentation. Do not use tabs or include Markdown fences.
6. Commit directly to `main` with the message `Add calculator CI workflow`.

```yaml
name: Calculator CI
run-name: CI - AB | ${{ github.event_name }} | ${{ github.ref_name }}

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]
  workflow_dispatch:

permissions:
  contents: read

env:
  STUDENT_INITIALS: AB

jobs:
  test:
    name: Test calculator
    runs-on: windows-latest

    steps:
      - name: Check out repository
        uses: actions/checkout@v6

      - name: Set up Python
        uses: actions/setup-python@v5
        with:
          python-version: '3.12'

      - name: Show run identity
        shell: pwsh
        run: |
          Write-Output "Student initials: $env:STUDENT_INITIALS"
          Write-Output "Repository: $env:GITHUB_REPOSITORY"
          Write-Output "Event: $env:GITHUB_EVENT_NAME"
          Write-Output "Ref: $env:GITHUB_REF"
          Write-Output "Commit: $env:GITHUB_SHA"
          Write-Output "Run ID: $env:GITHUB_RUN_ID"
          python --version

      - name: Run automated tests
        run: python -m unittest discover -s . -p "test_*.py" -v
```

### 8.2 Understand the Workflow

| Component | Purpose |
| :--- | :--- |
| `name` | Labels the workflow in GitHub Actions. |
| `run-name` | Labels each run with your initials, event and branch/ref information. |
| `push` on `main` | Runs when a commit reaches `main`, including a merge. |
| `pull_request` targeting `main` | Runs when a pull request into `main` is opened or its branch is updated. |
| `workflow_dispatch` | Allows optional manual execution; not required for submission. |
| `permissions: contents: read` | Requests read-only access to repository contents. |
| `env` | Supplies your initials to the workflow steps. |
| `runs-on: windows-latest` | Uses a hosted Windows runner, not your own computer. |
| `checkout` | Copies the repository onto the runner. |
| `setup-python` | Selects Python 3.xx; this workflow uses `3.12`. |
| `Show run identity` | Prints your initials, repository, event, ref, commit and run ID. |
| `unittest discover` | Finds `test_*.py` files and runs their tests. |
| `-v` | Shows individual test names and results. |

The versions following `@` are action versions, not Python versions. Keep the action references as supplied.

The workflow deliberately uses a specific Python version in its executable configuration. General descriptions in this guide use Python 3.xx.

Major action tags and `windows-latest` are not fixed environment identifiers; this is a teaching workflow rather than a fully pinned production environment.

No external Python dependencies are required. There is no custom report helper or artifact upload in the required activities; the Actions log contains the test results.

### 8.3 Inspect the First Run

1. Open Actions and select Calculator CI if necessary.
2. Open the run for `Add calculator CI workflow`.
3. Check that it has completed and open the Test calculator job.
4. Expand Show run identity.
5. Expand Run automated tests.

The output should report five tests and `OK`.

Confirm that five tests actually ran. An `OK` result with zero tests is not the required baseline.

### Learning Checkpoint

Identify:

- The event that triggered the workflow.
- The runner that executed the job.
- The command that ran the tests.
- The role of the checkout step.

Check your interpretation against the workflow and official documentation. If using AI, verify its explanation against your actual run.

No extra written response is required.

### Evidence for G3

Capture the successful run and five-test result with your identity visible. Combine the summary and log in one screenshot where readable; otherwise use two.

### First-Success Checkpoint

Do not introduce the deliberate defect until the starting version genuinely passes five tests. Use Section 16 if it does not.

---

## 9. G4 — Observe a Deliberate Failure

### 9.1 Create the Practice Branch

1. Return to Code and select `main`.
2. Open the branch selector.
3. Enter `practice-subtract-failure` and create the branch from `main`.
4. Confirm the selector now shows that branch.

### 9.2 Introduce the Defect

1. Open `calculator.py` on the practice branch and select edit.
2. Change only:

```python
def subtract(a, b):
    return a - b
```

To:

```python
def subtract(a, b):
    return a + b
```

3. Keep the tests unchanged.
4. Commit to `practice-subtract-failure` with the message:

```text
Introduce deliberate subtraction defect
```

This feature-branch push alone does not trigger the workflow because the `push` filter includes only `main`. Opening the pull request triggers the check.

### 9.3 Open the Pull Request

1. Select Compare & pull request, or Pull requests → New pull request.
2. Set:
   - Base: `main`
   - Compare: `practice-subtract-failure`
3. Use the title `AB — Investigate subtraction failure`, replacing `AB`.
4. Add the description:

   ```text
   This practice change introduces a subtraction defect to inspect CI feedback.
   ```

5. Create the pull request. Do not merge it.
6. Open the check details from the pull request or locate the matching run in Actions.

### 9.4 Read the Failure

Expand Run automated tests.

The output should identify:

```text
FAIL: test_subtract ...
AssertionError: 13 != 5
...
FAILED (failures=1)
```

Confirm that five tests executed with one failure.

The inputs `9` and `4` should produce `5`; the defective implementation produces `13`. A nonzero test exit status makes the step and job fail.

### Evidence for G4

Capture the failed check and relevant assertion output with identification. Preserve this evidence before repairing the code.

---

## 10. G5 — Repair and Merge

### 10.1 Diagnose the Failure

| Question | Answer |
| :--- | :--- |
| Which test failed? | `test_subtract`. |
| What was expected? | `5`. |
| What was observed? | `13`. |
| What caused the difference? | Addition replaced subtraction. |
| What should be repaired? | The function, not the correct expected value. |

### 10.2 Fix the Same Branch

1. On Code, select `practice-subtract-failure`.
2. Edit `calculator.py`.
3. Replace the defective function with:

```python
def subtract(a, b):
    # Keep subtraction distinct from addition.
    return a - b
```

The comment leaves a small, intentional reviewed change after the arithmetic is restored.

4. Commit to the same branch with the message:

   ```text
   Fix subtraction after CI feedback
   ```

5. Return to the existing pull request. Do not open a second one for the repair.
6. Inspect its latest completed checks.

Expected result: all five tests pass. The earlier failed run remains in history.

A rerun of the old failed commit would not repair the code. The new commit supplies the correction.

### 10.3 Review and Merge

1. Open Files changed and confirm the arithmetic is correct.
2. Confirm the latest checks have passed.
3. Select the available standard merge option and confirm the merge.
4. Open Actions. A new push run on `main` should appear.
5. Inspect that post-merge run in G6.

### Merge-Check Limitation

A visible failed check is not necessarily an enforced merge block. Enforcement depends on repository rules and permissions.

Configuring branch protection is outside the required activities. Follow the school’s rules and inspect the latest checks before merging.

### Evidence for G5

Capture the repaired pull request showing successful checks and its merged state.

Keep your initials or another identifier that demonstrates the work is your own visible.

---

## 11. G6 — Inspect Run Identity and History

1. Open the post-merge run on `main`.
2. Confirm that it is associated with the merge, rather than the earlier failed run.
3. Confirm the event is `push` and five tests pass.
4. Expand Show run identity and identify:
   - Your initials.
   - Repository.
   - Ref.
   - Commit.
   - Run ID.
5. Compare the failed practice run with the repaired/latest run in the Actions history.

### Understand What You Are Viewing

- The commit SHA links a result to a revision.
- The run ID identifies a particular workflow run.
- The event explains why the workflow started.
- A pull-request run can use GitHub’s test merge commit rather than the source branch’s last commit. Use the event and pull-request context as well as the SHA.
- The Actions log is the evidence source for this practical. A separate downloadable report is not required.

### Evidence for G6

Capture the post-merge run showing a successful five-test result and relevant run identity.

You may reference suitable evidence already captured under G5 instead of duplicating it.

---

## 12. Small Applied Practical Assessment

Parts A and B form one feature task, one branch and one pull request.

Retain all existing functions, tests and the workflow. AI use is optional.

### Part A — Add Multiplication and Its Tests

#### A1. Create the Feature Branch

From the latest `main`, create `assessment-multiply` using the branch selector.

#### A2. Add the Function

Edit `calculator.py` on that branch and append:

```python
def multiply(a, b):
    return a * b
```

Keep the existing initials, subtraction comment and other functions.

Commit to `assessment-multiply` with the message:

```text
Add multiplication
```

#### A3. Add Two Tests

Edit `test_calculator.py` on the same branch.

Change its calculator import to:

```python
from calculator import add, subtract, divide, multiply
```

Inside `TestCalculator`, add the following methods before the final `if __name__` block.

Match the existing indentation: four spaces before each `def` and eight before each assertion.

```python
    def test_multiply_positive_numbers(self):
        self.assertEqual(multiply(3, 4), 12)

    def test_multiply_by_zero(self):
        self.assertEqual(multiply(7, 0), 0)
```

Commit to the same feature branch with the message:

```text
Test multiplication and zero boundary
```

Do both file edits before opening the pull request so the function and its tests are checked together.

#### Evidence for Part A

Capture the added function and tests with repository identification. Use one or two screenshots as needed.

### Part B — Verify and Integrate the Feature

1. Open a pull request from `assessment-multiply` into `main`.
2. Include your initials in the title, for example:

   ```text
   AB — Add tested multiplication
   ```

3. Inspect the changed files and latest checks.
4. Confirm that seven tests pass: the original five plus two multiplication tests.
5. Merge after the latest checks pass.
6. Inspect the resulting push run on `main` and confirm seven tests pass.

Do not delete or skip existing tests, change correct expected values or configure the workflow to ignore failures.

#### Evidence for Part B

Capture the seven-test result, merged pull request and successful post-merge run with identification.

If a restriction prevents completion, record its actual state honestly.

### Expected Test Progression

| Stage | Tests Executed | Expected Result |
| :--- | ---: | :--- |
| G3 baseline | 5 | All pass |
| G4 deliberate defect | 5 | One failure |
| G5 repair | 5 | All pass |
| G6 post-merge baseline | 5 | All pass |
| Assessment feature | 7 | All pass |
| Assessment post-merge | 7 | All pass |

These counts refer to test methods, not assertions or workflow steps.

No additional deliberate defect is required for the assessment.

---

## 13. Reflection

Write approximately 100–150 words covering:

1. One CI concept you understood better through your own work.
2. How you diagnosed the failure or checked an explanation using this guide, official documentation or an optional AI tool.
3. One limitation, safety consideration or improvement you would apply next.

Use a specific example, such as `test_subtract`, a workflow event or the difference between the failed and repaired runs.

If you used AI, include one example of how you evaluated and verified its response. If not, describe your documentation and execution checks instead.

No additional report is required.

---

## 14. AI/LLM Usage Declaration

Place a brief declaration after your reflection. It is outside the reflection’s suggested word count.

### If You Used AI

> I used [tool name] to help with [specific question or task]. I checked its response by [documentation and/or execution checks]. I [used, adapted or rejected] the suggestion because [brief reason]. My screenshots show my own execution.

Acknowledge other assistance if applicable, including help with reflection wording.

### If You Did Not Use AI

> I did not use an AI/LLM tool for this practical.

No explanation for not using AI and no conversation transcript are required.

---

## 15. Assessment Criteria

Your work will be reviewed against the following criteria.

| Component | Criteria |
| :--- | :--- |
| G1 — Readiness | Creates and personalises an appropriate learning repository. |
| G2 — Code and tests | Creates the correct application and five starting tests. |
| G3 — Workflow | Configures the events, runner, Python version and test command; demonstrates a genuine successful baseline. |
| G4 — Failure detection | Shows the deliberate defect and identifies the failed test, expected result and actual result. |
| G5 — Repair | Repairs the implementation on the same pull request, checks the latest successful result and merges. |
| G6 — Traceability | Identifies the correct post-merge run, event and revision context. |
| Assessment Part A | Adds multiplication and two tests without removing existing checks. |
| Assessment Part B | Verifies seven passing tests and integrates the feature through a pull request. |
| Reflection | Explains specific learning, verification and a meaningful limitation or improvement. |
| AI declaration | Accurately states whether AI was used and describes assistance and checks if applicable. |
| Evidence quality | Provides readable, authentic screenshots with identification and relevant technical context. |

AI use is optional. The same criteria apply whether or not you use AI.

If work is incomplete, provide the actual state and available evidence. Identify the unfinished step rather than claiming a result that your evidence does not demonstrate.

---

## 16. Troubleshooting and Using AI Effectively

Investigate one check at a time. Read the actual message before changing files.

### 16.1 Choose the Starting Point

```text
No run? → Check file path, branch and event filter.
Queued run? → Check runner/account status.
Invalid workflow? → Check YAML spaces and structure.
Setup error? → Read checkout or Python setup output.
Test error? → Read the first relevant traceback or assertion.
Wrong result? → Check the run’s commit and latest branch changes.
```

### 16.2 Account or Actions Restrictions

Confirm you are in your own repository and have the required access. Review the school’s policy.

Do not enable billing, create an unauthorised runner or bypass restrictions.

Capture the limitation and record execution as incomplete.

### 16.3 No Run Appears

Check:

- The workflow path is exactly `.github/workflows/ci.yml`.
- The file was committed, not left as an unsaved edit.
- Your default/base branch is `main`.
- The event is a push to `main` or an opened/updated pull request targeting `main`.
- The workflow is not disabled.

A feature-branch commit with no open pull request does not meet this guide’s automatic event filters.

### 16.4 YAML Is Invalid

Compare with G3.

- Preserve colons and indentation.
- Preserve `${{ ... }}` expressions.
- Use spaces rather than tabs.
- Do not copy Markdown fences into `ci.yml`.

If the school’s policy disallows a supplied action version, record the restriction and use only an authorised alternative.

### 16.5 Python Import or Syntax Error

Check that:

- `calculator.py` and `test_calculator.py` are at the repository root.
- Filenames have not acquired a `.txt` extension.
- Imported function names exist and are spelled consistently.
- New test methods are indented inside `TestCalculator` and before the final `if __name__` block.
- Both application and test changes are committed to the intended branch.

Do not name a project file `unittest.py`, because it can conflict with the testing module.

### 16.6 Zero Tests or an Unexpected Count

Check:

- The filename is `test_calculator.py`.
- The test class inherits from `unittest.TestCase`.
- Test method names begin with `test_`.

This practical uses the standard unittest command. Always inspect the number executed: five for the starting version and seven after the assessment feature.

An `OK` status with zero tests is not adequate evidence.

### 16.7 An Assertion Fails

Identify:

1. The test name.
2. Inputs.
3. Expected result.
4. Actual result.

Compare the function with its intended behaviour.

Correct the implementation when it is wrong; do not weaken a valid test to hide the defect.

### 16.8 The Pull Request Still Shows Failure

Open its latest run and check the commit.

Confirm the repair was committed to its compare branch.

Old failed runs remain in history; they do not disappear after a later successful run.

### 16.9 A Run Is Queued or Has Not Completed

Check the displayed runner and account status messages.

Avoid creating duplicate runs. Do not claim an unfinished run has passed.

If access restrictions prevent completion, capture the state and identify the unfinished activity.

### 16.10 Identification Is Not Visible

Check the run title and `STUDENT_INITIALS` in `ci.yml`.

Expand Show run identity or show the same run’s identity in a second browser window beside the test output.

Do not add identification afterwards.

### 16.11 Optional AI Troubleshooting Prompt

```text
I am completing a browser-based continuous integration practical.
My computer uses Windows. CI uses windows-latest and Python 3.12.

Activity:
[Enter the activity]

Event and branch:
[Enter the actual event, base branch and working branch]

Relevant file or step:
[Paste only the relevant non-sensitive content]

Exact message:
[Paste the message]

Expected result and checks already completed:
[Explain briefly]

Please suggest one safe diagnostic check at a time.
Preserve the intended behaviour and existing tests.
Do not suggest disabling checks, exposing credentials or bypassing policy.
Explain how I can verify the result in my own run.
```

The prompt uses the specific Python version configured in the supplied workflow so that troubleshooting advice matches the actual environment.

Compare advice with your files and official documentation. A plausible explanation is not proof of successful execution.

### 16.12 Record Partial Progress Honestly

Capture the actual error or state with your initials or another identifier that demonstrates the work is your own.

Place it under the correct heading, briefly identify the unfinished step and declare any AI assistance used.

---

## 17. Final Submission Checklist

### Details and Guided Activities

- [ ] My name, student ID, class and repository URL are included.
- [ ] G1 shows my personalised repository.
- [ ] G2 shows the application and five tests.
- [ ] G3 shows a successful five-test baseline.
- [ ] G4 shows the deliberate failure before repair.
- [ ] G5 shows the repair, successful checks and merged pull request.
- [ ] G6 shows the correct post-merge run and identity, or references suitable existing evidence.

### Applied Assessment

- [ ] Part A shows multiplication and its two tests.
- [ ] Part B shows seven passing tests and the merged feature pull request.
- [ ] The final post-merge run is verified, or its unfinished state is recorded honestly.

### Reflection and Declaration

- [ ] My reflection is approximately 100–150 words and uses a specific example.
- [ ] If I used AI, I evaluated and verified relevant suggestions.
- [ ] My declaration accurately states whether and how I used AI.

### Evidence and Document Quality

- [ ] Every screenshot includes my initials or another identifier that demonstrates the work is my own, alongside the relevant work.
- [ ] Identification was visible during capture, not added afterwards.
- [ ] Screenshots are readable and under the correct headings.
- [ ] Relevant branch, event, test and run information is visible.
- [ ] Incomplete activities are identified honestly.
- [ ] Unrelated private information is excluded.
- [ ] I am submitting one `.docx` file only.

---

## 18. After Capturing Your Evidence

Keep the repository, runs and pull requests until review is complete and any retention instructions issued by the school have been met.

No local server, container or self-hosted runner needs to be stopped for this route.

### Project File Summary

The student project has four source/configuration files:

```text
ci-practical-ab/
├── README.md
├── calculator.py
├── test_calculator.py
└── .github/
    └── workflows/
        └── ci.yml
```

The teaching guide itself can be published as a single `README.md` in a separate teaching repository. Students create the files above in their own learning repository.

### Optional Follow-Up

These activities are not required and need no additional submission evidence:

- Manually run Actions → Calculator CI → Run workflow, choose `main` and inspect a `workflow_dispatch` run.
- Add a fractional-division test such as checking that `divide(7, 2)` returns `3.5`.
- Explore GitHub’s documentation on storing test results as artifacts.

Complete the required activities, evidence and reflection before attempting optional work.

---

## Official Documentation

- [GitHub Actions quickstart](https://docs.github.com/en/actions/writing-workflows/quickstart)
- [Building and testing Python](https://docs.github.com/en/actions/use-cases-and-examples/building-and-testing/building-and-testing-python)
- [Events that trigger workflows](https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows)
- [Python unittest documentation](https://docs.python.org/3/library/unittest.html)

Use the equivalent control if the GitHub website displays different interface wording.
