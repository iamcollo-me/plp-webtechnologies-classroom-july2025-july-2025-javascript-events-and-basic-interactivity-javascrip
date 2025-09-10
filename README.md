
<button id="showMsgBtn">Click Me!</button>
<p id="message" style="display:none;">You clicked the button!</p>

<script>
document.getElementById('showMsgBtn').addEventListener('click', function() {
    document.getElementById('message').style.display = 'block';
});
</script><button id="toggleMode">Toggle Light/Dark</button>

<script>
document.getElementById('toggleMode').addEventListener('click', function() {
    document.body.classList.toggle('dark-mode');
});
</script>

<style>
.dark-mode {
    background: #222;
    color: #fff;
}
</style><button id="counterBtn">Count</button>
<span id="countDisplay">0</span>

<script>
let count = 0;
document.getElementById('counterBtn').addEventListener('click', function() {
    count++;
    document.getElementById('countDisplay').textContent = count;
});
</script><form id="myForm">
  <input type="text" id="name" placeholder="Name">
  <input type="email" id="email" placeholder="Email">
  <input type="password" id="password" placeholder="Password">
  <button type="submit">Submit</button>
  <div id="feedback"></div>
</form>

<script>
document.getElementById('myForm').addEventListener('submit', function(e) {
    e.preventDefault();
    let name = document.getElementById('name').value.trim();
    let email = document.getElementById('email').value.trim();
    let password = document.getElementById('password').value;
    let feedback = '';

    if (name.length < 2) {
        feedback += 'Name must be at least 2 characters long.<br>';
    }
    if (!/^\S+@\S+\.\S+$/.test(email)) {
        feedback += 'Email is invalid.<br>';
    }
    if (password.length < 6) {
        feedback += 'Password must be at least 6 characters.<br>';
    }

    document.getElementById('feedback').innerHTML = feedback || 'Success!';
});
         </script>

* Use of event listeners and appropriate event types
* Creativity and functionality of interactive elements
* Form validation accuracy and helpfulness of feedback
* Clear, modular, and well-commented JavaScript code
* A clean and functional user experience

