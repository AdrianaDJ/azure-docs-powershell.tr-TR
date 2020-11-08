---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 1478a6fbe28e1d014767a829144138d7ada3dcfd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096291"
---
# <span data-ttu-id="49d6c-101">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="49d6c-101">Get-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="49d6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49d6c-102">SYNOPSIS</span></span>
<span data-ttu-id="49d6c-103">Geçerli kasa için site kurtarma ağ eşlemeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="49d6c-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

## <span data-ttu-id="49d6c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="49d6c-104">SYNTAX</span></span>

### <span data-ttu-id="49d6c-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="49d6c-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49d6c-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="49d6c-106">ByFabricObject</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49d6c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="49d6c-107">DESCRIPTION</span></span>
<span data-ttu-id="49d6c-108">**Get-AzRecoveryServicesAsrNetworkMapping** cmdlet 'ı, kurtarma hizmetleri Kasası Için Azure Site Recovery ağ eşlemeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="49d6c-108">The **Get-AzRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="49d6c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="49d6c-109">EXAMPLES</span></span>

### <span data-ttu-id="49d6c-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="49d6c-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="49d6c-111">Geçirilen ağın tüm ağ eşlemelerini alır.</span><span class="sxs-lookup"><span data-stu-id="49d6c-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="49d6c-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="49d6c-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="49d6c-113">Belirtilen Azure Site Recovery yapıda sağlanan adla Ağ eşlemesini alır.</span><span class="sxs-lookup"><span data-stu-id="49d6c-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="49d6c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="49d6c-114">PARAMETERS</span></span>

### <span data-ttu-id="49d6c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49d6c-115">-DefaultProfile</span></span>
<span data-ttu-id="49d6c-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="49d6c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="49d6c-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="49d6c-117">-Name</span></span>
<span data-ttu-id="49d6c-118">Alınacak ASR ağ eşleme nesnesinin adı.</span><span class="sxs-lookup"><span data-stu-id="49d6c-118">The name of the ASR network mapping object to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49d6c-119">-Ağ</span><span class="sxs-lookup"><span data-stu-id="49d6c-119">-Network</span></span>
<span data-ttu-id="49d6c-120">Belirtilen ağ ASR nesnesine karşılık gelen ASR ağ eşleştirmelerini edinin.</span><span class="sxs-lookup"><span data-stu-id="49d6c-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49d6c-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="49d6c-121">-PrimaryFabric</span></span>
<span data-ttu-id="49d6c-122">Belirtilen birincil Fabric nesnesine karşılık gelen ASR ağ eşleştirmelerini edinin.</span><span class="sxs-lookup"><span data-stu-id="49d6c-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49d6c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49d6c-123">CommonParameters</span></span>
<span data-ttu-id="49d6c-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="49d6c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49d6c-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="49d6c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49d6c-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="49d6c-126">INPUTS</span></span>

### <span data-ttu-id="49d6c-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="49d6c-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

### <span data-ttu-id="49d6c-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="49d6c-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="49d6c-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="49d6c-129">OUTPUTS</span></span>

### <span data-ttu-id="49d6c-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="49d6c-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="49d6c-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="49d6c-131">NOTES</span></span>

## <span data-ttu-id="49d6c-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="49d6c-132">RELATED LINKS</span></span>

[<span data-ttu-id="49d6c-133">Yeni-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="49d6c-133">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="49d6c-134">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="49d6c-134">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
