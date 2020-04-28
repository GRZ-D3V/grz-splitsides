<p align="center">
	<font color="red"><h1 align="center">
		SplitSides job by GRZ COMING SOON
	</h1></font>
	<p align="center">
		<img width="420" height="237" src="https://cdn.discordapp.com/attachments/672192669249961995/702795661619363930/SSWest-GTAV.jpg">
	</p>
	<h4 align="center">
		Join our Discord Server: &nbsp; <a href="https://discord.gg/ThNYDCQ"><img src="https://discordapp.com/api/guilds/577993482761928734/widget.png?style=shield"></img></a>
	</h4>
	<p align="center">
		<b>SplitSides</b> is a <b>unique job remade</b> with more than 160 new items.
	</p>
</p>

<br/>



## Main Features
- Easy start server.cfg
- General:
    - Boss, Bartender, Dancer grades
    - More than 160 new items
    - Unique dishes of its kind
    - Fully customizable job with dishes and items easily 
    - Cloakroom, Vault, Fridge, Vehicles, BossActions
    - Crafting menu (only with the right items)
    - Billing menu
    - Loyalty card (item card)

- Support:
	- Support via Discord only

- Informations:
	- Auto job restart on server lag
	- 2 languages available (French, English)
	- Compatible with the new artifax server 
	- ESX original job remade by GRZ
	- GPS to blip for items



## [REQUIRES]
- To make the job work:
    - Player management (billing and boss actions)
        - esx_society => https://github.com/ESX-Org/esx_society
        - esx_billing => https://github.com/ESX-Org/esx_billing

    - Items effects (hunger, thirst, drunk)
        - esx_status => https://github.com/ESX-Org/esx_status
        - esx_basicneeds => https://github.com/ESX-Org/esx_basicneeds
        - esx_optionalsneeds => https://github.com/ESX-Org/esx_optionalneeds

    - Items and effects should be added separately in their appropriate files
    - You need to add animations + items effects (basicneeds, optionnalneeds) for an optimal experience



## How to start 

<ol>
    <li>
        <p>CD in your resources/[esx] folder</P>
    </li>
    <li>
        <p>Import GRZ_SplitSidesJob.sql in your database</P>
    </li>
    <li>
        <p>Add this in your server.cfg :</P>
    </li>
</ol>
<pre>
    <code>
    start esx_splitsidesjob
    </code>
</pre>
<ol start="5">
    <li>
        <p>you want player management you have to set Config.EnablePlayerManagement to true in config.lua You can config VaultManagement & Helicopters with true/false (don't forget to comment the area in the same file)
        </P>
    </li>
</ol>



### Don't forget

 - Remember to add items and effects in their separately appropriate files



## License, Credits and Thanks

- This project is licensed under the [MIT License](https://github.com/tabarra/txAdmin/blob/master/LICENSE).
- Everything was made by me, all the menu was made by a friend. Thanks to him again.

Enjoy :)

