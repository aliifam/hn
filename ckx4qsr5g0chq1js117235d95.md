## How I add animate in Hashnode mobile sidebar

What made me really like and decided to migrate to Hashnode is that it has a lot of free features including customizing CSS.

But to get the custom CSS feature you have to be a Hashnode Ambassador read more [here](https://hashnode.com/ambassador) 

Because I'm already a Hasnode Ambassador then I have the feature okay go to the main topic I will give a tutorial on how to make your Hashnode blog mobile menu better by adding CSS animation effects.

## Mobile Menu Transition

%[https://www.loom.com/share/8957c7525c0f47509292ca8d0336b9ff]

How to add a mobile Hashnode menu transition, first you open your blog dashboard then go to the appearance menu then scroll down to activate the custom CSS feature then you enter the CSS edit menu.

Then you enter the CSS script below:


```css
.css-16u0epz {
    animation-duration: 0.3s;
    animation-fill-mode: both;
    animation-name: fadeInLeft;
}

@-webkit-keyframes fadeInLeft {
  0% {
    opacity: 0;
    -webkit-transform: translateX(-20px);
  }
  100% {
    opacity: 1;
    -webkit-transform: translateX(0);
  }
}

@keyframes fadeInLeft {
  0% {
    opacity: 0;
    transform: translateX(-20px);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}
``` 

After that press save styles and publish then look at the changes this is indeed simple but I think it makes it better, when opening the mobile menu there is an animation but I don't know how to add animation when closing the menu, because when I inspect the element it looks like the code from Hashnode closes mobile menu by removing the elements directly without adding the class so I don't know how to do it yet, maybe you know you can give suggestions in the comments column.

## Search Bar Transition

%[https://www.loom.com/share/dbfb1da84726403fa68b76907aa66966]

in addition to making mobile menu transition animations I also create search bar transition animations, this is indeed very simple but I really like this little interaction.

You can add the CSS syntax below to create a search bar transition :

```css
.css-10or7o {
    animation-duration: 0.3s;
    animation-fill-mode: both;
    animation-name: fadeInDown;
}

@-webkit-keyframes fadeInDown {
  0% {
    opacity: 0;
    -webkit-transform: translateY(-20px);
  }
  100% {
    opacity: 1;
    -webkit-transform: translateY(0);
  }
}

@keyframes fadeInDown {
  0% {
    opacity: 0;
    transform: translateY(-20px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}
``` 
Do you see the difference?

You can customize as you like with custom CSS features including animations and transitions.

## Smooth Scrolling

%[https://www.loom.com/share/69ca5a7d53ba428d9eac7a5ae6fb1eee]

As a bonus I also added a smooth scrolling effect to make it more interactive, here's the script I added to create a smooth scrolling effect :

```css
html {
  scroll-behavior: smooth;
}
``` 
Those are some simple CSS effects that I added in my Hashnode blog, hopefully it can be useful for you too, thank you for reading my article if you have any questions, or suggestions I am very open to that, please use the comments column.