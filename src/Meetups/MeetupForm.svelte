<!-- JS -->
<script>
    export let title = "";
    export let subtitle = "";
    export let description = "";
    export let contactEmail = "";
    export let meetupImg = "";
    export let address = "";

</script>

<style>
    .create-event-form {
        background: #FFF;
        padding: 3%;
        margin: 3%;
        border-radius: 3px;
    }
</style>

<!-- View -->
<div class="container">
    <div class="columns">
        <div class="column">
            <form on:submit|preventDefault class="create-event-form">
                <div class="field">
                    <label class="label">Event Title</label>
                    <div class="control has-icons-left has-icons-right">
                        <input class="input" type="text" placeholder="Fun event title" bind:value={title}>
                        <span class="icon is-small is-left">
                            <i class="fas fa-bullhorn"></i>
                        </span>
                    </div>
                </div>

                <div class="field">
                    <label class="label">Subtitle</label>
                    <div class="control has-icons-left has-icons-right">
                        <input class="input" type="text" placeholder="Clever tag line" bind:value={subtitle}>
                        <span class="icon is-small is-left">
                            <i class="fas fa-bolt"></i>
                        </span>
                    </div>
                </div>

                <div class="field">
                    <label class="label">Event Location</label>
                    <div class="control has-icons-left has-icons-right">
                        <input class="input" type="text" placeholder="123 Houston St, San Antonio, TX" bind:value={address}>
                        <span class="icon is-small is-left">
                            <i class="fas fa-thumbtack"></i>
                        </span>
                    </div>
                </div>

                <div class="columns">
                    <div class="column is-half">
                        <div class="field">
                            <label class="label">Email</label>
                            <div class="control has-icons-left">
                                <input class="input" type="email" placeholder="hello@" bind:value={contactEmail}>
                                <span class="icon is-small is-left">
                                     <i class="fas fa-envelope"></i>
                                </span>
                            </div>
                        </div>
                    </div>

                    <div class="column is-half">
                        <div class="field">
                            <label class="label">Event Image</label>
                            <div class="control has-icons-left">
                                <input class="input" type="text" placeholder="Link an image" bind:value={meetupImg}>
                                <span class="icon is-small is-left">
                                    <i class="fas fa-images"></i>
                                </span>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="field">
                    <label class="label">Event Description</label>
                    <div class="control">
                        <textarea class="textarea" placeholder="Details about the upcoming event" bind:value={description}></textarea>
                    </div>
                </div>

                <div class="field">
                    <div class="control">
                        <label class="checkbox">
                            <input type="checkbox" required>
                            I agree to the <a href="#">terms and conditions</a>
                        </label>
                    </div>
                </div>

                <div class="field is-grouped">
                    <div class="control">
                        <button on:submit|preventDefault class="button is-link">Submit</button>
                    </div>
                </div>
            </form>
        </div>
    </div>
</div>