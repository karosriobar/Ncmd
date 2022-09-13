[![Board Status](https://dev.azure.com/oscarbarrio-ferreiro/ca6e0121-de54-4cda-ae0c-c1b695920728/0cfbfc9d-f212-4b74-b206-b7c5acb715c1/_apis/work/boardbadge/32bc080a-2edf-4d5d-8a41-813264db7d7f)](https://dev.azure.com/oscarbarrio-ferreiro/ca6e0121-de54-4cda-ae0c-c1b695920728/_boards/board/t/0cfbfc9d-f212-4b74-b206-b7c5acb715c1/Microsoft.RequirementCategory)
# Ncmd
A library to support standard command line options on .NET programs

Initial specs
----------------------------------------------------------------------------------------
  - Create automatically a functional command line support class for main application
  - Commands and options must be defined using an external text file (format TBD)
  - Command line syntaxis must match standard cmd syntax (i.e. https://technet.microsoft.com/en-us/library/cc771080(v=ws.11).aspx)
  - Tool must can autogenerate the help command and show it using default output console
  - Tool API must provide a way to link each command with the specific method to be executed wen user use it


Basic command line syntax
----------------------------------------------------------------------------------------
<table>
  <tr>
    <th>Text without brackets or braces</th><th>Items you must type as shown</th>
  </tr>
  
  <tr>
    <th>&lt;Text inside angle brackets&gt</th><th>Placeholder for which you must supply a value</th>
  </tr>
  
  <tr>
    <th>[Text inside square brackets]</th><th>Optional items</th>
  </tr>
  
  <tr>
    <th>{Text inside braces}</th><th>Set of required items; choose one</th>
  </tr>
  
  <tr>
    <th>Vertical bar (|)</th><th>Separator for mutually exclusive items; choose one</th>
  </tr>
  
  <tr>
    <th>Ellipsis (...)</th><th>Items that can be repeated</th>
  </tr>
</table>

  - i.e.: attrib [{+|-}r] [{+|-}a] [{+|-}s] [{+|-}h] [{+|-}i] [<Drive>:][<Path>][<FileName>] [/s [/d] [/l]]
  - i.e.: append [[<Drive>:]<Path>[;...]] [/x[:on|:off]] [/path:[:on|:off] [/e]
