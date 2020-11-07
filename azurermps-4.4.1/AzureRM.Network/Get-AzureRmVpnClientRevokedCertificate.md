---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 8171a87ea744eb708e65c71a1d25b13190b6f0fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765155"
---
# Get-AzureRmVpnClientRevokedCertificate

## SYNOPSIS
VPN istemci iptal sertifikaları hakkında bilgi alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-Azurermvpnclientunkedcertificate** cmdlet 'i, sanal ağ geçidine atanan istemci iptal sertifikaları hakkında bilgi döndürür.
İstemci-iptal sertifikaları, istemci bilgisayarların kimlik doğrulama için belirtilen sertifikayı kullanmasını engelliyor.
**Get-Azurermvpnclientunkedcertificate** , tek bir sertifika hakkında bilgi almak için, ağ geçidinde tüm istemci iptal sertifikaları hakkında bilgi döndürmenizi veya *Vpnclientunkedcertificatename* parametresini kullanmaktır.

## ÖRNEKLERDEN

### Örnek 1: tüm istemci iptal sertifikaları hakkında bilgi edinme
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

Bu komut, ContosoVirtualNetworkGateway adındaki sanal ağ ağ geçidiyle ilişkili tüm istemci iptal sertifikaları hakkında bilgi alır.

### Örnek 2: belirli istemci iptal sertifikaları hakkında bilgi edinme
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

Bu komut, örnek 1 ' de gösterilen komutun bir çeşitlemesi.
Ancak, bu örnekte, döndürülen verileri belirli bir istemciye sınırlandırmak için *Vpnclientgeri* alınan bir sertifika kullanılır-iptal edildi sertifikası

## PARAMETRELERINE

### -ResourceGroupName
Sanal ağ geçidinin atandığı kaynak grubunun adını belirtir.

Kaynak grupları, stok yönetimini ve genel Azure yönetimini basitleştirmeye yardımcı olmak için öğeleri kategorilere ayırabilir.

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

### -VirtualNetworkGatewayName
İptal edilen sertifika bilgilerinin atandığı sanal ağ ağ geçidinin adını belirtir.

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

### -Vpnclientiptal
Bu cmdlet 'in aldığı VPN istemci sertifikasının adını belirtir.

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

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

###  
**Get-Azurermvpnclientgeri alma** **Microsoft. Azure. Commands. Network. model. psvpnclientekedcertificate** nesnesinin örneklerini döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-Azurermvpnclientekedcertificate](./Add-AzureRmVpnClientRevokedCertificate.md)

[Yeni-Azurermvpnclientgeri alınamaz sertifika](./New-AzureRmVpnClientRevokedCertificate.md)

[Remove-Azurermvpnclientekedcertificate](./Remove-AzureRmVpnClientRevokedCertificate.md)


