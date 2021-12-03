

## Axios Kullanımı
### npm install axios
#### import Axios from 'axios';
2 Şekilde veri geldiğinde ne yapacağınızı söyleyebilirsiniz, Then ve await şeklinde istediğiniz örneği kullanabilirsiniz.
#### .then : Data geldiğinde
#### .await : Data geldiğinde

Veri çekme ve post etme işşemleri
#### axios.get : Veri getirme
#### axios.post : Veri gönderme

```
export default class About extends Component
{ 

  state = {
    userList : [],
   
  }
  componentDidMount()
  {
    this.getUserList();
  }

THEN KULLANIMI

  getUserList = async () =>
  {
     Axios.get("https://jsonplaceholder.typicode.com/users").then( data => {

     this.setState({userList : data.data});

     });
  }

## AWAİT KULLANIMI

  getUserList = async () =>
  {
  
     var data = await Axios.get("https://jsonplaceholder.typicode.com/users");
     this.setState({userList : data.data});
  
  }
 

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



