---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: F801A78E-6C11-4BD1-BEF4-01C4D6CD36D7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: dcd7b85810c78fa772098f24c428b5f9c8c44183
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587777"
---
# <span data-ttu-id="87d79-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="87d79-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="87d79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87d79-102">SYNOPSIS</span></span>
<span data-ttu-id="87d79-103">Korumalı öğe oluşturarak korunabilir bir öğe için çoğaltmayı olanaklı kılar</span><span class="sxs-lookup"><span data-stu-id="87d79-103">Enables replication for a protectable item by creating a protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87d79-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="87d79-104">SYNTAX</span></span>

### <span data-ttu-id="87d79-105">DisableDR (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="87d79-105">DisableDR (Default)</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87d79-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="87d79-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87d79-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="87d79-107">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87d79-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="87d79-108">HyperVSiteToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87d79-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="87d79-109">DESCRIPTION</span></span>
<span data-ttu-id="87d79-110">**New-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet 'i yeni bir çoğaltma korumalı öğe oluşturur.</span><span class="sxs-lookup"><span data-stu-id="87d79-110">The **New-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet creates a new Replication Protected item.</span></span>
<span data-ttu-id="87d79-111">Korunabilir bir öğe için çoğaltmayı etkinleştirmek amacıyla bu cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="87d79-111">Use this cmdlet to enable replication for a protectable item.</span></span>

## <span data-ttu-id="87d79-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="87d79-112">EXAMPLES</span></span>

## <span data-ttu-id="87d79-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="87d79-113">PARAMETERS</span></span>

### <span data-ttu-id="87d79-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="87d79-114">-Name</span></span>
<span data-ttu-id="87d79-115">Azure Site Recovery çoğaltması korumalı öğesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87d79-115">Specifies the name of the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d79-116">-İşletim sistemi</span><span class="sxs-lookup"><span data-stu-id="87d79-116">-OS</span></span>
<span data-ttu-id="87d79-117">İşletim sistemi ailesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="87d79-117">Specifies the operating system family.</span></span>
<span data-ttu-id="87d79-118">Bu parametre için kabul edilebilir değerler: Windows veya Linux.</span><span class="sxs-lookup"><span data-stu-id="87d79-118">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d79-119">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="87d79-119">-OSDiskName</span></span>
<span data-ttu-id="87d79-120">İşletim sistemi diskinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87d79-120">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d79-121">-Korunabilir öğe</span><span class="sxs-lookup"><span data-stu-id="87d79-121">-ProtectableItem</span></span>
<span data-ttu-id="87d79-122">Azure Site Recovery korunabilir öğesi öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="87d79-122">Specifies the Azure Site Recovery Protectable Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87d79-123">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="87d79-123">-ProtectionContainerMapping</span></span>
<span data-ttu-id="87d79-124">Çoğaltma için kullanılacak Azure Site Recovery koruma kapsayıcısı eşleme nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="87d79-124">Specifies the Azure Site Recovery Protection Container mapping object to use for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d79-125">-Recoveryazurestorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="87d79-125">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="87d79-126">Bu cmdlet 'in çoğaltıldığı Azure depolama hesabının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="87d79-126">Specifies the ID of the Azure storage account that this cmdlet replicates to.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d79-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="87d79-127">-WaitForCompletion</span></span>
<span data-ttu-id="87d79-128">Cmdlet 'in tamamlanma için beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="87d79-128">Indicates that the cmdlet waits for completion.</span></span>

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

### <span data-ttu-id="87d79-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="87d79-129">-Confirm</span></span>
<span data-ttu-id="87d79-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="87d79-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87d79-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87d79-131">-WhatIf</span></span>
<span data-ttu-id="87d79-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="87d79-132">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="87d79-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="87d79-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87d79-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87d79-134">-DefaultProfile</span></span>
<span data-ttu-id="87d79-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="87d79-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d79-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87d79-136">CommonParameters</span></span>
<span data-ttu-id="87d79-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="87d79-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87d79-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87d79-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87d79-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="87d79-139">INPUTS</span></span>

### <span data-ttu-id="87d79-140">Asrkorunabilir öğe</span><span class="sxs-lookup"><span data-stu-id="87d79-140">ASRProtectableItem</span></span>
<span data-ttu-id="87d79-141">Parametre ' korunabilir öğe ', ardışık düzenin ' Asrkorunabilir öğe ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="87d79-141">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

## <span data-ttu-id="87d79-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="87d79-142">OUTPUTS</span></span>

### <span data-ttu-id="87d79-143">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="87d79-143">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="87d79-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="87d79-144">NOTES</span></span>

## <span data-ttu-id="87d79-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="87d79-145">RELATED LINKS</span></span>

[<span data-ttu-id="87d79-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="87d79-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="87d79-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="87d79-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="87d79-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="87d79-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
