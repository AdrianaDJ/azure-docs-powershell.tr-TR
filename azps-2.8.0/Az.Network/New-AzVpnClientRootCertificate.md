---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 9b9bafcae74f19873efc8e9649bed452bb25fd79
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918160"
---
# New-AzVpnClientRootCertificate

## SYNOPSIS
Yeni bir VPN istemcisi kök sertifikası oluşturur.

## INDEKI

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Yeni-AzVpnClientRootCertificate** cmdlet 'i sanal ağ geçidinde kullanılmak üzere yenı bir VPN kök sertifikası oluşturur.
Kök sertifikalar, kök sertifika yetkilinizi tanımlayan X. 509.440 sertifikalardır
Bu cmdlet, sanal ağ geçidine atanmamış tek başına bir sertifika oluşturur.
Bunun yerine, yeni ağ geçidi oluştururken, **Yeni-AzVpnClientRootCertificate** tarafından oluşturulan sertifika New-AzVirtualNetworkGateway cmdlet ile birlikte kullanılır.
Örneğin, yeni bir sertifika oluşturduğunuzu ve $Certificate adlı bir değişkende depolamanızı varsayalım.
Bu sertifika nesnesini, yeni sanal ağ geçidi oluştururken kullanabilirsiniz.
Örneğin, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`
Daha fazla bilgi için New-AzVirtualNetworkGateway cmdlet belgelerine bakın.

## ÖRNEKLERDEN

### Örnek 1: istemci kök sertifikası oluşturma
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

Bu örnek, bir istemci kök sertifikası oluşturur ve sertifika nesnesini $Certificate adlı bir değişkende depolar.
Bu değişken, yeni bir sanal ağ ağ geçidine kök sertifikası eklemek için **Yeni-AzVirtualNetworkGateway** cmdlet 'i tarafından kullanılabilir.
İlk komut **Get-Content** cmdlet 'ini kullanarak kök sertifikanın daha önce dışarı aktarılmış bir metin sunumunu alır; Bu metin verileri $Text adlı bir değişkende saklanır.
İkinci komut, ilk satır ve son satır dışında tüm metni ayıklamak için bir for döngüsü kullanır ve $CertificateText adlı bir değişkende ayıklanan metni saklar.
Üçüncü komut, sertifikayı oluşturmak için **New-AzVpnClientRootCertificate** cmdlet 'ini kullanarak, oluşturulan nesneyi $Certificate adlı bir değişkende saklar.

## PARAMETRELERINE

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
Yeni istemci kök sertifikası için bir ad belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicCertData
Eklenecek kök sertifikanın metin sunumunu belirtir.
Metin gösterimini almak için, sertifikanızı. cer biçiminde (base64 kodlamasını kullanarak) dışarı aktarın ve sonra sonuç dosyasını bir metin düzenleyicisinde açın.
Çıktıyı aşağıdakine benzer bir şekilde görmelisiniz (gerçek çıktının, burada gösterilen kısaltılmış örnekten çok daha fazla metin içerdiğine dikkat edin):---------------son SERTIFIKA-----, PublicCertData ilk satır (----------SERTIFIKA-----) ve son satır (-----son SERTIFIKA) arasındaki tüm satırlardan oluşmuştur.
Public Certdata 'ı, buna benzer Windows PowerShell komutlarını kullanarak da alabilirsiniz: $Text = Get-Content-yol "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = $i for = 1; $i-a $Text. length-1; $i + +) {$Text \[ $i \] }

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. PSVpnClientRootCertificate

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


