```html
<!-- ========================= -->
<!-- PROJECTS SECTION -->
<!-- ========================= -->

<section class="projects" id="projects">

  <div class="section-title">
    <h2>FEATURED PROJECTS</h2>
    <p>
      Explore cinematic gameplay worlds, immersive storytelling,
      and Unreal Engine 5 experiences crafted with passion.
    </p>
  </div>

  <div class="projects-grid">

    <!-- PROJECT 1 -->
    <a href="maze-runner.html" class="project-link">

      <div class="project-card magic-card">

        <div class="project-image">
          <img src="images/maze-runner.jpg" alt="Maze Runner">

          <div class="image-overlay">
            <span>ENTER PROJECT</span>
          </div>

        </div>

        <div class="project-content">

          <div class="tag">ACTION / PUZZLE</div>

          <h3>MAZE RUNNER</h3>

          <p>
            A high-intensity survival puzzle game focused on dynamic environments,
            procedural pathways, and immersive tension mechanics.
          </p>

          <div class="tech-stack">
            <span>UE5</span>
            <span>AI Logic</span>
            <span>Blueprints</span>
            <span>Puzzle Design</span>
          </div>

        </div>

      </div>

    </a>


    <!-- PROJECT 2 -->
    <a href="reddock.html" class="project-link">

      <div class="project-card magic-card">

        <div class="project-image">

          <video autoplay muted loop playsinline>
            <source src="videos/reddock.mp4" type="video/mp4">
          </video>

          <div class="image-overlay">
            <span>WATCH PROJECT</span>
          </div>

        </div>

        <div class="project-content">

          <div class="tag">TPS / CINEMATIC ACTION</div>

          <h3>RED DOCK</h3>

          <p>
            A cinematic third-person shooter where the player infiltrates
            an enemy-controlled port to rescue a hostage and survive brutal combat.
          </p>

          <div class="tech-stack">
            <span>TPS Combat</span>
            <span>UE5</span>
            <span>Cinematics</span>
            <span>Animation Blend</span>
          </div>

        </div>

      </div>

    </a>


    <!-- PROJECT 3 -->
    <a href="lava-land.html" class="project-link">

      <div class="project-card magic-card lava-card">

        <div class="project-image">
          <img src="images/lava-land.jpg" alt="The Lava Land">

          <div class="image-overlay">
            <span>EXPLORE WORLD</span>
          </div>

        </div>

        <div class="project-content">

          <div class="tag">DARK CINEMATIC WORLD</div>

          <h3>THE LAVA LAND</h3>

          <p>
            A narrative-driven volcanic world where environmental storytelling,
            destruction, and lighting create the feeling of a fallen civilization.
          </p>

          <div class="tech-stack">
            <span>World Building</span>
            <span>Lighting</span>
            <span>Environment Art</span>
            <span>Storytelling</span>
          </div>

        </div>

      </div>

    </a>

  </div>
</section>

<!-- ========================= -->
<!-- SUPER ANIMATION CSS -->
<!-- ========================= -->

<style>

.project-link{
  text-decoration:none;
  color:white;
}

/* MAGIC CARD */

.magic-card{
  position:relative;
  overflow:hidden;
  transition:0.6s ease;
}

.magic-card::before{
  content:'';
  position:absolute;
  width:300px;
  height:300px;
  background:radial-gradient(circle,
  rgba(212,175,55,0.25),
  transparent 70%);
  top:-150px;
  right:-150px;
  transition:0.6s ease;
  pointer-events:none;
}

.magic-card:hover::before{
  transform:scale(1.5);
}

/* HOVER EFFECT */

.magic-card:hover{
  transform:
  perspective(1200px)
  rotateX(5deg)
  rotateY(-5deg)
  translateY(-15px)
  scale(1.02);

  box-shadow:
  0 0 30px rgba(212,175,55,0.2),
  0 0 60px rgba(255,120,0,0.15),
  0 30px 60px rgba(0,0,0,0.6);
}

/* IMAGE */

.project-image{
  position:relative;
  overflow:hidden;
}

.project-image img,
.project-image video{
  width:100%;
  height:100%;
  object-fit:cover;
  transition:1s ease;
}

.magic-card:hover img,
.magic-card:hover video{
  transform:scale(1.1);
  filter:brightness(1.15);
}

/* OVERLAY */

.image-overlay{
  position:absolute;
  inset:0;
  background:linear-gradient(
  to top,
  rgba(0,0,0,0.9),
  rgba(0,0,0,0.1)
  );

  display:flex;
  justify-content:center;
  align-items:center;

  opacity:0;
  transition:0.5s ease;
}

.magic-card:hover .image-overlay{
  opacity:1;
}

.image-overlay span{
  color:#fff;
  border:1px solid #d4af37;
  padding:14px 26px;
  border-radius:40px;
  letter-spacing:3px;
  font-size:0.8rem;
  backdrop-filter:blur(10px);
  background:rgba(255,255,255,0.05);
  transform:translateY(20px);
  transition:0.5s ease;
}

.magic-card:hover .image-overlay span{
  transform:translateY(0);
}

/* LAVA EFFECT */

.lava-card::after{
  content:'';
  position:absolute;
  inset:0;

  background:
  linear-gradient(
  45deg,
  transparent,
  rgba(255,80,0,0.05),
  transparent
  );

  animation:lavaFlow 6s linear infinite;
  pointer-events:none;
}

@keyframes lavaFlow{

  0%{
    transform:translateX(-100%);
  }

  100%{
    transform:translateX(100%);
  }
}

/* FLOAT ANIMATION */

.project-card{
  animation:floatCard 5s ease-in-out infinite;
}

@keyframes floatCard{

  0%,100%{
    transform:translateY(0px);
  }

  50%{
    transform:translateY(-6px);
  }
}

/* GLOW EFFECT */

.project-content h3{
  transition:0.5s;
}

.magic-card:hover h3{
  color:#f5d97a;
  text-shadow:
  0 0 10px rgba(212,175,55,0.5),
  0 0 20px rgba(212,175,55,0.3);
}

/* TECH STACK */

.tech-stack span{
  transition:0.4s;
}

.tech-stack span:hover{
  background:#d4af37;
  color:black;
  transform:translateY(-4px);
}

/* MOBILE */

@media(max-width:768px){

  .magic-card:hover{
    transform:none;
  }

}

</style>

<!-- ========================= -->
<!-- REVEAL ANIMATION SCRIPT -->
<!-- ========================= -->

<script>

const observer = new IntersectionObserver((entries)=>{

  entries.forEach((entry)=>{

    if(entry.isIntersecting){

      entry.target.classList.add('visible');

    }

  });

},{
  threshold:0.2
});

document.querySelectorAll('.project-card').forEach((card)=>{

  observer.observe(card);

});


/* MOUSE GLOW EFFECT */

document.querySelectorAll('.magic-card').forEach(card=>{

  card.addEventListener('mousemove',(e)=>{

    const rect = card.getBoundingClientRect();

    const x = e.clientX - rect.left;
    const y = e.clientY - rect.top;

    card.style.background = `
    radial-gradient(
    circle at ${x}px ${y}px,
    rgba(212,175,55,0.12),
    rgba(20,20,20,0.9) 40%
    )`;

  });

});


</script>
```
