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

    background-color: #00004066;

    border: 1px solid #ffffff66;
    border-radius: 5px;

    display: flex;
    flex-direction: column;
    align-items: center;

    margin-bottom: 20px;
}

main > p {
    font-size: 25px;
}

p:hover {
    color: transparent;
    transition: 0.5s;
}

main > button {
    width: 50%;
    max-width: 200px;
    height: 32px;
    border: 1px solid #ffffff66;
    color: #ffffff66;
    border-radius: 5px;
    background-color: transparent;
}

main > button:hover {
    transition: 0.5s;
    background-color: #000040;
}

main > #result > p {
    padding: 15px;
}

@media screen and (max-width: 425px) {
    main > p {
        font-size: 22px;
    }
}
</style>
