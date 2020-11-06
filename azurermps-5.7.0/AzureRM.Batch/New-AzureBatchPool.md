---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
ms.openlocfilehash: 54a5d6dc737bc0bd6a7f1d236ce855b2a08dca6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594964"
---
# New-AzureBatchPool

## SYNOPSIS
Toplu Iş hizmetinde havuz oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Cloudserviceandtargetadanmış (varsayılan)
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Virtualmachineandtargetadanmış
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### CloudServiceAndAutoScale
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### VirtualMachineAndAutoScale
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
**New-AzureBatchPool** cmdlet 'ı, *batchcontext* parametresinde belirtilen hesap altında Azure Batch hizmetinde bir havuz oluşturur.

## ÖRNEKLERDEN

### Örnek 1: Targetadanmış parametre kümesini kullanarak yeni havuz oluşturma
```
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

Bu komut, Targetadanmış parametre kümesini kullanarak KIMLIĞI MyPool ile yeni bir havuz oluşturur.
Hedef ayırma üç COMPUTE düğümlerdir.
Havuz, Aile dörtte en son işletim sistemi sürümüyle görüntülü küçük sanal makineleri kullanacak şekilde yapılandırılmıştır.

### Örnek 2: otomatik ölçeklendirme parametre kümesini kullanarak yeni havuz oluşturma
```
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

Bu komut otomatik ölçeklendirme parametre kümesini kullanarak KIMLIK AutoScalePool ile yeni bir havuz oluşturur.
Havuz, Aile dördünü en son işletim sistemi sürümü ile görüntülü küçük sanal makineleri kullanacak şekilde yapılandırılmıştır ve hedef sayısı, otomatik ölçeklendirme formülüyle belirlenir.

### Örnek 3: alt ağda düğümleri bulunan havuz oluşturma
```
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### Örnek 4: özel kullanıcı hesaplarıyla havuz oluşturma
```
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## PARAMETRELERINE

### -Applicationlisansları
Toplu hizmet, havuzdaki her bir işlem düğümünde kullanılabilir olacak uygulama lisanslarının listesi.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: ApplicationLicense

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Applicationpackagereferfer
```yaml
Type: PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutoScaleEvaluationInterval
Havuz boyutu otomatik ölçeklendirme formülüne göre otomatik olarak düzeltilecek kadar geçen süreyi dakika cinsinden belirtir.
Varsayılan değer 15 dakikadır ve en az değer 5 dakikadır.

```yaml
Type: TimeSpan
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Otomatik ölçek formülü
Havuzu otomatik olarak ölçeklendirme formülünü belirtir.

```yaml
Type: String
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BatchContext
Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.
BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır. Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın. Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır. Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Certificatereferde
Havuz ile ilişkili sertifikaları belirtir.
Toplu Iş hizmeti, havuzun her bir COMPUTE düğümüne başvurulan sertifikaları yükler.

```yaml
Type: PSCertificateReference[]
Parameter Sets: (All)
Aliases: CertificateReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CloudServiceConfiguration
Azure bulut hizmeti platformuna dayalı bir havuzun yapılandırma ayarlarını belirtir.

```yaml
Type: PSCloudServiceConfiguration
Parameter Sets: CloudServiceAndTargetDedicated, CloudServiceAndAutoScale
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
Havuzun görünen adını belirtir.

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

### -ID
Oluşturulacak havuzun KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Intercomputenodecommunicationenabled
Bu cmdlet 'in adanmış işlem düğümleri arasında doğrudan iletişim için havuzu ayarlamadığını gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxTasksPerComputeNode
Tek bir işlem düğümünde çalıştırılabilecek en fazla görev sayısını belirtir.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Metadata
Yeni havuza eklemek için meta verileri anahtar/değer çiftleri olarak belirtir.
Anahtar, meta veri adıdır.
Değer, meta veri değeridir.

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkConfiguration
Havuzun ağ yapılandırması.

```yaml
Type: PSNetworkConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResizeTimeout
Havuza işlem düğümleri tahsis etmek için zaman aşımını belirtir.

```yaml
Type: TimeSpan
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTask
Havuzun başlangıç görevi belirtimini belirtir.
Başlangıç görevi, bir hesaplama düğümü havuza katıldığında veya hesaplama düğümü yeniden başlatıldığında veya yeniden başlatıldığında çalıştırılır.

```yaml
Type: PSStartTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TARGETTE
Havuza ayrılacak adanmış işlem düğümlerinin hedef sayısını belirtir.

```yaml
Type: Int32
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetLowPriorityComputeNodes
Havuza ayrılacak düşük öncelikli işlem düğümlerinin hedef sayısını belirtir.

```yaml
Type: Int32
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSchedulingPolicy
ComputeNodeFillType gibi görev zamanlama ilkesini belirtir.

```yaml
Type: PSTaskSchedulingPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kullanıcıhesabı
Havuzdaki her düğümde oluşturulacak Kullanıcı hesaplarının listesi.

```yaml
Type: PSUserAccount[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualMachineConfiguration
Sanal makineler Altyapısındaki bir havuzun yapılandırma ayarlarını belirtir.

```yaml
Type: PSVirtualMachineConfiguration
Parameter Sets: VirtualMachineAndTargetDedicated, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Virtualınines
Havuzdaki sanal makinelerin boyutunu belirtir.
Sanal makine boyutları hakkında daha fazla bilgi için bkz: sanal makinelerin boyutları https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) Microsoft Azure sitesinde).

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

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
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

### BatchAccountContext
' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchPool](./Get-AzureBatchPool.md)

[Remove-AzureBatchPool](./Remove-AzureBatchPool.md)

[Azure toplu Iş cmdlet 'Leri](./AzureRM.Batch.md)


