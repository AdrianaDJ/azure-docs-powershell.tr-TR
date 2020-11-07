---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: d08f91029940d60440d50be406dbdfe3652934a7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935460"
---
# Get-AzVpnClientPackage

## SYNOPSIS
VPN istemci paketi hakkında bilgi alır.

## INDEKI

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzVpnClientPackage** cmdlet 'i sanal ağ ağ GEÇIDINDEN sağlanan VPN istemci paketleriyle ilgili bilgileri alır.
İstemci paketleri, istemci bilgisayarın Azure sanal ağıyla VPN bağlantısı yapmasını etkinleştiren yapılandırma verilerini içerir; VPN bağlantısı oluşturmak için istemci bilgisayarlarda doğru yapılandırma paketinin yüklü olması gerekir.
Farklı yapılandırma paketleri, istemci bilgisayarın Windows sürümü (örneğin, Windows 7 veya Windows 10) ve istemci bilgisayarın işlemci mimarisi (AMD64 veya x86) temelinde kullanılabilir.
**Get-AzVpnClientPackage** çalıştırırken mimari türünü belirtmeniz gerekir.

## ÖRNEKLERDEN

### Örnek 1: işlemci mimarisi VPN istemci paketi hakkında bilgi alma
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

Bu komut, ContosoVirtualNetworkGateway adındaki sanal ağ geçidinde depolanan AMD64 VPN istemci paketi hakkında bilgi alır.
X86 istemci paketleri hakkında bilgi edinmek için, *ProcessorArchitecture* parametresinin değerini x86 olarak ayarlayın.

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

### -ProcessorArchitecture
İstemci paketinin tasarlandığı CPU mimarisinin türünü belirtir.
Geçerli değerler amd64 ve x86 değerleridir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
İstemci paketi bilgilerinin depolandığı sanal ağ ağ geçidinin adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Dizisi
' ResourceGroupName ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder

### Dizisi
' VirtualNetworkGatewayName ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder

## ÇıKıŞLAR

###  
**Get-AzVpnClientPackage** , System. String nesnesinin örneklerini döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Resize-AzVirtualNetworkGateway](./Resize-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGatewayVpnClientConfig](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


