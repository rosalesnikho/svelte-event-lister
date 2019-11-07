<script>
import Header from './UI/Header.svelte'
import MeetupGridList from './Meetups/MeetupGridList.svelte'

    export let title;
    export let subtitle;
    export let description;
    export let contactEmail;
    export let meetupImg;
    export let address;

    let events = [
        {
        	id: Math.random().toString(),
            title: 'Coding bootcamp',
            subtitle: 'Learn to code this weekend',
            description: 'Bacon ipsum dolor amet flank ham hock leberkas, filet mignon drumstick tri-tip rump short loin. Sirloin sausage meatball porchetta capicola biltong, ball tip pork chop tongue doner pig. Pastrami boudin tail pork turducken picanha tongue sirloin prosciutto cupim.',
            contactEmail: 'email@email.com',
            imgURL: 'https://picsum.photos/id/20/800/600',
            address: '110 E Houston St',
            city: 'San Antonio',
            state: 'TX',
        },
        {
            id: Math.random().toString(),
            title: 'Coding Meetup',
            subtitle: 'Learn to code this weekend',
            description: 'Bacon ipsum dolor amet flank ham hock leberkas, filet mignon drumstick tri-tip rump short loin. Sirloin sausage meatball porchetta capicola biltong, ball tip pork chop tongue doner pig. Pastrami boudin tail pork turducken picanha tongue sirloin prosciutto cupim.',
            contactEmail: 'email2@email.com',
            imgURL: 'https://picsum.photos/id/10/800/600',
            address: '120 E Houston St',
            city: 'Dallas',
            state: 'TX',
        },
        {
            id: Math.random().toString(),
            title: 'Coding Tutorial',
            subtitle: 'Learn to code this weekend',
            description: 'Bacon ipsum dolor amet flank ham hock leberkas, filet mignon drumstick tri-tip rump short loin. Sirloin sausage meatball porchetta capicola biltong, ball tip pork chop tongue doner pig. Pastrami boudin tail pork turducken picanha tongue sirloin prosciutto cupim.',
            contactEmail: 'email3@email.com',
            imgURL: 'https://picsum.photos/id/30/800/600',
            address: '130 E Houston St',
            city: 'San Francisco',
            state: 'CA',
        },

    ];

const addEvent = () => {
	const newEvent = {
        id: Math.random().toString(),
        title: title,
        subtitle: subtitle,
        description: description,
        contactEmail: contactEmail,
        imgURL: meetupImg,
        address: address
        };
    events = [newEvent,...events]
    };



</script>

<Header />
<MeetupGridList events="{events}" />

<div class="container">
    <div class="columns">
        <div class="column is-half">
            <form on:submit|preventDefault={addEvent}>

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
                            <label class="label">Event Banner Image</label>
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
                        <button class="button is-link">Submit</button>
                    </div>
                    <div class="control">
                        <button class="button is-link is-light is-danger">Cancel</button>
                    </div>
                </div>
            </form>
        </div>
    </div>
</div>


