<template>
<div class="pt-4">

	<div class="flex justify-center">
		<h2 class="text-center text-gray-800 border-b pb-2">
			<span class="text-center font-bold text-4xl">Linux</span> 
			<span class="mx-8 text-sm border rounded px-2 py-1">VS</span>
			<span class="text-center font-bold text-4xl">Windows</span>
		</h2>
	</div>
	<div class="py-10 px-6">

		<table class="mx-auto table-auto text-gray-700">
			<thead class="border-b">
			    <tr>
			      <th class="px-4 py-2"></th>
			      <th class="px-4 py-2">Linux</th>
			      <th class="px-4 py-2">Windows</th>
			    </tr>
			 </thead>
			<tbody>
				<tr v-for="({prop, linux, windows}, index) in diffWinLinux" :key="index"
				:class="{'bg-gray-100': index % 2}">
					<td class="px-4 py-2">{{ prop }}</td>
					<td class="px-4 py-2">{{ linux }}</td>
					<td class="px-4 py-2">{{ windows }}</td>
				</tr>
			</tbody>
		</table>
		
	</div>



</div>
</template>

<style lang="scss" scoped>
table {
	td::selection {
		color: white;
		background-color: #4a5568;
	}
}
</style>

<script>
	export default {
		name: 'search',
		data() {
			return {
				diffWinLinux: [
					{
						prop: "Coûts", 
						linux: "La plupart des distributions de Linux sont gratuites, du moins pour les utilisateurs privés.", 
						windows: "La dernière évolution de Windows est disponible dans différentes versions et à divers prix."
					},
					{
						prop: "Modèle de licence",
						linux: "Le noyau de Linux et la plupart des distributions sont en open source et (souvent) disponibles sous licence de logiciel libre GNU GPL.",
						windows: "Logiciel propriétaire",
					},
					{
						prop: "Convivialité",
						linux: "Il est vrai qu’Ubuntu est relativement facile à prendre en main pour les utilisateurs de Windows mais la plupart des autres distributions de Linux proposent une barrière à l’entrée plus élevée.",
						windows: "Dès son lancement, Windows a été conçu pour être facilement utilisable et compréhensible, y compris pour des utilisateurs n'ayant pas de compétences en informatique.",
					},
					{
						prop: "Environnement graphique",
						linux: "Les utilisateurs des distributions de Linux disposent d’une grande liberté vis-à-vis du GUI et peuvent même s’en passer complètement.",
						windows: "Microsoft s'appuie sur les standards de GUI Windows.",
					},
					{
						prop: "Aide",
						linux: "Sur Linux, l’offre d'assistance repose sur la communauté des développeurs et utilisateurs. Il est possible de trouver rapidement de l’aide en ligne sur un grand nombre de forums et wikis pour chaque problème.",
						windows: "Windows propose une offre étoffée d’aide hors ligne et en ligne. En outre, il existe une littérature spécialisée exhaustive adaptée à tous les niveaux de pratique.",
					},
					{
						prop: "Logiciels",
						linux: "Linux dispose d’une offre bien moins fournie, mais il est possible de faire fonctionner sur Linux des programmes créés pour Windows.",
						windows: "La plus grande partie des logiciels qui paraissent sont compatibles avec Windows.",
					},
					{
						prop: "Installation",
						linux: "Sur Linux, une grande partie des programmes, pilotes et paquets sont disponibles dans des bibliothèques très fournies.",
						windows: "L’installation des programmes se fait après téléchargement de fichiers d’installation depuis des sites Internet ou à partir de supports de stockage physiques.",
					},
					{
						prop: "Désinstallation",
						linux: "Sur Linux, les programmes sont purement et simplement supprimés.",
						windows: "La désinstallation des programmes laisse derrière elle des résidus dans le système.",
					},
					{
						prop: "Matériel",
						linux: "En comparaison, la prise en charge du matériel est bien plus limitée. Les pilotes sont en partie disponibles avec du retard.",
						windows: "Des pilotes pour Windows sont disponibles pour presque tous les types de matériel informatique.",
					},
					{
						prop: "Fiabilité",
						linux: "Linux et ses distributions sont connus pour être d’un fonctionnement particulièrement fiable.",
						windows: "La fiabilité a beau s’être améliorée ces dernières années sur Windows, elle n’est toujours pas au niveau de ce qui se fait dans la plupart des distributions de Linux.",
					},
					{
						prop: "Sécurité",
						linux: "Les distributions de Linux ne sont que rarement la cible d'attaques.",
						windows: "Les systèmes Windows sont régulièrement menacés par des virus et autres malwares.",
					},
					{
						prop: "Vitesse",
						linux: "En règle générale, Linux fonctionne très vite.",
						windows: "Windows est connu pour cela : plus on l’utilise, plus il est lent.",
					},
					{
						prop: "Mises à jour",
						linux: "Chaque utilisateur peut choisir lui-même les mises à jour à installer. Une partie d’entre elles sont expérimentales et donc pas forcément à mettre entre toutes les mains.",
						windows: "Les mises à jour sont souvent proposées à un rythme frénétique. La plupart des mises à jour sont stables.",
					},
					{
						prop: "Version d’essai",
						linux: "Dans la mesure où la plupart des distributions de Linux sont gratuites, il est possible de les tester sans problème. Certaines d’entre elles peuvent fonctionner depuis une clé USB sans qu’il soit nécessaire de les installer.",
						windows: "Il est possible de télécharger et d’installer Windows sans licence à titre d’essai.",
					},
					{
						prop: "Champs d'application",
						linux: "Pour utiliser Linux, il est nécessaire de posséder un minimum de compétences informatiques. En outre, dans la mesure où de nombreux jeux sur ordinateur ne sont pas disponibles, les distributions de Linux sont plutôt choisies par des gens dont le métier tourne autour de l’informatique.",
						windows: "Windows s’adresse à tous types d’utilisateurs, des plus novices aux experts. En raison de l’énorme offre de logiciels compatibles avec Windows, ce système d’exploitation est intéressant aussi bien pour une application professionnelle que dans un but de divertissement.",
					},
				],

				diffExt4Ntfs: [
					{
						prop: "", 
						ext4: "", 
						ntfs: ""
					},
				],
			}
		},
	}
</script>
