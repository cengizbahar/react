## Swiper Js 
### npm i swiper


```
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
        
<Route path="/navbar" exact component={Navbar}></Route>

```
