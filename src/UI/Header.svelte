<script>
    import {createEventDispatcher} from 'svelte'

    const dispatcher = createEventDispatcher();

    const activateModal = () => {
        const modal = document.getElementById('form-modal');
        dispatcher('activate-modal', modal.classList.add('is-active'))
    };


</script>

<nav class="navbar" role="navigation" aria-label="main navigation">
    <div class="navbar-brand">
        <a class="navbar-item" href="https://bulma.io">
            <img src="https://bulma.io/images/bulma-logo.png" width="112" height="28">
        </a>

        <a role="button" class="navbar-burger burger" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
            <span aria-hidden="true"></span>
            <span aria-hidden="true"></span>
            <span aria-hidden="true"></span>
        </a>
    </div>

    <div id="navbarBasicExample" class="navbar-menu">
        <div class="navbar-start">
            <a class="navbar-item">Home</a>
            <a class="navbar-item">Events</a>
            <div class="buttons">
                <a on:click={activateModal} class="button is-primary"><strong>Create Event</strong></a>
            </div>
        </div>

        <div class="navbar-end">
            <div class="navbar-item">
                <div class="buttons">
                    <a class="button is-primary"><strong>Sign up</strong></a>
                    <a class="button is-light">Log in</a>
                </div>
            </div>
        </div>
    </div>
</nav>
