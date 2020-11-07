---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: a10f7ffb1b05474e5d2b86fa7d7a55f825aaad25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764793"
---
# <span data-ttu-id="45a4b-101">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="45a4b-101">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="45a4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45a4b-102">SYNOPSIS</span></span>
<span data-ttu-id="45a4b-103">Kurtarma planı veya kurtarma hizmetleri kasasındaki tüm kurtarma planlarını alır</span><span class="sxs-lookup"><span data-stu-id="45a4b-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45a4b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="45a4b-104">SYNTAX</span></span>

### <span data-ttu-id="45a4b-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="45a4b-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan [<CommonParameters>]
```

### <span data-ttu-id="45a4b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="45a4b-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>] [<CommonParameters>]
```

### <span data-ttu-id="45a4b-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="45a4b-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>] [<CommonParameters>]
```

## <span data-ttu-id="45a4b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="45a4b-108">DESCRIPTION</span></span>
<span data-ttu-id="45a4b-109">**Get-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet 'ı, kurtarma hizmetleri kasasındaki belirtilen kurtarma planının veya tüm kurtarma planlarının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="45a4b-109">The **Get-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="45a4b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="45a4b-110">EXAMPLES</span></span>

### <span data-ttu-id="45a4b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="45a4b-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="45a4b-112">Belirtilen ada sahip kurtarma planını alır.</span><span class="sxs-lookup"><span data-stu-id="45a4b-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="45a4b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="45a4b-113">PARAMETERS</span></span>

### <span data-ttu-id="45a4b-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="45a4b-114">-FriendlyName</span></span>
<span data-ttu-id="45a4b-115">Alınacak kurtarma planının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="45a4b-115">Specifies the friendly name of the recovery plan to get.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a4b-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="45a4b-116">-Name</span></span>
<span data-ttu-id="45a4b-117">Alınacak kurtarma planının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="45a4b-117">Specifies the name of the recovery plan to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a4b-118">-Yol</span><span class="sxs-lookup"><span data-stu-id="45a4b-118">-Path</span></span>
<span data-ttu-id="45a4b-119">Bu cmdlet 'in kurtarma planı JSON tanımını kaydettiği dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="45a4b-119">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="45a4b-120">JSON tanımı, kurtarma planını değiştirmek ve Update-AzureRmRecoveryServicesASRRecoveryPlan cmdlet 'i aracılığıyla kurtarma planını güncelleştirmek için kullanılmak üzere düzenlenebilir.</span><span class="sxs-lookup"><span data-stu-id="45a4b-120">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzureRmRecoveryServicesASRRecoveryPlan cmdlet</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByFriendlyName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a4b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45a4b-121">CommonParameters</span></span>
<span data-ttu-id="45a4b-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="45a4b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45a4b-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45a4b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45a4b-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="45a4b-124">INPUTS</span></span>

### <span data-ttu-id="45a4b-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="45a4b-125">None</span></span>

## <span data-ttu-id="45a4b-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="45a4b-126">OUTPUTS</span></span>

### <span data-ttu-id="45a4b-127">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="45a4b-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="45a4b-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="45a4b-128">NOTES</span></span>

## <span data-ttu-id="45a4b-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="45a4b-129">RELATED LINKS</span></span>

[<span data-ttu-id="45a4b-130">Yeni-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="45a4b-130">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="45a4b-131">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="45a4b-131">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="45a4b-132">Güncelleştirme-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="45a4b-132">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
