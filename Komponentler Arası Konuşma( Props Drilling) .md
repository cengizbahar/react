# App Component

## State users arreyimizi oluşturuyoruz. Users componentimizden bilgileri dönüyoruz.

```html

import React, { Component } from 'react';
import Navbar from './components/Navbar';
import './App.css';
import Users from './components/Users';



class App extends Component {
state = {
  users: [
    {
      id : 1,
      name : "Mustafa Bahar",
      salary : "5000",
      department : "Bilişim"
    },
    {
      id : 2,
      name : "Sefer Bahar",
      salary : "5000",
      department : "Teknoloji"
    },
    {
      id : 3,
      name : "Caner Bahar",
      salary : "5000",
      department : "İT Manager"
    }
  ]
}

  render() {
    return (
      <div className="container">
          <Navbar/>
          <hr />
          <Users users = {this.state.users}  />
          
         
          
      </div>
    )
  }
}


export default App;

```

# Users Component

```html

import React, { Component } from 'react'
import User from "./User"

class Users extends Component {
    render() {
        const {users} = this.props;
        console.log(users);

        return (
            <div>
                {
                    users.map(user => {
                        return (
                            <User
                                key = {user.id}
                                name = {user.name}
                                salary = {user.salary}
                                departmant = {user.departmant}
                            />
                        )
                    })
                }
            </div>
        )
    }
}

export default Users;

```
