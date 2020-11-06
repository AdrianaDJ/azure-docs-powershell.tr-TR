---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 59C3E7D7-530F-4D07-904E-41610ECE9253
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/edit-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 8c078c97a1531863979b6182867e8900550b68b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592891"
---
# <span data-ttu-id="e68ac-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e68ac-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="e68ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e68ac-102">SYNOPSIS</span></span>
<span data-ttu-id="e68ac-103">Site kurtarma planını düzenler.</span><span class="sxs-lookup"><span data-stu-id="e68ac-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e68ac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e68ac-104">SYNTAX</span></span>

### <span data-ttu-id="e68ac-105">AppendGroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e68ac-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e68ac-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="e68ac-106">RemoveGroup</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e68ac-107">AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="e68ac-107">AddProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e68ac-108">RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="e68ac-108">RemoveProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e68ac-109">Addreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="e68ac-109">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e68ac-110">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="e68ac-110">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e68ac-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="e68ac-111">DESCRIPTION</span></span>
<span data-ttu-id="e68ac-112">**Edit-AzureRmSiteRecoveryRecoveryPlan** cmdlet 'ı bir Azure Site kurtarma planını düzenler.</span><span class="sxs-lookup"><span data-stu-id="e68ac-112">The **Edit-AzureRmSiteRecoveryRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="e68ac-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e68ac-113">EXAMPLES</span></span>

## <span data-ttu-id="e68ac-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e68ac-114">PARAMETERS</span></span>

### <span data-ttu-id="e68ac-115">-AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="e68ac-115">-AddProtectedEntities</span></span>
<span data-ttu-id="e68ac-116">Eklenecek bir korumalı varlık dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e68ac-116">Specifies an array of protected entities to add.</span></span>

```yaml
Type: ASRProtectionEntity[]
Parameter Sets: AddProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e68ac-117">-Addkorunabilir</span><span class="sxs-lookup"><span data-stu-id="e68ac-117">-AddProtectedItems</span></span>
```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e68ac-118">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="e68ac-118">-AppendGroup</span></span>
<span data-ttu-id="e68ac-119">Bu işlemin grubu kurtarma planı nesnesine ekleydiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e68ac-119">Indicates that this operation appends the group to the recovery plan object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AppendGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e68ac-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e68ac-120">-DefaultProfile</span></span>
<span data-ttu-id="e68ac-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e68ac-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e68ac-122">-Group</span><span class="sxs-lookup"><span data-stu-id="e68ac-122">-Group</span></span>
<span data-ttu-id="e68ac-123">Bir site kurtarma planı grubu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e68ac-123">Specifies a Site Recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: AddProtectedEntities, RemoveProtectedEntities, AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e68ac-124">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e68ac-124">-RecoveryPlan</span></span>
<span data-ttu-id="e68ac-125">Kurtarma planı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e68ac-125">Specifies a recovery plan.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e68ac-126">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="e68ac-126">-RemoveGroup</span></span>
<span data-ttu-id="e68ac-127">Belirtilen site kurtarma kurtarma planı grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e68ac-127">Removes the specified Site Recovery recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e68ac-128">-RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="e68ac-128">-RemoveProtectedEntities</span></span>
<span data-ttu-id="e68ac-129">Korumalı varlıklar dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e68ac-129">Specifies an array of protected entities.</span></span>

```yaml
Type: ASRProtectionEntity[]
Parameter Sets: RemoveProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e68ac-130">-Removekorunabilir</span><span class="sxs-lookup"><span data-stu-id="e68ac-130">-RemoveProtectedItems</span></span>
```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e68ac-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e68ac-131">CommonParameters</span></span>
<span data-ttu-id="e68ac-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e68ac-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e68ac-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e68ac-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e68ac-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e68ac-134">INPUTS</span></span>

### <span data-ttu-id="e68ac-135">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e68ac-135">ASRRecoveryPlan</span></span>
<span data-ttu-id="e68ac-136">' RecoveryPlan ' parametresi ardışık düzenin ' ASRRecoveryPlan ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="e68ac-136">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="e68ac-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e68ac-137">OUTPUTS</span></span>

## <span data-ttu-id="e68ac-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e68ac-138">NOTES</span></span>

## <span data-ttu-id="e68ac-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e68ac-139">RELATED LINKS</span></span>

[<span data-ttu-id="e68ac-140">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e68ac-140">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="e68ac-141">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e68ac-141">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)
