---
order: 14
title:
  zh-CN: ??
  en-US: Auto Open
---

## zh-CN

??

## en-US

Auto open on focus. Users can fill in dates while they "tab" through a form
```jsx
import { DatePicker } from 'antd';

function onChange(date, dateString) {
  console.log(date, dateString);
}

class AutoOpenDatePickerDemo extends React.Component {
  state = { focusablePanel : false, focusOnClose: false, autoOpen: true };

  render() {
    const { focusablePanel, focusOnClose, autoOpen } = this.state;
    return (
    <div>
      <div>
        <div><label htmlFor="autoopen"><input id="autoopen" checked={this.state.autoOpen} type="checkbox" />Auto open</label></div>
        <div><label htmlFor="focusablePanel"><input id="focusablePanel" checked={this.state.focusablePanel} type="checkbox" />Focusable panel</label></div>
        <div><label htmlFor="focusOnClose"><input id="focusOnClose" checked={this.state.focusOnClose} type="checkbox" />Focus on close</label></div>
      </div>
      <input style={{marginBottom: 12}} readOnly value="Start here and TAB" />
      <DatePicker autoOpen={autoOpen} focusOnClose={focusOnClose} focusablePanel={focusablePanel} onChange={onChange} />
      <br />
      <input style={{marginBottom: 12}} readOnly value="Some input" />
      <br />
      <DatePicker autoOpen={autoOpen} focusOnClose={focusOnClose} focusablePanel={focusablePanel} onChange={onChange} />
      <button type="submit">Submit</button>
    </div>);
  }
}

ReactDOM.render(
  <AutoOpenDatePickerDemo />,
  mountNode,
);
```
