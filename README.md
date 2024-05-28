## Hi there! My name is Rohan Sah
## About Me
## I go to school @ Iowa State University for computer science and applied mathematics. 
fetch('profile.json')
  .then(response => response.json())
  .then(data => {
    console.log(data);
    document.getElementById('name').textContent = data.name;
    document.getElementById('profession').textContent = data.profession;
    document.getElementById('learningFocus').textContent = data.learningFocus;
    document.getElementById('email').href = mailto:${data.contact.email};
    document.getElementById('linkedin').href = data.contact.linkedin;
    document.getElementById('twitter').href = data.contact.twitter;

    // Display projects
    const projectsList = document.getElementById('projects');
    data.projects.forEach(project => {
      const listItem = document.createElement('li');
      listItem.innerHTML = `<strong>${project.name}</strong>: ${project.description}`;
      projectsList.appendChild(listItem);
    });

    // Display technologies
    document.getElementById('languages').textContent = data.technologies.languages.join(', ');
    document.getElementById('frameworks').textContent = data.technologies.frameworks.join(', ');
    document.getElementById('tools').textContent = data.technologies.tools.join(', ');
 

<!--
**exploratoryprorammer/exploratoryprorammer** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
