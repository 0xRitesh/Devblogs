![Frame 36.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1629299293701/BLnQqiX69.png)
## My Journey Of Building pascaline 🧮
### Hi Everyone 👋, hope you all are doing well. 🚀 

In this article, I'll tell you how the notion of pascaline came to me.

Last week, I took part in the week-long  IBD WFH tool building challenge hosted by crio.do.
In this challenge, We were instructed to build useful open-source apps or extensions that would help us work more efficiently and increase productivity.

So I began thinking about what I could build and decided to work on an issue I found a few days ago.

# Problem

a while ago while filling out a form and had to answer some questions about my budget, so I think of quickly installed an extension to help me out. As soon as I opened the chrome store and explored some extensions, I found that all of them had a really unpleasant UI, they were working perfectly fine but the experience I found was not that pleasant. After that, I looked into some articles on how to build an extension and found the  [Chrome documentation](https://developer.chrome.com/docs/extensions/) &  [this article ](https://www.freecodecamp.org/news/how-to-implement-a-chrome-extension-3802d63b5376/) to be really informative and useful.

So I decided to build a new one because we all know from personal experience that a good User Interface is important in the sense that it allows everyone to clearly see and use the products. also, It was an excellent opportunity for me to implement the stack that I've recently learned.
 > “Good design is like a refrigerator—when it works, no one notices, but when it doesn’t, it sure stinks.” –Irene Au

# Design 
I've been going deeper into the world of UI/UX for a few months now, and I'm loving the procss.
Now, I started with a sketch.

![Frame 38.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1628051986433/qKKbLBcQ0.png)

After that, I began creating the Design in FIGMA,
screenshot of my untidy artboard
![image 26.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1627905202902/65k6OXC_pd.png)

# Development 
Basically, Extensions are software programs, built on web technologies that enable users to customize the browsing experience.
First, let's talk about the <br>
**Tech Stack I used**
- HTML
- CSS
- JavaScript

**Library I used**
- [math.js](https://mathjs.org/)

Now, ** Phases of Development**

1. Extension Interface
2. Manifest File
3. Testing

I will explain each phase of development with relevant screenshots and code for better understanding.

### 1. Extension Interface
To build the extension interface, we should have a fundamental knowledge of HTML, CSS, and JavaScript. HTML (index.html) is used to build the skeleton body of our extension and we style the components and button using CSS (style.css). We use JavaScript (script.js) to giving it life, i.e, make it work to solve the equations. 

So let’s dive into the first Part: The structure and design of our calculator.
In the HTML skeleton Inside Body, I’m defining a new div with a class named “button”. 

```
<div class="button"> </div>
``` 
I place one more div, inside this div and there will be text that our button should hold is placed between these two tags. Along with the tag, I’ll be giving them an id. This id will help at the time of back-end programming. See example below

```
<div class="button">
<div class="inner-button">
0
</div>
</div>
``` 
&, I’ve coded the same div approx 20 times to make the basic structure of the calculator.
You can find the whole HTML code below

<iframe width="100%" height="300" src="//jsfiddle.net/Wordssaysalot/k3hceavx/embedded/html/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>
<hr>
Let’s jump to the CSS section. 

I primarily worked on these properties in order to make the calculator look nice.
<br>
- background-color<br>
- Padding<br>
- Width<br>
- Text alignment<br>
- Font size<br>
- BORDER RADIUS<br>
- Box- Shadow<br>
<br>
complete CSS code for this:
<iframe width="100%" height="300" src="//jsfiddle.net/Wordssaysalot/k3hceavx/3/embedded/css/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>
<hr>
Now, We will be coming to the javascript part <br>
Until now the calculator is lifeless. We have to give it life.
So let’s dive into the backend section and make the calculator solve our problems.
Now we have to define a function, that can perform different tasks and for the calculation part I used  Math.js i.e an extensive math library for JavaScript, It features real and complex numbers, units, matrices, a large set of mathematical functions, and a flexible expression parser.<br>
Below is the complete script.js :

<iframe width="100%" height="300" src="//jsfiddle.net/Wordssaysalot/k3hceavx/5/embedded/js/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>
<hr>

2. Manifest File
<br>

We have now reached the second phase in our extension development and it involves creating a manifest.json file. The manifest.json file is the only file that every extension using WebExtension APIs must contain. Using manifest.json, we specify basic metadata about your extension such as the name and version, and can also specify aspects of your extension's functionality (such as background scripts, content scripts, and browser actions). We also add icons to our extension and test them in the browser to connect everything.<br>
<br>
We set our extension name in the name attribute. We define a version number and type out a description which the users can see after loading the extension. We set our background script in place. We use a 128px icon and a default icon to be displayed on the extension bar, both designed in Figma. Whenever the user opens a new tab we want our extension page to be loaded there. This is possible because of chrome_url_overrides which overrides the default new tab layout and loads our extension home index.html. We lastly add manifest version and security policies.<br>
Below is the complete manifest.json code:
<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C184%2C195%2C0%29&t=one-dark&wt=none&l=auto&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=true&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=14px&lh=133%25&si=false&es=2x&wm=false&code=%257B%250A%2520%2520%2520%2520%2522name%2522%253A%2520%2522Pascaline%2522%252C%250A%2520%2520%2520%2520%2522version%2522%253A%2520%25221.0%2522%252C%250A%2520%2520%2520%2520%2522manifest_version%2522%253A%25202%252C%250A%2520%2520%2520%2520%2522description%2522%253A%2520%2522a%2520simple%2520calculator%2520for%2520all%2520your%2520need.%2522%252C%250A%2520%2520%2520%2520%2522content_scripts%2522%253A%2520%255B%257B%250A%2520%2520%2520%2520%2520%2520%2520%2520%2522matches%2522%253A%2520%255B%2522https%253A%252F%252F*%252F*%2522%255D%252C%250A%2520%2520%2520%2520%2520%2520%2520%2520%2522js%2522%253A%2520%255B%2522popup%252Fmath.js%2522%255D%252C%250A%2520%2520%2520%2520%2520%2520%2520%2520%2522css%2522%253A%2520%255B%2522popup%252Fstyle.css%2522%255D%250A%2520%2520%2520%2520%257D%255D%252C%250A%2520%2520%2520%2520%2522icons%2522%253A%2520%257B%250A%2520%2520%2520%2520%2520%2520%2520%2520%252248%2522%253A%2520%2522logo.png%2522%250A%2520%2520%2520%2520%257D%252C%250A%2520%2520%2520%2520%2522permissions%2522%253A%2520%255B%2522activeTab%2522%255D%252C%250A%2520%2520%2520%2520%2522browser_action%2522%253A%2520%257B%250A%2520%2520%2520%2520%2520%2520%2520%2520%2522default_popup%2522%253A%2520%2522popup%252Findex.html%2522%252C%250A%2520%2520%2520%2520%2520%2520%2520%2520%2522default_title%2522%253A%2520%2522calculator%2522%252C%250A%2520%2520%2520%2520%2520%2520%2520%2520%2522default_icon%2522%253A%2520%2522logo.png%2522%250A%2520%2520%2520%2520%257D%250A%2520%2520%250A%257D"
  style="width: 656px; height: 563px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

### 3. Testing 

Loading and Testing the extension 
1. We open the Chrome web browser. On the top right corner customize button is represented by three vertical dots. Go to **More tools -> Extensions**.

2. **Enable Developer Mode** on the top left after opening the Extensions page. Then Click on Load unpacked and select the parent directory of the built extension.

![1.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1628009741532/rnsKldviD.png)
> Fact: While loading an unpacked extension, Chrome always looks for the manifest.json file and loads the extension using that file as a parent. Know we know the importance of manifest.json.


  <br> 3.  Once loaded, on the extension page, we can see our extension with the icon and description as below. Click on Details.

![2.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1628009754217/zAsVohw2_.png)

<br> 4. Here, we can see each and every detail about our extension which we put in our manifest.json file and the directory from which it was loaded.


![Frame 37.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1628009791902/kILPZGi9F.png)
<br> 5. Enable the extension and open a new tab. Voila! You should be able to see the extension up and running.

![image 9.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1628009807607/gqkppIiWp.png)
You can now see the Pascaline logo in the browser's extension bar on the top right, from which you can also launch the extension.


This brings us to the end of our development, and it was a great learning experience for me because I had never built an extension before.

> Feel free to star ⭐️ the project if you found it useful -
https://github.com/wordssaysalot/Pascaline 

## Thanks for reading!
Let me know your thoughts and feedback in the comments section.
