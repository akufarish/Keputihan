<script>
    import Icon from "@iconify/svelte";

    let message = $state()

    async function sendMessage() {
        console.log(message);
    }

</script>

<main class="flex items-center justify-center h-screen">
    <div class="w-[672px] flex flex-col h-[112px] bg-secondary rounded-2xl">
        <textarea bind:value={message} class="w-full rounded-t-2xl bg-secondary focus:outline-none placeholder:text-gray-400 text-gray-400 p-3.5 overflow-hidden resize-none" placeholder="Type your message here..." >
        </textarea>
        <div class="flex justify-between w-full p-2">
            <button class="w-[36px] h-[36px] rounded-full flex justify-center items-center ">
                <Icon icon="material-symbols:add" class="w-8 h-8 font-bold text-white" />
            </button>
            <button onclick={sendMessage} class="w-[32px] h-[32px] bg-white rounded-full flex justify-center items-center ">
                <Icon icon="material-symbols:arrow-upward-alt-rounded" class="w-8 h-8 font-bold" />
            </button>
        </div>
    </div>
</main>
