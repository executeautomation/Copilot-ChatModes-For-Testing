## Copilot ChatModes for Automation Testing

This repository collects reusable "chatmodes" (conversation templates/prompts) tailored for automation testing tasks. Each chatmode is a self-contained markdown file that encodes the prompt, instructions, examples, and expected input/output style so you can quickly run or adapt automation-related conversations.

One included chatmode is a Selenium → Playwright converter which helps translate Selenium test code (or test intents) into Playwright equivalents.

### Included chatmodes

- `SeleniumToPlaywrightConverter/🎭 Selenium ➡ Playwright.chatmode.md` — a focused chatmode that converts Selenium-based steps, locators, and patterns into Playwright code (JavaScript/TypeScript). Use this chatmode when migrating tests or porting examples from Selenium to Playwright.

### How to use a chatmode

1. Open the chatmode file you want to use (for example the Selenium → Playwright file above).
2. Provide the Selenium snippet, test steps, or a description of the test to the chat interface that's running the chatmode.
3. The chatmode defines the expected input shape and the preferred Playwright output style (sync/async, test runner, selectors, etc.). Copy the returned Playwright code into your project and run it after adding appropriate dependencies.

Example prompt you can paste into the Selenium → Playwright chatmode:

```
Convert the following Selenium test to Playwright (C#.NET + Playwright Test):

// Selenium WebDriver (Java)
driver.get("https://example.com");
driver.findElement(By.id("login")).sendKeys("user");
driver.findElement(By.id("password")).sendKeys("pass");
driver.findElement(By.cssSelector("button[type=submit]")).click();

Verify that user lands on dashboard with text "Welcome".
```

The chatmode will aim to produce a Playwright Test-style conversion, including imports, POM and assertions.

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

Files in this repo:

- `SeleniumToPlaywrightConverter/🎭 Selenium ➡ Playwright.chatmode.md` — Selenium to Playwright conversion chatmode (example included).