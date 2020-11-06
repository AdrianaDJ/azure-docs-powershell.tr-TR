---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 298443c4b962a2be6c5cf3849657d0fe8bbaf978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587456"
---
# <span data-ttu-id="9cf11-101">Update-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="9cf11-101">Update-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="9cf11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cf11-102">SYNOPSIS</span></span>
<span data-ttu-id="9cf11-103">Kaydettirilmiş bir vCenter için keşif ayrıntılarını güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="9cf11-103">Update discovery details for a registered vCenter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cf11-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9cf11-104">SYNTAX</span></span>

### <span data-ttu-id="9cf11-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9cf11-105">Default (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cf11-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="9cf11-106">ByResourceId</span></span>
```
Update-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cf11-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9cf11-107">DESCRIPTION</span></span>
<span data-ttu-id="9cf11-108">**Update-AzureRmRecoveryServicesAsrvCenter** cmdlet 'i, kaydedilen bir vCenter için keşif ayrıntılarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9cf11-108">The **Update-AzureRmRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="9cf11-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9cf11-109">EXAMPLES</span></span>

### <span data-ttu-id="9cf11-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9cf11-110">Example 1</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="9cf11-111">Kaydettirilmiş bir vCenter için keşif ayrıntılarını güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="9cf11-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="9cf11-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9cf11-112">PARAMETERS</span></span>

### <span data-ttu-id="9cf11-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="9cf11-113">-Account</span></span>
<span data-ttu-id="9cf11-114">vCenter oturum açma kimlik bilgileri hesabı.</span><span class="sxs-lookup"><span data-stu-id="9cf11-114">vCenter login credentials account.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf11-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="9cf11-115">-Confirm</span></span>
<span data-ttu-id="9cf11-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9cf11-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cf11-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cf11-117">-DefaultProfile</span></span>
<span data-ttu-id="9cf11-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9cf11-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cf11-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cf11-119">-InputObject</span></span>
<span data-ttu-id="9cf11-120">Keşif ayrıntılarını güncelleştirmek için vCenter Server nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9cf11-120">The vCenter server object to update discovery details for.</span></span>

```yaml
Type: ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cf11-121">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="9cf11-121">-Port</span></span>
<span data-ttu-id="9cf11-122">Bulma için kullanılacak vCenter sunucusundaki TCP bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="9cf11-122">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: Int32
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf11-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9cf11-123">-ResourceId</span></span>
<span data-ttu-id="9cf11-124">VCenter 'ın RESOURCEID 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="9cf11-124">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cf11-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cf11-125">-WhatIf</span></span>
<span data-ttu-id="9cf11-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9cf11-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cf11-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9cf11-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cf11-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cf11-128">CommonParameters</span></span>
<span data-ttu-id="9cf11-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9cf11-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cf11-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cf11-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cf11-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9cf11-131">INPUTS</span></span>

### <span data-ttu-id="9cf11-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="9cf11-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="9cf11-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9cf11-133">OUTPUTS</span></span>

### <span data-ttu-id="9cf11-134">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. Sıterecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9cf11-134">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9cf11-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9cf11-135">NOTES</span></span>

## <span data-ttu-id="9cf11-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9cf11-136">RELATED LINKS</span></span>
