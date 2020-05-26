# TCL/TTL scripts.
## TCL

### Overview

Tcl is shortened form of ```Tool Command Language```, where the source code of a Tcl script consists of commands. Tcl is a string based scripting language. The source code is compiled into bytecode, which is later interpreted by the Tcl interpreter. It was created by ```John Osterhout``` in 1988. The purpose was to create a language which is easily embeddable into applications. But it is often used outside its original area. The language is commonly used for rapid prototyping, scripted applications, GUIs, and testing.

Tcl is a procedural language. It has some functional features. ```OOP``` was added in ```Tcl verstion 8.6```.

The official web site for both Tcl and its Tk GUI toolkit is [tcl.tk][tcl.tk]

### Environment Setup

#### Local Environment Setup

If you are willing to set up your environment for Tcl, you need the following two software applications available on your computer:
* **Text Editor**: This will be used to type your program. Examples of a few text editors include Windows Notepad, OS Edit command, Brief, Epsilon, EMACS, and vim or vi.
* **Tcl Interpreter**: The SDK Arrive embedded TCL lib. Therefore, you can run a TCL script in that SDK with the syntax `run <path to tcl script>`. BTW, you can install TCL program on your PC also. It is just a small program that enables you to type Tcl commands and have them executed line by line. It stops execution of a tcl file, in case, it encounters an error unlike a compiler that executes fully.

Let's have a helloWorld.tcl file as follows. We will use this as a first program, we run on a platform you choose.

```tcl
#!/usr/bin/tclsh

puts "Hello World!"
```

##### Installation on Windows

Download the latest version for windows [installer][installer] from the list of Active Tcl binaries available. The active Tcl community edition is free for personal use.

Run the downloaded executable to install the Tcl, which can be done by following the on screen instructions.

Now, we can build and run a Tcl file say `helloWorld.tcl` by switching to folder containing the file using ``'cd'`` command and then execute the program using the following steps
```tcl
C:\Tcl> tclsh helloWorld.tcl
```

We can see the following output.
```tcl
C:\Tcl> helloWorld
```

`C:\Tcl` is the folder, I am using to save my samples. You can change it to the folder in which you have saved Tcl programs.

##### Installation on Linux

Most of the Linux operating systems come with Tcl inbuilt and you can get started right away in those systems. In case, it's not available, you can use the following command to download and install Tcl-Tk.
```tcl
$ yum install tcl tk
```
Now, we can build and run a Tcl file say `helloWorld.tcl` by switching to folder containing the file using ``'cd'`` command and then execute the program using the following steps −
```tcl
$ tclsh helloWorld.tcl
```
We can see the following output −
```tcl
$ hello world
```

##### Installation on Mac OS X

Download the latest version for Mac OS X [package][installer] from the list of Active Tcl binaries available. The active Tcl community edition is free for personal use.

Run the downloaded executable to install the Active Tcl, which can be done by following the on screen instructions.

Now, we can build and run a Tcl file say `helloWorld.tcl` by switching to folder containing the file using ``'cd'`` and then execute the program using the following steps −
```tcl
$ tclsh helloWorld.tcl
```
We can see the following output −
```tcl
$ hello world
```

### Syntax and fundamental semantics

The syntax and semantics of Tcl are covered by [twelve rules][twelve rules] known as the [Dodekalogue][Dodekalogue].

#### Commands

The syntax of Tcl command is as follows:
``commandName argument1 argument2 ... argumentN``

The Tcl interpreter takes each word of the sentence and evaluates it. The first word is considered to be the command. Most Tcl commands are variadic. This means that they can process variable number of arguments.

When a Tcl script is parsed the commands are evaluated. Each command interprets words in its own context.

#### The puts command

The puts command is used to print messages to the console or to other channels like a file. The command has the following syntax:
`puts ?-nonewline? ?channelId? string`

The `puts` is the command name. Optional parameters are specified between question marks.
The `-nonewline` switch suppresses the newline character. By default, the command puts a newline to each message. The `channelId` must be an identifier for an open channel such as the Tcl standard input channel `stdin`, the return value from an invocation of `open` or `socket`. It defaults to standard output channel `stdout` if not specified. Finally, the `string` is the message to be printed.

```
puts -nonewline "What is your name? " ;# The -nonewline option suppresses the newline. The prompt remains on the same line.
flush stdout ;# The output is buffered. To see the output immediately after the command runs, we can use the flush command. The stdout is the standard output. In our case it is a terminal; it is called a channel id in Tcl.
gets stdin name ;# The gets command reads a line from the standard input. The result is stored in the name variable.
puts "Hello $name" ;# Finally, we greet the user.
```

#### Substitution

There are three kinds of substitutions in Tcl.

|No. |Substitution |Main |
| ------ | ------ | ------ |
| 1 | Command substitution| square brackets are used to evaluate the scripts inside the square brackets|
| 2 |  Variable substitution | ``$`` is used before the variable name and this returns the contents of the variable. |
| 3 |  Backslash substitution | These are commonly called escape sequences; with each backslash, followed by a letter having its own meaning. |

#### Comments

Comments are used by humans to clarify source code. In Tcl comments start with the # character.
All characters after the # character are ignored by tclsh.
Inline comments are possible only if we use a semicolon.
```tcl
# example of a puts command
puts "Tcl language"; # example of a puts command
```

#### White space

White space is used to separate words in Tcl source. It is also used to improve readability of the source code.
We might use more spaces if we want to improve the clarity of the source code.

```tclsh
set age        31
set name       dangtv
set department DV
```

#### Variables

A `variable` is an identifier which holds a value. In programming we say that we assign or set a value to a variable. Technically speaking, a variable is a reference to a computer memory where the value is stored. Variable names are case sensitive. This means that `Name`, `name`, and `NAME` refer to three different variables.
Variables in Tcl are created with the set command. To obtain the value of a variable, its name is preceded with the $ character.
```tclsh
set name Dang
set Name Bang
set NAME Truong

puts $name ;# Dang
puts $Name ;# Bang
puts $NAME ;# Truong
```

#### Braces

Braces, {}, have special meaning in Tcl. Substitution of words is disabled inside braces.
* Braces can be used instead of double quotes to set strings separated by a white space.
* When using braces, the variable is not substituted. Everything is printed literally.
* Braces are used to create lists. A list is a basic data type in Tcl.
* Braces inside double quotes or inside other braces are taken as regular characters without special meaning.
```tclsh
set name {Julia Novak}
puts $name ;# Julia Novak

puts "Her name is $name" ;# Her name is Julia Novak
puts {Her name is $name} ;# Her name is $name

set numbers { 1 2 3 4 5 6 7 }
puts $numbers ;# 1 2 3 4 5 6 7

puts "Braces {} are reserved characters in Tcl" ;# Braces {} are reserved characters in Tcl
puts {Braces {} are reserved characters in Tcl} ; #Braces {} are reserved characters in Tcl
```

#### Square brackets

Square brackets, [], are used to create nested commands. These nested commands are executed before the main command on the Tcl source line. They are used to pass the result of one command as an argument to another command.

```tclsh
set cwd [pwd]
puts $cwd ;# /media/ram (Note: The pwd command returns the current working directory of the script)
```

#### Quotes

Double quotes group words as a single argument to commands. Dollar signs, square brackets, and the backslash are interpreted inside quotes.

```tcl
set distro Ubuntu
puts "The Linux distribution name is $distro" ;# The Linux distribution name is Ubuntu

puts "The current working directory: [pwd]" ;# The current working directory: /home/janbodnar/prog/tcl/lexis
puts "2000000\b\b\b miles" ;# 2000 miles
```

#### Backslash

The backslash character can be used in three different ways in Tcl. It introduces some special characters, called escape sequences. These can be newlines, tabs, backspaces among others. It escapes the meaning of special Tcl characters ($, {}, "", \, ()). Finally, it can serve as a line continuation character.

```tclsh
puts "0\t1" ;# 0       1

set name TruongPm
puts \$name ;# $name
puts \\$name ;#  \TruongPm

puts "He said: \"There are plenty of them\"" ;# He said: "There are plenty of them"
puts "There are currently many Linux\
distributions in the world" ; # There are currently many Linux distributions in the world
```

#### Round brackets

Round brackets are used to indicate an array subscript or to change the precedence of operators for the expr command.

```tclsh
set names(1) Truong
set names(2) Bang

puts $names(1) ;# Truong
puts $names(2) ;# Bang

puts [expr (1+3)*5] ;# 20
```

### Basic commands

The most important commands that refer to program execution and data operations are:
* ```set``` writes a new value to a variable (creates a variable if did not exist). If used only with one argument, it returns the value of the given variable (it must exist in this case).
* ```proc``` defines a new command, whose execution results in executing a given Tcl script, written as a set of commands. `return` can be used to immediately return control to the caller.

The usual execution control commands are:
* ```if``` executes given script body (second argument), if the condition (first argument) is satisfied. It can be followed by additional arguments starting from `elseif` with the alternative condition and body, or `else` with the complementary block.
* ```while``` repeats executing given script body, as long as the condition (first argument) remains satisfied
* ```foreach``` executes given body where the control variable is assigned list elements one by one.
* ```for``` shortcut for initializing the control variable, condition (as in `while`) and the additional "next iteration" statement (command executed after executing the body).

Those above looping commands can be additionally controlled by the following commands:
* ```break``` interrupts the body execution and returns from the looping command
* ```continue``` interrupts the body execution, but the control is still given back to the looping command. For `while` it means to `loop` again, for for and `foreach`, pick up the next iteration.
* ```return``` interrupts the execution of the current body no matter how deep inside a procedure, until reaching the procedure boundary, and returns given value to the caller.


### Advanced commands

* `expr` passes the argument to a separate expression interpreter and returns the evaluated value. Note that the same interpreter is used also for "conditional" expression for `if` and looping commands.
* `list` creates a `list` comprising all the arguments, or an empty string if no argument is specified. The lindex command may be used on the result to re-extract the original arguments.
* `array` manipulates `array` variables.
* `dict` manipulates dictionary `(since 8.5)`, which are lists with an even number of elements where every two elements are interpreted as a key/value pair.
* `regexp` matches a regular expression against a string.
* `uplevel` is a `command` that allows a command script to be executed in a scope other than the current innermost scope on the stack.
* `upvar` creates a link to variable in a different stack frame.
* `namespace` lets you create, access, and destroy separate contexts for commands and variables.
* `apply` applies an anonymous function (since 8.6).
* `coroutine`, `yield`, and `yieldto` create and produce values from coroutines `(since 8.6)`.
* `try` lets you trap and process errors and exceptions.
* `catch` lets you trap exceptional returns.
* `zlib` provides access to the compression and checksumming facilities of the Zlib library `(since 8.6)`.

### How to use TCL script in Arrive SDK

Arrive SW is embedded the TCL `(version 8.5)` in the SDK. We can use that language to create a script file (configure, check) and run it in that SDK with the syntax: `tcl <tcl script file>`.

We must add prefix name `atsdk::` before the CLI configure in TCL script.

By the way, SW is support process table in the SDK. You can use it as below:
```
* Clone global table    : atsdk::table cloneGlobalTable ?var_showtable_id?
* Get row size          : atsdk::table rowSize          ?<tableid>? ?var_row_size?
* Get column size       : atsdk::table columnSize       ?<tableid>? ?var_col_size?
* Get cell content      : atsdk::table cellContent      ?<tableid>? ?var_row? ?var_col? ?var_value?
* Iterate cells in table: atsdk::table foreach          ?<tableid>? ?var_row? ?var_col? ?var_value? ?script?
* Destroy table         : atsdk::table destroyTable     ?<tableid>?
* Get table row         : atsdk::table row              ?<tableid>? ?rowid? ?listname?
* Get table column      : atsdk::table column           ?<tableid>? ?columnName? ?listname?
```
We can use `atsdk::rd <register Id>` to get value of a register, it will return a decimal value.

If a function is use many times, we should define a common database file for that and use `source` to call it.

Here is a basic configure the normal traffic with `CEM (SONET/SDH Circuit Emulation Service Over MPLS)` and use `PRBS (Pseudo Random Bit Sequence) pattern` to check that traffic (That is a configure on [MRO Ciena product][ciena_pts_6500]. We should check full layers: Line, path, Pw, BERT. But, I will check only bert layer in this document to compact. You can refer to it and apply it similarly to other layers):

```
#<><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><>
# Normal traffic with BERT
#<><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><>
proc configure_normalTraffic_oc48sts48c_cem {} {
	# Initialize device
	atsdk::device init

	# Configure Line.
	atsdk::serdes mode 1,3,5,7,9,11,13,15 stm16
	atsdk::serdes powerup 1,3,5,7,9,11,13,15
	atsdk::serdes enable 1-16
	atsdk::sdh line mode 1,3,5,7,9,11,13,15 sonet
	atsdk::sdh line rate 1,3,5,7,9,11,13,15 stm16

	# Configure mapping
	atsdk::sdh map aug16.1.1-16.1,25.1-32.1 vc4_16c
	atsdk::sdh map vc4_16c.1.1-16.1,25.1-32.1 c4_16c

	# TSI
	atsdk::xc vc connect vc4_16c.1.1-16.1 vc4_16c.25.1-32.1 two-way

	# Configure paths
	atsdk::sdh path psl transmit vc4_16c.1.1-16.1 0xFE
	atsdk::sdh path psl expect vc4_16c.1.1-16.1 0xFE
	atsdk::sdh path tti monitor disable vc4_16c.1.1-16.1

	# Setup PWs
	atsdk::pw create cep 1-8 basic
	atsdk::pw psn 1-8 mpls
	atsdk::eth port enable 1
	atsdk::eth port maccheck 1 dis
	atsdk::pw ethport 1-8 1
	atsdk::pw jitterbuffer 1-8 4000
	atsdk::pw jitterdelay 1-8 2000
	atsdk::pw circuit bind 1-8 vc4_16c.25.1-32.1
	atsdk::pw enable 1-8


	# Create BERT (PRBS engine)
	atsdk::prbs engine create vc 1-8 vc4_16c.25.1-32.1
	atsdk::prbs engine side monitoring 1-8 psn
	atsdk::prbs engine enable 1-8

	# Loopback at backplane
	atsdk::serdes loopback 25,26 local

	# Loopback at faceplate
	atsdk::serdes loopback 1-16 local
}
#<><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><>
# Clear And Check BERT Status
#<><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><>
proc clear_prbsEngine {engineId} {
	atsdk::show prbs engine $engineId
	atsdk::show prbs engine counters $engineId r2c
}
proc check_bert_alarmSticky {} {
#AT SDK >show prbs engine 1
#+--------+--------------+-------+-------+------------+------------+------+----------+---------+---------+----------+----------+-----+--------+-------+-------+
#|        |              |       |       |            |            |      |          |         |         |          |          |     |        |       |       |
#|engineId|channel       |txMode |rxMode |txFixPattern|rxFixPattern|invert|forceError|txEnabled|rxEnabled|txBitOrder|rxBitOrder|alarm|sticky  |genSide|monSide|
#|        |              |       |       |            |            |      |          |         |         |          |          |     |        |       |       |
#+--------+--------------+-------+-------+------------+------------+------+----------+---------+---------+----------+----------+-----+--------+-------+-------+
#|1       |vc4_16c.25.1  |prbs15 |prbs15 |N/A         |N/A         |dis   |dis       |en       |en       |msb       |msb       |none |lossSync|tdm    |tdm    |
#+--------+--------------+-------+-------+------------+------------+------+----------+---------+---------+----------+----------+-----+--------+-------+-------+
	set globalTable 0
	atsdk::show prbs engine $engineId
	atsdk::table foreach $globalTable row columnName counterValue {
		if {$columnName == "alarm"	&& $counterValue != "none"}	{return 0}
		if {$columnName == "sticky"	&& $counterValue != "none"} {return 0}
	}
	return 1
}
proc check_bert_counter {} {
#AT SDK >show prbs engine counters 1 ro
#+--------------+--------+-------+---------+-------+-----+----------+-------------+------------------+---------+------+-----------+------------+
#|              |        |       |         |       |     |          |             |                  |         |      |           |            |
#|Channel       |engineId|txFrame|TxBit    |rxFrame|RxBit|RxBitError|RxBitLastSync|RxBitErrorLastSync|RxSync   |RxLoss|RxLostFrame|RxErrorFrame|
#|              |        |       |         |       |     |          |             |                  |         |      |           |            |
#+--------------+--------+-------+---------+-------+-----+----------+-------------+------------------+---------+------+-----------+------------+
#|vc4_16c.25.1  |1       |N/A    |370834808|N/A    |N/A  |93        |N/A          |N/A               |143827139|0     |N/A        |N/A         |
#+--------------+--------+-------+---------+-------+-----+----------+-------------+------------------+---------+------+-----------+------------+
	set globalTable 0
	atsdk::show prbs engine counters $engineId ro
	atsdk::table foreach $globalTable row columnName counterValue {
		if {$columnName == "TxBit"		&& $counterValue == 0} {return 0}
		if {$columnName == "RxBit"		&& $counterValue == 0} {return 0}
		if {$columnName == "RxSync"		&& $counterValue == 0} {return 0}

		if {$columnName == "RxBitError"	&& $counterValue != 0} {return 0}
		if {$columnName == "RxLoss"		&& $counterValue != 0} {return 0}
	}
	return 1
}
proc clear_and_check_prbs_engine {engineId} {
	# Clear BERT
	clear_prbsEngine $engineId
	# Delay 1s before check
	after 1000
	# Check Status
	if {![check_bert_alarmSticky] || ![check_bert_counter]} {
		return 0 ;# FAILED
	}

	return 1 ;# PASSED
}

#<><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><>
# Main
#<><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><>
proc Main {} {
	set engineId "1-8"
	# Setup data flow
	configure_normalTraffic_oc48sts48c_cem
	# Delay 1s before check
	after 1000
	# Check Status
	if {![clear_and_check_prbs_engine $engineId]} {
		return 0 ;# FAILED
	}

	return 1 ;# PASSED
}

#<><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><>
# Run
#<><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><>
proc input_ntimes {} {
	puts "\fGUIDE FOR USE: "
	puts "------------------------------------------------------------------------------------------"
	puts "|1. Input == \"Enter\"	-> Output = \"1 (Default)\" "
	puts "|2. Input >= 1 		 	-> Output = \"Input\" "
	puts "|3. Input == 0 			-> Output = \"Pause script\" "
	puts "------------------------------------------------------------------------------------------"
	puts -nonewline [commonColor_printColorForeground "yellow" "Enter nTimes to use: "
	flush stdout; set input [gets stdin
	if {$input == ""} {return 1}
	if {$input >= 0} {return $input}
	input_ntimes
}

set nTimes [input_ntimes]
for {set ntime 1} {$ntime <= $nTimes} {incr ntime} {
	if {![Main]} {
		puts "\033\31mThe Test-case was FAILED, with time: $ntime\033\[0m"
		return
	}

}

puts "\033\32mThe Test-case was PASSED, with time: $nTimes\033\[0m"

```

## TTL script

Tera Term is an opensource terminal emulator on MS-Windows commonly used by us developers. Tera Term supports a "rich" macro language that can help in automating user actions. These scripts usually remain personal.
In the Arrive lab, you can use this language to automation boot a system, or control SDK CLIs (In case, some products embedded Arrive SDK without TCL library).

TTL is a simple interpreted language like BASIC. To learn TTL quickly, study the sample macro files in the distribution package and the [command reference][ttl_command_reference].

You can get the [latest version][ttl_install] and install it on the Window OS. Follow [How to execute a TeraTerm script][execute_ttl],... to use it.

Here is a sample script to boot the Cisco router in the Arrive lab (Only use basic syntax `wait` and `sendln` to configure it):

```TeraTerm
;;  ============================================================================
;;  HISTORY
;;
;;      2019-Aug-25                      dangtv
;;          DV Team-Arrive tech
;;  ============================================================================


;;  ============================================================================
;;  Parameter
;;  ============================================================================
dirUsb = "dir bootflash:"
imageBoot = "u-boot_signed.bin"

ip_dec = "172.33.42.144"
ip_hex = "00:04:9f:03:05:90"

rsp3Image = "rsp3net_903_noAtInit"

;;  ============================================================================
;;  Run
;;  ============================================================================
;; 	1. Boot Linux OSyoutubw
wait ">"
sendln dirUsb

wait ">"
sendln "boot bootflash:"imageBoot

wait "=>"
sendln "usb start"

wait "=>"
sendln "ext2ls usb 0:1"

wait "=>"
sendln "ext2load usb 0:1 0x3000000 uImage-t1040rdb.bin"

wait "=>"
sendln "ext2load usb 0:1 0x7000000 fsl-image-core-t1040rdb.ext2.gz.u-boot"

wait "=>"
sendln "ext2load usb 0:1 0x5000000 warrior.dtb"

wait "=>"
sendln "bootm 0x3000000 0x7000000 0x5000000"

wait "t1040rdb login:"
sendln "root"

;; 	2. Config IP
wait "root@t1040rdb:~#"
sendln "ifconfig eth3 "ip_dec" netmask 255.255.224.0"
wait "root@t1040rdb:~#"
sendln "ifconfig eth3 down"
wait "root@t1040rdb:~#"
sendln "ifconfig eth3 hw ether "ip_hex
wait "root@t1040rdb:~#"
sendln "ifconfig eth3 up"
pause 5

;;	3. Login TFTP server and get files set-up
wait "root@t1040rdb:~#"
sendln "cd /media/ram"

wait "root@t1040rdb:/media/ram#"
sendln "ftp 172.33.39.6"
wait "Name (172.33.39.6:root):"
sendln "ftp"
wait "Password:"
sendln "ftp"

wait "ftp>"
sendln " cd /af6cci0011/working/sdk/reboot_cisco/sdk/"
wait "ftp>"
sendln "get bheem_v200100D1.bin"
wait "ftp>"
sendln "get flex_fw_app_alpha_0701.mem"
wait "ftp>"
sendln "get im_mmap_150820.ko"

wait "ftp>"
sendln "cd /af6cci0071/working/rsp3"
wait "ftp>"
sendln "get "rsp3Image
wait "ftp>"
sendln "get config.bcm"
wait "ftp>"
sendln "get cint_cisco_vlan.c"
;;wait "ftp>"
;;sendln "get im_10g_ms_top_x1_working_v0_14.bin"
;;sendln "get im_10g_ms_top_x1_working_v0_x39.bin"

wait "ftp>"
sendln "by"

wait "root@t1040rdb:/media/ram#"
sendln "cp /home/root/asr903/bheem_ASR903_v00020000_0_with_blank.bin /media/ram/"
wait "root@t1040rdb:/media/ram#"
sendln "cp /home/root/* ."
wait "root@t1040rdb:/media/ram#"
sendln "cp /home/root/asr903/* ."

wait "root@t1040rdb:/media/ram#"
sendln "insmod im_mmap_150820.ko"
wait "root@t1040rdb:/media/ram#"
sendln "rm -rf insmod im_mmap_150820.ko"
wait "root@t1040rdb:/media/ram#"
sendln "rm -rf mmap.ko"

wait "root@t1040rdb:/media/ram#"
sendln "chmod +x "rsp3Image

wait "root@t1040rdb:/media/ram#"
sendln "rm -rf rsp3net_903.gz"
wait "root@t1040rdb:/media/ram#"
;;sendln "chmod +x im_10g_ms_top_x1_working_v0_x39.bin config.bcm"
sendln "chmod +x config.bcm bheem_ASR903_v00020000_0_with_blank.bin cint_cisco_vlan.c"

;; 	4. Config to telnet router
wait "root@t1040rdb:/media/ram#"
sendln 'echo "telnet          stream  tcp     nowait  root    /usr/sbin/telnetd telnetd -i" >> /etc/inetd.conf'
wait "root@t1040rdb:/media/ram#"
sendln "inetd"

```

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)
[tcl.tk]:<http://tcl.tk/>
[twelve rules]:<http://www.tcl.tk/man/tcl/TclCmd/Tcl.htm>
[Dodekalogue]:<https://wiki.tcl-lang.org/page/Dodekalogue>
[installer]:<https://www.activestate.com/activetcl/downloads>
[ciena_pts_6500]:<https://media.ciena.com/documents/6500_PTS_Packet_Transport_System_DS.pdf>
[ttl_command_reference]:<https://ttssh2.osdn.jp/manual/4/en/macro/command/index.html>
[ttl_install]:<https://ttssh2.osdn.jp/index.html.en>
[execute_ttl]:<https://processors.wiki.ti.com/index.php/Teraterm_Scripts>
