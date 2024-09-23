<script>
  let freeHours = 0
  let profile = {
    name: "Elton",
    avatar: "https://github.com/eltonsantos.png"
  }
  let statusCount = {
    total: 2,
    progress: 1,
    done: 3
  }
</script>

<header class="page-header">
  <div class="container">
    <section id="top" class="animate-up">
      <h2 class="sr-only">Homepage</h2>
      <img id="logo" src="/images/logo.svg" alt="Logo" />
      <span id="notification">
        <img src="/images/alert-octagon.svg" alt="Alerta" />

        {#if freeHours <= 0 }
          Você não tem horas livres
        {:else}
          Você tem {freeHours} horas livres no seu dia
        {/if}
     
      </span>
      <a href="/profile" id="avatar-profile">
        <p>{profile.name} <span>Ver perfil</span></p>
        <img src="{profile.avatar}" alt="{profile.name}" />
      </a>
    </section>

    <div class="separator"></div>

    <section id="summary" class="animate-up delay-1">
      <h2 class="sr-only">Sumário</h2>

      <div class="info">
        <div class="total">
          <strong>{statusCount.total}</strong>
          Projetos ao total
        </div>
        <div class="in-progress">
          <strong>{statusCount.progress}</strong>
          Em andamento
        </div>
        <div class="finished">
          <strong>{statusCount.done}</strong>
          Encerrados
        </div>
      </div>
      <a class="button orange" href="/job">
        <span>
          <img src="/images/plus-24.svg" alt="Novo Job" />
        </span>
        Adicionar novo job
      </a>
    </section>
  </div>
</header>