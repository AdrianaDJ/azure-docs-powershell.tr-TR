---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
ms.openlocfilehash: ed5a2d3d004dfe1480d14e598b009cf6e49d2c1d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917988"
---
# Remove-AzVpnClientRootCertificate

## SYNOPSIS
Mevcut bir VPN istemcisi kök sertifikasını kaldırır.

## INDEKI

```
Remove-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Remove-AzVpnClientRootCertificate** cmdlet 'i, belirtilen kök sertifikayı sanal ağ ağ geçidinden kaldırır.
Kök sertifikalar, kök sertifika yetkilinizi tanımlayan X. 509.440 sertifikalardır
Kimlik doğrulama amacıyla sertifikayı kullanan bir kök sertifikayı kaldırırsanız, artık ağ geçidine bağlanamaz.
**Remove-AzVpnClientRootCertificate** kullandığınızda, sertifika verilerinin hem sertifika adını hem de metin gösterimini sağlamanız gerekir.
Sertifikanın metin gösterimi hakkında daha fazla bilgi için, *Publiccertdata* parametre açıklamasına bakın.

## ÖRNEKLERDEN

### Örnek 1: sanal ağ ağ geçidinden istemci kök sertifikası kaldırma
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway"-VpnClientRootCertificateName "ContosoRootCertificate"
```

Bu örnekte, ContosoRootCertificate adlı bir istemci kök sertifikası sanal ağ geçidinden ContosoVirtualGateway 'den kaldırılır.
İlk komut, sertifikanın önceden dışarı aktarılmış bir metin sunumunu almak için **Get-Content** cmdlet 'ini kullanır; Bu metin gösterimi $Text adlı bir değişkende saklanır.
İkinci komut, ilk satır ve son satır dışında $Text tüm metni ayıklamak için bir for döngüsü kullanır.
Bu ayıklanan metin $CertificateText adlı bir değişkende saklanır.
Üçüncü komut, **Remove-AzVpnClientRootCertificate** cmdlet 'i kullanarak sertifikayı ağ geçidinden kaldırmak için $CertificateText değişkeninde depolanan bilgileri kullanır.

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

### -PublicCertData
Kaldırılacak kök sertifikanın metin gösterimini belirtir.
Metin gösterimini almak için, sertifikanızı. cer biçiminde (base64 kullanarak) dışarı aktarın ve sonra sonuç dosyasını bir metin düzenleyicisinde açın.
Aşağıdakine benzer bir çıkışı görmeniz gerekir (gerçek çıktının, burada gösterilen kısaltılmış örnekten çok daha fazla metin içerdiğine dikkat edin):---------------son SERTIFIKAYı-----PublicCertData ilk satır (----------SERTIFIKA-----) ve son satır (-----son SERTIFIKA) arasındaki tüm satırlardan oluşmuştur.
PublicCertData 'ı, buna benzer Windows PowerShell komutlarını kullanarak da alabilirsiniz: $Text = Get-Content-yol "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = $i for = 1; $i-a $Text. length-1; $i + +) {$Text \[ $i \] }

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
Sertifikanın kaldırıldığı sanal ağ geçidinin adını belirtir.

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

### -VpnClientRootCertificateName
Bu cmdlet 'in kaldırıldığı istemci kök sertifikasının adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

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

### System. Boolean

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[Yeni-AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)


