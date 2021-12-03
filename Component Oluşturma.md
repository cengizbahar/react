## Src Klasörünün altına ' Components ' adında bir klasör oluşturuyoruz. İçerisine ilk componentimizi ekliyoruz. ' Users.js '
## App.js de Aşşağıdaki gibi Güncelliyoruz.

##  Yeni Users Component

```html

import React,{Component} from 'react';

export default class Users extends Component {
  render()  
  {
    
    const users = this.state.userList;

    return(
      <div>
       <ul>
       {
        users.map( (value) => (
          <li key={value.email}>{value.email}</li>
       ))}
       </ul>
        </div>

    );
  }

}

```

## App JS

```html

import React, { Component } from 'react';
import './App.css';
import './components/Users';


 class App extends Component {
  render() {
    return (
      <div>
        <Users />
      </div>
    )
  }
}

export default App;
```
