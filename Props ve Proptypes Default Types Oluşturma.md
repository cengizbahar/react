# Props Oluşturma

## APP.JS

```html

import React, { Component } from 'react';
import Navbar from './components/Navbar';
import './App.css';
import Users from './components/Users';


class App extends Component {
  render() {
    return (
      <div className="container">
          <Navbar/>
          <hr />
          <Users 
            name = "Cengiz"
            salary = "5000"
            department = "İT Uzmanı"

          />
          
      </div>
    )
  }
}

export default App;

```
## USERS.JS COMPONENT

```html
import React, { Component } from 'react'

class Users extends Component {
    render() {
        // Destructing 
        const {name,department,salary} = this.props;
        return (
            <div>
                <ul>
                    <li>
                        İsim : {name}
                    </li>
                    <li>
                        Departman : {department}
                    </li>
                    <li>
                        Maaş : {salary}
                    </li>
                </ul>
            </div>
        )
    }
}


export default Users;
```

# propTypes ve defaultProps Oluşturma

```html
import React, { Component } from 'react'

class Users extends Component {
    render() {
        // Destructing 
        const {name,department,salary} = this.props;
        return (
            <div>
                <ul>
                    <li>
                        İsim : {name}
                    </li>
                    <li>
                        Departman : {department}
                    </li>
                    <li>
                        Maaş : {salary}
                    </li>
                </ul>
            </div>
        )
    }
}

Users.defaultProps = {
    name : "bilgi yok",
    department : "bilgi yok",
    salary : "bilgi yok"
}

Users.propTypes = {
    name : PropTypes.string.isRequired,
    department : PropTypes.string.isRequired,
    salary : PropTypes.string.isRequired
}

export default Users;
```
