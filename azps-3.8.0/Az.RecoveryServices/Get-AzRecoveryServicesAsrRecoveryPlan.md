---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 4873c30caf0f1b59bf9be848f44c6e1358649b69
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096088"
---
# <span data-ttu-id="0e863-101">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0e863-101">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="0e863-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e863-102">SYNOPSIS</span></span>
<span data-ttu-id="0e863-103">Kurtarma planı veya kurtarma hizmetleri kasasındaki tüm kurtarma planlarını alır</span><span class="sxs-lookup"><span data-stu-id="0e863-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

## <span data-ttu-id="0e863-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0e863-104">SYNTAX</span></span>

### <span data-ttu-id="0e863-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0e863-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e863-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0e863-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e863-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="0e863-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e863-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0e863-108">DESCRIPTION</span></span>
<span data-ttu-id="0e863-109">**Get-AzRecoveryServicesAsrRecoveryPlan** cmdlet 'ı, kurtarma hizmetleri kasasındaki belirtilen kurtarma planının veya tüm kurtarma planlarının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="0e863-109">The **Get-AzRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="0e863-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0e863-110">EXAMPLES</span></span>

### <span data-ttu-id="0e863-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0e863-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="0e863-112">Belirtilen ada sahip kurtarma planını alır.</span><span class="sxs-lookup"><span data-stu-id="0e863-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="0e863-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0e863-113">PARAMETERS</span></span>

### <span data-ttu-id="0e863-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e863-114">-DefaultProfile</span></span>
<span data-ttu-id="0e863-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0e863-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0e863-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="0e863-116">-FriendlyName</span></span>
<span data-ttu-id="0e863-117">Alınacak kurtarma planının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e863-117">Specifies the friendly name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="0e863-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="0e863-118">-Name</span></span>
<span data-ttu-id="0e863-119">Alınacak kurtarma planının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e863-119">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="0e863-120">-Yol</span><span class="sxs-lookup"><span data-stu-id="0e863-120">-Path</span></span>
<span data-ttu-id="0e863-121">Bu cmdlet 'in kurtarma planı JSON tanımını kaydettiği dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e863-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="0e863-122">JSON tanımı, kurtarma planını değiştirmek ve Update-AzRecoveryServicesASRRecoveryPlan cmdlet 'i aracılığıyla kurtarma planını güncelleştirmek için kullanılmak üzere düzenlenebilir.</span><span class="sxs-lookup"><span data-stu-id="0e863-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzRecoveryServicesASRRecoveryPlan cmdlet</span></span>

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

### <span data-ttu-id="0e863-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e863-123">CommonParameters</span></span>
<span data-ttu-id="0e863-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0e863-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e863-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0e863-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e863-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0e863-126">INPUTS</span></span>

### <span data-ttu-id="0e863-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0e863-127">None</span></span>

## <span data-ttu-id="0e863-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0e863-128">OUTPUTS</span></span>

### <span data-ttu-id="0e863-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0e863-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="0e863-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0e863-130">NOTES</span></span>

## <span data-ttu-id="0e863-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0e863-131">RELATED LINKS</span></span>

[<span data-ttu-id="0e863-132">Yeni-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0e863-132">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="0e863-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0e863-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="0e863-134">Güncelleştirme-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0e863-134">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
