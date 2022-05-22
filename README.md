# GroupService2
Welcome to GroupService2. A new roblox module built with more functions and easy use with roblox-lua-promises.

# Documentation
Ensure you require GroupService2 at the top of your code.

As standard most of the time, functions called will return a ``GroupObject`` type which can be found at ``GroupService2.types.GroupObject``. Some functions have the option to disable this and return a standard table containing usual properties.

## Getting a ``GroupObject``

Run this as standard: ``GroupService2:GetGroup(GroupId: number, GroupObjectSettings(optional))``
This will return an object with lots of feature rich functions!

``local GroupLoadedBoolean, Group = GroupService2:GetGroup(GroupId: number, GroupObjectSettings(optional)):await()``

### Getting a Group Member (PARAMETERS: USERID OR USERNAME)
``Group:GetMember(UserIdentifier: string or number)``

### Getting Ingame Group Members
``Group:GetIngameMembers()``

### Getting Allies (PARAMETERS: RETURN AS GROUP OBJECT [TRUE/FALSE], UPDATECACHE: [TRUE/FALSE] (default false)
``Group:GetAllies(ReturnGroupObject: boolean, UpdateCacheBoolean: boolean)``

### Getting Enemies (PARAMETERS: RETURN AS GROUP OBJECT [TRUE/FALSE], UPDATECACHE: [TRUE/FALSE] (default false)
``Group:GetEnemies(ReturnGroupObject: boolean, UpdateCacheBoolean: boolean)``

### Checking Group Ally (PARAMETERS: GROUPID, CHECKCACHE: BOOLEAN)
``Group.IsAllyOf(QueryAllyId: number, OptionCheckCache: boolean)``

### Checking Group Enemy (PARAMETERS: GROUPID, CHECKCACHE: BOOLEAN)
``Group.IsEnemyOf(QueryAllyId: number, OptionCheckCache: boolean)``

## Events
Ensure ``Events`` is enabled when getting your ``GroupObject`` (default true)

### Group Member Joined Game:
``Group.Data.GroupPlayerJoinedGame:Connect(function(Player) end``

### Group Member Left Game:
``Group.Data.GroupPlayerLeftGame:Connect(function(Player) end``

Any questions, message my portfolio server.
[Discord Server](https://discord.gg/AUxEh8mGTx)

More features will be added soon such as an ranking system etc.
