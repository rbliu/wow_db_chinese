# wow_db_chinese
==============
## TrinityCore database translation to Chinese
## Trinity 数据库汉化

As we know, the latest (Nov 2017) -[TrinityCore database (branch 3.3.5)](https://github.com/TrinityCore/TrinityCore/releases) uses English (enUS) as the primary language, with 5 other locales (deDE, frFR, esES, esMX, ruRU). Therefore, the issue is that even we extract dbc and maps files from a Chinese WoW client, we still see lots of default language (i.e. enUS) in the game due to the TDB file release. In my case, I have most of the text correct (e.g. NPC, item, creature) in game, but anything related to quest is still in enUS. To fix this problem, I use these sql file to update some tables in the installed database.

目前的TDB文件中只包含了除英语以外的五种语言，其中并不包含简体或繁体中文。在我使用3.3.5-12340繁体中文客户端的测试中，游戏的大部分语言都能够显示为中文，唯任务相关的一切描述都仍显示为英文。为了修复这个问题，我对原数据库进行修改及汉化。

### Envirionment:
* TrinityCore Server 3.3.5(build 12340)
* WoWLK Traditional Chinese Client (zhTW)
* HeidiSQL or MySQL Workbench

### TODO:

- []access_requirement
- []achievement_reward
- []areatrigger_tavern
- []areatrigger_teleport
- []battleground_template
- []creature_template
- []creature_text
- []db_script_string
- []game_event
- []game_tele
- []gameobject_template
- []gossip_menu_option
- []item_set_names
- []item_template
- []npc_text
- []outdoorpvp_template
- []page_text
- []points_of_interest
- [x]quest_template_locale
- []transports
- []trinity_string

*  2017-11-3: quest_template_locale: 将world数据库中的quest_template_locale表格中的esMX修改为zhTW，如需要zhCN亦可以进行相应的替换。

所有原始数据fork于其他github库
