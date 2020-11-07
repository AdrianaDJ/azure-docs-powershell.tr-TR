---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4BF1E20A-46EA-48E2-8C7A-F121AE6815AF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 1b01fef6563fef97f78913f916a6481acd6f6ed3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764508"
---
# <span data-ttu-id="7ba24-101">New-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7ba24-101">New-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="7ba24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ba24-102">SYNOPSIS</span></span>
<span data-ttu-id="7ba24-103">Sanal ağlar arasında eşleme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7ba24-103">Creates a mapping between virtual networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ba24-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7ba24-104">SYNTAX</span></span>

### <span data-ttu-id="7ba24-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="7ba24-105">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryNetworkMapping [-Name <String>] -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ba24-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="7ba24-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryNetworkMapping [-Name <String>] -PrimaryNetwork <ASRNetwork> -AzureVMNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ba24-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7ba24-107">DESCRIPTION</span></span>
<span data-ttu-id="7ba24-108">**New-AzureRMSiteRecoveryNetworkMapping** cmdlet iki sanal ağ arasında bir eşleme oluşturur ve bunu izlemek Için bir Azure Site kurtarma işi döndürür.</span><span class="sxs-lookup"><span data-stu-id="7ba24-108">The **New-AzureRMSiteRecoveryNetworkMapping** cmdlet creates a mapping between two virtual networks and returns an Azure Site Recovery job to track it.</span></span>

## <span data-ttu-id="7ba24-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7ba24-109">EXAMPLES</span></span>

## <span data-ttu-id="7ba24-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7ba24-110">PARAMETERS</span></span>

### <span data-ttu-id="7ba24-111">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="7ba24-111">-AzureVMNetworkId</span></span>
<span data-ttu-id="7ba24-112">Azure sanal ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ba24-112">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba24-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="7ba24-113">-Name</span></span>
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

### <span data-ttu-id="7ba24-114">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="7ba24-114">-PrimaryNetwork</span></span>
<span data-ttu-id="7ba24-115">Birincil ağ nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ba24-115">Specifies the primary network object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ba24-116">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="7ba24-116">-RecoveryNetwork</span></span>
<span data-ttu-id="7ba24-117">Kurtarma ağı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ba24-117">Specifies the recovery network object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba24-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ba24-118">-DefaultProfile</span></span>
<span data-ttu-id="7ba24-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7ba24-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ba24-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ba24-120">CommonParameters</span></span>
<span data-ttu-id="7ba24-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7ba24-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ba24-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ba24-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ba24-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7ba24-123">INPUTS</span></span>

### <span data-ttu-id="7ba24-124">ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="7ba24-124">ASRNetwork</span></span>
<span data-ttu-id="7ba24-125">' PrimaryNetwork ' parametresi ardışık düzene ' ASRNetwork ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="7ba24-125">Parameter 'PrimaryNetwork' accepts value of type 'ASRNetwork' from the pipeline</span></span>

## <span data-ttu-id="7ba24-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7ba24-126">OUTPUTS</span></span>

### <span data-ttu-id="7ba24-127">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7ba24-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7ba24-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7ba24-128">NOTES</span></span>

## <span data-ttu-id="7ba24-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7ba24-129">RELATED LINKS</span></span>

[<span data-ttu-id="7ba24-130">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7ba24-130">Get-AzureRmSiteRecoveryNetworkMapping</span></span>](./Get-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="7ba24-131">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7ba24-131">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>](./Remove-AzureRmSiteRecoveryNetworkMapping.md)
