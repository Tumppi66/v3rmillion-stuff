Symbols:

[NH] = The function/value/table is not hidden.
[B] = The function/value/table is/might be broken/not working/crashy.
[A] = The function/value/table is hidden due to being a simple alias for comatibility. (eg. getmenv)
[PS] = The function/value/table is from ProtoSmasher.
[SH] = The function/value/table is from SirHurt.
[NR] = The function/value/table is not recommanded to be used.
[?] = The explination is/might not be accurate/wrong/not complete/missing.

Extra Info:

<void> = no argument/s
??? = unknown arguments
<...> = any arguments allowed
<o> = "o" can be anything (o comes from "object")

Credits:
3dsboy08 - creating Synapse X (lol) + explination contribuitor
randomrobloxian (Stefan#6965) - idea,almost everything
Kiriot22 - explination contribuitor
webo - explination contribuitor

-----------------------

FUNCTION setnonreplicatedproperty(<instance>,<string> prop's name) - [NH] [NR] [B] (set's an instance's proprety to not replicate to the server; good for bypassing anticheats)
FUNCTION isluau(<void>) - (returns true if the game is running lua u, false if not)
FUNCTION getmenv(<instance> ModuleScript) - [A] (returns the env of a ModuleScript)
FUNCTION firesignal(<RBXScriptSignal> Event,<...>) - [B] (fires a signal, and i hope that defcon will make it possible to pass the "<...>" arguments to it)
FUNCTION makefolder(<string> folder name) - (creates a folder inside Synapse X's "workspace" folder)
FUNCTION is_synapse_function(<function>) - (checks if the function is a synapse function)
FUNCTION is_protosmasher_caller(<function>) - [A] [PS] (alias for checkcaller)
FUNCTION replaceclosure(<function>,<function>) - [NR] [PS] (replaces closure A with closure B)
FUNCTION getinstancefromstate(<thread>) - (returns the instnace/script that runs the thread;if the script is made by Synapse X it will return nil)
FUNCTION validfgwindow(<void>) - (checks if roblox is the foreground window or not)
FUNCTION getstates(<void>) - [?] (returns all states)
FUNCTION get_instances(<void>) - [A] [PS] (alias for getinstances)
FUNCTION setrawmetatable(<o>,<table> metatable) - [A] (sets the metatable of <o> to the given table)
FUNCTION get_nil_instances(<void>) - [A] [PS] (alias for getnilinstances)
FUNCTION getnamecallmethod(<void>) - (when called in a function assigned to __namecall, it will get the method; works only on lua u games)
FUNCTION setnamecallmethod(<void>,<string>) - (when called in a function assigned to __namecall, it will set the method to <string>; works only on lua u games)
FUNCTION gbmt(<void>) - [A] (returns the original metatable of the game)
FUNCTION XPROTECT(<string>) - [SH] (runs a SirHurt only script)
FUNCTION getconstants(<function>) - [A] (alias for debug.getconstants)  
FUNCTION hookfunc(<function> F1,<function> F2) - [A] (alias for hookfunction)
FUNCTION get_calling_script(<void>) - [A] [PS] (alias for getcallingscript)  
FUNCTION get_scripts(<void>) - [A] [PS] (alias for getscripts)
FUNCTION make_readonly(<table>) - [A] [PS] (alias for setreadonly)
FUNCTION getstack(<number>,<number> index) - [A] (alias for debug.getstack)
FUNCTION setstack(<number> stackpos,<number> index,<o> value) - [A] (alias for debug.setstack)
FUNCTION get_loaded_modules(<void>) - [A] [PS] (alias for getloadedmodules)
FUNCTION unlockmodulescript(<instance> ModuleScript) - [A] [PS] (unlocks the ModuleScript given)
FUNCTION getupvalue(<function/number> func/stack,<string> upvalue name) -
FUNCTION printconsole(<string>) - [NR] (forces a print inside Synapse X Internal UI's console even if output redirection is disabled; unlike print, the function will error if no argument is provided)
FUNCTION htgetf(<string> url,<string> data,<...>) - [A] (alias for game.HttpGet/syn.request)
FUNCTION is_lclosure(<function>) - (checks if <function> is a lclosure)
FUNCTION mousemoveabs(<number> x,<number> y) - (moves the mouse to the given pos)
FUNCTION getstateenv(<thread>) -  (returns the env of a thread; thread must be from getstates)
FUNCTION setupvalue(<function/number> func/stack,<string> upvalue name,<o> upvalue value) - [A] (alias for debug.setupvalue)
FUNCTION getcallstack(<void>) - (gets the caller's stack)
FUNCTION getinfo(<function>,<string>) - [A] (alias for debug.getinfo)
FUNCTION is_protosmasher_closure() - [A] [PS] (checks if the closure is an exploit's closure)
FUNCTION getpointerfromstate(<state>) - [?] [B] (if u dont give it a state, it crashes)
FUNCTION getpropvalue(<o>,<string> prop name) - (attempts to index and return the value of "<string>" inside "<o>" without invoking any metamethods)
FUNCTION getupvalues(<function/number> func/stack) - [A] (alias for debug.getupvalues)
FUNCTION rconsoleclear(<void>) - (clears the console)
FUNCTION getlocals(<number> stack) - [A] [B] (alias for debug.getlocals)
FUNCTION is_redirection_enabled(<void>) - [?]
FUNCTION setpropvalue(<o>,<string> prop name,<o> new value) - (attempts to index and set the value of "<string>" inside "<o>" to "new value" without invoking any metamethods)
FUNCTION setlocal(<number> stack) - [A] [B] (alias for debug.setlocal)
FUNCTION make_writeable(<table>) - [A] [PS] (alias for setreadonly)
VALUE _VERSION - (returns the current Lua version)
TABLE syn - [NH] {
   TABLE crypto - [NR] [A] (the whole thing is an alias for syn.crypt) {
         FUNCTION encrypt(<string> data,<string> key) - [A] (alias for syn.crypt.encrypt)
         FUNCTION decrypt(<string> data,<string> key) - [A] (alias for syn.crypt.decrypt)
         FUNCTION derive(<string>,<number>) - [A] (alias for syn.crypt.derive)
         FUNCTION random(<number>) - [A] (alias for syn.crypt.random)
         FUNCTION hash(<string>) - [A] (alias for syn.crypt.hash)
         TABLE custom - {
               FUNCTION decrypt(<string>,<string>,<string>,<string>) - [A] (alias for syn.crypt.custom.decrypt)
               FUNCTION encrypt(<string>,<string>,<string>,<string>) - [A] (alias for syn.crypt.custom.encrypt)
               FUNCTION hash(<string>,<string>) - [A] (alias for syn.crypt.custom.hash)
         }
         TABLE base64 - {
               FUNCTION encode(<string>) - [A] (alias for syn.crypt.base64.encode)
               FUNCTION decode(<string>) - [A] (alias for syn.crypt.base64.decode)
         }
   }
   TABLE crypt [NH] - {
         FUNCTION random(<number>) - [?]
         FUNCTION derive(<string>,<number>) - [?]
         TABLE custom - {
               FUNCTION decrypt(<string>,<string>,<string>,<string>) - [?]
               FUNCTION encrypt(<string>,<string>,<string>,<string>) - [?]
               FUNCTION hash(<string>,<string>) - [?]
         }
   }
   FUNCTION request(<string> url,<string> data,<...>) - [A] (alias for game.HttpPost/game.HttpPostAsync)
   FUNCTION run_secure_function(<string>) - (used to run a Synapse X only script)
   FUNCTION create_secure_function(<string>,<string>) - (used to create a Synapse X only script; ████████████████████████)
   FUNCTION is_beta(<void>) - (returns true if Synapse X is using beta mode, false if not)
}
TABLE debug - [NH] {
   FUNCTION getstack(<number>,<number> index) - (returns the stack for the function; put "index" for a single value)
   FUNCTION setstack(<number> stackpos,<number> index,<o> value) - (sets stack at "stackpos" with "index" to "value")
   FUNCTION setupvaluename(<o>) - (sets an upvalue's name)
   FUNCTION getprotos(<function/number>) - (returns all protos)
   FUNCTION getproto(<function/number>,<number> index,<bool> activated) - (returns a specific proto)
   FUNCTION setproto(<function/number>,<number> index,<func>,<bool>) - (sets a specific proto)
}
TABLE bit32 - (some lua thing, not going to doc it since it has a lot of stuff, if you want to know more about it, search on lua.org)
TABLE Drawing - [?] (ProtoSmasher's Drawing API) {
   FUNCTION new(<string> ClassName) - (creates a new DrawObject based on the given class name and returns it)
   TABLE Fonts - [?] (this has more weird shit, not going to doc it)
}
TABLE game [NH] - {
    FUNCTION HttpGetAsync(<string> url) [A] - (alias for game.HttpGet)
    FUNCTION HttpGet(<string> url) - (returns "data" from site "url"; it is recommanded that "http://" or "https://" is used)
    FUNCTION HttpPost(<string> url,<string> data,<...>) - [B] [NR] (sends "data" to the site "url"; it is recommanded that "http://" or "https://" is used)
    FUNCTION HttpPostAsync(<string> url,<string> data,<...>) - (the fixed version of HttpPost; it is recommanded that "http://" or "https://" is used)
}
![random12](https://github.com/Tumppi66/v3rm-archive/assets/61348006/f5532085-c3d2-4e84-afef-d3cda69cc65a)
