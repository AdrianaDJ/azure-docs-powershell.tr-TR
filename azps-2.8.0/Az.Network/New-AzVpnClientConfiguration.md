---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: 388275b4b182c9f9f054ba4965deebfb2c08556a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918171"
---
# New-AzVpnClientConfiguration

## SYNOPSIS
Bu komut, kullanıcıların VPN ağ geçidinde önceden yapılandırılmış VPN ayarları temelinde, örneğin bazı kök sertifikaları için kullanıcıların yapılandırması gerekebilecek bazı ek ayarlara ek olarak VPN profili paketini oluşturmasına olanak tanır.

## INDEKI

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 -AuthenticationMethod <String> [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
Bu, kullanıcıların VPN ağ geçidinde önceden yapılandırılmış VPN ayarları temelinde, örneğin bazı kök sertifikaları için kullanıcıların yapılandırması gerekebilecek bazı ek ayarlara ek olarak VPN profili paketini oluşturmasına olanak tanır.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

Bu cmdlet, "ContosoResourceGroup" tablosunda "ContosoVirtualNetworkGateway" için bir VPN istemci profili ZIP dosyası oluşturmak için kullanılır. Profil, VpnProfileRadiusCert sertifika dosyasıyla "EAPTLS" kimlik doğrulama yöntemini kullanacak şekilde yapılandırılmış önceden yapılandırılmış bir RADIUS sunucusu için oluşturulur.

## PARAMETRELERINE

### -AuthenticationMethod
Kimlik doğrulama yöntemi EAPMSCHAPv2 veya EAPTLS değerlerini alabilir. EAPMSCHAPv2 belirtildiğinde cmdlet, EAP-MSCHAPv2 kimlik doğrulama protokolünü kullanan Kullanıcı adı/parola kimlik doğrulaması için bir istemci yapılandırması yükleyicisi oluşturur. EAPTLS belirtilmişse cmdlet, EAP-TLS protokolünü kullanan sertifika kimlik doğrulaması için bir istemci yapılandırması yükleyicisi oluşturur. "EapTls" seçeneği, hem RADIUS tabanlı sertifika kimlik doğrulaması hem de sanal ağ geçidi tarafından gerçekleştirilen sertifika kimlik doğrulaması için, güvenilen kök yükleyerek kullanılabilir. Cmdlet, nelerin yapılandırıldığını otomatik olarak algılar.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ClientRootCertificateFileList
İstemci kök sertifikası yollarının listesi

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Ad
Kaynak adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProcessorArchitecture
ProcessorArchitecture

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RadiusRootCertificateFile
RADIUS sunucusu kök sertifikası yolu. Bu, RADIUS kimlik doğrulaması kullanılan EAP-TLS kullanıldığında belirtilmesi gereken zorunlu bir parametredir. Bu, istemcinin kimlik doğrulama sırasında RADIUS sunucusunu doğrulamak için kullandığı RADIUS kök sertifikasını içeren tam yol adıdır.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubu adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### System. String []

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. PSVpnProfile

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzVpnClientConfiguration](./Get-AzVpnClientConfiguration.md)
