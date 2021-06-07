<template>
  <div>
    <div class="layout-div">
      <div class="side-bar"><Sidebar /></div>
      <div class="header">
        <Header />
    <div class="main-content">
      <Nuxt />
    </div>
      </div>
    </div>
  </div>
</template>

<style>
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

.layout-div {
  display: flex;
  flex-direction: row;
  overflow: hidden;
}
.side-bar {
  flex-basis: 25%;
}
.header{
  flex-basis: 74%;
}
.main-content {
    margin-left: 4vw;
    margin-top: 70px;
    width: 66vw;
    overflow: auto;
    z-index: -2;
    padding-bottom: 30vh;
}
</style>
