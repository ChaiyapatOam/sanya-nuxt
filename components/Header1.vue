<template>
  <div class="m-4">
    <nav class="navbar navbar-expand-sm navbar-light bg-light">
      <div class="container-fluid">
        <a href="#" class="navbar-brand">Brand</a>
        <button
          type="button"
          class="navbar-toggler"
          data-bs-toggle="collapse"
          data-bs-target="#navbarCollapse"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div id="navbarCollapse" class="collapse navbar-collapse">
          <ul class="nav navbar-nav">
            <li class="nav-item">
              <a href="#" class="nav-link">Home</a>
            </li>
            <li class="nav-item">
              <a href="#" class="nav-link">Profile</a>
            </li>
            <li class="nav-item dropdown">
              <a
                href="#"
                class="nav-link dropdown-toggle"
                data-bs-toggle="dropdown"
                >Messages</a
              >
              <div class="dropdown-menu">
                <a href="#" class="dropdown-item">Inbox</a>
                <a href="#" class="dropdown-item">Drafts</a>
                <a href="#" class="dropdown-item">Sent Items</a>
                <div class="dropdown-divider"></div>
                <a href="#" class="dropdown-item">Trash</a>
              </div>
            </li>
          </ul>
          <ul class="nav navbar-nav ms-auto">
            <li class="nav-item dropdown">
              <a
                href="#"
                class="nav-link dropdown-toggle"
                data-bs-toggle="dropdown"
                >Admin</a
              >
              <div class="dropdown-menu dropdown-menu-end">
                <a href="#" class="dropdown-item">Reports</a>
                <a href="#" class="dropdown-item">Settings</a>
                <div class="dropdown-divider"></div>
                <a href="#" class="dropdown-item">Logout</a>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </div>
</template>
