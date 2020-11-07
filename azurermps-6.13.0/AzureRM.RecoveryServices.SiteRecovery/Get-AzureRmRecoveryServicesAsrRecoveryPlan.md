---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 571fe3c2afc8c2bf2932980f2b8f4de16fcda7c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762293"
---
# <span data-ttu-id="6ee8f-101">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6ee8f-101">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="6ee8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ee8f-102">SYNOPSIS</span></span>
<span data-ttu-id="6ee8f-103">Kurtarma planı veya kurtarma hizmetleri kasasındaki tüm kurtarma planlarını alır</span><span class="sxs-lookup"><span data-stu-id="6ee8f-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ee8f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ee8f-104">SYNTAX</span></span>

### <span data-ttu-id="6ee8f-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6ee8f-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ee8f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6ee8f-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ee8f-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6ee8f-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ee8f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ee8f-108">DESCRIPTION</span></span>
<span data-ttu-id="6ee8f-109">**Get-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet 'ı, kurtarma hizmetleri kasasındaki belirtilen kurtarma planının veya tüm kurtarma planlarının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="6ee8f-109">The **Get-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="6ee8f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ee8f-110">EXAMPLES</span></span>

### <span data-ttu-id="6ee8f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6ee8f-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="6ee8f-112">Belirtilen ada sahip kurtarma planını alır.</span><span class="sxs-lookup"><span data-stu-id="6ee8f-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="6ee8f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ee8f-113">PARAMETERS</span></span>

### <span data-ttu-id="6ee8f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ee8f-114">-DefaultProfile</span></span>
<span data-ttu-id="6ee8f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6ee8f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6ee8f-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6ee8f-116">-FriendlyName</span></span>
<span data-ttu-id="6ee8f-117">Alınacak kurtarma planının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ee8f-117">Specifies the friendly name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="6ee8f-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="6ee8f-118">-Name</span></span>
<span data-ttu-id="6ee8f-119">Alınacak kurtarma planının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ee8f-119">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="6ee8f-120">-Yol</span><span class="sxs-lookup"><span data-stu-id="6ee8f-120">-Path</span></span>
<span data-ttu-id="6ee8f-121">Bu cmdlet 'in kurtarma planı JSON tanımını kaydettiği dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ee8f-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="6ee8f-122">JSON tanımı, kurtarma planını değiştirmek ve Update-AzureRmRecoveryServicesASRRecoveryPlan cmdlet 'i aracılığıyla kurtarma planını güncelleştirmek için kullanılmak üzere düzenlenebilir.</span><span class="sxs-lookup"><span data-stu-id="6ee8f-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzureRmRecoveryServicesASRRecoveryPlan cmdlet</span></span>

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

### <span data-ttu-id="6ee8f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ee8f-123">CommonParameters</span></span>
<span data-ttu-id="6ee8f-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ee8f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ee8f-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ee8f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ee8f-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ee8f-126">INPUTS</span></span>

### <span data-ttu-id="6ee8f-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6ee8f-127">None</span></span>

## <span data-ttu-id="6ee8f-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ee8f-128">OUTPUTS</span></span>

### <span data-ttu-id="6ee8f-129">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6ee8f-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6ee8f-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ee8f-130">NOTES</span></span>

## <span data-ttu-id="6ee8f-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ee8f-131">RELATED LINKS</span></span>

[<span data-ttu-id="6ee8f-132">Yeni-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6ee8f-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="6ee8f-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6ee8f-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="6ee8f-134">Güncelleştirme-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6ee8f-134">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
