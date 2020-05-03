<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated class="bg-dark text-primary">
      <q-toolbar class="q-py-sm q-px-md">
        <q-toolbar-title>
          <q-avatar>
            <img src="https://cdn.quasar.dev/logo/svg/quasar-logo.svg" />
          </q-avatar>
          Luminarly
        </q-toolbar-title>

        <div class="q-pl-sm q-gutter-sm row items-center no-wrap">
          <q-btn v-if="$q.screen.lt.sm" dense flat>
            <div class="row items-center no-wrap">
              <q-icon name="add" size="20px" />
              <q-icon
                name="arrow_drop_down"
                size="xs"
                style="margin-left: -2px"
              />
            </div>
            <q-menu auto-close>
              <q-list dense style="min-width: 100px">
                <q-item clickable class="menu-link">
                  <q-item-section>New project</q-item-section>
                </q-item>
              </q-list>
            </q-menu>
          </q-btn>

          <q-btn
            v-if="$q.screen.gt.xs"
            no-caps
            dense
            push
            class="glossy"
            color="primary"
            text-color="dark"
          >
            <div class="row items-center no-wrap">
              <q-icon name="add" size="xs" />
              New project
            </div>
          </q-btn>

          <q-btn dense flat no-wrap>
            <q-avatar rounded size="sm">
              <img src="https://cdn.quasar.dev/img/avatar3.jpg" />
            </q-avatar>
            <q-icon name="arrow_drop_down" size="xs" />

            <q-menu auto-close>
              <q-list dense>
                <q-item class="menu-link-signed-in">
                  <q-item-section>
                    <div>Signed in as <strong>Gaby</strong></div>
                  </q-item-section>
                </q-item>
                <q-separator />
                <q-item clickable class="menu-link">
                  <q-item-section>Your profile</q-item-section>
                </q-item>
                <q-item clickable class="menu-link">
                  <q-item-section>Your projects</q-item-section>
                </q-item>
                <q-separator />
                <q-item clickable class="menu-link">
                  <q-item-section>Help</q-item-section>
                </q-item>
                <q-item clickable class="menu-link">
                  <q-item-section>Settings</q-item-section>
                </q-item>
                <q-item clickable class="menu-link">
                  <q-item-section>Sign out</q-item-section>
                </q-item>
              </q-list>
            </q-menu>
          </q-btn>
        </div>
      </q-toolbar>
    </q-header>

    <q-page-container style="min-height: inherit;">
      <router-view />
    </q-page-container>

    <q-footer class="bg-grey-10 text-white q-pa-lg footer-links">
      <div class="row justify-center items-center">
        <div class="col-12 col-md-8">
          <div class="row justify-center items-center">
            <div v-if="$q.screen.gt.xs" class="col-3">
              <q-toolbar-title class="text-primary">
                Luminarly
              </q-toolbar-title>
            </div>
            <div class="col-3">
              <a href="">Home</a>
            </div>
            <div class="col-3">
              <a href="">About</a>
            </div>
            <div class="col-3">
              <a href="">Signup</a>
            </div>
          </div>

          <div class="row justify-center q-mt-sm">
            <div v-if="$q.screen.gt.xs" class="col-3"></div>
            <div class="col-3">
              <a href="">Explore</a>
            </div>
            <div class="col-3">
              <a href="">Contact</a>
            </div>
            <div class="col-3">
              <a href="">Login</a>
            </div>
          </div>

          <div class="row justify-center q-mt-lg">
            &copy; 2020 Luminarly
          </div>
        </div>
      </div>
    </q-footer>
  </q-layout>
</template>

<script>
export default {
  name: 'MainLayout'
};
</script>

<style lang="sass">
.footer-links
  a
    color: white
    text-decoration: none
    &:hover
      opacity: 0.7
.menu-link:hover
  background: $primary
  color: $dark
</style>
