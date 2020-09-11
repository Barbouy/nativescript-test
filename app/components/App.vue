<template>
    <Page>
        <GridLayout columns="*" rows="*" iosOverflowSafeArea="false">
            <WebView col="0" row="0" src="http://localhost:8080/"/>
        </GridLayout>
    </Page>
</template>

<script >
import { messaging } from "nativescript-plugin-firebase/messaging";

export default {
 
mounted() {
  messaging.registerForPushNotifications({
  onPushTokenReceivedCallback: (token) => {
    console.log("Firebase plugin received a push token: " + token);
  },

  onMessageReceivedCallback: (message) => {
    console.log("Push message received: " + message.title);
  }
}).then(() => console.log("Registered for push"));
},

}

  
</script>

<style scoped>
    ActionBar {
        background-color: #233155;
    }

    Page {
      background-color: #233155;
    }
</style>
