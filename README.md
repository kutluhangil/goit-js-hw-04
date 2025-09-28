<h1>📘 JavaScript Homework 4</h1>

<p>This repository contains solutions for 3 tasks focused on <strong>objects, arrays, and methods</strong> in JavaScript. Each task is implemented in a separate file (<code>task-1.js</code>, <code>task-2.js</code>, <code>task-3.js</code>).</p>

<hr>

<h2>🔹 Task 1: Product Packaging (<code>task-1.js</code>)</h2>

<p>A function that checks if all products can fit into a container with limited size.</p>

<pre><code>function isEnoughCapacity(products, containerSize) {
  const total = Object.values(products).reduce((sum, qty) =&gt; sum + qty, 0);
  return total &lt;= containerSize;
}
</code></pre>

<p>✅ <strong>Test Results</strong></p>

<pre><code>isEnoughCapacity({ apples: 2, grapes: 3, carrots: 1 }, 8); 
// true

isEnoughCapacity({ apples: 4, grapes: 6, lime: 16 }, 12); 
// false

isEnoughCapacity({ apples: 1, lime: 5, tomatos: 3 }, 14); 
// true

isEnoughCapacity({ apples: 18, potatos: 5, oranges: 2 }, 7); 
// false
</code></pre>

<hr>

<h2>🔹 Task 2: Average Calories (<code>task-2.js</code>)</h2>

<p>A function that calculates the average daily calories consumed over a week. If no data is provided, it returns 0.</p>

<pre><code>function calcAverageCalories(days) {
  if (days.length === 0) return 0;
  const total = days.reduce((sum, item) =&gt; sum + item.calories, 0);
  return total / days.length;
}
</code></pre>

<p>✅ <strong>Test Results</strong></p>

<pre><code>calcAverageCalories([
  { day: "monday", calories: 3010 },
  { day: "tuesday", calories: 3200 },
  { day: "wednesday", calories: 3120 },
  { day: "thursday", calories: 2900 },
  { day: "friday", calories: 3450 },
  { day: "saturday", calories: 3280 },
  { day: "sunday", calories: 3300 }
]);
// 3180

calcAverageCalories([
  { day: "monday", calories: 2040 },
  { day: "tuesday", calories: 2270 },
  { day: "wednesday", calories: 2420 },
  { day: "thursday", calories: 1900 },
  { day: "friday", calories: 2370 },
  { day: "saturday", calories: 2280 },
  { day: "sunday", calories: 2610 }
]);
// 2270

calcAverageCalories([]);
// 0
</code></pre>

<hr>

<h2>🔹 Task 3: Player Profile (<code>task-3.js</code>)</h2>

<p>An object representing a player profile with username, play time, and methods to update data and return formatted information.</p>

<pre><code>const profile = {
  username: "Jacob",
  playTime: 300,

  changeUsername(newName) {
    this.username = newName;
  },

  updatePlayTime(hours) {
    this.playTime += hours;
  },

  getInfo() {
    return `${this.username} has ${this.playTime} active hours!`;
  },
};
</code></pre>

<p>✅ <strong>Test Results</strong></p>

<pre><code>profile.getInfo(); 
// "Jacob has 300 active hours!"

profile.changeUsername("Marco");
profile.getInfo(); 
// "Marco has 300 active hours!"

profile.updatePlayTime(20);
profile.getInfo(); 
// "Marco has 320 active hours!"
</code></pre>

<hr>

<h2>📌 Summary & Reflection</h2>

<p>With this homework, you practiced:</p>

<ul>
  <li>Creating and updating objects</li>
  <li>Iterating over object properties</li>
  <li>Working with arrays of objects</li>
  <li>Adding and using methods inside objects</li>
  <li>Using <code>spread</code> and <code>rest</code> operators</li>
  <li>Applying <code>this</code> to access object properties</li>
</ul>

<p>These exercises strengthen your foundation in JavaScript and help you write cleaner, reusable code 🚀</p>

<hr>

<h2>📌 Overview</h2>

<ul>
  <li><strong>Task 1:</strong> Product Packaging with object values and reduce</li>
  <li><strong>Task 2:</strong> Average calories from an array of objects</li>
  <li><strong>Task 3:</strong> Player profile with methods and <code>this</code></li>
</ul>
