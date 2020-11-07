---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4BF1E20A-46EA-48E2-8C7A-F121AE6815AF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverynetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 36f5c6e535cc67029fac7c951cbc6dbbe3c73091
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763969"
---
# <span data-ttu-id="e48a9-101">New-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="e48a9-101">New-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="e48a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e48a9-102">SYNOPSIS</span></span>
<span data-ttu-id="e48a9-103">Sanal ağlar arasında eşleme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e48a9-103">Creates a mapping between virtual networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e48a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e48a9-104">SYNTAX</span></span>

### <span data-ttu-id="e48a9-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="e48a9-105">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryNetworkMapping [-Name <String>] -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e48a9-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="e48a9-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryNetworkMapping [-Name <String>] -PrimaryNetwork <ASRNetwork> -AzureVMNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e48a9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e48a9-107">DESCRIPTION</span></span>
<span data-ttu-id="e48a9-108">**New-AzureRMSiteRecoveryNetworkMapping** cmdlet iki sanal ağ arasında bir eşleme oluşturur ve bunu izlemek Için bir Azure Site kurtarma işi döndürür.</span><span class="sxs-lookup"><span data-stu-id="e48a9-108">The **New-AzureRMSiteRecoveryNetworkMapping** cmdlet creates a mapping between two virtual networks and returns an Azure Site Recovery job to track it.</span></span>

## <span data-ttu-id="e48a9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e48a9-109">EXAMPLES</span></span>

## <span data-ttu-id="e48a9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e48a9-110">PARAMETERS</span></span>

### <span data-ttu-id="e48a9-111">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="e48a9-111">-AzureVMNetworkId</span></span>
<span data-ttu-id="e48a9-112">Azure sanal ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e48a9-112">Specifies the Azure virtual network ID.</span></span>

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

### <span data-ttu-id="e48a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e48a9-113">-DefaultProfile</span></span>
<span data-ttu-id="e48a9-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e48a9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e48a9-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="e48a9-115">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e48a9-116">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="e48a9-116">-PrimaryNetwork</span></span>
<span data-ttu-id="e48a9-117">Birincil ağ nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e48a9-117">Specifies the primary network object.</span></span>

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

### <span data-ttu-id="e48a9-118">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="e48a9-118">-RecoveryNetwork</span></span>
<span data-ttu-id="e48a9-119">Kurtarma ağı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e48a9-119">Specifies the recovery network object.</span></span>

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

### <span data-ttu-id="e48a9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e48a9-120">CommonParameters</span></span>
<span data-ttu-id="e48a9-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e48a9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e48a9-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e48a9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e48a9-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e48a9-123">INPUTS</span></span>

### <span data-ttu-id="e48a9-124">ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="e48a9-124">ASRNetwork</span></span>
<span data-ttu-id="e48a9-125">' PrimaryNetwork ' parametresi ardışık düzene ' ASRNetwork ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="e48a9-125">Parameter 'PrimaryNetwork' accepts value of type 'ASRNetwork' from the pipeline</span></span>

## <span data-ttu-id="e48a9-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e48a9-126">OUTPUTS</span></span>

### <span data-ttu-id="e48a9-127">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e48a9-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e48a9-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e48a9-128">NOTES</span></span>

## <span data-ttu-id="e48a9-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e48a9-129">RELATED LINKS</span></span>

[<span data-ttu-id="e48a9-130">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="e48a9-130">Get-AzureRmSiteRecoveryNetworkMapping</span></span>](./Get-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="e48a9-131">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="e48a9-131">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>](./Remove-AzureRmSiteRecoveryNetworkMapping.md)
