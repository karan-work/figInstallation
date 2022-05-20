
# Installation of storybook-figma addon

## Installation

User either NPM or Yarn to install as dev dependency

```bash
npm install —save-dev storybook-addon-designs
```
```bash
yarn add -D storybook-addon-designs
```

## Register the addon in the Storybook main.js file

```javascript
// .storybook/main.js
module.exports = {
  addons: [‘storybook-addon-designs’]
}
```

## Test Example
Try importing the design for leaderboard cutline into Storybook.

Add a `withDesign` decorator and `design` parameter to a specific story
```javascript
// myStories.stories.jsx
export const myStory = () => < cutLineComponent />

myStory.parameters = {
  design: {
    type: 'figma',
    url:
      'https://www.figma.com/file/ny6LqQXsRc9BPChzL8N91U/Main-%E2%80%A2-Web?node-id=1087%3A201896',
  },
}
```
