<template>
  <div>
    <aside id="mySidenav" class="sidenav">
      <ul>
        <li className="active-top">
          <a @click="scroll('home')" class="site-title" className="active"><span class="material-icons md-48">
              home
            </span></a>
        </li>
        <li className="active">
          <a @click="scroll('about')"><span class="material-icons md-48">
              portrait
            </span></a>
        </li>
        <li className="active">
          <a @click="scroll('projects')"><span class="material-icons md-48">
              engineering
            </span></a>
        </li>
        <li className="active-bottom">
          <a @click="scroll('contact')"><span class="material-icons md-48">
              connect_without_contact
            </span></a>
        </li>
      </ul>
    </aside>
  </div>
</template>

<script>
export default {
  name: 'navBar',
  data: () => ({
    buttonText: <span class="material-icons md-48">portrait</span>
  }),
  methods: {
    scroll(toSection) {
      const element = document.getElementById(toSection);
      element.scrollIntoView({ behavior: 'smooth' });
    }
  }
}
</script>

<style>
.sidenav {
  background-color: #333;
  color: white;
  display: flex;
  flex-direction: column;
  margin: 1rem;
  align-items: stretch;
  gap: 2rem;
  padding: 0 1rem;
  position: fixed;
  transition: top 0.3s;
  top: 100px;
  padding: 10px;
  border-radius: 3rem;
  animation: animatetop 3s;
}

@keyframes animatetop {
  from {
    top: -50px;
    opacity: 0
  }

  to {
    top: 100px;
    opacity: 1
  }
}

.site-title {
  font-size: 2rem;
}

.sidenav ul {
  padding: 0;
  margin: 0;
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.sidenav a {
  color: inherit;
  text-decoration: none;
  height: 100%;
  display: block;
  align-items: center;
  padding: .25rem;
}

.sidenav li.active {
  background-color: #555;
}

.sidenav li.active-top {
  background-color: #555;
  border-top-left-radius: 1.5rem;
  border-top-right-radius: 1.5rem;
}

.sidenav li.active-bottom {
  background-color: #555;
  border-bottom-left-radius: 1.5rem;
  border-bottom-right-radius: 1.5rem;
}

.sidenav li:hover {
  background-color: #777;
}
</style>