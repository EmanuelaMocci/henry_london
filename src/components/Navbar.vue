<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container-fluid">
      <div class="navbar-brand">WATCH/LAB</div>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarTogglerDemo03"
        aria-controls="navbarTogglerDemo03"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="menu collapse navbar-collapse" id="navbarTogglerDemo03">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <a class="nav-link active" aria-current="page" href="#">About us</a>
          </li>
          <li class="nav-item">
            <a class="nav-link active" aria-current="page" href="#">Brand</a>
          </li>
          <li class="nav-item">
            <a class="nav-link active" aria-current="page" href="#">Projects</a>
          </li>
          <li class="nav-item">
            <a class="nav-link active" aria-current="page" href="#">Magazine</a>
          </li>
          <li class="nav-item">
            <a class="nav-link active" aria-current="page" href="#">Press</a>
          </li>
          <li class="nav-item">
            <a class="nav-link active" aria-current="page" href="#">Contacts</a>
          </li>
        </ul>
        <form class="d-flex">
          <input class="form-control me-2" type="search" aria-label="Search" />
          <button class="search-btn" type="submit">
            <font-awesome-icon icon="fas fa-search" />
          </button>
        </form>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style lang="scss" scoped>
@import "../style/partials/variables.scss";
@import "../style/app.scss";

.navbar {
  padding: 0;
  background-color: $basic-color-2;
  position: fixed;
  top: 0px;
  width: 100%;
  z-index: 2;
  .container-fluid {
    padding: 0;
    font-family: $font4;
    .navbar-brand {
      background-color: $bg-logo;
      font-family: $font3;
      color: $basic-color-1;
      letter-spacing: 2px;
      padding: 15px;
      font-size: 28px;
    }
    .navbar-toggler {
      margin-right: 20px;
    }
    .menu {
      ul {
        width: 100%;
        display: flex;
        justify-content: space-evenly;
        li {
          font-size: 13px;
          min-width: 50px;
          transition: all 0.3s;
          position: relative;
          cursor: pointer;
          padding: 0 15px;
          .nav-link {
            transition: all 0.3s;
            min-width: 80px;
            text-align: center;
          }
        }
      }
      form {
        padding-bottom: 15px;
        .form-control {
          border: none;
          background-color: transparent;
          border-bottom: 1px solid $basic-color-6;
          border-radius: 0;
          width: 50%;
          min-width: 50%;
          padding-right: 0;
          margin-left: 10px;
        }
        .search-btn {
          border: none;
          background-color: transparent;
          font-size: 15px;
          margin-bottom: -20px;
        }
      }
    }
  }
}
.nav-item::before {
  content: "";
  position: absolute;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
  opacity: 0;
  transition: all 0.3s;
  border-top-width: 2px;
  border-bottom-width: 2px;
  border-top-style: solid;
  border-bottom-style: solid;
  border-top-color: $bg-logo;
  border-bottom-color: $bg-logo;
  transform: scale(0.1, 1);
}
.nav-item:hover::before {
  opacity: 1;
  transform: scale(1, 1);
}
.nav-item::after {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
  transition: all 0.3s;
}
.nav-item:hover::after {
  opacity: 0;
  transform: scale(0.1, 1);
}

// media query
$breakpoint-ipad: 991px;

@media (max-width: $breakpoint-ipad) {
  .menu {
    margin-bottom: 50px;
  }
  form {
    margin: 0 50px;
    display: flex;
    justify-content: center;
  }
  ul {
    margin-top: 50px;

    li {
      text-align: center;
    }
  }
}
</style>
