; NSIS Script - Comanche Gold (Full Install) with Desktop Shortcut

!define PRODUCT_NAME "Comanche Gold"
!define PRODUCT_VERSION "1.0"           ; Assume 1.0, update if exact version is known
!define PRODUCT_PUBLISHER "Novalogic"
!define MAIN_EXECUTABLE "Wc3.exe"       
!define UNINSTALL_NAME "Uninstall Comanche Gold"

;--------------------------------
; General Settings
Name "${PRODUCT_NAME} ${PRODUCT_VERSION} (Full Install)"
OutFile "ComancheGold_Setup.exe"

; Set installation directory
InstallDir "$PROGRAMFILES\Novalogic\${PRODUCT_NAME}"
InstallDirRegKey HKLM "Software\Microsoft\Windows\CurrentVersion\Uninstall\${PRODUCT_NAME}" "InstallLocation"

RequestExecutionLevel admin
SetCompressor zlib

;--------------------------------
; Pages
Page directory
Page instfiles

;--------------------------------
; Section: Full Installation (46 Files)

Section "Comanche Gold Full Installation" SecFull
  
  SetOutPath "$INSTDIR"

  ; --- Core Executables and Data ---
  File "SourceFiles\Novawrld.exe"
  File "SourceFiles\${MAIN_EXECUTABLE}" ; Wc3.exe
  File "SourceFiles\Editor.exe"
  File "SourceFiles\Pack.exe"
  File "SourceFiles\Msvcrt.dll"
  File "SourceFiles\Netsock.dll"
  File "SourceFiles\Wsetup.cfg"
  File "SourceFiles\readme.txt"
  File "SourceFiles\Startup.htm"
  File "SourceFiles\Browser.htm"
  
  ; --- Primary Game Files (Corrected .pff file) ---
  File "SourceFiles\Cgold.pff"
  File "SourceFiles\Resource.pff"
  File "SourceFiles\Template.smo"
  File "SourceFiles\C3.nam"
  File "SourceFiles\C3.SAV"
  File "SourceFiles\epass.bin"
  
  ; --- Graphics and Config ---
  File "SourceFiles\Texture.pcx"
  File "SourceFiles\Nwlogo.pcx"
  File "SourceFiles\Texture.gif"
  File "SourceFiles\Nwlogo.gif"
  File "SourceFiles\Nw.cfg"
  
  ; --- DirectX Components (ddraw.dll REMOVED) ---
  File "SourceFiles\DPLAY.DLL"
  File "SourceFiles\DPLAY.INF"
  File "SourceFiles\DPLAYX.DLL"
  
  ; --- KDV Video Files ---
  File "SourceFiles\HINTRO.KDV"
  File "SourceFiles\HOVRVIEW.KDV"
  File "SourceFiles\H_AIR.KDV"
  File "SourceFiles\H_AMC.KDV"
  File "SourceFiles\H_CAM.KDV"
  File "SourceFiles\H_DSC.KDV"
  File "SourceFiles\H_IND.KDV"
  File "SourceFiles\H_KYR.KDV"
  File "SourceFiles\H_MON.KDV"
  File "SourceFiles\H_MSM.KDV"
  File "SourceFiles\H_SAK.KDV"
  File "SourceFiles\H_SLS.KDV"

  ; --- Utilities, Menus, and Documentation ---
  File "SourceFiles\CGoldIP.exe"
  File "SourceFiles\CGoldIPH.cmd"
  File "SourceFiles\CGoldIPJ.cmd"
  File "SourceFiles\Editor.pdf"
  File "SourceFiles\manual.pdf"
  File "SourceFiles\ReadmeCGOLDIP.txt"
  File "SourceFiles\reference.pdf"
  File "SourceFiles\Revupdat.exe"
  File "SourceFiles\Setup.CD"
  File "SourceFiles\Uninst.isu"
  File "SourceFiles\Update.exe"
  File "SourceFiles\Update.inf"
  File "SourceFiles\Update.wiz"
  File "SourceFiles\WC3.MNU"

  ; --- Shortcuts ---
  ; Create Desktop Shortcut for the main executable
  CreateShortCut "$DESKTOP\${PRODUCT_NAME}.lnk" "$INSTDIR\${MAIN_EXECUTABLE}"
  
  ; --- Registry and Uninstaller Setup ---
  WriteUninstaller "$INSTDIR\Uninstall.exe"
  WriteRegStr HKLM "Software\Microsoft\Windows\CurrentVersion\Uninstall\${PRODUCT_NAME}" "DisplayName" "${UNINSTALL_NAME}"
  WriteRegStr HKLM "Software\Microsoft\Windows\CurrentVersion\Uninstall\${PRODUCT_NAME}" "UninstallString" "$INSTDIR\Uninstall.exe"
  WriteRegStr HKLM "Software\Microsoft\Windows\CurrentVersion\Uninstall\${PRODUCT_NAME}" "Publisher" "${PRODUCT_PUBLISHER}"
  WriteRegStr HKLM "Software\Microsoft\Windows\CurrentVersion\Uninstall\${PRODUCT_NAME}" "DisplayVersion" "${PRODUCT_VERSION}"
  WriteRegStr HKLM "Software\Microsoft\Windows\CurrentVersion\Uninstall\${PRODUCT_NAME}" "InstallLocation" "$INSTDIR"

SectionEnd

;--------------------------------
; Uninstallation

Section "Uninstall"
  
  ; Delete All Installed Files (Reverse order for cleanliness)
  Delete "$INSTDIR\WC3.MNU"
  Delete "$INSTDIR\Update.wiz"
  Delete "$INSTDIR\Update.inf"
  Delete "$INSTDIR\Update.exe"
  Delete "$INSTDIR\Uninst.isu"
  Delete "$INSTDIR\Setup.CD"
  Delete "$INSTDIR\Revupdat.exe"
  Delete "$INSTDIR\reference.pdf"
  Delete "$INSTDIR\ReadmeCGOLDIP.txt"
  Delete "$INSTDIR\manual.pdf"
  Delete "$INSTDIR\Editor.pdf"
  Delete "$INSTDIR\CGoldIPJ.cmd"
  Delete "$INSTDIR\CGoldIPH.cmd"
  Delete "$INSTDIR\CGoldIP.exe"
  Delete "$INSTDIR\H_SLS.KDV"
  Delete "$INSTDIR\H_SAK.KDV"
  Delete "$INSTDIR\H_MSM.KDV"
  Delete "$INSTDIR\H_MON.KDV"
  Delete "$INSTDIR\H_KYR.KDV"
  Delete "$INSTDIR\H_IND.KDV"
  Delete "$INSTDIR\H_DSC.KDV"
  Delete "$INSTDIR\H_CAM.KDV"
  Delete "$INSTDIR\H_AMC.KDV"
  Delete "$INSTDIR\H_AIR.KDV"
  Delete "$INSTDIR\HOVRVIEW.KDV"
  Delete "$INSTDIR\HINTRO.KDV"
  Delete "$INSTDIR\DPLAYX.DLL"
  Delete "$INSTDIR\DPLAY.INF"
  Delete "$INSTDIR\DPLAY.DLL"
  Delete "$INSTDIR\Nw.cfg"
  Delete "$INSTDIR\Nwlogo.gif"
  Delete "$INSTDIR\Nwlogo.pcx"
  Delete "$INSTDIR\Texture.gif"
  Delete "$INSTDIR\Texture.pcx"
  Delete "$INSTDIR\epass.bin"
  Delete "$INSTDIR\C3.SAV"
  Delete "$INSTDIR\C3.nam"
  Delete "$INSTDIR\Template.smo"
  Delete "$INSTDIR\Resource.pff"
  Delete "$INSTDIR\Cgold.pff"
  Delete "$INSTDIR\Browser.htm"
  Delete "$INSTDIR\Startup.htm"
  Delete "$INSTDIR\readme.txt"
  Delete "$INSTDIR\Wsetup.cfg"
  Delete "$INSTDIR\Netsock.dll"
  Delete "$INSTDIR\Msvcrt.dll"
  Delete "$INSTDIR\Pack.exe"
  Delete "$INSTDIR\Editor.exe"
  Delete "$INSTDIR\${MAIN_EXECUTABLE}"
  Delete "$INSTDIR\Novawrld.exe"
  
  ; Delete Shortcut
  Delete "$DESKTOP\${PRODUCT_NAME}.lnk"
  
  ; Delete Uninstaller and Registry Keys
  Delete "$INSTDIR\Uninstall.exe"
  RMDir "$INSTDIR"
  RMDir "$PROGRAMFILES\Novalogic"
  
  DeleteRegKey HKLM "Software\Microsoft\Windows\CurrentVersion\Uninstall\${PRODUCT_NAME}"
SectionEnd
