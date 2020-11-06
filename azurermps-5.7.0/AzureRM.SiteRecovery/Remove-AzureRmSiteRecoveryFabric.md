---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 612D343A-89BA-491C-B20B-147715A2EF4F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 43d9603a5938ecef084191ebe77888a5f1769673
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593382"
---
# <span data-ttu-id="d9b01-101">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="d9b01-101">Remove-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="d9b01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9b01-102">SYNOPSIS</span></span>
<span data-ttu-id="d9b01-103">Bir Azure Site kurtarma yapısı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d9b01-103">Removes an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9b01-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d9b01-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryFabric -Fabric <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9b01-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d9b01-105">DESCRIPTION</span></span>
<span data-ttu-id="d9b01-106">**Remove-AzureRmSiteRecoveryFabric** cmdlet 'ı bir Azure Site kurtarma yapısı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d9b01-106">The **Remove-AzureRmSiteRecoveryFabric** cmdlet removes an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="d9b01-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d9b01-107">EXAMPLES</span></span>

## <span data-ttu-id="d9b01-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d9b01-108">PARAMETERS</span></span>

### <span data-ttu-id="d9b01-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9b01-109">-DefaultProfile</span></span>
<span data-ttu-id="d9b01-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d9b01-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9b01-111">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="d9b01-111">-Fabric</span></span>
<span data-ttu-id="d9b01-112">Azure Site Recovery Fabric nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9b01-112">Specifies the Azure Site Recovery Fabric object.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9b01-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d9b01-113">-Force</span></span>
<span data-ttu-id="d9b01-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="d9b01-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9b01-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="d9b01-115">-Confirm</span></span>
<span data-ttu-id="d9b01-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d9b01-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9b01-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9b01-117">-WhatIf</span></span>
<span data-ttu-id="d9b01-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d9b01-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="d9b01-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d9b01-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9b01-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9b01-120">CommonParameters</span></span>
<span data-ttu-id="d9b01-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d9b01-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9b01-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9b01-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9b01-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d9b01-123">INPUTS</span></span>

### <span data-ttu-id="d9b01-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="d9b01-124">ASRFabric</span></span>
<span data-ttu-id="d9b01-125">Parametre ' Fabric ', ardışık düzenin ' ASRFabric ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d9b01-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="d9b01-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d9b01-126">OUTPUTS</span></span>

### <span data-ttu-id="d9b01-127">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d9b01-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d9b01-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d9b01-128">NOTES</span></span>

## <span data-ttu-id="d9b01-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d9b01-129">RELATED LINKS</span></span>

[<span data-ttu-id="d9b01-130">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="d9b01-130">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="d9b01-131">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="d9b01-131">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)
