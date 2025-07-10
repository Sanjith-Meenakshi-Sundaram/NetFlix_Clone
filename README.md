# NetFlix_Clone
## Date:10/7/2025
## Objective:
To create a modern, responsive navigation bar using CSS Flexbox, mimicking real-world websites like Netflix. This helps reinforce alignment, spacing, and layout structuring using Flexbox properties.

## Tasks:

#### 1. Structure the HTML Layout:
Use a ```<nav>``` tag as the main container.

Add a brand logo/title on the left using a ```<div> or <h1>```.

Add navigation links like Home, Menu, About, Contact, and Login using a ```<ul> with <li> and <a>```.

#### 2. Apply Flexbox for Layout:
Use display: flex on the ```<nav>``` container.

Use justify-content: space-between to align the logo and menu.

Use align-items: center to vertically center both sections.

Style list items with horizontal spacing using gap or margin.

#### 3. Style Like a Real-World Navbar:
Add background color (e.g., dark or gradient like Netflix/Zomato).

Style text with bold fonts, hover effects, and link styling.

Remove default ul and li styles (list-style: none, text-decoration: none).

#### 4. Bonus Enhancements:
Add a hover underline or button effect on links.

Make it responsive using flex-wrap or media queries.

Fix the nav bar to top with position: sticky.
## HTML Code:
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Netflix Clone</title>
  <link rel="stylesheet" href="color.css"/>
</head>
<body>
  <nav class="navbar">
    <div class="logo">NETFLIX</div>
    <ul class="nav-links">
      <li><span>Home</span></li>
      <li><span>Movies</span></li>
      <li><span>TV Shows</span></li>
      <li><span>My List</span></li>
    </ul>
    <div class="profile">
      <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcREm3FQDjfaZ7vHq-kXdUwfbxvdT90H_7T5Iw&s" alt="Profile" />
    </div>
  </nav>
  <header class="banner">
    <div class="banner-content">
      <p class="tags">WAR | ACTION</p>
      <h1 class="title">FURY</h1>
      <p class="info">2014 | DIRECTOR : DAVID AYER </p>
      <p class="desc">The film is set in April 1945, during the final weeks of World War II's European theater. It follows a battle-hardened army sergeant (Brad Pitt) and his five-man Sherman tank crew on a mission behind enemy lines in Nazi Germany.</p>
      <div class="buttons">
        <button class="stream">WATCH NOW</button>
        <button class="episodes">ALL TO WISHLIST</button>
      </div>
    </div>
    <div class="trailer">
      <button class="play-button">▶</button>
      <p>Watch Trailer</p>
    </div>
  </header>
  <section class="popular">
    <h2>POPULAR MOVIES THIS WEEK</h2>
    <div class="shows">
      <div class="show"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQjCGjzj9HN_2zA0p7ZJzFUH4c2uYJinKiWKA&s" alt="Bruce Almighty"/><p>Bruce Almighty</p></div>
      <div class="show"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT1OBxU77lgUTf6iFs9XlYYPSInXdeTGAmksw&s" alt="Free Guy"/><p>Free Guy</p></div>
      <div class="show"><img src="https://panethos.wordpress.com/wp-content/uploads/2015/01/the-intouchables.jpg?w=584" alt="The Intouchables"/><p>The Intouchables</p></div>
      <div class="show"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRTGdXc2S_t_nY7fa8J-oPyaqxd8attaxr_jg&s" alt="Troy"/><p>Troy</p></div>
    </div>
  </section>
  <div class="age-badge">12+</div>
</body>
</html>

```
## CSS Code:
```
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body{
  font-family: Arial, sans-serif;
  background-color: #000;
  color: white;
}
.navbar{
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 40px;
  background-color: #111;
  position: sticky;
  top: 0;
  z-index: 1000;
}
.logo{
  font-size: 24px;
  font-weight: bold;
  color: red;
}
.nav-links{
  display: flex;
  gap: 30px;
  list-style: none;
}
.profile img{
  width: 30px;
  height: 30px;
  border-radius: 50%;
}
.banner{
  display: flex;
  justify-content: space-between;
  padding: 60px 40px;
  background: linear-gradient(to right, rgba(0,0,0,0.8), rgba(0,0,0,0.2)),
              url('https://m.media-amazon.com/images/S/pv-target-images/94a254e040d69d516a1497203496dc7347e72a7d81bfe763086a4e632a1bd626.jpg') no-repeat center center/cover;
  min-height: 80vh;
}
.banner-content{
  max-width: 55%;
}
.tags{
  color: gray;
  font-size: 14px;
}
.title{
  font-size: 80px;
  font-weight: bold;
}
.info{
  margin: 10px 0;
  font-size: 14px;
  color: #ccc;
}
.desc{
  font-size: 14px;
  color: #aaa;
  max-width: 500px;
}
.buttons{
  margin-top: 20px;
}
button.stream,
button.episodes{
  padding: 10px 20px;
  margin-right: 10px;
  font-weight: bold;
  border: none;
  cursor: pointer;
}
button.stream{
  background: red;
  color: white;
}
button.episodes{
  background: transparent;
  border: 1px solid white;
  color: white;
}
.trailer{
  text-align: center;
  margin-right: 200px;
  margin-top: 40px;
}
.play-button{
  font-size: 40px;
  border: none;
  background: white;
  color: black;
  border-radius: 50%;
  width: 60px;
  height: 60px;
  margin-bottom: 10px;
  cursor: pointer;
}
.popular{
  padding: 40px;
}
.popular h2{
  font-size: 20px;
  margin-bottom: 20px;
}
.shows{
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
}
.show img{
  width: 150px;
  height: 200px;
  object-fit: cover;
  border-radius: 4px;
}
.show p{
  margin-top: 5px;
  font-weight: bold;
  text-align: center;
}

.age-badge{
  position: fixed;
  bottom: 20px;
  right: 30px;
  background-color: red;
  color: white;
  padding: 6px 12px;
  font-weight: bold;
  border-radius: 4px;
}
@media screen and (max-width: 768px){
  .banner {
    flex-direction: column;
  }
  .banner-content {
    max-width: 100%;
  }
  .trailer {
    margin-top: 30px;
    margin-right: 0;
  }
  .shows {
    justify-content: center;
  }
}

```
## Output:
![image](https://github.com/user-attachments/assets/0224b003-9609-4a81-8c9b-d492a2525245)

## Result:
A modern, responsive navigation bar using CSS Flexbox, mimicking real-world websites like Netflix. This helps reinforce alignment, spacing, and layout structuring using Flexbox properties is created successfully.
