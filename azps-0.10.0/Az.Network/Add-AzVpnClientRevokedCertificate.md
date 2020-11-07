---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 384d5b88ce9a52ad5f68c009c7b610610c695ce2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935607"
---
# Add-AzVpnClientRevokedCertificate

## SYNOPSIS
VPN istemcisi iptal sertifikası ekler.

## INDEKI

```
Add-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Add-Azvpnclientunkedcertificate** cmdlet 'i sanal ağ geçidine bir istemci iptal sertifikası atar.
İstemci-iptal sertifikaları, istemci bilgisayarların kimlik doğrulama için belirtilen sertifikayı kullanmasını engelliyor.
Bu cmdlet 'i kullanmak için hem sertifika adını hem de sertifika parmak izini belirtmeniz gerekir.

## ÖRNEKLERDEN

### Örnek 1: sanal ağ geçidine yeni bir istemci iptal sertifikası ekleme
```
PS C:\>Add-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

Bu komut, ContosoVirtualNetwork adlı sanal ağ geçidine yeni bir istemci iptal sertifikası ekler.
Sertifikayı eklemek için hem sertifika adını hem de sertifika parmak izini belirtmeniz gerekir.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Sanal ağ geçidinin atandığı kaynak grubunun adını belirtir.

Kaynak grupları, stok yönetimini ve genel Azure yönetimini basitleştirmeye yardımcı olmak için öğeleri kategorilere ayırabilir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Parmak izi
Eklenmekte olan sertifikanın benzersiz tanımlayıcısını belirtir.
Örneğin:

-Parmak izi "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"

Aşağıdaki gibi bir Windows PowerShell komutunu kullanarak sertifikalarınız için parmak izi bilgilerini alabilirsiniz: `Get-ChildItem -Path Cert:\LocalMachine\Root` .

Yukarıdaki komut, kök sertifika deposunda bulunan tüm yerel bilgisayar sertifikalarının bilgilerini alır.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
Sertifikanın ekleneceği sanal ağ ağ geçidinin adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Vpnclientiptal
Eklenecek VPN istemci sertifikasının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. Psvpnclientiptal edilmiş sertifikası

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azvpnclientgeri alma](./Get-AzVpnClientRevokedCertificate.md)

[Yeni-Azvpnistemci geri alınamaz sertifikası](./New-AzVpnClientRevokedCertificate.md)

[Remove-Azvpnclientiptal](./Remove-AzVpnClientRevokedCertificate.md)


