let word = {
	ru: [
		'количество',
		'точный',
		'временный',
		'достигать',
		'зависеть от',
		'подходящий',
		'полезный',
		'бесполезный',
		'расширять',
		'восстановить',
		'вместимость',
],
	en: [
		'amount',
		'exact',
		'templorary',
		'to reach / to achieve',
		'to depend',
		'suitable',
		'useful',
		'useless',
		'to expand',
		'to recover',
		'capacity',
],
}

function gameWord(RuOrEn,EnOrRu) {
let wordTrue = 0

	for (i=0; i <= word[RuOrEn].length-1; i++) {
		
		wordPrompt = prompt(word[RuOrEn][i])

		if (wordPrompt == word[EnOrRu][i]) {
			alert('Правильно!')
			++wordTrue
		} else {
			alert('Не правильно!' +'\n'+
				'Вы написали: ' + wordPrompt +'\n'+
				'а надо: ' + word[EnOrRu][i])
		}

	}
alert(wordTrue + ' правильных из: ' + word[RuOrEn].length)
}

function buttonGame() {
	let game = prompt('ru или en?')
	if (game == 'ru') {
		gameWord('ru','en')
	} else if (game == 'en') {
		gameWord('en','ru')
	} else {
		alert('/-_-/ errore')
	}
}
