# State Oluşturma

## 2. Yöntemli State Oluşturma

```html

import React, { Component } from 'react'
import PropTypes from 'prop-types'


class Users extends Component {
    // 1 . Yöntem
//    constructor (props) {
//        super(props);
//    
//        this.state = {
//            isVisible : true
//        }
//    } 
    // 2. Yöntem
    state = {
        isVisible : true
    }
    render() {
        // İsvisible
        const {isVisible} = this.state;
        return (
            <div>
                {
                    isVisible ?
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
                </ul> : null
                }
                
            </div>
        )
    }
}


export default Users;

```
