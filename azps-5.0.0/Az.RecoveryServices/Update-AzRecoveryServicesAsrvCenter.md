---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 9e4ee275bf003dfa011eba4f00aad0029b5152de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279168"
---
# <span data-ttu-id="8c552-101">Update-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="8c552-101">Update-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="8c552-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c552-102">SYNOPSIS</span></span>
<span data-ttu-id="8c552-103">Kaydettirilmiş bir vCenter için keşif ayrıntılarını güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="8c552-103">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="8c552-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8c552-104">SYNTAX</span></span>

### <span data-ttu-id="8c552-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8c552-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c552-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="8c552-106">ByResourceId</span></span>
```
Update-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c552-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8c552-107">DESCRIPTION</span></span>
<span data-ttu-id="8c552-108">**Update-AzRecoveryServicesAsrvCenter** cmdlet 'i, kaydedilen bir vCenter için keşif ayrıntılarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8c552-108">The **Update-AzRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="8c552-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8c552-109">EXAMPLES</span></span>

### <span data-ttu-id="8c552-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8c552-110">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="8c552-111">Kaydettirilmiş bir vCenter için keşif ayrıntılarını güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="8c552-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="8c552-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8c552-112">PARAMETERS</span></span>

### <span data-ttu-id="8c552-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="8c552-113">-Account</span></span>
<span data-ttu-id="8c552-114">vCenter oturum açma kimlik bilgileri hesabı.</span><span class="sxs-lookup"><span data-stu-id="8c552-114">vCenter login credentials account.</span></span>

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

### <span data-ttu-id="8c552-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c552-115">-DefaultProfile</span></span>
<span data-ttu-id="8c552-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8c552-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c552-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c552-117">-InputObject</span></span>
<span data-ttu-id="8c552-118">Keşif ayrıntılarını güncelleştirmek için vCenter Server nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8c552-118">The vCenter server object to update discovery details for.</span></span>

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

### <span data-ttu-id="8c552-119">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="8c552-119">-Port</span></span>
<span data-ttu-id="8c552-120">Bulma için kullanılacak vCenter sunucusundaki TCP bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="8c552-120">The TCP port on the vCenter server to use for discovery.</span></span>

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

### <span data-ttu-id="8c552-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8c552-121">-ResourceId</span></span>
<span data-ttu-id="8c552-122">VCenter 'ın RESOURCEID 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c552-122">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="8c552-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="8c552-123">-Confirm</span></span>
<span data-ttu-id="8c552-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8c552-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c552-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c552-125">-WhatIf</span></span>
<span data-ttu-id="8c552-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8c552-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c552-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8c552-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c552-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c552-128">CommonParameters</span></span>
<span data-ttu-id="8c552-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8c552-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c552-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8c552-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c552-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8c552-131">INPUTS</span></span>

### <span data-ttu-id="8c552-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8c552-132">System.String</span></span>

### <span data-ttu-id="8c552-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="8c552-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="8c552-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8c552-134">OUTPUTS</span></span>

### <span data-ttu-id="8c552-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8c552-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8c552-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8c552-136">NOTES</span></span>

## <span data-ttu-id="8c552-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8c552-137">RELATED LINKS</span></span>
