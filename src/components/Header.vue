<template>
  <div>
      <a href="/">
        <img src="@/assets/img/dc-logo.png" alt="Logo DC">
      </a>

      <nav>
          <ul>
              <li><a href="#">CHARACTERS</a></li>
              <li><a href="#">COMICS</a></li>
              <li><a href="#">MOVIES</a></li>
              <li><a href="#">TV</a></li>
              <li><a href="#">GAMES</a></li>
              <li><a href="#">COLLECTIBLES</a></li>
              <li><a href="#">VIDEOS</a></li>
              <li><a href="#">FANS</a></li>
              <li><a href="#">NEWS</a></li>
              <li><a href="#">SHOP</a></li>
          </ul>
      </nav>
  </div>
</template>

<script>
export default {
    name: "Header",
}
</script>

<style lang="scss" scoped>
    header{
        text-align: center;

        ul{
            list-style: none;

            li{
                text-decoration: none;
                display: inline-block;

                &:hover{
                    color: red;
                }
            }
        }
    }
</style>