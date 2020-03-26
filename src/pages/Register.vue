<template>
    <q-page>
        Halaman Register
    <q-form
      @submit="onSubmit"
      @reset="onReset"
      class="q-gutter-md"
    >
      <q-input
        filled
        v-model="name"
        label="Nama Anda"
        lazy-rules
        :rules="[ val => val && val.length > 0 || 'Please type your name']"
      />

      <q-input
        filled
        v-model="username"
        label="username Anda"
        lazy-rules
        :rules="[ val => val && val.length > 0 || 'Please type username']"
      />

      <q-input
        filled
        type="password"
        v-model="password"
        label="password anda"
        lazy-rules
        :rules="[
          val => val !== null && val !== '' || 'Please type your password',
        ]"
      />

      <q-input
        filled
        type="password"
        v-model="rpassword"
        label="ulangi password anda"
        lazy-rules
        :rules="[
          val => val !== null && val !== '' || 'Please type your password',
        ]"
      />
      <div>
        <q-btn label="Submit" type="submit" color="primary"/>
        <q-btn label="Reset" type="reset" color="primary" flat class="q-ml-sm" />
      </div>
    </q-form>
    </q-page>
</template>
<script>
export default {
  data () {
    return {
      name: null,
      username: null,
      password: null,
      rpassword: null
    }
  },
  methods: {
    onSubmit () {
      console.log('ini fungsi submit')
    },
    onReset () {
      console.log('in fungsi reset')
    }
  }
}
</script>
