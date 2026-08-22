# Learning Record 0018: AI-Assisted Browser Testing & Network Mocking (Chrome DevTools MCP & MSW)

## Concept Overview
- **Angular Pattern**: Protractor / Cypress E2E testing with CSS/XPath element locators, coupled with unit-test-scoped `HttpClientTestingModule` / `HttpTestingController` for network mocking.
- **AI-Augmented React Pattern**: Chrome DevTools MCP allowing AI pair programmers and subagents to perform autonomous browser validation loops (DOM snapshots, accessibility tree inspection, console/network auditing), combined with Mock Service Worker (MSW v2) for network-layer request interception across both browser sessions and local dev.

## Key Bridges & Translations
1. Imperative Cypress/Protractor test scripts &rarr; Chrome DevTools MCP autonomous agent testing and DOM validation loops.
2. `cy.get('.submit-btn')` &rarr; Accessible semantic roles & labels inspected directly via Chrome DevTools Protocol.
3. `HttpTestingController` / `httpMock.expectOne()` &rarr; MSW v2 (`http.get('/api/...', () => HttpResponse.json(...))`).
4. Flaky timeouts & assertions &rarr; Real-time DevTools console log inspection and network request monitoring.

## Packages & References
- [`msw`](https://www.npmjs.com/package/msw) &bull; [MSW Documentation](https://mswjs.io)
- [Chrome DevTools](https://developer.chrome.com/docs/devtools) &bull; [Chrome DevTools Overview](https://developer.chrome.com/docs/devtools/overview)
