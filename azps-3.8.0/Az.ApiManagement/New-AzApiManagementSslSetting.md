---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: 709e8483a5f21e3afc58add1046b5dae22bea7b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097687"
---
# New-AzApiManagementSslSetting

## SYNOPSIS
PsApiManagementSslSetting örneği oluşturur

## INDEKI

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
Bir PsApiManagementSslSetting örneği oluşturmak için yardımcı komutu.
Bu komut New-AzApiManagement komutuyla kullanılır.

## ÖRNEKLERDEN

### Örnek 1: TLS 1,0 hem arka uç hem de ön uçta etkinleştirmek için SSL ayarı oluşturma
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

Psapsananagementssl1,0 Setting 'in hem ön uç (istemci ve APıM arasında) hem de arka uç (APıM ve arka uç arasında) ile Apsananaağ geçidi

## PARAMETRELERINE

### -BackendProtocol
Arka uç güvenlik protokolü ayarları. Bu parametre isteğe bağlıdır.
Geçerli protokol ayarları: `Tls11` -tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CipherSuite
Belirtilen düzende SSL şifre paketleri ayarları. Bu parametre isteğe bağlıdır.
Geçerli ayarlar şunlardır: `TripleDes168` üç durumlu PE Des 168

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Frontenvseçprotocol
Ön uç güvenlik iletişim kuralları ayarları. Bu parametre isteğe bağlıdır.
Geçerli protokol ayarları: `Tls11` -tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0


```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerProtocol
Http2 gibi sunucu protokolü ayarları. Bu parametre isteğe bağlıdır.
Geçerli ayarlar şunlardır: `Http2` Http 2,0

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. apsananad

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-azlı bir](./New-AzApiManagement.md)

