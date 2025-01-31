# React component wrapper for [Mathquill](http://mathquill.com/)

[![npm version](https://badge.fury.io/js/react-mathquill.svg)](https://badge.fury.io/js/react-mathquill)

## Example

> Link to an [example](https://viktorstrate.github.io/react-mathquill/)

```javascript
import React from 'react'
import MathQuill, { addStyles as addMathquillStyles } from 'react-mathquill'

// inserts the required css to the <head> block.
// You can skip this, if you want to do that by your self.
addMathquillStyles()

export default class App extends React.Component {
  constructor() {
    this.state = {
      latex: '\\frac{1}{\\sqrt{2}}\\cdot 2',
    }
  }

  render() {
    return (
      <MathQuill
        latex={this.state.latex} // Initial latex value for the input field
        onChange={latex => {
          // Called everytime the input changes
          this.setState({ latex })
        }}
      />
    )
  }
}
```
