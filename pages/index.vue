<template>
  <div class="page">
    <base-notification  v-for="(notif, index) in notifications" :key="notif.variant" :variant="notif.variant" :title="notif.title" @close-click="removeNotification(index)"></base-notification>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      /**
       * Liste des notifications à afficher pour l'étape 1
       * @example [{
       *   title // titre de la notification
       *   content // contenu de la notification
       *   variant // type de notification (sert pour déterminer quelle couleur utiliser)
       * }]
       */
      notifications: [
        {
          title: 'Danger Window',
          content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit ut aliquam, purus sit amet luctus venenatis, lectus magna fringilla urna, porttitor",
          variant: 'danger',
        },
        {
          title: 'Success Window',
          content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit ut aliquam, purus sit amet luctus venenatis, lectus magna fringilla urna, porttitor",
          variant: 'success',
        },
        {
          title: 'Warning Window',
          content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit ut aliquam, purus sit amet luctus venenatis, lectus magna fringilla urna, porttitor",
          variant: 'warning',
        },
        {
          title: 'Info Window',
          content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit ut aliquam, purus sit amet luctus venenatis, lectus magna fringilla urna, porttitor",
          variant: 'info',
        }
      ],
    }
  },
  methods: {
    removeNotification(index){
      this.notifications.splice(index, 1)
    }
  }
}


</script>
<style lang="scss" scoped>
.page {
  position: relative;
  min-height: 100vh;
}
</style>
