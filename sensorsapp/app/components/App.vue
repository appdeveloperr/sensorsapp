<template>
    <Page>
        <ActionBar title="Welcome to NativeScript-Vue!"/>
        <StackLayout columns="*" rows="*">
   
            <Label class="message" :text="msg"/>
   
            <button text="Show Toast Message" @tap="toast"></button>
   
        </StackLayout>
    </Page>
</template>

<script >

var toaster = require("nativescript-toaster");
/*function pageLoaded(args) {
    var page = args.object;
     
    // show the toast as soon as the app loads
    toaster.showToast();
}*/
//exports.pageLoaded = pageLoaded;

  export default {
    data() {
      return {
        msg: 'Hello World!'
      }
    },

    methods:{

      toast(){

        console.log("Toast Triggered..!");
        toaster.show();
      }
    }
  }
</script>

<style scoped>
    ActionBar {
        background-color: #53ba82;
        color: #ffffff;
    }

    .message {
        margin-top:200px;
        vertical-align: center;
        text-align: center;
        font-size: 20;
        color: #333333;
    }
</style>
