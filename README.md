#!url=https://raw.githubusercontent.com/DungHoang120401/Nobita/refs/heads/main/Module/Locket_Gold_Nobita.sgmodule
#!name=Locket Gold (NTT)
#!desc=By: NTT 

[Script]

revenuecat = type=http-response, pattern=^https:\/\/api\.revenuecat\.com\/.+\/(receipts$|subscribers\/[^/]+$), script-path=https://raw.githubusercontent.com/DungHoang120401/Nobita/refs/heads/main/Scripts/Locket_Gold.js, requires-body=true, max-size=-1, timeout=60

deleteHeader = type=http-request, pattern=^https:\/\/api\.revenuecat\.com\/.+\/(receipts|subscribers), script-path=https://raw.githubusercontent.com/DungHoang120401/Nobita/refs/heads/main/Scripts/LKG_delete_header.js, timeout=60

[MITM]
hostname = %APPEND% api.revenuecat.com
