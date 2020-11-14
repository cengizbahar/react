#  onClickEvent & SetState Kullanımı
```html

import React, { Component } from 'react'
import PropTypes from 'prop-types'


class Users extends Component {
    
    // onClickEvent & SetState Kullanımı
    state = {
        isVisible: false
    }

    onClickEvent = (e) => {
       this.setState ({
            isVisible : !this.state.isVisible
       }) 
       
    }
    render() {
        // Destructing 
        const { name, department, salary } = this.props;
        // İsvisible
        const { isVisible } = this.state;
        return (
            <div className="card mt-5">
                
                    <div className="card-header">
                        <h5 className="card-title" onClick = { this.onClickEvent } style = {{cursor : "pointer"}}>İsim : { name }</h5>
                        
                    </div>
                

                {
                    isVisible ?

                        <div className="card-body">

                            <p className="card-text">Departman : { department }</p>
                            <p>Maaş : { salary }</p>

                        </div> : null
                

                }

            </div>
        )
    }
}



export default Users;

```
