# AI ChatBot

## Básico
&nbsp; O foco principal deste projeto é o quão útil ele pode ser. Basicamente:
* &nbsp; A resposta compreende o que foi pedido e responde a mensagem ou solicitação da mesma maneira que uma pessoa inteligente faria.
* &nbsp; A resposta segue qualquer instrução dada, em particular se você pede por conteúdos criativos.
	* &nbsp; Por exemplo, se você pede uma lista curta de items em formato "_bullet point_", a resposta que faz isso geralmente (mas nem sempre) é melhor que a outra que não o faz, a menos que outros erros sejam cometidos (como fabricar detalhes ou mentir sobre algo).
	* &nbsp; Quando se trata de criatividade e seguir instruções explicitas (por exemplo, uma história criativa que completamente ignore o pedido de contagem de palavras VS. Uma que segue a contagem de palavras mas é levemente entediante/sem criatividade), você não terá que favorecer automaticamente aquela que segue as instruções explícitas. Tente imaginar o que a maioria dos usuários iria preferir, se não for imediatamente óbvio para si, você pode usar uma das opções "**unsure**".
* &nbsp; As afirmações feitas na resposta são **precisas**. Você não necessita checar literalmente todas as afirmações feitas, porém, as afirmações principais não podem ser obviamente incorretas.
	* &nbsp; Esteja atento ao fato de que modelos de IA/ChatBots são muito bons em prover detalhes "plausíveis" que são completamente inventados e incorretos (normalmente chamado de "alucinações"), este é o porquê você deve procurar obre as afirmações que você não possui certeza se são verdadeiras.
	* &nbsp; Caso ambas as respostas estejam apenas parcialmente correta, dê uma pontuação melhor para a resposta que estiver mais correta (assumindo que todo o resto esteja igual).
	* &nbsp; Isso também se extende às situações onde o ChatBot assume detalhes que você não providenciou. Por exemplo, talvez você solicite idéias de presente para seu irmão e por alguma razão ele assume que seu irmão é mais novo que você, esses detalhes são considerados alucinações.
	* &nbsp; Caso você simplesmente aceite afirmações que parecem verdadeiras mas você não tem certeza se realmente são, você estará reforçando esse comportamento de "inventar detalhes". Particulamente quando você estiver se acostumando com o projeto, **focar principalmente em tópicos e áreas que lhe são muito familiares é uma ótima forma de abordar a tarefa.**
* &nbsp; A resposta fazem um trabalho decente em agir como "segura" e amigável enquanto responde.
	* &nbsp; Atualmente não estamos testando se os modelos estão ou não a dizer algo que poderá ser perigoso, porém isso poderá ocorrer. Caso isso aconteça você deve selecionar a resposta mais segura, selecione "unsure" caso não haja uma resposta segura, e finalize a conversa.
		* &nbsp; Caso você seja novo em projetos como este, a coisa mais óbvia que a IA não deve fazer é agir como se pudesse interagir com o mundo da mesma forma que um humano pode (ela não possui um corpo e não consegue interagir com o mundo como um humano).
			* &nbsp; Por exemplo, se perguntar à IA qual tipo de pão ela já assou antes é provável que receba uma resposta onde ela finja que pode assar pães. Obviamente, ela não pode, então não pode agir como se pudesse, mas certamente poderá ter uma opção sobre como assar pães (as receitas).
		* &nbsp; Para além disso, a linguagem usada e os tipos de opiniões partilhadas são algo que um assistente deveria incluir?
		* Por exemplo, ela não deveria partilhar opiniões controversiais (ou qualquer opinião política de todo). Imagine os tipos de conversas que você teria no trabalho e com pessoas que você não conhece bem, você teria a certeza de evitar certos tópicos (política, religião, sexo, etc.) e provavelmente não ofereceria dicas que alguém deveria procurar em um profissional (médico, auxiliar financeiro, advogado, etc.)
			*  &nbsp; [[Assuntos a Evitar#Categorias a Evitar|Aqui está uma lista de assuntos você não pode entrar intencionalmente.]]
			* &nbsp; Importante, caso você tenha esses tipos de conversa, nosso time de verificadores irá remover você de todos os projetos de AI ChatBot pois isto demonstra que você não está a ler as instrções corretamente, entra outros problemas.

> [!NOTE] Precisa de Idéias de Como Começar uma Conversa?
> * &nbsp; [AI ChatBot - Response Comparisons](https://docs.google.com/spreadsheets/d/1cZGQNL4oGYqU8QvPwgJKwoHE_tsBLIMLpqAbPw6yMc4/edit?usp=sharing).
> 
> &nbsp; É compreensível que seja difícil inventar algo completamente novo continuamente. Portanto, não é necessário que todas as conversas sejam completamente diferentes umas das outras (até porque os modelos precisam de bastante experiência com todos os tipos de situações para melhorar).

>[!TIP] Dica
>&nbsp; Você pode começar com as mesmas idéias ou temas. Você pode por exemplo abordar o mesmo assunto porém de diferentes maneiras. Ou então ocasionalmente começar com o mesmo prompt caso você queira seguir depois para uma outra direção.

> [!WARNING] Cuidado
> &nbsp; O que você não pode fazer, é ter uma biblioteca ou documento com prompts para você usar sempre, ou qualquer coisa que se assemelhe a uma "fórmula". Ao invés disso, tente ter idéias e conversas que podem te levar a novos e interessantes lugares. Caso você se encontre colando uma mensagem na janela de mensagens, você está indo muito longe.



