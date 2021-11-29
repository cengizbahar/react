

import React,{Component} from 'react';


export default class Form extends Component
{ 

  constructor(props)
  {
    super(props);
    this.HandleChange = this.HandleChange.bind(this);


  }
  state = {
    kullanici_adi : "",
    soyadi : "",  }
 
  HandleChange(e)
  {
    this.setState({
      [e.target.name] : e.target.value
    })
  }


  render()  
  {

    return(
      <div>
      
        <label>Kullanıcı Adı</label>
        <input type="text" name="kullanici_adi" value={this.state.kullanici_adi} onChange={this.HandleChange}></input> <br></br>
        <label>Soyadi</label>
        <input type="text" name="soyadi" value={this.state.soyadi} onChange={this.HandleChange}></input> <br></br>
  
        <span>{this.state.kullanici_adi} - {this.state.soyadi}</span>
        </div>

    );
  }
}


