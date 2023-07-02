<script lang="ts">
    /** @type {import('./$types').PageData} */
    export let data;
</script>

<div class="navbar bg-base-100">
    <a href="/" class="btn outline normal-case text-lg">Home</a>
    <h3 class="text-lg mx-6">You are in room {data.room.id}</h3>
</div>
