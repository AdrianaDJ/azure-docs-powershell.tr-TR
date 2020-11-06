---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: F801A78E-6C11-4BD1-BEF4-01C4D6CD36D7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 28b2f976b85d7db40cdb80cf2b9b58a2d7692952
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593384"
---
# <span data-ttu-id="34379-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="34379-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="34379-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34379-102">SYNOPSIS</span></span>
<span data-ttu-id="34379-103">Korumalı öğe oluşturarak korunabilir bir öğe için çoğaltmayı olanaklı kılar</span><span class="sxs-lookup"><span data-stu-id="34379-103">Enables replication for a protectable item by creating a protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34379-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34379-104">SYNTAX</span></span>

### <span data-ttu-id="34379-105">DisableDR (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="34379-105">DisableDR (Default)</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34379-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="34379-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34379-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="34379-107">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34379-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="34379-108">HyperVSiteToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34379-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="34379-109">DESCRIPTION</span></span>
<span data-ttu-id="34379-110">**New-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet 'i yeni bir çoğaltma korumalı öğe oluşturur.</span><span class="sxs-lookup"><span data-stu-id="34379-110">The **New-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet creates a new Replication Protected item.</span></span>
<span data-ttu-id="34379-111">Korunabilir bir öğe için çoğaltmayı etkinleştirmek amacıyla bu cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="34379-111">Use this cmdlet to enable replication for a protectable item.</span></span>

## <span data-ttu-id="34379-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34379-112">EXAMPLES</span></span>

## <span data-ttu-id="34379-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34379-113">PARAMETERS</span></span>

### <span data-ttu-id="34379-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34379-114">-DefaultProfile</span></span>
<span data-ttu-id="34379-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34379-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34379-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="34379-116">-Name</span></span>
<span data-ttu-id="34379-117">Azure Site Recovery çoğaltması korumalı öğesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="34379-117">Specifies the name of the Azure Site Recovery Replication Protected Item.</span></span>

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

### <span data-ttu-id="34379-118">-İşletim sistemi</span><span class="sxs-lookup"><span data-stu-id="34379-118">-OS</span></span>
<span data-ttu-id="34379-119">İşletim sistemi ailesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="34379-119">Specifies the operating system family.</span></span>
<span data-ttu-id="34379-120">Bu parametre için kabul edilebilir değerler: Windows veya Linux.</span><span class="sxs-lookup"><span data-stu-id="34379-120">The acceptable values for this parameter are: Windows or Linux.</span></span>

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

### <span data-ttu-id="34379-121">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="34379-121">-OSDiskName</span></span>
<span data-ttu-id="34379-122">İşletim sistemi diskinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="34379-122">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="34379-123">-Korunabilir öğe</span><span class="sxs-lookup"><span data-stu-id="34379-123">-ProtectableItem</span></span>
<span data-ttu-id="34379-124">Azure Site Recovery korunabilir öğesi öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="34379-124">Specifies the Azure Site Recovery Protectable Item.</span></span>

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

### <span data-ttu-id="34379-125">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="34379-125">-ProtectionContainerMapping</span></span>
<span data-ttu-id="34379-126">Çoğaltma için kullanılacak Azure Site Recovery koruma kapsayıcısı eşleme nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="34379-126">Specifies the Azure Site Recovery Protection Container mapping object to use for replication.</span></span>

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

### <span data-ttu-id="34379-127">-Recoveryazurestorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="34379-127">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="34379-128">Bu cmdlet 'in çoğaltıldığı Azure depolama hesabının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="34379-128">Specifies the ID of the Azure storage account that this cmdlet replicates to.</span></span>

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

### <span data-ttu-id="34379-129">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="34379-129">-WaitForCompletion</span></span>
<span data-ttu-id="34379-130">Cmdlet 'in tamamlanma için beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="34379-130">Indicates that the cmdlet waits for completion.</span></span>

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

### <span data-ttu-id="34379-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="34379-131">-Confirm</span></span>
<span data-ttu-id="34379-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="34379-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34379-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34379-133">-WhatIf</span></span>
<span data-ttu-id="34379-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="34379-134">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="34379-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="34379-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34379-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34379-136">CommonParameters</span></span>
<span data-ttu-id="34379-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34379-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34379-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34379-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34379-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34379-139">INPUTS</span></span>

### <span data-ttu-id="34379-140">Asrkorunabilir öğe</span><span class="sxs-lookup"><span data-stu-id="34379-140">ASRProtectableItem</span></span>
<span data-ttu-id="34379-141">Parametre ' korunabilir öğe ', ardışık düzenin ' Asrkorunabilir öğe ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="34379-141">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

## <span data-ttu-id="34379-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34379-142">OUTPUTS</span></span>

### <span data-ttu-id="34379-143">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="34379-143">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="34379-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34379-144">NOTES</span></span>

## <span data-ttu-id="34379-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34379-145">RELATED LINKS</span></span>

[<span data-ttu-id="34379-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="34379-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="34379-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="34379-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="34379-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="34379-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
