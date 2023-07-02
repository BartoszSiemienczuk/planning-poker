<script lang="ts">
    import {goto} from "$app/navigation";

    let roomId = "";

    const joinRoom = () => {
        console.log("Joining " + roomId);
        goto("/room/" + roomId);
    }

    const createRoom = () => {
        console.log("Creating a new room.");
    }
</script>

<div class="card w-96 bg-neutral text-neutral-content shadow-xl mx-auto">
    <div class="card-body items-center text-center">
        <h2 class="card-title">Join a room</h2>
        <p>Join an existing room or create a new one!</p>
        <div class="card-actions justify-items-center">
            <input bind:value={roomId} type="text" placeholder="Room no#" class="input input-bordered input-primary w-full max-w-xs" />
            <button on:click={joinRoom} class="btn btn-primary">Join a room</button>
            <button on:click={createRoom} class="btn btn-secondary btn-outline">Create a room</button>
        </div>
    </div>
</div>
