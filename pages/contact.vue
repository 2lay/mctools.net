<template>
    <div style="text-align: center;">
        <h1 style="margin-bottom: 15px;">Contact <em style="text-decoration: line-through 4px;">us</em> me!</h1>
        <h2>You can contact me on Discord using the handle <strong>2lay</strong>, or by mailing me at
            <strong>mail@2lay.net</strong>
        </h2>
        <br>
        <div style="display: flex; justify-content: center;">
            <NuxtLink to="https://github.com/2lay/mctools.net">
                <mct-button icon-name="mdiGithub" label="Source code" class="mct-button-primary"></mct-button>
            </NuxtLink>
        </div>
    </div>
</template>

<script>
import MctButton from '../components/MctButton.vue';

export default {
    components: {
        MctButton
    }
}
</script>
