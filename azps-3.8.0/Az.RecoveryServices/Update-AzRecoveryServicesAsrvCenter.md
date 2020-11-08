---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 9e4ee275bf003dfa011eba4f00aad0029b5152de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098989"
---
# <span data-ttu-id="bb039-101">Update-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="bb039-101">Update-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="bb039-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb039-102">SYNOPSIS</span></span>
<span data-ttu-id="bb039-103">Kaydettirilmiş bir vCenter için keşif ayrıntılarını güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="bb039-103">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="bb039-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bb039-104">SYNTAX</span></span>

### <span data-ttu-id="bb039-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bb039-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb039-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="bb039-106">ByResourceId</span></span>
```
Update-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb039-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bb039-107">DESCRIPTION</span></span>
<span data-ttu-id="bb039-108">**Update-AzRecoveryServicesAsrvCenter** cmdlet 'i, kaydedilen bir vCenter için keşif ayrıntılarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="bb039-108">The **Update-AzRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="bb039-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bb039-109">EXAMPLES</span></span>

### <span data-ttu-id="bb039-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bb039-110">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="bb039-111">Kaydettirilmiş bir vCenter için keşif ayrıntılarını güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="bb039-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="bb039-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bb039-112">PARAMETERS</span></span>

### <span data-ttu-id="bb039-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="bb039-113">-Account</span></span>
<span data-ttu-id="bb039-114">vCenter oturum açma kimlik bilgileri hesabı.</span><span class="sxs-lookup"><span data-stu-id="bb039-114">vCenter login credentials account.</span></span>

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

### <span data-ttu-id="bb039-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb039-115">-DefaultProfile</span></span>
<span data-ttu-id="bb039-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bb039-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb039-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb039-117">-InputObject</span></span>
<span data-ttu-id="bb039-118">Keşif ayrıntılarını güncelleştirmek için vCenter Server nesnesi.</span><span class="sxs-lookup"><span data-stu-id="bb039-118">The vCenter server object to update discovery details for.</span></span>

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

### <span data-ttu-id="bb039-119">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="bb039-119">-Port</span></span>
<span data-ttu-id="bb039-120">Bulma için kullanılacak vCenter sunucusundaki TCP bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="bb039-120">The TCP port on the vCenter server to use for discovery.</span></span>

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

### <span data-ttu-id="bb039-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bb039-121">-ResourceId</span></span>
<span data-ttu-id="bb039-122">VCenter 'ın RESOURCEID 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb039-122">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="bb039-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="bb039-123">-Confirm</span></span>
<span data-ttu-id="bb039-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bb039-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb039-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb039-125">-WhatIf</span></span>
<span data-ttu-id="bb039-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bb039-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb039-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bb039-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb039-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb039-128">CommonParameters</span></span>
<span data-ttu-id="bb039-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bb039-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb039-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bb039-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb039-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bb039-131">INPUTS</span></span>

### <span data-ttu-id="bb039-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bb039-132">System.String</span></span>

### <span data-ttu-id="bb039-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="bb039-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="bb039-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bb039-134">OUTPUTS</span></span>

### <span data-ttu-id="bb039-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="bb039-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bb039-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bb039-136">NOTES</span></span>

## <span data-ttu-id="bb039-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bb039-137">RELATED LINKS</span></span>
