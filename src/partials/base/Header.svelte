<script>
  import Icon from '@iconify/svelte';
  import Menu from "../../content/menu.json"

  let isMobile = false;
  let isSubMenu;

  const subMenu = (key) => {
    if (isSubMenu === key) {
      isSubMenu = !isSubMenu
    } else {
      isSubMenu = key
    }
  }

</script>

<header class="header">
  <div class="wrapper py-6">
    <div class="flex just-b g-4">
      <div class="flex lg:none item-c">
        <button class="flex item-c" on:click={() => (isMobile = !isMobile)}>
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="30" height="30" stroke="currentColor" stroke-linecap="round" stroke-width="1.5" stroke-linejoin="round">
            <path d="M4 6h16M4 12h16M4 18h16" />
          </svg>
        </button>
      </div>
      <div class="logo flex item-c">
        <a href="/">Hostinger</a>
      </div>
      <div class="menu flex item-c flex-1 {isMobile ? 'active' : ''}">
        <ul>
          {#each Menu as item}
          <li on:click={() => subMenu(item.id)}>
            <button>
              <span>{item.name}</span>
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="20" height="20" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <polyline points="6 9 12 15 18 9" />
              </svg>
            </button>
            <ul class={isSubMenu === item.id ? 'active' : ''}>
              {#each item.child as child}
              <li>
                <a href="/">
                  <div class="flex item-c bg-soft brdr round-sm p-2">
                    <Icon icon={child.icon} width="28" />
                  </div>
                  <div class="grid">
                    <strong class="text-md">{child.name}</strong>
                    <p class="text-xs">{child.info}</p> 
                  </div>
                </a>
              </li>
              {/each}
            </ul>
          </li>
          {/each}
        </ul>
      </div>
      <div class="none lg:flex item-c">
        <a class="btn text-xs round-sm" href="/">Sign Up</a>
      </div>
      <div class="cart flex item-c">
        <button class="flex item-c">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24" fill="currentColor">
            <path d="M4 6.414L.757 3.172l1.415-1.415L5.414 5h15.242a1 1 0 0 1 .958 1.287l-2.4 8a1 1 0 0 1-.958.713H6v2h11v2H5a1 1 0 0 1-1-1V6.414zM6 7v6h11.512l1.8-6H6zm-.5 16a1.5 1.5 0 1 1 0-3 1.5 1.5 0 0 1 0 3zm12 0a1.5 1.5 0 1 1 0-3 1.5 1.5 0 0 1 0 3z"/>
          </svg>
        </button>
      </div>
    </div>
  </div>
</header>

<style>
  .header {
    position: sticky;
    top: 0;
    background-color: rgb(13 14 51 / 60%);
    border-bottom: 1px solid var(--brdr-color);
    backdrop-filter: blur(16px);
    z-index: 4;
    transition: 0.2s ease;
  }
  .menu > ul {
    display: flex;
    margin-left: 1.5rem;
    gap: 2rem;
  }
  .menu > ul > li {
    position: relative;
  }
  .menu > ul > li > button {
    display: flex;
    gap: .5rem;
    width: 100%;
    align-items: center;
    justify-content: space-between;
    transition: 0.2s ease;
  }
  .menu > ul > li > button:hover {
    cursor: pointer;
    color: var(--main-color);
  }
  .menu > ul > li > ul:not(.active) {
    visibility: hidden;
  }
  .menu > ul > li > ul {
    display: grid;
    padding: .5rem 0;
    transition: .2s ease;
  }
  .menu > ul > li > ul > li > a {
    display: flex;
    align-items: center;
    padding: 12px 20px;
    gap: 1.25rem
  }
  .btn {
    padding: 6px 12px;
  }
  @media (max-width: 992px) {
    .menu:not(.active) {
      visibility: hidden;
      height: 0;
    }
    .menu {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100vh;
      flex-direction: column;
      padding-top: .75rem;
      margin-top: 86px;
      overflow: hidden;
      border-top: 1px solid var(--brdr-color);
      background-color: var(--body-color);
      transition: .2s ease;
    }
    .menu > ul {
      flex-direction: column;
      width: 100%;
      overflow-y: auto;
      height: calc(100% - 86px);
      gap: 0;
      margin-left: 0;
    }
    .menu > ul > li > button {
      padding: 16px 20px;
    }
    .menu > ul > li > ul:not(.active) {
      opacity: 0;
      height: 0;
      padding: 0;
    }
    .menu > ul > li > ul {
      overflow: hidden;
    }
  }
  @media (min-width: 992px) {
    .menu > ul > li > ul:not(.active) {
      opacity: 0;
      top: 40px;
    }
    .menu > ul > li > ul {
      position: absolute;
      top: 64px;
      left: 50%;
      background-color: var(--soft-color);
      border: 1px solid var(--brdr-color);
      border-radius: 1rem;
      transform: translate(-50%,0);
      min-width: 400px;
    }
    .menu > ul > li > ul > li > a {
      padding: 10px 20px;
    }
    .menu > ul > li > ul > li > a:hover {
      background-color: var(--brdr-color);
    }
  }
</style>
