## Src Klasörünün altına ' Components ' adında bir klasör oluşturuyoruz. İçerisine ilk componentimizi ekliyoruz. ' Users.js '

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
