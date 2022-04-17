# FileGetAttrib
$sTmp = _IsDir('Folder') ; $sTmp = _IsDir('C:WINDOWS') ; $sTmp = _IsDir('C:Boot.ini') If Not (@error Or $sTmp) Then     MsgBox(0, ';)', 'File') ElseIf $sTmp Then     MsgBox(0, ';)', 'Folder') Else     MsgBox(0, ';)', 'Error') EndIf  Func _IsDir($sTmp)     $sTmp = FileGetAttrib($sTmp)     Return SetError(@error, 0, StringInStr($sTmp, 'D', 2) > 0) EndFunc
