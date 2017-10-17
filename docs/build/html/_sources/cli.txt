=============================
Command-Line Interface (CLI)
=============================

.. contents::
   :local:
   :depth: 1

Command-line interface (CLI) គឺជាinterfaceសំរាប់អ្នកប្រើប្រាស់ ក្នុងការconfiguring, monitoring​ ហើយនឹង​maintainingឧបករណ៍Cisco។ User interfaceនេះអនុញ្ញាតអោយអ្នកមានភាពងាយស្រួលក្នុងការអនុវត្តផ្ទាល់ និងប្រតិបត្តិការបញ្ជា Cisco IOS (execute Cisco IOS commands) មិនថាឡើយប្រើrouter console ឫ terminal ឫremote access នោះទេ។

Primary Command Mode
---------------------

នៅក្នុងការconfigure ឧបករណ៍Cisco, Cisco IOS command-line interfaceត្រូវបានបែងចែកជាច្រើនប្រភេទ(command modes)។ 

User EXEC​ mode
----------------

នៅពេលដែលអ្នកចាប់ផ្ដើមដំណើរការrouterដំបូង ជាធម្មតាគឺអ្នកចាប់ផ្ដើមដោយ `user EXEC mode` ។ នៅជាUser EXEC modeអនុញ្ញាតអោយអ្នកមានសិទ្ធត្រឹមតែmonitoring commandsមួយចំនួនតែប៉ុណ្ណោះ ហើយភាគច្រើនវាសំដៅទៅលើmode​ដែលមើលតែប៉ុណ្ណោះ(view-only mode)។

Access Method: log in (user + password)

Promt>

Exit Method: logout


Privileged EXEC mode
---------------------

Access Method: ពីuser EXEC modeប្រើcommand `enable`

Promt: Route#

Exit Method: disable


Global configuration mode
--------------------------

Access Method: configure terminal ពីprivileged EXEC command

Promt: Router(config)#

Exit Method: type `end` or Ctrl+Z


Interface configuration
------------------------

Access Method: ពីglobal configuration modeវាបញ្ចូល interface ជាមួយនឹងinterfaceជាក់លាក់ណាមួយ

Promt: Router(config-if)

Exit Method: type `end` or Ctrl+Z

Subinterface configuration
---------------------------
Promt: Router(config-subif)#
