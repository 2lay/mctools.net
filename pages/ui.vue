<template>
  <div>
    <h1 style="text-align: center; margin-bottom: 15px;">UI Preview</h1>
    <h2 style="text-align: center;">Here's all our elements</h2>
    <hr>

    <p>Buttons:</p>
    <br>

    <!-- button, primary color -->
    <mct-button icon-name="mdiHomeFlood" label="Primary" class="mct-button-primary"
      style="margin-bottom: 10px; margin-right: 10px;"></mct-button>

    <!-- button, danger color -->
    <mct-button icon-name="mdiDelete" label="Danger" class="mct-button-danger"
      style="margin-bottom: 10px; margin-right: 10px;"></mct-button>

    <!-- button, warning color -->
    <mct-button icon-name="mdiAlertCircle" label="Warning" class="mct-button-warning"
      style="margin-bottom: 10px; margin-right: 10px;"></mct-button>

    <!-- button, success color -->
    <mct-button icon-name="mdiCheckCircle" label="Success" class="mct-button-success"
      style="margin-bottom: 10px; margin-right: 10px;"></mct-button>

    <br><br>
    <p>Text area:</p>
    <br>

    <!-- text area with predefined text, also use ' taText="asd" ' -->
    <mct-text-area taName="Meow" taPlaceholder="Example placeholder text" taCols="30" taRows="5"></mct-text-area>
  </div>
</template>

<script>
import MctButton from '../components/MctButton.vue';
import MctTextArea from '../components/MctTextArea.vue';
export default {
  components: {
    MctButton,
    MctTextArea
  }
}
</script>
