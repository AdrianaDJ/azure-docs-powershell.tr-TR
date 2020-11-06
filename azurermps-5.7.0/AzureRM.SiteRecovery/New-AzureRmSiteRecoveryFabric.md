---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B087194B-DA3F-4E45-BD2D-788F9E6F03EA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 38a7f8ee32f02db10dc971d5be2016d5dea0b538
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573274"
---
# <span data-ttu-id="701e9-101">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="701e9-101">New-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="701e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="701e9-102">SYNOPSIS</span></span>
<span data-ttu-id="701e9-103">Azure Site kurtarma yapısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="701e9-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="701e9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="701e9-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="701e9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="701e9-105">DESCRIPTION</span></span>
<span data-ttu-id="701e9-106">**New-AzureRmSiteRecoveryFabric** cmdlet 'i belirtilen türde bir Azure Site kurtarma yapısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="701e9-106">The **New-AzureRmSiteRecoveryFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="701e9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="701e9-107">EXAMPLES</span></span>

## <span data-ttu-id="701e9-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="701e9-108">PARAMETERS</span></span>

### <span data-ttu-id="701e9-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="701e9-109">-DefaultProfile</span></span>
<span data-ttu-id="701e9-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="701e9-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="701e9-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="701e9-111">-Name</span></span>
<span data-ttu-id="701e9-112">Azure Site Recovery yapısı adını belirtir</span><span class="sxs-lookup"><span data-stu-id="701e9-112">Specifies the name of the Azure Site Recovery Fabric</span></span>

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

### <span data-ttu-id="701e9-113">-Tür</span><span class="sxs-lookup"><span data-stu-id="701e9-113">-Type</span></span>
<span data-ttu-id="701e9-114">Azure Site Recovery Fabric türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="701e9-114">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="701e9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="701e9-115">CommonParameters</span></span>
<span data-ttu-id="701e9-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="701e9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="701e9-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="701e9-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="701e9-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="701e9-118">INPUTS</span></span>

### <span data-ttu-id="701e9-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="701e9-119">None</span></span>
<span data-ttu-id="701e9-120">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="701e9-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="701e9-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="701e9-121">OUTPUTS</span></span>

### <span data-ttu-id="701e9-122">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="701e9-122">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="701e9-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="701e9-123">NOTES</span></span>

## <span data-ttu-id="701e9-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="701e9-124">RELATED LINKS</span></span>

[<span data-ttu-id="701e9-125">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="701e9-125">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="701e9-126">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="701e9-126">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)
