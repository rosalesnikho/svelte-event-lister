<script>
    import {createEventDispatcher} from 'svelte';
    import MeetupForm from '../Meetups/MeetupForm.svelte'


    const dispatcher = createEventDispatcher();

    const closeModal = () => {
        const closeModalBtn = document.getElementById('form-modal');
        dispatcher('close-modal', closeModalBtn.classList.remove('is-active')
        )
    }
</script>

<div class="modal" id="form-modal">
    <div class="modal-background"></div>
    <div class="modal-content">
        <MeetupForm />
    </div>
    <button id="modal-close-button" class="modal-close is-large" aria-label="close" on:click={closeModal}></button>
</div>