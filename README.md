
TypeScript Kurs
https://kursbil.com/en-iyi-typescript-kurslari-online-egitimleri-top-6-2021/

## Swiper Js 
### npm i swiper


```
index.html
    <!-- Swiper -->
     <link rel="stylesheet" href="https://unpkg.com/swiper/swiper-bundle.css">
     <link rel="stylesheet" href="https://unpkg.com/swiper/swiper-bundle.min.css">
     <script src="https://unpkg.com/swiper/swiper-bundle.js"></script>
    <script src="https://unpkg.com/swiper/swiper-bundle.min.js"></script>
    
    

App.Js İmport
// Import Swiper React components
import { Swiper, SwiperSlide } from 'swiper/react';

<Swiper
      spaceBetween={50}
      slidesPerView={3}
      onSlideChange={() => console.log('slide change')}
      onSwiper={(swiper) => console.log(swiper)}
    >
      <SwiperSlide>Slide 1</SwiperSlide>
      <SwiperSlide>Slide 2</SwiperSlide>
      <SwiperSlide>Slide 3</SwiperSlide>
      <SwiperSlide>Slide 4</SwiperSlide>
      ...
</Swiper>
```




## Redux
### npm install redux react-redux
## redux devtools chrome

## redux devtools extension code -> zalmoxisus


### STORE -> GLOBALIZED STATE
### ACTION -> ARTTIRMA
### REDUCER -> NE DISPATCH EDİLİRSE ONU ÇALIŞTIRIR
### REDUCER ACTIONA A GÖRE STORU MODIFY EDER

### DISPATCH -> ACTIONU EXECUTE ETTİGİMİZ YANİ ÇALIŞTIRDIGIĞIMIZ YER DISPATCH 


## İNDEX.JS linkleri yazdığımız yer
```
    
 
    
    // İMPORT
    import {createStore} from 'redux';
    import allReducers from '.reducers'; // direk tanıyor
    import {Provider} from 'react-redux';
    
        
     const store=createStore(allReducers,window.__REDUX_DEVTOOLS_EXTENSION__&& window.__REDUX_DEVTOOLS_EXTENSION__());
    
        ReactDOM.render (
            <Provider store={store}>
                <App />
            </Provider>,
        )
    

    
    
    
    // alttakiler örnek silebilirsiniz
    
    // ACTION -> ARTTIRMA
    const increment = () => {
        return {
            type: 'INCREMENT'
        }
    }
     const decrement = () => {
        return {
            type: 'DECREMENT'
        }
     }
     
     // reducer 
     const counter={state=0, action} => 
     {
        switch(action.type)
        {
            case 'INCREMENT':
                return state + 1;
            case 'DECREMENT':
                return state - 1;
        }
     }
     
     let store=createStore(counter);
     
     // Display it on the screen
     store.subscribe(()=>console.log(store.getState()));
     
     // DISPATCH
     store.dispatch(increment()); +1
     store.dispatch(decrement()); 0
     store.dispatch(decrement()); -1
     
     
     / alttakiler örnek silebilirsiniz
     
```

## Src nin Altına actions ve reducers adında 2 tane klasör ekle
## reducers içerisine index.js ekle
## reducers 'in icerisine counter.js
## reducers 'in icerisine logedReducer.js

# reducers / counter.js
```
     const counterReducer = {state = 0, action} => 
     {
        switch(action.type)
        {
            case 'INCREMENT':
                return state + 1;
            case 'DECREMENT':
                return state - 1;
             default :
                return state
        }
     };
     
     export default counterReducer;
```

# reducers / logReducer.js
```
    const loggedReducer=(state=false,action) =>
    {
        switch(action.type) 
        {
            case 'SIGN_IN':
                return !state
            default: // girmediği durum
                return state;
        }
    };
    
    export default loggedReducer;
```

# reducers / index.js
```
    import counterReducer from './counter';
    import loggedReducer from './loggedReducer';
    import {combineReducers} from 'redux';
    
    const allReducers=combineReducers(
        {
            counter : counterReducer,
            isLogged : loggedReducer,
                  
            
        }
    );
    export default allReducers;
```
## APP.JS
import {useSelector,useDispatch} from 'react-redux';
import {increment,decrement} from './actions';
```

function App() {

   const counter=useSelector(state=>state.counter);
   const dispatch=useDispatch();
   return (
        <div className="App">
        <h1>Counter {counter} </h1>
            <button onClick={()=>dispatch(increment())}>+</button>
            <button onClick={()=>dispatch(decrement())}>-</button>
        </div>
    );
}
```

## action folderin içine index.js açıyoruz
```

    export const increment = () => 
    {
        return {
            type: 'INCREMENT'
        };
    };
    
     export const decrement = () => 
    {
        return {
            type: 'DECREMENT'
        };
    };
    
```

## Güncel Route Path Kullanımı = Menü oluşturma
## npm instal react-router-dom
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
