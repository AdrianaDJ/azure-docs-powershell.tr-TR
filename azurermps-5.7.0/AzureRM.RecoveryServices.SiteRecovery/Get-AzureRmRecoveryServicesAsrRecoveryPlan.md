---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: b95c3ab14d50558ef184beabcd461a59bb1a05ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588831"
---
# <span data-ttu-id="b229d-101">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b229d-101">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="b229d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b229d-102">SYNOPSIS</span></span>
<span data-ttu-id="b229d-103">Kurtarma planı veya kurtarma hizmetleri kasasındaki tüm kurtarma planlarını alır</span><span class="sxs-lookup"><span data-stu-id="b229d-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b229d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b229d-104">SYNTAX</span></span>

### <span data-ttu-id="b229d-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b229d-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b229d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b229d-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b229d-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="b229d-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b229d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b229d-108">DESCRIPTION</span></span>
<span data-ttu-id="b229d-109">**Get-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet 'ı, kurtarma hizmetleri kasasındaki belirtilen kurtarma planının veya tüm kurtarma planlarının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="b229d-109">The **Get-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="b229d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b229d-110">EXAMPLES</span></span>

### <span data-ttu-id="b229d-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b229d-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="b229d-112">Belirtilen ada sahip kurtarma planını alır.</span><span class="sxs-lookup"><span data-stu-id="b229d-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="b229d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b229d-113">PARAMETERS</span></span>

### <span data-ttu-id="b229d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b229d-114">-DefaultProfile</span></span>
<span data-ttu-id="b229d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b229d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="b229d-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b229d-116">-FriendlyName</span></span>
<span data-ttu-id="b229d-117">Alınacak kurtarma planının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b229d-117">Specifies the friendly name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="b229d-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="b229d-118">-Name</span></span>
<span data-ttu-id="b229d-119">Alınacak kurtarma planının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b229d-119">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="b229d-120">-Yol</span><span class="sxs-lookup"><span data-stu-id="b229d-120">-Path</span></span>
<span data-ttu-id="b229d-121">Bu cmdlet 'in kurtarma planı JSON tanımını kaydettiği dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b229d-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="b229d-122">JSON tanımı, kurtarma planını değiştirmek ve Update-AzureRmRecoveryServicesASRRecoveryPlan cmdlet 'i aracılığıyla kurtarma planını güncelleştirmek için kullanılmak üzere düzenlenebilir.</span><span class="sxs-lookup"><span data-stu-id="b229d-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzureRmRecoveryServicesASRRecoveryPlan cmdlet</span></span>

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

### <span data-ttu-id="b229d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b229d-123">CommonParameters</span></span>
<span data-ttu-id="b229d-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b229d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b229d-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b229d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b229d-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b229d-126">INPUTS</span></span>

### <span data-ttu-id="b229d-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b229d-127">None</span></span>

## <span data-ttu-id="b229d-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b229d-128">OUTPUTS</span></span>

### <span data-ttu-id="b229d-129">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b229d-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b229d-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b229d-130">NOTES</span></span>

## <span data-ttu-id="b229d-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b229d-131">RELATED LINKS</span></span>

[<span data-ttu-id="b229d-132">Yeni-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b229d-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="b229d-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b229d-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="b229d-134">Güncelleştirme-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b229d-134">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
