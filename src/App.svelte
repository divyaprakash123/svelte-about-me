<script>
  let name = "Divya"; // Change this to your name
  let favoriteNumber = 7; // Change this to your favorite number
  let bio =
    "I am a robotics researcher & developer 🦾  with a passion for building cool things that help people 🫂 + the environment 🌱!";
  let hobbies = [
    "Robotics 🤖",
    "Film Photography 🎞️",
    "Traveling 🚀",
    "Barista-ing 🍵",
    "Running 🏃🏽‍♀️",
    "Music 🎧",
  ]; // List some hobbies

  import ImageCard from "./lib/ImageCard.svelte";

  let cardData = [
    {
      image: "/images/robotics.JPG",
      title: "Robotics",
      description:
        "ft. min 🤖 : a clinically assistive robot! ~ I love building + developing cool robots that can help people and solve problems.",
    },
    {
      image: "/images/film.jpeg",
      title: "Film Photography",
      description:
        "📍 pacific beach, san diego ~ I love the style of film photos & have been taking film pics for almost 7 years!",
    },
    {
      image: "/images/traveling.JPG",
      title: "Traveling",
      description:
        "📍baku, azerbaijan ~ baku book center 📚 ~ I love exploring new places & learning from different cultures!",
    },
  ];
</script>

<div class="container">
  <h1>About Me 💌</h1>

  <img src="/images/me.JPG" alt="Photo of me!" class="profile-pic" />

  <p>Hello, my name is <strong>{name}</strong>!</p>
  <p>My favorite number is <strong>{favoriteNumber}</strong>.</p>
  <p>{bio}</p>

  <h2>My Hobbies💡</h2>
  <div class="hobbies">
    {#each hobbies as hobby}
      <div class="hobby">{hobby}</div>
    {/each}
  </div>

  <h2>Some of My Favorite Things 🧩</h2>
  <div class="card-container">
    {#each cardData as { image, title, description }}
      <ImageCard {image} {title} {description} />
    {/each}
  </div>
</div>

<style>
  h1 {
    color: #b0c5e4;
    font-family: Arial, sans-serif;
  }
  .container {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
    text-align: center;
  }
  .hobbies {
    display: flex;
    justify-content: center;
    gap: 15px;
    flex-wrap: wrap;
  }
  .hobby {
    background-color: #168568;
    color: white;
    padding: 10px 15px;
    border-radius: 5px;
  }
  .profile-pic {
    width: 300px;
    height: 300px;
    object-fit: cover;
    border-radius: 50%;
    margin: 20px auto;
    display: block;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  }
</style>
