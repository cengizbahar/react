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

## Route Path
### npm install react-router-dom

```
<a className="aasd" href="/footer">Footer</a>
        
<Route exact path="/navbar" component={Navbar}></Route>

```


## Redux
### npm install redux react-redux


### STORE -> GLOBALIZED STATE
### ACTION -> ARTTIRMA
### REDUCER -> NE DISPATCH EDİLİRSE ONU ÇALIŞTIRIR
### REDUCER ACTIONA A GÖRE STORU MODIFY EDER

### DISPATCH -> ACTIONU EXECUTE ETTİGİMİZ YANİ ÇALIŞTIRDIGIĞIMIZ YER DISPATCH 


## İNDEX.JS
```
    import {createStore} from 'redux';


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
     
```
