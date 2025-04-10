<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>IngreGenius - Create Recipes from Your Ingredients</title>
  <style>
    body {
      font-family: 'Helvetica Neue', Arial, sans-serif;
      line-height: 1.6;
      color: #333;
      width: 100%;
      margin: 0;
      padding: 0;
    }
    
    header {
      padding: 30px 20px;
      border-bottom: 1px solid #eee;
      margin-bottom: 40px;
      display: flex;
      flex-direction: column;
      align-items: flex-start;
    }
    
    .logo {
      font-size: 32px;
      font-weight: 700;
      color: #d32f2f;
      margin-bottom: 5px;
    }
    
    .tagline {
      font-size: 18px;
      color: #666;
    }
    
    .hero {
      display: flex;
      align-items: center;
      margin-bottom: 50px;
      flex-wrap: wrap;
      padding: 0 20px;
    }
    
    .hero-text {
      flex: 1;
      padding-right: 40px;
      min-width: 280px;
    }
    
    .hero-image {
      flex: 1;
      min-width: 280px;
    }
    
    .hero-image img {
      width: 100%;
      border-radius: 4px;
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    }
    
    h1 {
      font-size: 42px;
      font-weight: 300;
      margin-bottom: 20px;
    }
    
    .cta-button {
      display: inline-block;
      background-color: #d32f2f;
      color: white;
      padding: 12px 25px;
      text-decoration: none;
      border-radius: 4px;
      font-weight: 500;
      margin-top: 20px;
      transition: background-color 0.3s;
    }
    
    .cta-button:hover {
      background-color: #b71c1c;
    }
    
    .features {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 30px;
      margin: 60px 20px;
    }
    
    .feature {
      text-align: center;
      padding: 20px;
    }
    
    .feature-icon {
      font-size: 36px;
      color: #d32f2f;
      margin-bottom: 15px;
    }
    
    .feature h3 {
      font-weight: 500;
      margin-bottom: 10px;
    }
    
    .how-it-works {
      background-color: #f9f9f9;
      padding: 50px 20px;
      margin: 60px 0;
    }
    
    .how-it-works h2 {
      text-align: center;
      margin-bottom: 40px;
    }
    
    .steps {
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
      max-width: 1200px;
      margin: 0 auto;
    }
    
    .step {
      flex: 1;
      text-align: center;
      padding: 0 20px;
      min-width: 200px;
    }
    
    .step-number {
      background-color: #d32f2f;
      color: white;
      width: 40px;
      height: 40px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 auto 15px;
      font-weight: 700;
    }
    
    section {
      margin-bottom: 60px;
      padding: 0 20px;
    }
    
    /* Recipe Finder and Results */
    #recipe-finder textarea {
      width: 100%;
      height: 100px;
      padding: 10px;
      border: 1px solid #ddd;
      border-radius: 4px;
      font-size: 16px;
    }
    
    #recipe-finder button {
      margin-top: 15px;
      background-color: #d32f2f;
      color: white;
      padding: 12px 25px;
      border: none;
      border-radius: 4px;
      font-size: 16px;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    
    #recipe-finder button:hover {
      background-color: #b71c1c;
    }
    
    #results {
      margin-top: 30px;
    }
    
    .recipe-card {
      border: 1px solid #eee;
      border-radius: 4px;
      padding: 20px;
      margin-top: 20px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    }
    
    .recipe-card h3 {
      margin: 0 0 10px;
      color: #d32f2f;
    }
    
    .recipe-card p {
      margin: 5px 0;
    }
    
    .recipe-card ol {
      margin: 10px 0 0 20px;
    }
    
    .no-results {
      color: #d32f2f;
      text-align: center;
      font-size: 18px;
      margin-top: 20px;
    }
    
    /* Popular Videos Section */
    .videos-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
      margin-top: 30px;
      max-width: 1200px;
      margin-left: auto;
      margin-right: auto;
    }
    
    .videos-grid img {
      width: 100%;
      border-radius: 4px;
    }
    
    .videos-grid h3 {
      margin-top: 10px;
    }
    
    .videos-grid a {
      color: #d32f2f;
      text-decoration: none;
    }
    
    footer {
      text-align: center;
      padding: 30px 20px;
      border-top: 1px solid #eee;
      margin-top: 60px;
      color: #666;
    }
  </style>
</head>
<body>
  <header>
    <div class="logo">IngreGenius</div>
    <div class="tagline">Transform your pantry into culinary masterpieces</div>
  </header>
  
  <section class="hero">
    <div class="hero-text">
      <h1>Discover recipes from ingredients you already have</h1>
      <p>No more wasted groceries or last-minute store runs. IngreGenius helps you create delicious meals with what's in your kitchen right now.</p>
      <a href="#recipe-finder" class="cta-button">Find Recipes Now</a>
    </div>
    <div class="hero-image">
      <img src="https://images.unsplash.com/photo-1546069901-ba9599a7e63c?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Delicious home-cooked meal">
    </div>
  </section>
  
  <section class="features">
    <div class="feature">
      <div class="feature-icon">🍳</div>
      <h3>Waste Less</h3>
      <p>Use up ingredients before they go bad and reduce food waste in your home.</p>
    </div>
    <div class="feature">
      <div class="feature-icon">⏱️</div>
      <h3>Save Time</h3>
      <p>No more searching for recipes then realizing you're missing key ingredients.</p>
    </div>
    <div class="feature">
      <div class="feature-icon">🧑‍🍳</div>
      <h3>Learn Cooking</h3>
      <p>Video tutorials guide you through each recipe step-by-step.</p>
    </div>
  </section>
  
  <section class="how-it-works">
    <h2>How IngreGenius Works</h2>
    <div class="steps">
      <div class="step">
        <div class="step-number">1</div>
        <h3>Enter Your Ingredients</h3>
        <p>List what you have in your fridge, pantry, or freezer.</p>
      </div>
      <div class="step">
        <div class="step-number">2</div>
        <h3>Get Recipe Matches</h3>
        <p>Our algorithm finds recipes you can make using any of the ingredients you provide.</p>
      </div>
      <div class="step">
        <div class="step-number">3</div>
        <h3>Cook & Enjoy</h3>
        <p>Follow our step-by-step guides and enjoy your home-cooked meal.</p>
      </div>
    </div>
  </section>
  
  <section id="recipe-finder">
    <h2>Find Recipes Now</h2>
    <p>Enter the ingredients you have on hand (separated by commas). We'll suggest recipes that use one or more of your ingredients:</p>
    <form id="recipe-form">
      <textarea id="ingredient-input" placeholder="e.g. chicken, rice, tomatoes, onion, garlic"></textarea>
      <button type="submit">Generate Recipes</button>
    </form>
    <!-- Container for recipe results -->
    <div id="results"></div>
  </section>
  
  <section>
    <h2>Popular Recipe Videos</h2>
    <div class="videos-grid">
      <div>
        <img src="https://images.unsplash.com/photo-1512621776951-a57141f2eefd?ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80" alt="Salad recipe">
        <h3>5-Ingredient Rainbow Salad</h3>
        <a href="#">Watch Video →</a>
      </div>
      <div>
        <img src="https://images.unsplash.com/photo-1490645935967-10de6ba17061?ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80" alt="Pasta recipe">
        <h3>Pantry Pasta Primavera</h3>
        <a href="#">Watch Video →</a>
      </div>
      <div>
        <img src="https://images.unsplash.com/photo-1547592180-85f173990554?ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80" alt="Stir fry recipe">
        <h3>Anything Stir Fry</h3>
        <a href="#">Watch Video →</a>
      </div>
    </div>
  </section>
  
  <footer>
    <p>© 2023 IngreGenius. All rights reserved.</p>
    <p style="margin-top: 10px;">
      <a href="#" style="color: #666; margin: 0 10px; text-decoration: none;">About</a>
      <a href="#" style="color: #666; margin: 0 10px; text-decoration: none;">Contact</a>
      <a href="#" style="color: #666; margin: 0 10px; text-decoration: none;">Privacy</a>
      <a href="#" style="color: #666; margin: 0 10px; text-decoration: none;">Terms</a>
    </p>
  </footer>
  
  <script>
    // Sample recipe data with additional new recipes
    const recipes = [
      {
        title: "Tofu Stir Fry",
        ingredients: ["tofu", "bell pepper", "garlic", "soy sauce", "ginger"],
        instructions: [
          "Cut tofu into cubes and fry until golden.",
          "Stir-fry sliced bell peppers in a hot pan.",
          "Add minced garlic and ginger; cook for another 2 minutes.",
          "Mix in tofu and drizzle with soy sauce.",
          "Serve hot with rice or noodles."
        ]
      },
      {
        title: "Fried Rice",
        ingredients: ["rice", "egg", "carrot", "peas", "soy sauce", "green onion"],
        instructions: [
          "Use day-old rice for best results.",
          "Scramble eggs in a large wok and set aside.",
          "Sauté diced carrots, peas, and chopped green onions.",
          "Mix in the rice and scrambled eggs.",
          "Season with soy sauce and stir-fry until heated through."
        ]
      },
      {
        title: "Pho",
        ingredients: ["beef", "rice noodles", "broth", "basil", "lime", "bean sprouts", "cinnamon"],
        instructions: [
          "Prepare a beef broth with cinnamon and spices.",
          "Blanch rice noodles in boiling water.",
          "Assemble a bowl with noodles, thinly sliced beef, and broth.",
          "Garnish with fresh basil, a squeeze of lime, and bean sprouts."
        ]
      },
      {
        title: "Burger",
        ingredients: ["beef patty", "bun", "lettuce", "tomato", "cheese", "onion","bread", "pickles"],
        instructions: [
          "Grill a beef patty to your desired doneness.",
          "Toast the bun lightly.",
          "Layer the patty with cheese, lettuce, tomato, onion, and pickles.",
          "Assemble your burger and serve with condiments."
        ]
      },
      {
        title: "Simple Sandwich",
        ingredients: ["bread slices", "butter", "lettuce", "tomato", "cucumber", "mayonnaise", "cheese slices"],
        instructions: [
          "Spread butter evenly on one side of each bread slice.",
          "Layer lettuce, tomato slices, cucumber slices, and cheese on one bread slice.",
          "Add a dollop of mayonnaise on top of the layered ingredients.",
          "Cover the sandwich with the second bread slice, butter side down.",
          "Cut into halves or quarters if desired, and serve."
        ]
      },
      {
        title: "Vegetable Stir-Fry",
        ingredients: ["vegetables (e.g., carrots, broccoli, bell peppers)", "oil", "soy sauce", "garlic", "onion"],
        instructions: [
          "Heat oil in a pan over medium heat.",
          "Add chopped garlic and onion, sauté until fragrant.",
          "Add your choice of chopped vegetables and stir-fry until tender but still crisp.",
          "Drizzle soy sauce on top, toss to coat evenly, and serve hot!"
        ]
      },
      {
        title: "Chicken Curry",
        ingredients: ["chicken", "curry powder", "coconut milk", "onion", "garlic", "ginger"],
        instructions: [
          "Sauté chopped onions, garlic, and ginger until fragrant.",
          "Add chicken pieces and cook until browned.",
          "Stir in curry powder and coconut milk; simmer until chicken is cooked through.",
          "Serve with rice or naan."
        ]
      },
      {
        title: "Omelette",
        ingredients: ["eggs", "milk", "cheese", "bell pepper", "onion", "salt", "pepper"],
        instructions: [
          "Whisk eggs with a splash of milk, salt, and pepper.",
          "Sauté chopped bell pepper and onion in a pan.",
          "Pour the egg mixture over the vegetables; cook until set.",
          "Sprinkle cheese on top, fold, and serve."
        ]
      },
      
      {
        title: "Vegetable Soup",
        ingredients: ["broth", "carrot", "celery", "onion", "garlic", "tomato", "potato", "salt", "pepper"],
        instructions: [
          "Sauté chopped onions, garlic, carrots, and celery until soft.",
          "Add broth, diced tomatoes, and potato cubes.",
          "Simmer until vegetables are tender.",
          "Season with salt and pepper before serving."
        ]
      },
      {
        title: "Spaghetti with Marinara Sauce",
        ingredients: ["spaghetti", "tomato", "garlic", "basil", "olive oil", "salt"],
        instructions: [
          "Cook spaghetti according to package instructions.",
          "Heat olive oil in a pan and sauté garlic until fragrant.",
          "Add crushed tomatoes and simmer; season with salt and basil.",
          "Toss the spaghetti with the marinara sauce.",
          "Serve hot with a drizzle of olive oil."
        ]
      },
      {
        title: "Fried Noodle Stir-Fry",
        ingredients: ["noodles", "soy sauce", "vegetable oil", "garlic", "vegetables"],
        instructions: [
          "Boil noodles until just tender and drain.",
          "Heat oil in a wok and stir-fry minced garlic.",
          "Add mixed vegetables and stir-fry until crisp-tender.",
          "Add the noodles and soy sauce; stir-fry until combined.",
          "Serve immediately."
        ]
      },
      {
        title: "Fresh Garden Salad",
        ingredients: ["lettuce", "tomato", "cucumber", "olive oil", "lemon", "salt"],
        instructions: [
          "Chop lettuce, tomato, and cucumber.",
          "Mix olive oil, lemon juice, and salt to make a dressing.",
          "Toss the vegetables with the dressing just before serving.",
          "Serve fresh and enjoy a light, crisp salad."
        ]
      }
    ];
    
    // Listen for form submission
    document.getElementById("recipe-form").addEventListener("submit", function(e) {
      e.preventDefault();
      findRecipes();
    });
    
    function findRecipes() {
      const input = document.getElementById("ingredient-input").value;
      const resultsDiv = document.getElementById("results");
      resultsDiv.innerHTML = '';  // Clear previous results
      
      if (!input.trim()) {
        resultsDiv.innerHTML = '<p class="no-results">Please enter at least one ingredient.</p>';
        return;
      }
      
      // Split input by commas, trim whitespace, and convert to lowercase for matching
      const userIngredients = input.split(',')
                                   .map(item => item.trim().toLowerCase())
                                   .filter(item => item);
      
      // Suggest recipes if one or more ingredient matches
      const matchingRecipes = recipes.filter(recipe => {
        return recipe.ingredients.some(ing => {
          return userIngredients.some(ui => ing.toLowerCase().includes(ui));
        });
      });
      
      if (matchingRecipes.length === 0) {
        resultsDiv.innerHTML = '<p class="no-results">No recipes found. Try adding more ingredients.</p>';
        return;
      }
      
      // Display each matching recipe with a summary of matched vs. remaining ingredients
      matchingRecipes.forEach(recipe => {
        // Determine which ingredients the user provided (matches) and which are needed
        const provided = recipe.ingredients.filter(ing => {
          return userIngredients.some(ui => ing.toLowerCase().includes(ui));
        });
        const additional = recipe.ingredients.filter(ing => {
          return !userIngredients.some(ui => ing.toLowerCase().includes(ui));
        });
        
        const recipeHTML = `
          <div class="recipe-card">
            <h3>${recipe.title}</h3>
            <p><strong>You provided:</strong> ${provided.join(", ")}</p>
            <p><strong>Also needed:</strong> ${additional.join(", ")}</p>
            <ol>
              ${recipe.instructions.map(step => `<li>${step}</li>`).join("")}
            </ol>
          </div>
        `;
        resultsDiv.innerHTML += recipeHTML;
      });
    }
  </script>
</body>
</html>
