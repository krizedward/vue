<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-buttons slot="start">
          <ion-menu-button color="primary"></ion-menu-button>
        </ion-buttons>
        <ion-title>{{ $route.params.id }}</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">{{ $route.params.id }}</ion-title>
        </ion-toolbar>
      </ion-header>
      <!-- isi content aplikasi -->
      <div id="container">
        <!-- <strong class="capitalize">{{ $route.params.id }}</strong>
        <p>Selamat Datang <a target="_blank" rel="noopener noreferrer" href="https://ionicframework.com/docs/components">Nihon Uwu</a></p> -->
        <ion-button>Open</ion-button>

          <ion-accordion-group>
            <ion-accordion value="first">
              <ion-item slot="header" color="light">
                <ion-label>First Accordion</ion-label>
              </ion-item>
              <div class="ion-padding" slot="content">
                First Content
              </div>
            </ion-accordion>
            <ion-accordion value="second">
              <ion-item slot="header" color="light">
                <ion-label>Second Accordion</ion-label>
              </ion-item>
              <div class="ion-padding" slot="content">
                Second Content
              </div>
            </ion-accordion>
            <ion-accordion value="third">
              <ion-item slot="header" color="light">
                <ion-label>Third Accordion</ion-label>
              </ion-item>
              <div class="ion-padding" slot="content">
                Third Content
              </div>
            </ion-accordion>
          </ion-accordion-group>
        
              <!-- <ion-button @click="presentActionSheet">Open</ion-button>
              <code>{{ result }}</code> -->
      </div>
    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
import { IonButtons, IonContent, IonHeader, IonMenuButton, IonPage, IonTitle, IonToolbar } from '@ionic/vue';

</script>

<script lang="ts">
  import {
    IonAccordion,
    IonAccordionGroup,
    IonItem,
    IonLabel
  } from '@ionic/vue';
  
  import { defineComponent } from 'vue';

  export default defineComponent({
    components: {
      IonAccordion,
      IonAccordionGroup,
      IonItem,
      IonLabel
    },
  });
</script>

<!-- 
<script lang="ts">
  import { ref } from 'vue';
  import { IonButton, actionSheetController } from '@ionic/vue';

  export default {
    components: { IonButton },
    setup() {
      const result = ref('');

      const presentActionSheet = async () => {
        const actionSheet = await actionSheetController.create({
          header: 'Example header',
          subHeader: 'Example subheader',
          buttons: [
            {
              text: 'Delete',
              role: 'destructive',
              data: {
                action: 'delete',
              },
            },
            {
              text: 'Share',
              data: {
                action: 'share',
              },
            },
            {
              text: 'Cancel',
              role: 'cancel',
              data: {
                action: 'cancel',
              },
            },
          ],
        });

        await actionSheet.present();

        const res = await actionSheet.onDidDismiss();
        result.value = JSON.stringify(res, null, 2);
      };

      return {
        result,
        presentActionSheet,
      };
    },
  };
</script> -->

<style scoped>
#container {
  text-align: center;
  position: absolute;
  left: 0;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
}

#container strong {
  font-size: 20px;
  line-height: 26px;
}

#container p {
  font-size: 16px;
  line-height: 22px;
  color: #8c8c8c;
  margin: 0;
}

#container a {
  text-decoration: none;
}
/* .container {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
  flex-direction: column;
}

code {
  white-space: pre-wrap;
} */

</style>