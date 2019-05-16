<template>
    <div class="columns is-variable is-multiline is-mobile is-2-mobile is-5-widescreen">
      <div class="column is-half-mobile is-half-tablet">
        <div class="red"></div>
      </div>
      <div class="column is-half-mobile is-half-tablet">
        <div class="blue"></div>
      </div>
      <div class="column is-full-mobile is-half-tablet is-7-widescreen">
          <div class="red"></div>
      </div>
      <div class="column is-full-mobile is-half-tablet is-5-widescreen">
          <div class="blue"></div>
      </div>
      <div class="column is-full-mobile is-half-tablet is-4-desktop">
          <div class="green"></div>
      </div>
      <div class="column is-full-mobile is-half-tablet is-4-desktop">
          <div class="yellow"></div>
      </div>
      <div class="column is-full-mobile is-half-tablet is-4-desktop">
          <div class="orange"></div>
      </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
    .columns{
        .column {
            div {
                height: 164px;
            }
            .red {
                background-color: #BE1717;
            }
            .blue {
                background-color: #1F95D7;
            }
            .green {
                background-color: #39D520;
            }
            .yellow {
                background-color: #D1D520;
            }
            .orange {
                background-color: #F97D0B;
            }
        }
    }
    @media screen and (min-width: 769px) {
        .columns {
            .column {
                .red, .blue {
                    height: 313px;
                }
                .green, .yellow, .orange {
                    height: 285px;
                }
            }
        }
    }
    @media screen and (min-width: 1216px) {
        .columns {
            .column {
                .red, .blue {
                    height: 499px;
                }
            }
        }
    }
</style>
