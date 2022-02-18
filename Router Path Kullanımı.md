## Güncel Route Path Kullanımı = Menü oluşturma
## npm i react-router-dom
## Exact : İlk açılmasını istediğiniz sayfayı belirtir.
````
import { BrowserRouter as Router, Route, Routes } from 'react-router-dom';

render()  
  {
   

    return(
    <div>
      <div>
      <Router>
    
        <Routes>
          <Route  exact path="/" element={<Home/>}/>
          <Route  path="/about" element={<About/>}/>
          <Route  path="/form" element={<Form/>}/>
          
        </Routes>
     
      </Router>
    </div>

    </div>

    );
  }
}

export default App;
````
