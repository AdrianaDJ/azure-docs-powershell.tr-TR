---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: b4ab525623dd6bcb5aee57aeecf70ae36bdac380
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935610"
---
# Add-AzVpnClientRootCertificate

## SYNOPSIS
VPN istemcisi kök sertifikası ekler.

## INDEKI

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Add-AzVpnClientRootCertificate** cmdlet 'i sanal ağ geçidine kök sertifikası ekler.
Kök sertifikalar, kök sertifika yetkilinize tanımlayan X. 509.440 sertifikalardır.
Tasarım olarak, ağ geçidinde kullanılan tüm sertifikalar kök sertifikaya güvenir.

Bu cmdlet, var olan bir sertifikayı ağ geçidi kök sertifikası olarak atar.
Bir X. 509.440 sertifikanız yoksa, ortak anahtar altyapınız üzerinden bir tane oluşturabilir veya makecert.exe gibi bir sertifika Oluşturucusu kullanabilirsiniz.

Kök sertifika eklemek için, sertifika adını belirtmeniz ve sertifikanın salt metin bir gösterimini sağlamanız gerekir (daha fazla bilgi için *PublicCertData* parametresine bakın).
Azure, bir ağ geçidine birden fazla kök sertifikası atamanıza olanak tanır.
Birden çok kök sertifika genellikle birden fazla şirketten Kullanıcı içeren kuruluşlar tarafından dağıtılır.

## ÖRNEKLERDEN

### Örnek 1: sanal ağ geçidine istemci kök sertifikası ekleme
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

Bu örnek, ContosoVirtualGateway adlı sanal bir ağ geçidine bir istemci kök sertifikası ekler.

İlk komut **Get-Content** cmdlet 'ini kullanarak kök sertifikanın önceden dışarı aktarılmış bir metin sunumunu alır ve bu metin verilerinin $Text adlı değişkeni depolar.

İkinci komut, ilk satır ve son satır dışında tüm metni ayıklamak için bir for döngüsü kullanır.
Ayıklanan metin $CertificateText adlı bir değişkende saklanır.

Üçüncü komut, kök sertifikayı ağ geçidine eklemek için **Add-AzVpnClientRootCertificate** cmdlet 'i ile $CertificateText depolanan metni kullanır.

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

### -PublicCertData
Eklenecek kök sertifikanın metin gösterimini belirtir.
Metin gösterimini almak için, sertifikanızı. cer biçiminde (base64 kodlamasını kullanarak) dışarı aktarın ve sonra sonuç dosyasını bir metin düzenleyicisinde açın.
Bunu yaptığınızda, çıktıyı aşağıdakine benzer şekilde görürsünüz (gerçek çıktının, burada gösterilen kısaltılmış örnekten çok daha fazla metin satırı içereceği unutmayın):

---------------Son SERTIFIKA-----

PublicCertData, dosyadaki ilk satır (-----SERTIFIKA-----) ve son satır (-----son SERTIFIKA-----) arasındaki tüm satırlardan oluşmaktadır.
Bu verileri, aşağıdakine benzer Windows PowerShell komutlarını kullanarak alabilirsiniz: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`

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

### -ResourceGroupName
Kök sertifikanın atandığı kaynak grubunun adını belirtir.

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

### -VirtualNetworkGatewayName
Sertifikanın eklendiği sanal ağ ağ geçidinin adını belirtir.

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

### -VpnClientRootCertificateName
Bu cmdlet 'in eklediği istemci kök sertifikasının adını belirtir.

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

### Microsoft. Azure. Commands. Network. model. PSVpnClientRootCertificate

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[Yeni-AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


