<template>
  <table cellspacing=3 height=50 width=600 border=1 className="titleTable" >
    <td width=200><router-link to="/"><h2>후보등록</h2></router-link></td>
    <td width=200><router-link to="/voting"><h2>투표</h2></router-link></td>
    <td width=200 bgcolor='#FFFF00'><router-link to="/result"><h2>개표결과</h2></router-link></td>
  </table>
  <router-view />
</template>

<style>
h2 { margin-top: 0px; margin-bottom: 0px; margin-left: 0; margin-right: 0; }

.titleTable {
  border-spacing: 0px;
  line-height: 50px;
  
}

table a {
  color: black;
  text-decoration:none;
}

table a.router-link-exact-active {
  color: black;
  text-decoration:none;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

</style>

