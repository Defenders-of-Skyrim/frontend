<template>
  <div class="navbar-container">
    <div class="container">
      <div class="row">
        <div class="col">
          <b-navbar
            toggleable="lg"
            type="dark"
          >
            <b-navbar-brand :to="localePath('/')">
              <client-only>
                <img
                  svg-inline
                  src="@/assets/images/logo.svg"
                >
                <template slot="placeholder">
                  <img src="@/assets/images/logo.svg">
                </template>
              </client-only>
              <p>{{ $t('navbar.logo.subtitle') }}</p>
            </b-navbar-brand>
            <b-navbar-toggle target="nav-collapse" />
            <b-collapse id="nav-collapse" is-nav>
              <b-navbar-nav>
                <b-nav-item-dropdown
                  class="columns"
                  :text="$t('navbar.characters.index')"
                  lazy
                  no-caret
                >
                  <b-dropdown-group
                    id="characters"
                    :header="$t('navbar.characters.subitems.header')"
                  >
                    <b-dropdown-item :to="localePath('/characters/followers')">
                      {{ $t('navbar.characters.subitems.followers') }}
                    </b-dropdown-item>
                    <b-dropdown-item :to="localePath('/characters/trainers')">
                      {{ $t('navbar.characters.subitems.trainers') }}
                    </b-dropdown-item>
                    <b-dropdown-item :to="localePath('/characters/traders')">
                      {{ $t('navbar.characters.subitems.traders') }}
                    </b-dropdown-item>
                    <b-dropdown-item :to="localePath('/characters/pets')">
                      {{ $t('navbar.characters.subitems.pets') }}
                    </b-dropdown-item>
                    <b-dropdown-item :to="localePath('/characters/other')">
                      {{ $t('navbar.characters.subitems.other') }}
                    </b-dropdown-item>
                  </b-dropdown-group>

                  <b-dropdown-group
                    id="characters-universes"
                    :header="$t('navbar.characters.subitems.headerUniverse')"
                  >
                    <b-dropdown-item to="/characters/dota">
                      {{ $t('universes.dota') }}
                    </b-dropdown-item>
                    <b-dropdown-item to="/characters/league-of-legends">
                      {{ $t('universes.league-of-legends') }}
                    </b-dropdown-item>
                    <b-dropdown-item to="/characters/overwatch">
                      {{ $t('universes.overwatch') }}
                    </b-dropdown-item>
                  </b-dropdown-group>
                </b-nav-item-dropdown>

                <b-nav-item-dropdown
                  class="columns"
                  :text="$t('navbar.apparel.index')"
                  lazy
                  no-caret
                >
                  <b-dropdown-group
                    id="apparel-weapons"
                    :header="$t('navbar.apparel.subitems.headerWeapons')"
                  >
                    <b-dropdown-item :to="localePath('/weapons/onehanded')">
                      {{ $t('navbar.apparel.subitems.onehanded') }}
                    </b-dropdown-item>
                    <b-dropdown-item :to="localePath('/weapons/twohanded')">
                      {{ $t('navbar.apparel.subitems.twohanded') }}
                    </b-dropdown-item>
                    <b-dropdown-item :to="localePath('/weapons/ranged')">
                      {{ $t('navbar.apparel.subitems.ranged') }}
                    </b-dropdown-item>
                    <b-dropdown-item :to="localePath('/weapons/staves')">
                      {{ $t('navbar.apparel.subitems.staves') }}
                    </b-dropdown-item>
                  </b-dropdown-group>
                  <b-dropdown-group
                    id="apparel-armor"
                    :header="$t('navbar.apparel.subitems.headerArmor')"
                  >
                    <b-dropdown-item :to="localePath('/armor/light')">
                      {{ $t('navbar.apparel.subitems.lightArmor') }}
                    </b-dropdown-item>
                    <b-dropdown-item :to="localePath('/armor/heavy')">
                      {{ $t('navbar.apparel.subitems.heavyArmor') }}
                    </b-dropdown-item>
                    <b-dropdown-item :to="localePath('/armor/clothes')">
                      {{ $t('navbar.apparel.subitems.clothes') }}
                    </b-dropdown-item>
                  </b-dropdown-group>
                  <!--<b-dropdown-item to="/about">Артефакты</b-dropdown-item>
                  <b-dropdown-item to="/about">Аксессуары</b-dropdown-item>-->
                </b-nav-item-dropdown>
                <!--<b-nav-item-dropdown
                  text="Магия"
                  lazy
                  no-caret
                >
                  <b-dropdown-group id="apparel-magic" header="Школы магии">
                    <b-dropdown-item to="/about">Восстановление</b-dropdown-item>
                    <b-dropdown-item to="/about">Иллюзия</b-dropdown-item>
                    <b-dropdown-item to="/about">Изменение</b-dropdown-item>
                    <b-dropdown-item to="/about">Колдовство</b-dropdown-item>
                    <b-dropdown-item to="/about">Разрушение</b-dropdown-item>
                  </b-dropdown-group>
                  <b-dropdown-item to="/about">Активные эффекты</b-dropdown-item>
                </b-nav-item-dropdown>-->
                <!--<b-nav-item-dropdown
                  text="Локации"
                  lazy
                  no-caret
                >
                  <b-dropdown-group id="locations" header="Страны / миры">
                    <b-dropdown-item to="/about">Греция</b-dropdown-item>
                    <b-dropdown-item to="/about">Египет</b-dropdown-item>
                    <b-dropdown-item to="/about">Преисподняя</b-dropdown-item>
                    <b-dropdown-item to="/about">Штаб Защитников Скайрима</b-dropdown-item>
                  </b-dropdown-group>
                </b-nav-item-dropdown>-->
                <!--<b-nav-item-dropdown
                  text="Квесты"
                  lazy
                  no-caret
                >
                  <b-dropdown-group id="quests" header="Типы заданий">
                    <b-dropdown-item to="/about">Главные</b-dropdown-item>
                    <b-dropdown-item to="/about">Побочные</b-dropdown-item>
                    <b-dropdown-item to="/about">Задания напарников</b-dropdown-item>
                    <b-dropdown-item to="/about">Задания Штаба Защитников Скайрима</b-dropdown-item>
                  </b-dropdown-group>
                </b-nav-item-dropdown>-->
                <b-nav-item-dropdown
                  :text="$t('books.header')"
                  lazy
                  no-caret
                >
                  <b-dropdown-group id="quests" :header="$t('books.subitem')">
                    <b-dropdown-item to="/books/biographic">
                      {{ $t('books.biographic') }}
                    </b-dropdown-item>
                    <b-dropdown-item
                      v-if="$store.state.user.showMatureContent"
                      to="/books/not-lusty-argonian-maid"
                    >
                      {{ $t('books.not-lusty-argonian-maid') }}
                    </b-dropdown-item>
                  </b-dropdown-group>
                </b-nav-item-dropdown>
                <b-nav-item-dropdown
                  :text="$t('navbar.maps.index')"
                  lazy
                  no-caret
                >
                  <b-dropdown-group id="locations">
                    <b-dropdown-item to="/maps/headquarters">
                      {{ $t('navbar.maps.subitems.headquarters') }}
                    </b-dropdown-item>
                  </b-dropdown-group>
                </b-nav-item-dropdown>
                <b-nav-item :to="localePath('/download')">
                  {{ $t('navbar.download') }}
                </b-nav-item>
                <b-nav-item :to="localePath('/diary')">
                  {{ $t('navbar.diary') }}
                </b-nav-item>
              </b-navbar-nav>
            </b-collapse>
            <b-navbar-nav class="nav-right">
              <navbar-user />
            </b-navbar-nav>
          </b-navbar>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Vue, Component } from 'nuxt-property-decorator';
import NavbarUser from '@/components/NavbarUser.vue';

@Component({
  components: {
    NavbarUser,
  },
})
export default class Navbar extends Vue {}
</script>
