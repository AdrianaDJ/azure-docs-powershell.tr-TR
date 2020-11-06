---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: cec626d48e5daebe04ad33b13713b56c96e27b17
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589160"
---
# <span data-ttu-id="c1abc-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c1abc-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="c1abc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1abc-102">SYNOPSIS</span></span>
<span data-ttu-id="c1abc-103">Çoğaltma korumalı bir öğe oluşturarak, bir ASR korunabilir öğesi için çoğaltmayı olanaklı kılar</span><span class="sxs-lookup"><span data-stu-id="c1abc-103">Enables replication for an ASR protectable item by creating a replication protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1abc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c1abc-104">SYNTAX</span></span>

### <span data-ttu-id="c1abc-105">DisableDR (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c1abc-105">DisableDR (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1abc-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="c1abc-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1abc-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="c1abc-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1abc-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="c1abc-108">HyperVSiteToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> -RecoveryResourceGroupId <String> [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1abc-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1abc-109">DESCRIPTION</span></span>
<span data-ttu-id="c1abc-110">**Yeni-Azurermrecoveryservicesasrreplicationkorunabilir** , yeni bir çoğaltma korumalı öğesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c1abc-110">The **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="c1abc-111">ASR korunabilir öğesi için yinelemeyi etkinleştirmek üzere bu cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="c1abc-111">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="c1abc-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c1abc-112">EXAMPLES</span></span>

### <span data-ttu-id="c1abc-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c1abc-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="c1abc-114">Belirtilen ASR korunabilir öğesi için çoğaltma korumalı öğe oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="c1abc-114">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c1abc-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c1abc-115">PARAMETERS</span></span>

### <span data-ttu-id="c1abc-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="c1abc-116">-Name</span></span>
<span data-ttu-id="c1abc-117">ASR çoğaltması korumalı öğesi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1abc-117">Specifies a name for the ASR replication protected item.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1abc-118">-İşletim sistemi</span><span class="sxs-lookup"><span data-stu-id="c1abc-118">-OS</span></span>
<span data-ttu-id="c1abc-119">İşletim sistemi ailesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1abc-119">Specifies the operating system family.</span></span>
<span data-ttu-id="c1abc-120">Bu parametre için kabul edilebilir değerler: Windows veya Linux.</span><span class="sxs-lookup"><span data-stu-id="c1abc-120">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1abc-121">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="c1abc-121">-OSDiskName</span></span>
<span data-ttu-id="c1abc-122">İşletim sistemi diskinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1abc-122">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1abc-123">-Korunabilir öğe</span><span class="sxs-lookup"><span data-stu-id="c1abc-123">-ProtectableItem</span></span>
<span data-ttu-id="c1abc-124">Çoğaltmanın etkinleştirildiği ASR korunabilir öğe nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1abc-124">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1abc-125">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="c1abc-125">-ProtectionContainerMapping</span></span>
<span data-ttu-id="c1abc-126">Çoğaltma için kullanılacak çoğaltma ilkesine karşılık gelen ASR koruma kapsayıcısı eşleme nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1abc-126">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1abc-127">-Recoveryazurestorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="c1abc-127">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="c1abc-128">Çoğaltılacak Azure depolama hesabının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1abc-128">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1abc-129">-Recoveryresourcegroupıd</span><span class="sxs-lookup"><span data-stu-id="c1abc-129">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="c1abc-130">Yük devretme olayında sanal makinenin oluşturulduğu kaynak grubunun ARM tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1abc-130">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1abc-131">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="c1abc-131">-WaitForCompletion</span></span>
<span data-ttu-id="c1abc-132">Cmdlet 'in işlemin tamamlanması için beklemesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1abc-132">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="c1abc-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="c1abc-133">-Confirm</span></span>
<span data-ttu-id="c1abc-134">İşlemi başlatmadan önce onay ister.</span><span class="sxs-lookup"><span data-stu-id="c1abc-134">Prompts  for confirmation before starting the operation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1abc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1abc-135">-WhatIf</span></span>
<span data-ttu-id="c1abc-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c1abc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1abc-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c1abc-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1abc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1abc-138">CommonParameters</span></span>
<span data-ttu-id="c1abc-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c1abc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1abc-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1abc-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1abc-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c1abc-141">INPUTS</span></span>

### <span data-ttu-id="c1abc-142">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrkorunabilir öğesi</span><span class="sxs-lookup"><span data-stu-id="c1abc-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="c1abc-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c1abc-143">OUTPUTS</span></span>

### <span data-ttu-id="c1abc-144">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c1abc-144">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c1abc-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c1abc-145">NOTES</span></span>

## <span data-ttu-id="c1abc-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c1abc-146">RELATED LINKS</span></span>

[<span data-ttu-id="c1abc-147">Get-Azurermrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="c1abc-147">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="c1abc-148">Remove-Azurermrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="c1abc-148">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="c1abc-149">Set-Azurermrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="c1abc-149">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
