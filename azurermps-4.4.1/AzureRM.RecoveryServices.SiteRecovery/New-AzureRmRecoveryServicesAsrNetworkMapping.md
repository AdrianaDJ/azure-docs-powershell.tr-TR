---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: ab2cca2fc0b517d8923d117978887c6dd0196ce5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593040"
---
# <span data-ttu-id="67cbc-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="67cbc-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="67cbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67cbc-102">SYNOPSIS</span></span>
<span data-ttu-id="67cbc-103">İki ağ arasında ASR ağ eşlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="67cbc-103">Creates an ASR network mapping between two networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67cbc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="67cbc-104">SYNTAX</span></span>

### <span data-ttu-id="67cbc-105">EnterpriseToEnterprise (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="67cbc-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67cbc-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="67cbc-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67cbc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="67cbc-107">DESCRIPTION</span></span>
<span data-ttu-id="67cbc-108">**Yeni-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet 'i, iki ağ arasında ASR ağ eşlemesi oluşturma işlemini başlatır ve işlemi izlemek IÇIN kullanılan ASR ışı için ASR iş nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="67cbc-108">The **New-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="67cbc-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="67cbc-109">EXAMPLES</span></span>

### <span data-ttu-id="67cbc-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="67cbc-110">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="67cbc-111">Belirtilen adı, birincil ve kurtarma ağlarını kullanarak ağ eşlemesi oluşturma işlemini başlatır ve işlemi izlemek için bir ASR işi döndürür.</span><span class="sxs-lookup"><span data-stu-id="67cbc-111">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

## <span data-ttu-id="67cbc-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="67cbc-112">PARAMETERS</span></span>

### <span data-ttu-id="67cbc-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="67cbc-113">-Name</span></span>
<span data-ttu-id="67cbc-114">Oluşturulacak ASR ağ eşlemesinin adı.</span><span class="sxs-lookup"><span data-stu-id="67cbc-114">Name of the ASR network mapping to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67cbc-115">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="67cbc-115">-PrimaryNetwork</span></span>
<span data-ttu-id="67cbc-116">Ağ eşlemesi için birincil ağ nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="67cbc-116">Specifies the primary network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67cbc-117">-Recoveryazurenetworkıd</span><span class="sxs-lookup"><span data-stu-id="67cbc-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="67cbc-118">Ağ eşlemesi için kurtarma Azure ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="67cbc-118">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67cbc-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="67cbc-119">-RecoveryNetwork</span></span>
<span data-ttu-id="67cbc-120">Ağ eşlemesi için kurtarma ağı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="67cbc-120">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67cbc-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="67cbc-121">-Confirm</span></span>
<span data-ttu-id="67cbc-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="67cbc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67cbc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67cbc-123">-WhatIf</span></span>
<span data-ttu-id="67cbc-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="67cbc-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67cbc-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="67cbc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67cbc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67cbc-126">CommonParameters</span></span>
<span data-ttu-id="67cbc-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="67cbc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67cbc-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67cbc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67cbc-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="67cbc-129">INPUTS</span></span>

### <span data-ttu-id="67cbc-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="67cbc-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="67cbc-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="67cbc-131">OUTPUTS</span></span>

### <span data-ttu-id="67cbc-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="67cbc-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="67cbc-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="67cbc-133">NOTES</span></span>

## <span data-ttu-id="67cbc-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="67cbc-134">RELATED LINKS</span></span>

[<span data-ttu-id="67cbc-135">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="67cbc-135">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="67cbc-136">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="67cbc-136">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
