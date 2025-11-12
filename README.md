## Copilot ChatModes for Automation Testing

This repository collects reusable "chatmodes" (conversation templates/prompts) tailored for automation testing tasks. Each chatmode is a self-contained markdown file that encodes the prompt, instructions, examples, and expected input/output style so you can quickly run or adapt automation-related conversations.

### Included chatmodes

#### Test Conversion & Migration
- **`SeleniumToPlaywrightConverter/🎭 Selenium ➡ Playwright.chatmode.md`** — Converts Selenium Page Object Model (POM) code to Playwright in C# .NET. Maintains structure, functionality, and test logic while modernizing to Playwright's async patterns and built-in waiting mechanisms.

- **`CypressToPlaywrightConverter/🎭 Cypress ➡ Playwright.chatmode.md`** — Converts Cypress test code to Playwright in JavaScript/TypeScript. Transforms Cypress test implementations into modern, robust Playwright tests while preserving business logic and improving reliability.

#### BDD & Test Scenarios
- **`PlaywrightBDDScenarios/🎭 Playwright BDD Scenarios (Reqnroll).chatmode.md`** — Creates BDD test scenarios for Playwright in C# .NET using Reqnroll (formerly SpecFlow). Helps structure feature files with Gherkin syntax, generate step definitions, and integrate with Playwright for robust test automation.

#### Reporting & Analytics
- **`PlaywrightExtentReports/🎭 Playwright Extent Reports.chatmode.md`** — Implements ExtentReports for Playwright test automation in C# .NET. Sets up comprehensive HTML reporting with screenshots, test execution logs, detailed metrics, and beautiful visualizations for test results.

### How to use a chatmode

1. Open the chatmode file you want to use from the folders above.
2. Provide your test code, requirements, or description to the chat interface that's running the chatmode.
3. The chatmode defines the expected input shape and the preferred output style. Copy the returned code into your project and run it after adding appropriate dependencies.

#### Example Usage Scenarios

**Selenium to Playwright (C#.NET):**
```
Convert the following Selenium test to Playwright (C#.NET + Playwright Test):

// Selenium WebDriver
driver.Navigate().GoToUrl("https://example.com");
driver.FindElement(By.Id("login")).SendKeys("user");
driver.FindElement(By.Id("password")).SendKeys("pass");
driver.FindElement(By.CssSelector("button[type=submit]")).Click();
```

**Cypress to Playwright (JavaScript):**
```
Convert this Cypress test to Playwright:

cy.visit('/login');
cy.get('#username').type('testuser');
cy.get('#password').type('password123');
cy.get('button[type="submit"]').click();
cy.url().should('include', '/dashboard');
```

**BDD Scenarios (Reqnroll):**
```
Create BDD scenarios for a login feature with valid/invalid credentials and 
empty field validation using Playwright and Reqnroll.
```

**Extent Reports:**
```
Implement Extent Reports for my Playwright C# .NET test project with 
screenshots on failure and detailed test logging.
```

### Naming and file conventions

- Chatmodes are markdown files containing the instructions and examples. Use descriptive filenames and include the source → target when the chatmode performs conversions (for example: `Selenium ➡ Playwright`).
- Keep the `🎭` prefix for human-recognizable chatmode files if helpful; it's optional and purely cosmetic.

### Adding new chatmodes

1. Create a new markdown file at the repository root or inside a dedicated folder, following the naming convention above.
2. Include: intent description, example inputs, expected outputs, and any configuration toggles (language, runner, sync/async).
3. Add a short README entry in this file referencing the new chatmode (or submit a PR to update this repository README).

### Contribution

Contributions are welcome. Simple steps:

1. Fork this repository.
2. Add or improve chatmode markdown files.
3. Open a pull request describing the change and example usage.

### License

This repository does not ship a license by default — if you'd like to apply one, MIT is a good permissive choice. Add a `LICENSE` file in the repo root for clarity.

---

### Quick Reference

| Chatmode | Purpose | Language/Framework | Use Case |
|----------|---------|-------------------|----------|
| Selenium ➡ Playwright | Test Migration | C# .NET | Converting Selenium POM tests to Playwright |
| Cypress ➡ Playwright | Test Migration | JavaScript/TypeScript | Converting Cypress tests to Playwright |
| BDD Scenarios (Reqnroll) | BDD Framework | C# .NET + Reqnroll | Creating Gherkin scenarios with Playwright |
| Extent Reports | Test Reporting | C# .NET | Adding comprehensive HTML reports to tests |

### Repository Structure

```
Copilot-ChatModes-For-Testing/
├── SeleniumToPlaywrightConverter/
│   └── 🎭 Selenium ➡ Playwright.chatmode.md
├── CypressToPlaywrightConverter/
│   └── 🎭 Cypress ➡ Playwright.chatmode.md
├── PlaywrightBDDScenarios/
│   └── 🎭 Playwright BDD Scenarios (Reqnroll).chatmode.md
├── PlaywrightExtentReports/
│   └── 🎭 Playwright Extent Reports.chatmode.md
└── README.md
```