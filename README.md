<p align="center">
	<font color="red"><h1 align="center">
		SplitSides job by GRZ
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



### License, Credits and Thanks

- This project is licensed under the [MIT License](https://github.com/tabarra/txAdmin/blob/master/LICENSE).
- Everything was made by me, all the menu was made by a friend. Thanks to him again.

Enjoy :)






## How to add more shops in job:

#### Edit client/main.lua ->

- Try to find the line  670 and add this line
<pre>
    <code>
    {label = 'LABEL NAME HERE',            value = 'gpsLABEL'},
    </code>
</pre>
- Try now to find the line  691 and add this line
<pre>
    <code>
    if data.current.value == 'gpsLABEL' then
			x, y, z = Config.LABEL.x, Config.LABEL.y, Config.LABEL.z
			SetNewWaypoint(x, y, z)
			local source = GetPlayerServerId();
			ESX.ShowAdvancedNotification('Split Sides', 'Ajout du point sur le GPS', '', 'CHAR_ALL_PLAYERS_CONF', 1)
    end
    </code>
</pre>


- Try now to find the line  1201 and add this line after " zone == 'Food' "
<pre>
    <code>
    or zone == 'LABEL'
    </code>
</pre>

#### Edit config.lua ->

- Try to find the line  39 and add this line
    - Don't forget to change the position X,Y,Z
<pre>
    <code>
    Config.LABEL = {x = POS.pos, y = POS.pos, z = POS.pos} -- Shop 5 
    </code>
</pre>

- Try now to find the line  691 and add this line
<pre>
    <code>
    LABEL = {
        Name  = "LABEL shop",
        Pos   = { x = -2955.242, y = 385.897, z = 14.041 }, -- CHANGE SAME POSITION OF SHOP 5
        Size  = { x = 1.6, y = 1.6, z = 1.0 },
        Color = { r = 238, g = 0, b = 0 },
        Type  = 23,
        Items = {
            { name = 'item_name',      label = 'item_label',   price = 5 },
            { name = 'item_name',    label = 'item_label', price = 5 }
        },
    },
    </code>
</pre>

# Here you go :)



