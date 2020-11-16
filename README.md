# Code 

```js
function getArr(...arg){
    return arg.map(element => element+element);
} 

```   

```js 
/* 
Object + data
*/  

const posts = [

    {
        id: 1,
        author: 'Binatik',
        text: 'This id will not show the function, because the property is an empty string.',
        photos: '',
    },

    {
        id: 2,
        author: 'Binatik',
        test: 'This id will be shown by the function.',
        photos: '/url/photos',
    },

]

function getPosts(arr){
    return arr.filter(({ photos }) => (photos.length !== 0));
}

getPosts(posts);

```     

```js 
/* 
Class
*/ 
 
class Popup {
    constructor(popup) {
        this.popup = popup;
        this.popup.addEventListener('click', (event) => this.modalClose(event));
    }

    modalOpen(){
        this.popup.classList.add('modal-open');
    };

    modalClose(e){
        const target = e.target;
        if (target.classList.contains('modal')){
            target.classList.remove('modal-open');
        }

        if (target.classList.contains('btn-close')){
            this.popup.classList.remove('modal-open');
        }
    };
}
```   
```js  
/* 
React + next
*/ 

import Link from "next/link";
import React from "react";

const list =[
    {
        id: 1,
        title: 'Home',
        url: '/',
    },

    {
        id: 2,
        title: 'Skills',
        url: '/skills',
    },

    {
        id: 3,
        title: 'Portfolio',
        url: '/portfolio',
    },
];


export function Navigation() {
    return (
        <React.Fragment>
            <nav>
                {list.map(({url, title, id}) =>
                    <Link href={url} key={id}>
                        <a>{title}</a>
                    </Link>)
                }
            </nav>
        </React.Fragment>
    )
}
```   
