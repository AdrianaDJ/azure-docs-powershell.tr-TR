---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 6fe6f6345f9208a524e1162fb317b88c450f3909
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761194"
---
# Update-AzVmss

## SYNOPSIS
Bir VMSUBNET 'in durumunu güncelleştirir.

## INDEKI

### DefaultParameter (varsayılan)
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-BootDiagnosticsEnabled <Boolean>] [-Tag <Hashtable>]
 [-UpgradePolicyMode <UpgradeMode>] [-DisablePasswordAuthentication <Boolean>]
 [-ManagedDiskStorageAccountType <String>] [-AutomaticOSUpgrade <Boolean>] [-SkuTier <String>]
 [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-SinglePlacementGroup <Boolean>] [-PlanPublisher <String>]
 [-BootDiagnosticsStorageUri <String>] [-Overprovision <Boolean>] [-DisableAutoRollback <Boolean>]
 [-TimeZone <String>] [-PlanPromotionCode <String>] [-MaxBatchInstancePercent <Int32>] [-SkuCapacity <Int32>]
 [-OsDiskWriteAccelerator <Boolean>] [-ImageReferenceOffer <String>] [-ImageReferenceSku <String>]
 [-VhdContainer <String[]>] [-MaxUnhealthyInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-ProvisionVMAgent <Boolean>] [-SkuName <String>] [-ImageReferenceVersion <String>]
 [-PauseTimeBetweenBatches <String>] [-ImageUri <String>] [-PlanName <String>] [-PlanProduct <String>]
 [-ImageReferenceId <String>] [-EnableAutomaticUpdate <Boolean>] [-CustomData <String>] [-LicenseType <String>]
 [-OsDiskCaching <CachingTypes>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ExplicitIdentityParameterSet
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-BootDiagnosticsEnabled <Boolean>] [-Tag <Hashtable>]
 [-UpgradePolicyMode <UpgradeMode>] [-DisablePasswordAuthentication <Boolean>]
 -IdentityType <ResourceIdentityType> [-ManagedDiskStorageAccountType <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SkuTier <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-SinglePlacementGroup <Boolean>]
 [-PlanPublisher <String>] [-BootDiagnosticsStorageUri <String>] [-Overprovision <Boolean>]
 [-DisableAutoRollback <Boolean>] [-TimeZone <String>] [-PlanPromotionCode <String>]
 [-MaxBatchInstancePercent <Int32>] [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>]
 [-ImageReferenceOffer <String>] [-ImageReferenceSku <String>] [-VhdContainer <String[]>]
 [-MaxUnhealthyInstancePercent <Int32>] [-ImageReferencePublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-SkuName <String>] [-ImageReferenceVersion <String>] [-PauseTimeBetweenBatches <String>] [-ImageUri <String>]
 [-PlanName <String>] [-PlanProduct <String>] [-ImageReferenceId <String>] [-EnableAutomaticUpdate <Boolean>]
 [-CustomData <String>] [-LicenseType <String>] [-OsDiskCaching <CachingTypes>] [-IdentityId <String[]>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
**Update-AzVmss** cmdlet 'ı sanal makine ölçek kümesi 'nın (VMSS) durumunu yerel BIR VMSS nesnesinin durumuna güncelleştirir.

## ÖRNEKLERDEN

### Örnek 1: bir VMSS durumunu yerel bir VMSS nesnesinin durumuna güncelleyin.
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS 'nin durumunu yerel bir VMSS nesnesinin durumuna güncelleştirir $LocalVMSS.

## PARAMETRELERINE

### -Iş
Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Automaticosupgrad
Resmin daha yeni bir sürümü kullanılabilir hale geldiğinde, bir yerde ölçeklendirme kümesi örneklerine otomatik olarak işletim sistemi yükseltmeleri uygulanıp uygulanmayacağı.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootDiagnosticsEnabled
Sanal makine ölçek kümesinde önyükleme tanılaması 'nın etkinleştirilmesi gerekip gerekmediği.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootDiagnosticsStorageUri
Konsol çıkışını ve ekran görüntüsünü yerleştirmek için kullanılacak depolama hesabının URI 'SI.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomData
Özel verilerin Base-64 kodlu dizesini belirtir.
Bu, sanal makinede dosya olarak kaydedilmiş bir ikili diziye çözülür.
İkili dizinin en fazla uzunluğu 65535 bayttır.

```yaml
Type: System.String
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

### -DisableAutoRollback
Otomatik OS yükseltme Ilkesi için otomatik geri almayı devre dışı bırakma

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisablePasswordAuthentication
Bu cmdlet 'in Linux OS için parola kimlik doğrulamasını devre dışı bırakacağını gösterir.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutomaticUpdate
VMSS 'deki Windows sanal makinelerinin otomatik güncelleştirmeler için etkinleştirilip etkinleştirilmediğini gösterir.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentityType
Sanal makine ölçek kümesi için kullanılan kimlik türünü belirtir.
' Systemassigneduserın ' türü, örtülü olarak oluşturulmuş bir kimlik ve Kullanıcı tarafından atanan kimlikler kümesini içerir.
' None ' türü, sanal makine ölçek kümesindeki tüm kimlikleri kaldırır.
Bu parametre için kabul edilebilir değerler şunlardır:
- SystemAssigned
- Kullanıcı tarafından atanmış
- Systemassigneduseratandı
- Yabilirsiniz

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Imagereferenceıd
Resim başvuru KIMLIĞINI belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Imagereferenceteklif
Sanal makine görüntüsünün (Vmımage) teklifinin türünü belirtir.
Resim teklifi edinmek için Get-AzVMImageOffer cmdlet 'ini kullanın.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Imagereferencepublisher
Vmımage yayımcısı adını belirtir.
Yayımcı edinmek için Get-AzVMImagePublisher cmdlet 'ini kullanın.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Imagereferencesku
VMImage SKU 'SU belirtir.
STB 'ler almak için Get-AzVMImageSku cmdlet 'ini kullanın.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Imagereferenceversion
VMImage sürümünü belirtir.
En son sürümü kullanmak için belirli bir sürüm yerine en son sürümünü belirtin.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Imageurı
Kullanıcı görüntüsü için blob URI 'sini belirtir.
VMSS, Kullanıcı görüntüsünün aynı kapsayıcısında bir işletim sistemi diski oluşturur.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LicenseType
Kendi lisans senaryonuzu verecek lisans türünü belirtin.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedDiskStorageAccountType
Yönetilen disk için depolama hesabı türünü belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
- Standartlrs
- PremiumLRS

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Maxbatchınstancepercent
Tek bir toplu işlemde çalışırken yükseltme tarafından aynı anda Yükseltilecek toplam sanal makine örneklerinin en yüksek yüzdesi.
Bu en yüksek düzeyde, önceki veya gelecekteki toplu işlemdeki sağlıksız örnekler, daha yüksek güvenilirlik sağlamak amacıyla toplu işteki örneklerin yüzdesine neden olabilir.
Değer belirtilmezse, 20 olarak ayarlanır.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Maxunhealthyınstancepercent
Ölçek kümesindeki toplam sanal makine örneklerinin, yükseltilme sonucu olarak, yükseltme sonucu olan veya çalışırken yükseltme iptal edilmeden önce sanal makine durumu denetimleri tarafından sağlıksız bir durumda bulunabildiği en yüksek oranı.
Bu kısıtlama, toplu işlem başlatılmadan önce işaretlenir.
Değer belirtilmezse, 20 olarak ayarlanır.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Maxunhealthyyükseltildi Dedınstancepercent
Sağlıksız durumda olabilecek en yüksek yükseltilmiş sanal makine örneği yüzdesi.
Bu denetim her toplu iş yükseltildikten sonra gerçekleşir.
Bu yüzde aşılırsa, çalışırken güncelleştirme iptal edilir.
Değer belirtilmezse, 20 olarak ayarlanır.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OsDiskCaching
İşletim sistemi diskinin önbelleğe alma modunu belirtir. Bu parametre için kabul edilebilir değerler şunlardır:
- Yabilirsiniz
- Özelliğinin
- ReadWrite varsayılan değer ReadWrite.
Önbellek değerini değiştirirseniz cmdlet sanal makineyi yeniden başlatır.
Bu ayar, diskin tutarlılığını ve performansını etkiler.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OsDiskWriteAccelerator
İşletim sistemi diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Overprovision
Cmdlet 'in VMSS 'yi içerip içermediğini gösterir.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pausetimebetweentoplu Işler
Bir toplu işteki tüm sanal makinelerin güncelleştirmesini tamamlama ve sonraki toplu işlemi başlatma arasındaki bekleme süresi.
Süre ISO 8601 biçiminde belirtilmelidir.
Varsayılan değer 0 saniyedir (PT0S).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlanName
Plan adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Planürün
Plan ürünü belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlanPromotionCode
Plan promosyon kodunu belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlanPublisher
Publisher planı 'nı belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProvisionVMAgent
VMSS 'deki Windows sanal makinelerinde sanal makine aracısının sağlanması gerekip gerekmediğini gösterir.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
VMSS 'nin ait olduğu kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SinglePlacementGroup
Tek yerleşim grubunu belirtir.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Skukapasitesi
VMSS 'deki örneklerin sayısını belirtir.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkuName
Tüm VMSS örneklerinin boyutunu belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkuTier
VMSS 'nin katmanını belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
- Ardından
- Ana

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Etiketli
Karma tablo biçiminde anahtar-değer çiftleri. Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}

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

### -TimeZone
Windows işletim sisteminin saat dilimini belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UltraSSDEnabled
Sanal makine ölçek kümesinde UltraSSD_LRS depolama hesabı türüne sahip bir veya birden çok yönetilen veri diskine sahip olan bir veya birden çok yönetilen veri diski
Depolama hesap türü UltraSSD_LRS yönetilen diskler yalnızca bu özellik etkinse bir VMSUBNET 'e eklenebilir.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UpgradePolicyMode
Belirtilen ölçek kümesindeki sanal makinelere yükseltme modu.
Bu parametre için kabul edilebilir değerler şunlardır:
- Otomatik
- El ile
- Melerdeki

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VhdContainer
VMSS işletim sistemi disklerini depolamak için kullanılan kapsayıcı URL 'Lerini belirtir.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Yerel bir VMSS nesnesini belirtir.
Bir VMSS nesnesi edinmek için Get-AzVmss cmdlet 'ini kullanın.
Bu sanal makine nesnesi, VMSS 'nin güncelleştirilmiş durumunu içerir.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VMScaleSetName
Bu cmdlet 'in oluşturduğu VMSS 'nin adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet

### System. Boolean

## ÇıKıŞLAR

### Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzVmss](./Get-AzVmss.md)

[Yeni-AzVmss](./New-AzVmss.md)

[Remove-AzVmss](./Remove-AzVmss.md)

[Restart-AzVmss](./Restart-AzVmss.md)

[Set-AzVmss](./Set-AzVmss.md)

[Başlangıç-AzVmss](./Start-AzVmss.md)

[Dur-AzVmss](./Stop-AzVmss.md)


