---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 856a316104e0e660f170de8f519dbcb66c55bd53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593918"
---
# <span data-ttu-id="f796b-101">Update-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="f796b-101">Update-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="f796b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f796b-102">SYNOPSIS</span></span>
<span data-ttu-id="f796b-103">Kaydettirilmiş bir vCenter için keşif ayrıntılarını güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="f796b-103">Update discovery details for a registered vCenter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f796b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f796b-104">SYNTAX</span></span>

### <span data-ttu-id="f796b-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f796b-105">Default (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f796b-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="f796b-106">ByResourceId</span></span>
```
Update-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f796b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f796b-107">DESCRIPTION</span></span>
<span data-ttu-id="f796b-108">**Update-AzureRmRecoveryServicesAsrvCenter** cmdlet 'i, kaydedilen bir vCenter için keşif ayrıntılarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f796b-108">The **Update-AzureRmRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="f796b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f796b-109">EXAMPLES</span></span>

### <span data-ttu-id="f796b-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f796b-110">Example 1</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="f796b-111">Kaydettirilmiş bir vCenter için keşif ayrıntılarını güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="f796b-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="f796b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f796b-112">PARAMETERS</span></span>

### <span data-ttu-id="f796b-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="f796b-113">-Account</span></span>
<span data-ttu-id="f796b-114">vCenter oturum açma kimlik bilgileri hesabı.</span><span class="sxs-lookup"><span data-stu-id="f796b-114">vCenter login credentials account.</span></span>

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

### <span data-ttu-id="f796b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f796b-115">-DefaultProfile</span></span>
<span data-ttu-id="f796b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f796b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f796b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f796b-117">-InputObject</span></span>
<span data-ttu-id="f796b-118">Keşif ayrıntılarını güncelleştirmek için vCenter Server nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f796b-118">The vCenter server object to update discovery details for.</span></span>

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

### <span data-ttu-id="f796b-119">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="f796b-119">-Port</span></span>
<span data-ttu-id="f796b-120">Bulma için kullanılacak vCenter sunucusundaki TCP bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="f796b-120">The TCP port on the vCenter server to use for discovery.</span></span>

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

### <span data-ttu-id="f796b-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f796b-121">-ResourceId</span></span>
<span data-ttu-id="f796b-122">VCenter 'ın RESOURCEID 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="f796b-122">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="f796b-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="f796b-123">-Confirm</span></span>
<span data-ttu-id="f796b-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f796b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f796b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f796b-125">-WhatIf</span></span>
<span data-ttu-id="f796b-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f796b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f796b-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f796b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f796b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f796b-128">CommonParameters</span></span>
<span data-ttu-id="f796b-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f796b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f796b-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f796b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f796b-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f796b-131">INPUTS</span></span>

### <span data-ttu-id="f796b-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="f796b-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="f796b-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f796b-133">OUTPUTS</span></span>

### <span data-ttu-id="f796b-134">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. Sıterecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f796b-134">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f796b-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f796b-135">NOTES</span></span>

## <span data-ttu-id="f796b-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f796b-136">RELATED LINKS</span></span>
