## Src Klasörünün altına ' Components ' adında bir klasör oluşturuyoruz. İçerisine ilk componentimizi ekliyoruz. ' Users.js '
## App.js de Aşşağıdaki gibi Güncelliyoruz.

## Yeni Component

```html

import React, { Component } from 'react'

 class Users extends Component {
    render() {
        return (
            <div>
                <form>
                    <input type="text" /> 
                    <button>Gönder</button>
                </form>
            </div>
        )
    }
}

export default Users;

```

## App JS

```html

import React, { Component } from 'react'
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
