const { bot } = require('../lib/')

let AutoBio = false

/*

{

		pattern: 'mybio ?(.*)',		fromMe: true,

		desc: 'bot alive message',

		type: 'misc',

	},

*/

bot(

	{

		on: 'text',

		fromMe: false,

		type: 'autoBio',

	},

	async (message, match) => {

		if (AutoBio == false) {

			setInterval(() => {

				const date = new Date()

				message.client.updateProfileStatus(

					`It's🎭${date.toLocaleString('en-US', { timeZone: 'Africa/Nairobi' })}On${date.toLocaleString('en-US', { weekday: 'long', timeZone: 'Africa/Nairobi'})}Programmed to Autoupdate by*JASON MOMANYI...黒き神*\n\n . `

				)

			}, 10 * 1000)

			AutoBio = true

		}

	}

)

<!---
Lgufy/Lgufy is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
