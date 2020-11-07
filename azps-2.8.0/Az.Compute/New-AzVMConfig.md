---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 5dda2e33496e3391d55e7be20348fef681bc22b9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752834"
---
# New-AzVMConfig

## SYNOPSIS
Yapılandırılabilir bir sanal makine nesnesi oluşturur.

## INDEKI

### DefaultParameterSet (varsayılan)
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ExplicitIdentityParameterSet
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AssignIdentityParameterSet
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-AssignIdentity] [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-VmssId <String>] [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>]
 [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**New-AzVMConfig** cmdlet 'i Azure için yapılandırılabilir bir yerel sanal makine nesnesi oluşturur.
Diğer cmdlet 'ler, set-AzVMOperatingSystem, set-AzVMSourceImage, Add-Azvmnetworkınterface ve set-AzVMOSDisk gibi bir sanal makine nesnesini yapılandırmak için kullanılabilir.

## ÖRNEKLERDEN

### Örnek 1: sanal makine nesnesi oluşturma
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

İlk komut, ResourceGroup11 adındaki kaynak grubundaki AvailabilitySet03 adındaki kullanılabilirlik kümesini alır ve bu nesneyi $AvailabilitySet değişkeninde depolar.
İkinci komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.
Bu komut sanal makineye bir ad ve boyut atar.
Sanal makine, $AvailabilitySet depolanan kullanılabilirlik kümesine aittir.

## PARAMETRELERINE

### -Atama kimliği
Sanal makine için sistem tarafından atanan kimliği belirtin.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kullanılabilirlik
Bir kullanılabilirlik kümesinin KIMLIĞINI belirtir.
Bir kullanılabilirlik kümesi nesnesi edinmek için Get-AzAvailabilitySet cmdlet 'ini kullanın.
Kullanılabilirlik kümesi nesnesi bir KIMLIK içeriyor.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
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

### -EnableUltraSSD
VM 'de UltraSSD_LRS depolama hesabı türüyle bir veya birden çok yönetilen veri diskine sahip olmak olanak verir.
Depolama hesabı türü UltraSSD_LRS yönetilen diskler, yalnızca bu özellik etkinleştirilirse sanal makineye eklenebilir.


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Çıkarma Ilkesi
Düşük öncelikli sanal makine için çıkarma ilkesi.  Yalnızca desteklenen değer ' ayırması '.

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

### -HostId
Ana bilgisayar kimliği

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

### -IdentityId
Sanal makine ölçek kümesiyle ilişkili kullanıcı kimliklerinin listesini belirtir.
Kullanıcı kimliği başvuruları formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IdentityType
Yapılandırılmış sanal makinenin kimliği.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LicenseType
Kendi lisans senaryonuzu veren lisans türü.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxPrice
Düşük öncelikli VM/VMSS için ödemek istediğiniz en yüksek fiyatı belirtir. Bu fiyat ABD doları cinsindendir. Bu fiyat VM boyutu için geçerli düşük öncelik fiyatıyla karşılaştırılır. Ayrıca, düşük öncelikli VM/VMSS oluşturma/güncelleştirme sırasında fiyatlar karşılaştırılır ve işlem yalnızca maxPrice geçerli düşük öncelik fiyatından büyükse başarıdır. Geçerli düşük öncelik fiyatının VM/VMSS oluşturulduktan sonra maxPrice 'den fazla olması durumunda, maxPrice de düşük öncelikli VM/VMSS çıkarmak için kullanılacaktır. Olası değerler: sıfırdan büyük herhangi bir ondalık değer. Örnek: 0,01538.  -1 düşük öncelikli VM/VMSS 'nin fiyat nedenlerinin çıkarılmamalıdır. Ayrıca, sizin sağlanmadıysa varsayılan en fazla fiyat-1 ' dir.

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Öncelik
Sanal makinenin önceliği.  Yalnızca desteklenen değerler ' Regular ' ve ' Low ' değerleridir.

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

### -ProximityPlacementGroupId
ProximityPlacementGroup kimliği

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

### -Etiketler
Kaynağa iliştirilmiş etiketler.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Sanal makine için bir ad belirtir.

```yaml
Type: System.String
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
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VmssId
Sanal makine ölçek kümesi kimliği

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

### -Bölge
Sanal makinenin kullanılabilirlik bölgesi listesini belirtir. İzin verilen değerler, bölgenin yeteneklerine bağlıdır. İzin verilen değerler normalde 1, 2, 3 olur.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

### System. String []

### System. topluluklar. Hashtable

### System. Management. Automation. SwitchParameter

## ÇıKıŞLAR

### Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Update-AzVM](./Update-AzVM.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)

[Set-Azvmsourceımage](./Set-AzVMSourceImage.md)

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)


