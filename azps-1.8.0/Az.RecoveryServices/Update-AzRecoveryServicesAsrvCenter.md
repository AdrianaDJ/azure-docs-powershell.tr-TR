---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: d6e26eb293a2b87fccc0749b6d5c53d15d7d860f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759567"
---
# <span data-ttu-id="bbda1-101">Update-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="bbda1-101">Update-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="bbda1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbda1-102">SYNOPSIS</span></span>
<span data-ttu-id="bbda1-103">Kaydettirilmiş bir vCenter için keşif ayrıntılarını güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="bbda1-103">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="bbda1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bbda1-104">SYNTAX</span></span>

### <span data-ttu-id="bbda1-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bbda1-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbda1-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="bbda1-106">ByResourceId</span></span>
```
Update-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbda1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bbda1-107">DESCRIPTION</span></span>
<span data-ttu-id="bbda1-108">**Update-AzRecoveryServicesAsrvCenter** cmdlet 'i, kaydedilen bir vCenter için keşif ayrıntılarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="bbda1-108">The **Update-AzRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="bbda1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bbda1-109">EXAMPLES</span></span>

### <span data-ttu-id="bbda1-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bbda1-110">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="bbda1-111">Kaydettirilmiş bir vCenter için keşif ayrıntılarını güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="bbda1-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="bbda1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bbda1-112">PARAMETERS</span></span>

### <span data-ttu-id="bbda1-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="bbda1-113">-Account</span></span>
<span data-ttu-id="bbda1-114">vCenter oturum açma kimlik bilgileri hesabı.</span><span class="sxs-lookup"><span data-stu-id="bbda1-114">vCenter login credentials account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbda1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbda1-115">-DefaultProfile</span></span>
<span data-ttu-id="bbda1-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bbda1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbda1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbda1-117">-InputObject</span></span>
<span data-ttu-id="bbda1-118">Keşif ayrıntılarını güncelleştirmek için vCenter Server nesnesi.</span><span class="sxs-lookup"><span data-stu-id="bbda1-118">The vCenter server object to update discovery details for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbda1-119">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="bbda1-119">-Port</span></span>
<span data-ttu-id="bbda1-120">Bulma için kullanılacak vCenter sunucusundaki TCP bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="bbda1-120">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbda1-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bbda1-121">-ResourceId</span></span>
<span data-ttu-id="bbda1-122">VCenter 'ın RESOURCEID 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="bbda1-122">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbda1-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="bbda1-123">-Confirm</span></span>
<span data-ttu-id="bbda1-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bbda1-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbda1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbda1-125">-WhatIf</span></span>
<span data-ttu-id="bbda1-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bbda1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbda1-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bbda1-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbda1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbda1-128">CommonParameters</span></span>
<span data-ttu-id="bbda1-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bbda1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbda1-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbda1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbda1-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bbda1-131">INPUTS</span></span>

### <span data-ttu-id="bbda1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bbda1-132">System.String</span></span>

### <span data-ttu-id="bbda1-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="bbda1-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="bbda1-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bbda1-134">OUTPUTS</span></span>

### <span data-ttu-id="bbda1-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="bbda1-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bbda1-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bbda1-136">NOTES</span></span>

## <span data-ttu-id="bbda1-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bbda1-137">RELATED LINKS</span></span>
