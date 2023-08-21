<template>
    <div>
        <nav class="navbar navbar-expand-lg bg-body-tertiary" data-bs-theme="dark">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Navbar</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="/">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/about">About us</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/limitmessage">Limit Message</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/previewImage">PreviewImage</a>
        </li>
        <li class="nav-item">
          <a class="nav-link disabled" aria-disabled="true">Disabled</a>
        </li>
      </ul>
      <form class="d-flex" role="search">
        <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
        <button class="btn btn-outline-success" type="submit">Search</button>
      </form>
    </div>
  </div>
</nav>
    </div>
<slot />

<footer>
    <nav data-bs-theme="dark">
    <div class="card text-center">
  <div class="card-header">
    <i class="bi bi-caret-right-fill"></i><u>Featured</u><i class="bi bi-caret-left-fill"></i>
  </div>
  <div class="card-body">
    <h5 class="card-title"><img src="http://www.tatc.ac.th/files/display_20100887_12051611113634.gif" alt="" width="70px"></h5>
    <p class="card-text"><i class="bi bi-globe"></i>วิทยาลัยเทคนิคสัตหีบ</p>
    <p class="card-text"><i class="bi bi-person-fill"></i>Mr.Karan Sannog</p>
    <p class="card-text"><i class="bi bi-list-ol"></i>66309010002</p>
    <a class="card-text" href="https://www.facebook.com/profile.php?id=100015556067288"><i class="bi bi-facebook"></i>Karan Sannog</a>
  </div>
</div>
</nav>
</footer>
</template>
<style>
footer{
    position: none;
    bottom: 0;
    width: 100%;
    height: auto;
}
</style>