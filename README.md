# wow_db_chinese

## TrinityCore database translation to Chinese / Trinity 数据库汉化


As we know, the latest (Nov 2017) -[TrinityCore database (branch 3.3.5)](https://github.com/TrinityCore/TrinityCore/releases) uses English (`enUS`) as the primary language, with 5 other locales (`deDE`, `frFR`, `esES`, `esMX`, `ruRU`). Therefore, the issue is that even we extract dbc and maps files from a Chinese WoW client, we still see lots of default language (i.e. `enUS`) in the game due to the TDB file release. In my case, I have most of the text correct (e.g. NPC, item, creature) in game, but anything related to quest is still in `enUS`. To fix this problem, I use these sql file to update some tables in the installed database.

目前的TDB文件中只包含了除英语以外的五种语言，其中并不包含简体或繁体中文。在我使用3.3.5-12340繁体中文客户端的测试中，游戏的大部分语言都能够显示为中文，唯与任务相关的一切描述都仍显示为英文。为了修复这个问题，我对原数据库进行修改及汉化。

*注：本库中包含的数据库均为简体中文，因测试需要我可能会将表格中的`locale`栏写作`zhTW`，但如改写作`zhCN`也是完全可以的。此数据库文件仅供个人研究学习使用，请勿用于公共库之相关服务。*

### Envirionment:
* TrinityCore Server 3.3.5(build 12340)
* TDB 335.63 (2017-4-18 release)
* WoWLK Chinese Client (`zhTW` or `zhCN`)
* HeidiSQL or MySQL Workbench

### TODO:

- [x] access_requirement
- [x] achievement_reward
- [x] areatrigger_tavern
- [x] areatrigger_teleport
- [x] battleground_template
- [x] creature_template
- [x] creature_text
- [ ] db_script_string   -- **Not Found in TDB**
- [ ] game_event   -- **eventEntry dismatch**
- [x] game_tele
- [x] gameobject_template
- [ ] gossip_menu_option   -- **MenuID, OptionID dismatch**
- [x] item_set_names
- [x] item_template
- [ ] npc_text
- [ ] outdoorpvp_template
- [ ] page_text
- [ ] points_of_interest
- [x] quest_template_locale
- [ ] transports
- [ ] trinity_string

------

* 2017-11-4: 对大部分sql文件进行修改使其符合TDB及world数据库中的格式。部分数据库文件中的条目编号与TDB所提供不一致，暂未做出修改。

*  2017-11-3: `quest_template_locale`: 将`world`数据库中`quest_template_locale`表格中的`ruRU`修改为`zhCN`，如需要`zhTW`亦可以进行相应的替换。

------

*所有原始数据取自于其他github库*

*The very original data was forked from other github repo*
