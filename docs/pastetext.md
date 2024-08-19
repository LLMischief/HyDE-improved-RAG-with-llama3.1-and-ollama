Paste any text copied with copyTextFrom into the currently focused field.

Note: Make sure your text field is in focus before using this command.
```yaml
- pasteText
```
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