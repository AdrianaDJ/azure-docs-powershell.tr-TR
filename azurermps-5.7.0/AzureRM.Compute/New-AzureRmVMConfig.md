---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMConfig.md
ms.openlocfilehash: 45cb93e652f9c1524ef1bb11972f184336ef7328
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762752"
---
# New-AzureRmVMConfig

## SYNOPSIS
Yapılandırılabilir bir sanal makine nesnesi oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [-LicenseType <String>] [-IdentityType <ResourceIdentityType>] [-Tags <Hashtable>] [<CommonParameters>]
```

## Tanım
**Yeni-AzureRmVMConfig** cmdlet 'i Azure için yapılandırılabilir bir yerel sanal makine nesnesi oluşturur.
Diğer cmdlet 'ler, set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage, Add-Azurermvmnetworkınterface ve set-Azurermvmosdısk gibi bir sanal makine nesnesini yapılandırmak için kullanılabilir.

## ÖRNEKLERDEN

### Örnek 1: sanal makine nesnesi oluşturma
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

İlk komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet03 adındaki kullanılabilirlik kümesini alır ve bu nesneyi $AvailabilitySet değişkeninde depolar.

İkinci komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.
Bu komut sanal makineye bir ad ve boyut atar.
Sanal makine, $AvailabilitySet depolanan kullanılabilirlik kümesine aittir.

## PARAMETRELERINE

### -Kullanılabilirlik
Bir kullanılabilirlik kümesinin KIMLIĞINI belirtir.
Bir kullanılabilirlik kümesi nesnesi edinmek için Get-AzureRmAvailabilitySet cmdlet 'ini kullanın.
Kullanılabilirlik kümesi nesnesi bir KIMLIK içeriyor.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IdentityType
Yapılandırılmış sanal makinenin kimliği.

```yaml
Type: ResourceIdentityType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LicenseType
Kendi lisans senaryonuzu veren lisans türü.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Etiketler
Kaynağa iliştirilmiş etiketler.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Sanal makine için bir ad belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMSize
Sanal makinenin boyutunu belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Güncelleştirme-AzureRmVM](./Update-AzureRmVM.md)

[Set-AzureRmVMOperatingSystem](./Set-AzureRmVMOperatingSystem.md)

[Set-AzureRmVMSourceImage](./Set-AzureRmVMSourceImage.md)

[Get-AzureRmAvailabilitySet](./Get-AzureRmAvailabilitySet.md)


