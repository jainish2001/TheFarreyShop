<div>
  <label for="tags">Filter content:</label>
  <select id="tags" onchange="filterContent()">
    <option value="">--Select a tag--</option>
    <option value="overview">Project Overview</option>
    <option value="features">Features</option>
    <option value="technologies">Technologies Used</option>
    <option value="howItWorks">How It Works</option>
    <option value="contributions">Contributions</option>
  </select>
</div>
<div id="content">
  <div class="section overview">
    <h2>Project Overview</h2>
    <p>*Welcome to The Farrey Shop!* This web application assists students by providing easy access to various exam resources. Key features include:</p>
    <h3>Dark Mode Toggle</h3>
    <p>A switch to toggle between light and dark themes. The user's theme preference is saved using <code>localStorage</code>, ensuring consistency across sessions.</p>
    <h3>Dynamic Button Links</h3>
    <p>Buttons link to different theory and lab exam resources. Links can be updated based on exam requirements, making it a versatile academic tool.</p>
  </div>
  <div class="section features">
    <h2>Features</h2>
    <h3>Responsive Design</h3>
    <p>The layout adapts to different screen sizes, ensuring accessibility on both desktop and mobile devices.</p>
    <h3>Smooth Transitions</h3>
    <p>Aesthetic transitions for theme changes and animations enhance the user experience.</p>
    <h3>LocalStorage Integration</h3>
    <p>The selected theme (light or dark) is remembered across sessions, providing a personalized experience.</p>
  </div>
  <div class="section technologies">
    <h2>Technologies Used</h2>
    <p>- HTML<br>- CSS<br>- JavaScript</p>
  </div>
  <div class="section howItWorks">
    <h2>How It Works</h2>
    <h3>Dark Mode Toggle</h3>
    <p>Users can switch between light and dark modes using a toggle switch. The selection is saved in the browser's <code>localStorage</code> and applied automatically on page load.</p>
    <h3>Dynamic Resources</h3>
    <p>Buttons link to various resources, including PDFs and videos. Links can be modified to suit different exams.</p>
    <h3>Cross-Window Communication</h3>
    <p>The main page and the iframe synchronize the theme to ensure a consistent appearance.</p>
  </div>
  <div class="section contributions">
    <h2>Contributions</h2>
    <p>*Feel free to contribute by suggesting new features or improvements. If you encounter any issues, please open an issue on the GitHub repository.*</p>
  </div>
</div>
<script>
  function filterContent() {
    var selectedTag = document.getElementById('tags').value;
    var sections = document.querySelectorAll('.section');
    
    sections.forEach(function(section) {
      if (selectedTag === "" || section.classList.contains(selectedTag)) {
        section.style.display = "block";
      } else {
        section.style.display = "none";
      }
    });
  }
</script>
