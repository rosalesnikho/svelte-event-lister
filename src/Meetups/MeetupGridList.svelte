<script>
    import MeetupItem from './MeetupItem.svelte'

    export let events;
</script>

<style>
    .meetup-list {
        margin-top: 3%;
    }
</style>

<div class="container">
    <section class="meetup-list">
        <div class="columns is-mobile">
            {#each events as event, index(event.id)}
            <div class="column is-3">
                    <MeetupItem
                            title="{event.title}"
                            subtitle="{event.subtitle}"
                            address="{event.address}"
                            meetupImg="{event.imgURL}"
                            contactEmail="{event.contactEmail}"
                    />
                </div>
            {/each}
        </div>
    </section>
</div>
