<script setup>
    import { reactive, ref } from 'vue';
    let initial_count= reactive({count : 0, name: 'Counter'});
    const increment = () => {
        initial_count.count++;
    }
    const decrement = () => {
        initial_count.count--;
    }
    const reset = () => {
        initial_count.count = 0;
    }
    let gifs = reactive({current_gif:"https://media.giphy.com/media/xT1Ra3zOOeo8kKSaBO/giphy.gif" , bool:true})
    const gif_link=["https://media.giphy.com/media/xT1Ra3zOOeo8kKSaBO/giphy.gif",
    "https://media.giphy.com/media/tZqOHiclM4N8kIxV7H/giphy.gif",
    ];
    const toggle = () =>{
        gifs.bool = !gifs.bool;
        if(gifs.bool === true){
            gifs.current_gif=gif_link[0];
            console.log("GIF 1");
        } else if(gifs.bool === false) {
            gifs.current_gif=gif_link[1];
            console.log("GIF 2");
        }
    }

    let fizzbuzz_gif = reactive({current_fizzbuzz_gif:"", number:1, msg:"CLick button to display message"});
    const fizzbuzz_links = [
        "https://media.giphy.com/media/3o6nUZoNVfceusBKZG/giphy.gif",
        "https://media.giphy.com/media/v1.Y2lkPWVjZjA1ZTQ3ZTJkbnp6aXEzMzA2Y2ZqNzR2anFzNHRleHpsYTdsOXBoOHM5OHd1ayZlcD12MV9naWZzX3JlbGF0ZWQmY3Q9Zw/3o6nUWPZqiuSRhvuY8/giphy.gif",
        "https://media.giphy.com/media/xT1R9D0QaX7Mp9qLxC/giphy.gif",
        "https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExcGxxN2lpZTBsejZ5bzVndGZ5bzIzbWZlN2JnY3NpMW9sMnBlMmhsYSZlcD12MV9naWZzX3NlYXJjaCZjdD1n/PnIpBoEJl7aaoBDxHt/giphy.gif"
    ];
    const messages = {
        msg1:"Fizz because divisible by 3 (wait a sec for gif to load)",
        msg2:"Buzz because divisible by 5 (wait a sec for gif to load)",
        msg3:"FizzBuzz because divisible by both 3 and 5 (wait a sec for gif to load)",
        msg4:"float in void cuz the number is neither divisible by 3 or 5"
    }
    const fizz_buzz_function = () => {
        fizzbuzz_gif.number++;
        if(fizzbuzz_gif.number % 3 === 0 && fizzbuzz_gif.number % 5 === 0){
            fizzbuzz_gif.current_fizzbuzz_gif = fizzbuzz_links[2];
            fizzbuzz_gif.msg = messages.msg3;
        }
        else if (fizzbuzz_gif.number % 5 === 0){
            fizzbuzz_gif.current_fizzbuzz_gif = fizzbuzz_links[1];
            fizzbuzz_gif.msg = messages.msg2;
        }
        else if (fizzbuzz_gif.number % 3 === 0 ){
            fizzbuzz_gif.current_fizzbuzz_gif = fizzbuzz_links[0];
            fizzbuzz_gif.msg = messages.msg1;
        }
        else {
            fizzbuzz_gif.current_fizzbuzz_gif = fizzbuzz_links[3];
            fizzbuzz_gif.msg = messages.msg4;
        }
    }
</script>

<template>
    <p>Using the Reactive() Function</p>
    <p>Count: {{ initial_count.count }}</p>
    <button @click="increment">Increment Count</button>
    <button @click="decrement">Decrement</button>
    <button @click="reset">Reset</button>
    <p>Watch Post Malone GIFs</p>
    <img :src="gifs.current_gif"/>
    <button @click="toggle">Toggle GIFS</button>
    <p>Fizz Buzz Program using Post Malone GIFS</p>
    <img :src="fizzbuzz_gif.current_fizzbuzz_gif" class="fb_gif" alt=""/>
    <h3>Current Number is : {{ fizzbuzz_gif.number }}</h3>
    <h4>Your message is : {{fizzbuzz_gif.msg}}</h4>
    <button @click="fizz_buzz_function">Toggle GIFS</button>
</template>

<style scoped>  
    .fb_gif{
        width:480px;
        height:270px;
        border-style: solid;
        border-color: black;
    }
</style>