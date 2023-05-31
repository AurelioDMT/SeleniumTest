tags: #web/ferramenta #audiovisual
status: #zettel/fleeting

# Introdução
- DaVinci Resolve é um editor de vídeo muito usado.

# Curso
- Path: `C:\Users\luizh\Documents\CURSO GRATUITO DAVINCI RESOLVE`
- Possui 7 interfaces diferentes, sendo elas:
	- Media; Cut; Edit; Fusion; Color; Fairlight; e Deliver.

## MÓDULO 1
- Path: `C:\Users\luizh\Documents\CURSO GRATUITO DAVINCI RESOLVE\Editing`

### Aula 1
#### Organização - Metadata
1. Primeira instrução: **importar** os arquivos disponíveis no site oficial para download. Os arquivos importados devem estar na mesma estrutura que os originais.
	- Na interface "Media", em "Media Storage" procure a/as pasta(s) desejada(s), com o botão esquerdo do mouse, seleciona a terceira opção, dessas três: 
		1. "Add Folder Into Media Pool"
			- Importa somente a primeira camada de pastas, não conseguindo o conteúdo de sub-pastas, em uma única pasta "master" .
		2. "Add Folder and SubFolders into Media Pool"
			- Importa todo o conteúdo em uma única pasta "master".
		3. "Add Folder and SubFolders into Media Pool (Create Bins)"
			- Importa o conteúdo e a estrutura de pastas.
2. Organizar os aúdios importados.
	-  Para criar pastas, basta clicar com botão direito do mouse no "bin list" — parte inferior da interface "Media".
- (ATALHO) Shift + S em "Media", muta o som do preview.
3. Insira uma metadata em vídeos de intrevistas.
	- Na segunda fileira de ferramentas na parte superior direita. em "Metadata", é possível selecionar vários arquivos e adicionar metadata neles. Nesse caso, iremos utilizar o campo "Keywords", colocando "Interview" e salvando.
	- Para ver essas "Keywords", na barra de navegação da "bin list" terá os navegadores dos arquivos e, em baixo, os navegadores de acordo com as "Keywords" — a "Smart Bins".
4. Importe metadatas de terceiros.
	- Na primeira fileira de ferramentas, em "file", dentro do menu vá na opção "Import Metadata To Media Pool" e selecione o arquivo .csv contendo as metadatas.
	- É possível também olhar as metadatas dos arquivos em "Inspector" na seguinda fileira de ferramentas do lado direito. Em "File".
	- Metadatas são importantes porque facilitam a pesquisa de conteúdo. Caso haja uma equipe trabalhando em um projeto, os arquivos, provavelmente, estarão todos compilados, contento metadatas neles. Logo, facilitando o serviço de todo mundo.
5. Configure a "Smart Bins" para mostrar, além das "Keywords", as "Scene" que nada mais são atributos da metadata.
	- Primeira linha, DaVinci Resolve, "preferences", "User", "Editing", em "Automatic Smart Bins" selecione "Automatic smart bins for scene metadata". Save. 
6. Crie uma "Smart Bin" (Pasta inteligente).
	- É possível, inclusive, criar "Smart bins" com Primeira linha, "File", "New Smart Bin".
	- Nela é possível declarar condicionais de acordo com as metadatas.
7. Renomeie todos os arquivos executando um padrão ligado aos metadados.
	- Selecionando todos os clipes e clicando com o botão direito do mouse, "Clip Attributes", "Name". Aqui você pode colocar qualquer nome e separar com "`_`" (underscore), é possível atribuir variáveis das metadatas utilizando o "%".

#### Editing
- Interface: Edit
1. Crie uma "timeline", coloque um vídeo e o reproduza.
	- Na "Media Pool" selecione sua "master". Ctrl + N.
	- Agora selecione um vídeo e arraste para a tela direita em "Insert". Arrastando para a tela esquerda é possível a vizualização sem inserir.
	- Precione "L" para rodar o vídeo, precionando novamente haverá aumento na velocidade.
2. Utilizando a tela da esquerda, defina os IN/OUT de um vídeo e faça um "Overwrite".
	- Para ver as ondas de audio na tela, clique no canto superior-direito, "Show Zoomed Audio Weveform". Os controles são: "J" para voltar, "L e Space" para avançar, "I" para definir o IN, "O" para definir o OUT.
	- Selecione a parte desejada e vá na primeira linha, "Playback", "Play Around/To Out".
	- Precione F10 para executar o "Overwritting" no local da agulha. Assim, subistituindo todo o vídeo após a agulha.
3. Faça uma inserção no corte desses dois vídeos.
	- Mesmo processo, definir in/out, mas agora é "Incert", com o F9.
	- Em vídeo com audio, é possível inserir essas funções separadamente, com a tela da esquerda.
	- No temporizador no canto superior-direito da tela, é possível utilizar operação de adição e subtração com o tempo.
4. Separe o audio do vídeo e delete o vídeo.
	- Para separa o audio do vídeo, existe uma ferramenta na "timeline" ou o atalho Ctrl + Shift + L. Se você deletar a parte do vídeo com o Shift precionado, vai acontecer um "Ripple Delete", quando o vídeo posterior toma o espaço vazio deixado pelo vídeo apagado.
5. Ferramenta de corte.
	- Pressionando B "Blade Edit Mode" — corta a parte selecionada.
	- Pressionando T "Trim Edit Mode" — pode tanto avançar o vídeo na mesma posição da timeline quanto cortar o vídeo pelo começo, arrastando toda a timeline até ele.
	- "<" e ">" para voltar ou avançar um frame de um vídeo na mesma posição da timeline.

# References
- [Curso em português](https://www.youtube.com/playlist?list=PLq_fPiVBOzyjnmMXPauFnjVZgVfTj7aLU) baseado no [curso oficial](https://www.blackmagicdesign.com/br/products/davinciresolve/training).
