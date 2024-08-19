You can copy text from an element and save it in-memory, to paste later. To find the element you wish to copy text from you can use Selectors. For a full list of what selectors are available, please refer to the Selectors page.
Copies text from an element and pastes it into a search field.
```yaml
appId: com.example.app
---
- launchApp
- copyTextFrom:
    id: "someId"
- tapOn:
    id: "searchFieldId"
- pasteText
```