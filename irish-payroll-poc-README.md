# Irish Payroll Engine — Proof of Concept

A browser-based proof of concept for an Irish payroll calculation engine. No installation required — open `index.html` in any browser.

## What it demonstrates

### Single payslip
- PAYE calculation using 2026 rate bands (20% / 40%)
- USC calculation across all four bands
- PRSI (Class A, S, M) — employee and employer contributions
- Cumulative, Week 1 / Month 1, and Emergency tax basis
- Pension contribution (pre-tax relief)
- Benefit in kind
- My Future Fund auto-enrolment (phased contributions — Year 1 rates)
- Full calculation workings shown step by step

### Pay run
- Add multiple employees with individual tax details
- Run the full pay run in one click
- View net pay per employee
- Pay run summary: total gross, net pay, PAYE/USC liability, total employer cost
- Click any employee to see their full payslip breakdown

## Tax year

2026 rates and thresholds. All figures are illustrative for demonstration purposes.

| Tax | Rates used |
|-----|-----------|
| PAYE | 20% standard / 40% higher rate |
| USC | 0.5% / 2% / 4% / 8% (standard), 0.5% / 2% (reduced) |
| PRSI Class A | Employee 4%, Employer 11.5% |
| PRSI Class S | Employee 4%, Employer 0% |
| My Future Fund | Employee 1.5%, Employer 1.5%, State top-up €1:€3 |

## How to use

1. Clone or download this repository
2. Open `index.html` in a browser
3. No server, no dependencies, no build step required

## How to put this in Git

```bash
git init
git add .
git commit -m "Irish payroll engine POC — initial version"
```

To push to GitHub/GitLab, create a new repository there and follow their instructions to add the remote.

## Notes

- This is a proof of concept only — not for use in live payroll
- RPN retrieval from Revenue is simulated (tax credits and cut-off entered manually)
- PSR submission to Revenue is not included in this POC
- NAERSA (pension auto-enrolment authority) API integration is not included
- Rounding follows standard Irish payroll convention (to the cent)

## Next steps toward production

1. Integrate with Revenue's RPN API to pull live tax details per employee
2. Build PSR submission module for post-pay-run Revenue reporting
3. Connect employee data from HR module via API
4. Add NAERSA API integration for My Future Fund reporting
5. Implement proper audit logging and calculation history
