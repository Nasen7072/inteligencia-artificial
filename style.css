const caixaPrincipal = document.querySelector(".caixa-principal");
const caixaPerguntas = document.querySelector(".caixa-perguntas");
const caixaAlternativas = document.querySelector(".caixa-alternativas");
const caixaResultado = document.querySelector(".caixa-resultado");
const textoResultado = document.querySelector(".texto-resultado");

const perguntas = [
    {
        enunciado: "Você é um jovem aventureiro que acaba de deixar sua vila em busca de glória. No caminho pela floresta, você encontra uma espada cravada em uma pedra. O que faz?",
        alternativas: [
            {
                texto: "Tenta puxar a espada com toda sua força.",
                afirmacao: "Você retira a espada da pedra, sentindo um poder antigo percorrer seu corpo. Agora carrega uma arma lendária."
            },
            {
                texto: "Ignora a espada, prefere confiar em sua inteligência e não em armas mágicas.",
                afirmacao: "Você segue viagem, acreditando que a verdadeira força está na mente, não na lâmina."
            }
        ]
    },
    {
        enunciado: "Ao atravessar uma ponte, uma criatura sombria bloqueia seu caminho exigindo um tributo. Como reage?",
        alternativas: [
            {
                texto: "Luta contra a criatura com bravura.",
                afirmacao: "Após uma batalha intensa, você derrota a criatura, ganhando respeito entre os viajantes."
            },
            {
                texto: "Tenta conversar e convencê-la a deixá-lo passar.",
                afirmacao: "Com palavras sábias, você acalma a criatura, que revela ser um guardião antigo e concede sua bênção."
            }
        ]
    },
    {
        enunciado: "Você chega a uma vila cercada por soldados de um rei tirano. Os moradores pedem ajuda. Qual é sua decisão?",
        alternativas: [
            {
                texto: "Ajuda os moradores a organizar uma revolta.",
                afirmacao: "Você lidera o povo contra os soldados, tornando-se símbolo de esperança."
            },
            {
                texto: "Segue seu caminho, evitando problemas maiores.",
                afirmacao: "Você decide que essa batalha não é sua, mas a imagem dos rostos aflitos o acompanha..."
            }
        ]
    },
    {
        enunciado: "Durante a noite, você encontra um mago ferido que oferece um feitiço em troca de proteção. O que faz?",
        alternativas: [
            {
                texto: "Aceita ajudá-lo e aprende magia.",
                afirmacao: "Você protege o mago e ele ensina magias ancestrais que salvam sua vida mais de uma vez."
            },
            {
                texto: "Recusa, desconfiando de sua origem.",
                afirmacao: "Você segue desconfiado, mas perde a chance de aprender conhecimentos místicos."
            }
        ]
    },
    {
        enunciado: "No fim da jornada, você encontra o castelo do rei tirano. Sozinho, o que decide fazer?",
        alternativas: [
            {
                texto: "Invade o castelo e enfrenta o rei.",
                afirmacao: "Você derrota o rei em um duelo épico e é coroado como novo governante do reino."
            },
            {
                texto: "Foge, levando o conhecimento de tudo o que viu.",
                afirmacao: "Você retorna à sua terra como um contador de histórias, inspirando uma nova geração de heróis."
            }
        ]
    },
];

let atual = 0;
let perguntaAtual;
let historiaFinal = "";

function mostraPergunta() {
    if (atual >= perguntas.length) {
        mostraResultado();
        return;
    }
    perguntaAtual = perguntas[atual];
    caixaPerguntas.textContent = perguntaAtual.enunciado;
    caixaAlternativas.textContent = "";
    mostraAlternativas();
}

function mostraAlternativas(){
    for(const alternativa of perguntaAtual.alternativas) {
        const botaoAlternativas = document.createElement("button");
        botaoAlternativas.textContent = alternativa.texto;
        botaoAlternativas.addEventListener("click", () => respostaSelecionada(alternativa));
        caixaAlternativas.appendChild(botaoAlternativas);
    }
}

function respostaSelecionada(opcaoSelecionada) {
    const afirmacoes = opcaoSelecionada.afirmacao;
    historiaFinal += afirmacoes + " ";
    atual++;
    mostraPergunta();
}

function mostraResultado() {
    caixaPerguntas.textContent = "A sua lenda foi escrita...";
    textoResultado.textContent = historiaFinal;
    caixaAlternativas.textContent = "";
}

mostraPergunta();
