# Echoverse QA Project

Manual testing of **Echoverse**, a web application that converts text, TXT, PDF and image content into audio. This repository holds the test scenarios, test cases and bug reports created during testing.

**Tester:** Mahrukh Khan (QA Engineer)
**Last updated:** 18 November 2026

---

## Application under test

Echoverse is a web app where a user signs up, logs in, and creates tabs. Inside a tab the user can type text or upload a TXT, PDF or image file, which is converted to audio. The app also offers translation, a language list, copy, chat history and a profile window.

## Modules tested

| Module | What was covered |
|---|---|
| Signup | UI, field validations, duplicate email, password rules, navigation |
| Login | UI, validations, Google sign-in window, session access, security observations |
| Dashboard | Sidebar, New Tab, search, Today's and Previous Tabs, delete tab, collapse, profile and logout |
| Tab page | Text, TXT, PDF and image to audio, audio player, translation, copy, chat history, Profile window |

Test types used: functional, UI, negative, boundary, usability, compatibility and exploratory testing.

**Out of scope:** Forgot password (not available), the full Google account flow, changing the password through the Update Password form, performance and load testing.

---

## Results summary

| Module | Scenarios | Test cases | Passed | Failed | Blocked |
|---|---|---|---|---|---|
| Signup | 11 | 58 | 52 | 6 | 0 |
| Login | 11 | 52 | 49 | 2 | 1 |
| Dashboard | 10 | 53 | 47 | 5 | 1 |
| Tab page | 13 | 88 | 63 | 11 | 14 |
| **Total** | **45** | **251** | **211** | **24** | **16** |

**Blocked test cases:** Test cases that need audio conversion (TXT, PDF and image uploads and some text cases) could not be run because the API credits were finished. They will be run once credits are available.

---

## Bugs reported in Jira

Bugs were logged in Jira (space: *Echoverse Bug Tracker*, key `ECHO`). Each bug has a summary, preconditions, steps to reproduce, test data, expected result, actual result, priority, labels and the linked test case.

| Bug | Module | Summary | Linked test case |
|---|---|---|---|
| ECHO-1 | Signup | Signup accepts a 7-character password although the minimum is 8 | TC_SIGNUP_36 |
| ECHO-2 | Signup | First Name with only spaces is accepted on Signup | TC_SIGNUP_24 |
| ECHO-3 | Login | Login button keeps its disabled grey look when credentials are autofilled by the browser | TC_LOGIN_47 |
| ECHO-4 | Dashboard | Selected tab is not highlighted in the Dashboard sidebar | TC_DASH_29 |
| ECHO-5 | Dashboard | Tab key focus order on the Dashboard is not as expected | TC_DASH_49 |
| ECHO-6 | Tab page | Tab key focus order on the tab page is not logical | TC_TAB_88 |
| ECHO-7 | Tab page | 'Uploaded Image' window closes only with the X icon | TC_TAB_52 |
| ECHO-8 | Tab page | Picture preview in chat bubble cuts off the edges of the text | TC_TAB_53 |

The full list is in `bug-reports/`. Some failed test cases are listed as questions for the team instead of bugs, because the expected behaviour needs confirmation.

---

## Repository structure

```
Echoverse-QA-Project/
├── README.md
├── test-scenarios/
│   └── Echoverse_Test_Scenarios.xlsx
├── test-cases/
│   ├── ECHOVERSE-SIGNUP-TESTCASES.xlsx
│   ├── Echoverse_Login_Testcases.xlsx
│   ├── Echoverse_Dashboard_Testcases.xlsx
│   └── Echoverse_Tab_Testcases.xlsx
├── bug-reports/
│   └── Echoverse_Jira_Bugs.csv
└── screenshots/
```

## How the documents are organised

- **Test scenarios** list what is tested in each module and show the pass, fail and blocked count for each scenario.
- **Test cases** have an ID, scenario ID, title, type, priority, precondition, steps, test data, expected result, actual result and status (Pass, Fail, Blocked).
- **Bug reports** are exported from Jira and link back to the failed test case.

## Tools used

- **Jira**: bug logging and tracking
- **Postman**: API testing
- **Microsoft Excel**: test scenarios and test cases
- **Google Chrome** (DevTools): browser testing
- **GitHub**: storing the project documents

---

## Contact

Mahrukh Khan, QA Engineer
