### Using CHCCLP
> [!NOTE]
> CHCCLP command can be run interactively, batch with script, or imbedded in Java.  
> Use [java](https://github.com/DimSumDev/replication/tree/main/cdc/chcclp/java) subfolder for Java information  
> Run `chcclp` (windows) or `./chcclp` linux frm the bin directory of the Access server or  Management Console machine  
> Use [Issues](https://github.com/DimSumDev/replication/issues) to search for chcclp comand usage and example  

### Using chcclp in batch mode `chcclp -f <file name>`
```sh
  [-i]            Starts the command line processor in interactive mode.
  [-f <filename>] Executes a series of commands from file. Specify the fully qualified path to the file.
  [-L <locale>]   Specifies the locale.
  [-a]            Starts the command line processor with embedded Access Server which runs on default port 10101.
  [-ap <port>]    Starts the command line processor with embedded Access Server which runs on specified port.
  [-log <folder>] Specifies the log folder location when the command line processor runs with embedded Access Server.
  [key:value]*    Specifies one or more key/value pairs where the key is used in the script
                  as %key%. At runtime, the value is substituted. A key can appear
                  multiple times in the file.
  [-b]            Suppresses the interactive session banner.
  [-e]            Echos the command when the interactive prompt receives all input at once.
  [-la <address>] Specifies the local address to bind a socket when establishing connections to Access Server. When not specified, the OS will determine the network interface.
  [-lp <port>]    Specifies the port number for the connection to Access Server. When not specified, the OS will select any open port.
```

### chcclp interactive comands
```sh
For more information on a specific command, type help "command";  
  
ENVIRONMENT  
----------------------------------------------------------------------------  
chcclp session set to cdc                   clear context   
exit                                        help  
print                                       quit  
save session                                set debug  
set property                                set variable  
set verbose                                 show context  
show session                                show variables  
show version  
  
ACCESS SERVER  
----------------------------------------------------------------------------  
connect server                              disconnect server  
modify server                               show server  
export audit log  
  
DATASTORES  
----------------------------------------------------------------------------  
add system parameter                        connect datastore  
define external target datastore            delete system parameter  
disconnect datastore                        list database tables  
list database schemas                       list databases  
list datastores                             list datatypes  
list encodings                              list journal control fields  
list system parameters                      modify system parameter  
select datastore                            show datastore  
  
TABLES  
----------------------------------------------------------------------------  
add replication table                       list index columns  
list replication tables                     list table columns  
list table indexes                          readd replication table  
remove replication table  
  
SUBSCRIPTIONS  
----------------------------------------------------------------------------  
add subscription                            delete subscription  
describe subscription                       export datastage job definition  
export subscription                         import subscription  
list subscriptions                          list subscription lock history    
lock subscription                           modify latency thresholds  
modify subscription                         modify subscription datastage properties  
modify subscription cloudant properties     modify subscription kafka properties  
modify subscription hadoop properties       modify subscription publishing properties  
modify subscription user exit               promote subscription  
select subscription                         show latency thresholds  
show subscription                           show subscription datastage properties  
show subscription cloudant properties       show subscription kafka properties  
show subscription hadoop properties         show subscription publishing properties  
show subscription user exit                 unlock subscription  
update subscription target  
  
TABLE MAPPINGS/RULE SETS  
----------------------------------------------------------------------------  
add rule set                                add table mapping  
delete rule set                             delete table mapping  
export rule set                             export table mapping  
filter table member                         flag refresh  
list refresh order                          list rule set tables  
list rule sets                              list table mappings  
list table members                          mark capture point  
modify refresh order                        modify rule set  
modify table mapping                        park table mapping  
promote rule set                            promote table mapping  
reassign table mapping                      select rule set  
select table mapping                        show rule set  
show table mapping  
  
MAPPING DETAILS  
----------------------------------------------------------------------------  
add data translation                        add derived column  
clear user exit                             delete data translation  
delete derived column                       filter source column  
list column encodings                       list column mappings   
list source columns                         map column  
modify column encoding                      modify data translation   
modify derived column                       modify operations  
modify user exit cdll                       modify user exit function  
modify user exit javaclass                  modify user exit storedproc  
show data translation                       show derived column  
show operations                             show user exit   
unmap column  
  
NOTIFICATIONS  
----------------------------------------------------------------------------
list datastore notification categories      list datastore notification filters  
list datastore notification settings        list subscription notification categories  
list subscription notification settings     modify datastore notification filters  
modify datastore notification settings      modify subscription notification settings  
  
REPLICATION  
----------------------------------------------------------------------------  
clear datastore events                      clear subscription events  
end replication                             export subscription performance snapshot  
list datastore events                       list subscription events  
list subscription performance metrics       list table performance metrics  
monitor replication                         monitor subscription activity  
monitor subscription busy tables            monitor subscription latency  
monitor subscription performance            monitor subscription refresh  
monitor table performance                   show datastore event details  
show subscription event details             start mirroring    
start refresh  
  
ACCESS MANAGER  
----------------------------------------------------------------------------  
add access connection                       add access datastore  
add access user                             add ldap access manager  
change login password                       close access user connections  
delete access connection                    delete access datastore  
delete access user                          list access connections  
list access datastores                      list access users  
modify access connection                    modify access datastore  
modify access user                          show access connection  
show access datastore                       show access user  
  
SUPPORT  
----------------------------------------------------------------------------  
run support assistant   
```
