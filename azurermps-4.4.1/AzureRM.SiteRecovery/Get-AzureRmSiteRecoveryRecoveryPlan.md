---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3B879056-5BF3-4262-8BAA-E79589149370
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 2d9f087b87d99003b559fc363265fdb4b996c3f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589073"
---
# <span data-ttu-id="c598c-101">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c598c-101">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="c598c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c598c-102">SYNOPSIS</span></span>
<span data-ttu-id="c598c-103">Site kurtarma 'da kurtarma planı alır.</span><span class="sxs-lookup"><span data-stu-id="c598c-103">Gets a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c598c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c598c-104">SYNTAX</span></span>

### <span data-ttu-id="c598c-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c598c-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c598c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c598c-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c598c-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="c598c-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c598c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c598c-108">DESCRIPTION</span></span>
<span data-ttu-id="c598c-109">**Get-AzureRmSiteRecoveryRecoveryPlan** cmdlet 'ı Azure Site Recovery 'de bir kurtarma planı alır.</span><span class="sxs-lookup"><span data-stu-id="c598c-109">The **Get-AzureRmSiteRecoveryRecoveryPlan** cmdlet gets a recovery plan in Azure Site Recovery.</span></span>

## <span data-ttu-id="c598c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c598c-110">EXAMPLES</span></span>

## <span data-ttu-id="c598c-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c598c-111">PARAMETERS</span></span>

### <span data-ttu-id="c598c-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c598c-112">-FriendlyName</span></span>
<span data-ttu-id="c598c-113">Bu cmdlet 'in aldığı kurtarma planının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c598c-113">Specifies the friendly name of the recovery plan that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c598c-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="c598c-114">-Name</span></span>
<span data-ttu-id="c598c-115">Bu cmdlet 'in aldığı kurtarma planının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c598c-115">Specifies the name of the recovery plan that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c598c-116">-Yol</span><span class="sxs-lookup"><span data-stu-id="c598c-116">-Path</span></span>
<span data-ttu-id="c598c-117">Bu cmdlet 'in kurtarma planını kaydettiği dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c598c-117">Specifies the file path to which this cmdlet saves the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByFriendlyName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c598c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c598c-118">-DefaultProfile</span></span>
<span data-ttu-id="c598c-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c598c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c598c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c598c-120">CommonParameters</span></span>
<span data-ttu-id="c598c-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c598c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c598c-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c598c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c598c-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c598c-123">INPUTS</span></span>

## <span data-ttu-id="c598c-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c598c-124">OUTPUTS</span></span>

### <span data-ttu-id="c598c-125">System. Koleksiyonlar. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRRecoveryPlan]</span><span class="sxs-lookup"><span data-stu-id="c598c-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan]</span></span>

## <span data-ttu-id="c598c-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c598c-126">NOTES</span></span>

## <span data-ttu-id="c598c-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c598c-127">RELATED LINKS</span></span>

[<span data-ttu-id="c598c-128">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c598c-128">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="c598c-129">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c598c-129">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="c598c-130">Güncelleştirme-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c598c-130">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)
