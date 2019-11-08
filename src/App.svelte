<script>

    import Header from './UI/Header.svelte'
    import StandardModal from './UI/StandardModal.svelte'
    import MeetupGridList from './Meetups/MeetupGridList.svelte'
    import MeetupForm from './Meetups/MeetupForm.svelte'

    export let title;
    export let subtitle;
    export let description;
    export let contactEmail;
    export let meetupImg;
    export let address;



    export let events = [
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
</script>

<Header on:activate-modal />
<MeetupGridList events="{events}" />
<StandardModal on:close-modal>
    <MeetupForm />
</StandardModal>

