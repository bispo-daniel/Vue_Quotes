<script>
export default {
    methods: {
        handleClick() {
            const url = "https://api.quotable.io/random";

            let resultParagraph = document.createElement('p')
            let appendHere = document.getElementById('result')

            let myFetch = fetch(url)
                .then((res) => res.json())
                .then((data) => {
                    let author = data.author;
                    let quote = data.content;

                     resultParagraph.innerHTML = `${author}: ${quote}`;
                     appendHere.appendChild(resultParagraph)
                });
        },
    },
};
</script>

<template>
    <main>
        <p>Random Quotes App</p>

        <button @click="handleClick()">Generate</button>

        <div id="result"></div>
    </main>
</template>

<style>
main {
    width: 60%;
    max-width: 600px;
    min-width: 250px;
    min-height: 350px;

    border: 1px solid #043927;
    border-radius: 5px;

    display: flex;
    flex-direction: column;
    align-items: center;

    margin-bottom: 20px;
}

main > p {
    font-size: 25px;
}

main > button {
    width: 50%;
    max-width: 200px;
    height: 32px;
    border: 1px solid purple;
    border-radius: 5px;
    background-color: transparent;
    color: #043927;
}

main > button:hover {
    transition: 0.5s;
    background-color: purple;
}

main > #result > p {
    color: wheat;
    padding: 15px;
}

@media screen and (max-width: 425px) {
    main > p {
        font-size: 22px;
    }
}
</style>
