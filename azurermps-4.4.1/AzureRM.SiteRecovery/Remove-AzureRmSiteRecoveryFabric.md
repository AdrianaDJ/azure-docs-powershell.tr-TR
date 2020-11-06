---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 612D343A-89BA-491C-B20B-147715A2EF4F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 3d4530090bc1386a34056b315c79a826be5d771f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590619"
---
# <span data-ttu-id="05b82-101">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="05b82-101">Remove-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="05b82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05b82-102">SYNOPSIS</span></span>
<span data-ttu-id="05b82-103">Bir Azure Site kurtarma yapısı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="05b82-103">Removes an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05b82-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="05b82-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryFabric -Fabric <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05b82-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="05b82-105">DESCRIPTION</span></span>
<span data-ttu-id="05b82-106">**Remove-AzureRmSiteRecoveryFabric** cmdlet 'ı bir Azure Site kurtarma yapısı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="05b82-106">The **Remove-AzureRmSiteRecoveryFabric** cmdlet removes an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="05b82-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="05b82-107">EXAMPLES</span></span>

## <span data-ttu-id="05b82-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="05b82-108">PARAMETERS</span></span>

### <span data-ttu-id="05b82-109">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="05b82-109">-Fabric</span></span>
<span data-ttu-id="05b82-110">Azure Site Recovery Fabric nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="05b82-110">Specifies the Azure Site Recovery Fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05b82-111">-Force</span><span class="sxs-lookup"><span data-stu-id="05b82-111">-Force</span></span>
<span data-ttu-id="05b82-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="05b82-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05b82-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="05b82-113">-Confirm</span></span>
<span data-ttu-id="05b82-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="05b82-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05b82-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05b82-115">-WhatIf</span></span>
<span data-ttu-id="05b82-116">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="05b82-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="05b82-117">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="05b82-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05b82-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05b82-118">-DefaultProfile</span></span>
<span data-ttu-id="05b82-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="05b82-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05b82-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05b82-120">CommonParameters</span></span>
<span data-ttu-id="05b82-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="05b82-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05b82-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05b82-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05b82-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="05b82-123">INPUTS</span></span>

### <span data-ttu-id="05b82-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="05b82-124">ASRFabric</span></span>
<span data-ttu-id="05b82-125">Parametre ' Fabric ', ardışık düzenin ' ASRFabric ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="05b82-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="05b82-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="05b82-126">OUTPUTS</span></span>

### <span data-ttu-id="05b82-127">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="05b82-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="05b82-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="05b82-128">NOTES</span></span>

## <span data-ttu-id="05b82-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="05b82-129">RELATED LINKS</span></span>

[<span data-ttu-id="05b82-130">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="05b82-130">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="05b82-131">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="05b82-131">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)
