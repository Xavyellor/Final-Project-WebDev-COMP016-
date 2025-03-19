
# Cascading Style Sheet Group : Group collaboration (part 2)




![HTML](https://img.shields.io/badge/HTML5-%23E34F26.svg?&style=for-the-badge&logo=html5&logoColor=white)  

Pylon Esports is the official esports organization of the Polytechnic University of the Philippines (PUP). They represent PUP in various esports competitions, including:

- 🎯 **Valorant**  
- 📱 **Mobile Legends: Bang Bang (MLBB)**  
- 🏹 **League of Legends (LoL)**  

## ❓ Problem

From the previous group collaboration modify
your output and apply CSS selectors that
discuss a while ago.

## ✅ Answer
Through the second part of the collaboration, we modified our file to make all the css within our app external so we can easily identify the different types of selector used within our files. Here is the examples of the selectors we used in our application:

1. Universal Selector (*)
    "home.css"
    * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    }
2. Type/Element Selector (p,h1,etc.)
    "home.css"
    body {
    font-family: Arial, sans-serif;
    background-color: #000; /* Black background */
    color: #fff; /* White text */
    }
3. Class Selector (.)
    "league.css"
    .container {
    display: flex;
    align-items: center;
    gap: 40px;
    max-width: 1500px;
    margin: 0 auto;
    position: relative;
    z-index: 1;
    }  
4. ID Selector (#)
    "mlbb.css"
    #team-image {
    height: 100%;
    width: auto;
    position: fixed;
    margin-left: 50px;
    }
5. Descendant Combinator Selector (ex. article p{})
    "valorant.css"
    .title-section h1 {
    color: #FFFFFF;
    text-shadow: 0 0 10px #6b62f3;
    margin: 0;
    line-height: 1;
    }
6. Pseudo-class Selector(ex. p::hover)
    "home.css"
    .navbar li a:hover {
    color: #ff0000; /* Red text on hover */
    }
7. Pseudo-elements Selector (ex. a::before)
    "home.css"
    .hero::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5); /* Dark overlay for better text contrast */
    z-index: 1;
    }









## 👷👷‍♀️ Collaborators


| Name | Role |
|------|------|
| **Alano, Ruzel Luigi** | 🎨 UI Design |
| **Hinay, Anthony John C.** | 📲 MLBB Page |
| **Llesis, Earl Gem** | ⚔️ League of Legends Page |
| **Rolle, Xavier B.** | 🏠 Home Page |
| **Quijano, Katherine P.** | 🎯 Valorant Page |