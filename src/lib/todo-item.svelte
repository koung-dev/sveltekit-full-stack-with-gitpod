<div class="todo">
    <form action="" method="">
        <input type="hidden" name="done" value="">
        <button class="toggle" aria-label='Mark done/not done'>
            <svg fill="none" height="20" viewBox="0 0 24 24" width="20" xmlns="http://www.w3.org/2000/svg"><path d="m3 12 6 6 12-12" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/></svg>
        </button>
    </form>

    <form action="" method="" class="text">
        <input type="text">
        <button aria-label='Save todo' class="save">
            <svg fill="#000000" version="1.1" id="Capa_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" 
                width="15px" height="15px" viewBox="0 0 407.096 407.096"
                xml:space="preserve">
                <g>
                    <g>
                        <path d="M402.115,84.008L323.088,4.981C319.899,1.792,315.574,0,311.063,0H17.005C7.613,0,0,7.614,0,17.005v373.086
                            c0,9.392,7.613,17.005,17.005,17.005h373.086c9.392,0,17.005-7.613,17.005-17.005V96.032
                            C407.096,91.523,405.305,87.197,402.115,84.008z M300.664,163.567H67.129V38.862h233.535V163.567z"/>
                        <path d="M214.051,148.16h43.08c3.131,0,5.668-2.538,5.668-5.669V59.584c0-3.13-2.537-5.668-5.668-5.668h-43.08
                            c-3.131,0-5.668,2.538-5.668,5.668v82.907C208.383,145.622,210.92,148.16,214.051,148.16z"/>
                    </g>
                </g>
            </svg>
        </button>
    </form>

    <form action="" method="">
        <button class='delete' aria-label='Delete todo'>
            <svg viewBox="0 0 448 512" xmlns="http://www.w3.org/2000/svg"><path d="m432 32h-120l-9.4-18.7a24 24 0 0 0 -21.5-13.3h-114.3a23.72 23.72 0 0 0 -21.4 13.3l-9.4 18.7h-120a16 16 0 0 0 -16 16v32a16 16 0 0 0 16 16h416a16 16 0 0 0 16-16v-32a16 16 0 0 0 -16-16zm-378.8 435a48 48 0 0 0 47.9 45h245.8a48 48 0 0 0 47.9-45l21.2-339h-384z"/></svg>
        </button>
    </form>
</div>

<style>
    .todo{
        display: grid;
        grid-template-columns: 2rem 1fr 2rem;
        gap: 0.5rem;
        align-items: center;
        margin: 0 0 0.5rem 0;
        padding: 0.5rem;
        background-color: white;
        border-radius: 8px;
        filter: drop-shadow(2px 4px 6px rgba(0, 0, 0, 0.1));
        transform: translate(-1px, -1px);
        transition: filter 0.2s, transform 0.2s;
    }

    .todo button {
        width: 2em;
        height: 2em;
        background-color: transparent;
        background-position: 50% 50%;
        background-repeat: no-repeat;
    }

    .todo input{
        flex: 1;
        padding: 0.5em 2em 0.5em 0.8em;
        border-radius: 3px;
    }

    .toggle {
        border: 1px solid rgba(0, 0, 0, 0.2);
        border-radius: 50%;
        box-sizing: border-box;
        background-size: 1em auto;
    }

    .text {
        position: relative;
        display: flex;
        align-items: center;
        flex: 1;
    }

    .save {
        position: absolute;
        right: 0;
        opacity: 0;
    }

    .todo input:focus + .save,
    .save:focus {
        transition: opacity 0.2s;
        opacity: 1;
    }

    .delete {
        opacity: 0.2;
    }

    .delete:hover,
    .delete :focus{
        transition: opacity 0.2s;
        opacity: 1;
    }

    .done{
        transform: none;
        opacity: 0.4;
        filter: drop-shadow(0px 0px 1px rgba(0, 0, 0, 0.1));
    }

</style>