<script>
    export let title;
    export let subtitle;
    export let author;
    export let date;
    export let description;
    export let contactEmail;
    export let meetupImg;
    export let address;
</script>

<div class="card">
    <div class="card-image">
        <figure class="image is-4by3">
            <img src="{meetupImg}" alt="{title}">
        </figure>
    </div>
    <div class="card-content">
        <div class="media">
            <div class="media-left">
                <figure class="image is-48x48">
                    <img src="https://bulma.io/images/placeholders/96x96.png" alt="{title}">
                </figure>
            </div>
            <div class="media-content">
                <p class="title is-4">{title}</p>
                <p class="subtitle is-6">{subtitle}</p>
            </div>
        </div>

        <div class="content">
            <p class="subtitle is-6">Address: {address}</p>
            <br>
            <time datetime="2016-1-1">11:09 PM - 1 Jan 2019</time>
            <p class="subtitle is-6">{contactEmail}</p>
        </div>
    </div>
    <footer class="card-footer">
        <a href="#" class="card-footer-item">Save</a>
        <a href="#" class="card-footer-item">Edit</a>
        <a href="#" class="card-footer-item">Favorite</a>
    </footer>
</div>