# TVM Calculator — Assignment 1

A browser-based Time Value of Money (TVM) calculator application for **BS3210: Finance for Engineers, Designers and Professionals**.

## Assignment coverage

The application implements all seven required calculators:

1. Future Value (FV)
2. Present Value (PV)
3. Simple Interest
4. Compound Interest
5. EMI Calculation
6. Loan Amortization Schedule
7. Scenario Analysis for 8%, 10%, 12%, and 15%

The assignment requires an **HTML-based web application** and states that only executable HTML/Web Applications will be evaluated.

## Files

- `index.html` — complete application (HTML, CSS, and JavaScript in one file)

## Run locally

No installation is required.

Open `index.html` directly in a browser, or serve the folder with a local web server:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## GitHub Pages deployment

1. Create a new GitHub repository, for example:
   `tvm-calculator-assignment-1`
2. Put `index.html` in the repository root.
3. Commit and push to the `main` branch.
4. On GitHub, open:

   `Settings → Pages`

5. Under **Build and deployment**, choose:
   - Source: **Deploy from a branch**
   - Branch: `main`
   - Folder: `/ (root)`
6. Save and wait for GitHub Pages to publish the site.

The deployed URL will normally follow this pattern:

```text
https://YOUR-USERNAME.github.io/tvm-calculator-assignment-1/
```

## Suggested Git commands

```bash
git init
git add .
git commit -m "Complete TVM calculator assignment"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/tvm-calculator-assignment-1.git
git push -u origin main
```

## Validation and UX

The application includes:
- Numeric input validation
- Clear error messages
- Responsive layout for desktop and mobile
- Financial result formatting in INR
- Automatically generated monthly amortization schedule
- Scenario comparison for the four rates specified in the assignment

## Formula implementation

The JavaScript contains the core formulas used by the calculators:

- Future Value: `FV = P(1+r)^t`
- Present Value: `PV = FV/(1+r)^t`
- Simple Interest: `SI = P*r*t`
- Compound Amount: `A = P(1+r/n)^(n*t)`
- EMI: `EMI = P*r(1+r)^n / ((1+r)^n - 1)`

The amortization schedule calculates monthly interest and principal repayment and adjusts the final payment when necessary so the closing balance reaches zero.

## Assignment reference

This project was implemented against the supplied Assignment 1 brief for BS3210. The brief lists the seven required calculators, the required amortization columns, and the scenario rates 8%, 10%, 12%, and 15%.
