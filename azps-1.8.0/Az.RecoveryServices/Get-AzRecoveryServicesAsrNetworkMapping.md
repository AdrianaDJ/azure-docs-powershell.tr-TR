---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 56b8f70494a8575c569aa7a2ee9636521f8a87ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759742"
---
# <span data-ttu-id="efaad-101">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="efaad-101">Get-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="efaad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efaad-102">SYNOPSIS</span></span>
<span data-ttu-id="efaad-103">Geçerli kasa için site kurtarma ağ eşlemeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="efaad-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

## <span data-ttu-id="efaad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="efaad-104">SYNTAX</span></span>

### <span data-ttu-id="efaad-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="efaad-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efaad-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="efaad-106">ByFabricObject</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efaad-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="efaad-107">DESCRIPTION</span></span>
<span data-ttu-id="efaad-108">**Get-AzRecoveryServicesAsrNetworkMapping** cmdlet 'ı, kurtarma hizmetleri Kasası Için Azure Site Recovery ağ eşlemeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="efaad-108">The **Get-AzRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="efaad-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="efaad-109">EXAMPLES</span></span>

### <span data-ttu-id="efaad-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="efaad-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="efaad-111">Geçirilen ağın tüm ağ eşlemelerini alır.</span><span class="sxs-lookup"><span data-stu-id="efaad-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="efaad-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="efaad-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="efaad-113">Belirtilen Azure Site Recovery yapıda sağlanan adla Ağ eşlemesini alır.</span><span class="sxs-lookup"><span data-stu-id="efaad-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="efaad-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="efaad-114">PARAMETERS</span></span>

### <span data-ttu-id="efaad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efaad-115">-DefaultProfile</span></span>
<span data-ttu-id="efaad-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="efaad-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="efaad-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="efaad-117">-Name</span></span>
<span data-ttu-id="efaad-118">Alınacak ASR ağ eşleme nesnesinin adı.</span><span class="sxs-lookup"><span data-stu-id="efaad-118">The name of the ASR network mapping object to get.</span></span>

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

### <span data-ttu-id="efaad-119">-Ağ</span><span class="sxs-lookup"><span data-stu-id="efaad-119">-Network</span></span>
<span data-ttu-id="efaad-120">Belirtilen ağ ASR nesnesine karşılık gelen ASR ağ eşleştirmelerini edinin.</span><span class="sxs-lookup"><span data-stu-id="efaad-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

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

### <span data-ttu-id="efaad-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="efaad-121">-PrimaryFabric</span></span>
<span data-ttu-id="efaad-122">Belirtilen birincil Fabric nesnesine karşılık gelen ASR ağ eşleştirmelerini edinin.</span><span class="sxs-lookup"><span data-stu-id="efaad-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

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

### <span data-ttu-id="efaad-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efaad-123">CommonParameters</span></span>
<span data-ttu-id="efaad-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="efaad-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efaad-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efaad-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efaad-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="efaad-126">INPUTS</span></span>

### <span data-ttu-id="efaad-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="efaad-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

### <span data-ttu-id="efaad-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="efaad-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="efaad-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="efaad-129">OUTPUTS</span></span>

### <span data-ttu-id="efaad-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="efaad-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="efaad-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="efaad-131">NOTES</span></span>

## <span data-ttu-id="efaad-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="efaad-132">RELATED LINKS</span></span>

[<span data-ttu-id="efaad-133">Yeni-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="efaad-133">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="efaad-134">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="efaad-134">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
