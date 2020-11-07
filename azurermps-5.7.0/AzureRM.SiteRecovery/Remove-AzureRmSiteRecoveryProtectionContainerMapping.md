---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B1D914F8-4181-4BF1-B1D3-A5857DA8254C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 27c90687b212c0ed41dcb080df1be5686a876725
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763962"
---
# <span data-ttu-id="3afcf-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="3afcf-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="3afcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3afcf-102">SYNOPSIS</span></span>
<span data-ttu-id="3afcf-103">Azure Site Recovery koruma kapsayıcısı eşlemesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3afcf-103">Removes an Azure Site Recovery Protection Container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3afcf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3afcf-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryProtectionContainerMapping
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3afcf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3afcf-105">DESCRIPTION</span></span>
<span data-ttu-id="3afcf-106">**Remove-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet 'ı bir Azure Site Recovery Protection kapsayıcısı eşlemesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3afcf-106">The **Remove-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet removes an Azure Site Recovery Protection Container mapping.</span></span>

## <span data-ttu-id="3afcf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3afcf-107">EXAMPLES</span></span>

## <span data-ttu-id="3afcf-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3afcf-108">PARAMETERS</span></span>

### <span data-ttu-id="3afcf-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3afcf-109">-DefaultProfile</span></span>
<span data-ttu-id="3afcf-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3afcf-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3afcf-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3afcf-111">-Force</span></span>
<span data-ttu-id="3afcf-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="3afcf-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3afcf-113">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="3afcf-113">-ProtectionContainerMapping</span></span>
<span data-ttu-id="3afcf-114">Azure Site Recovery koruma kapsayıcısı eşleme nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3afcf-114">Specifies the Azure Site Recovery Protection Container mapping object.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3afcf-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="3afcf-115">-Confirm</span></span>
<span data-ttu-id="3afcf-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3afcf-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3afcf-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3afcf-117">-WhatIf</span></span>
<span data-ttu-id="3afcf-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3afcf-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="3afcf-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3afcf-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3afcf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3afcf-120">CommonParameters</span></span>
<span data-ttu-id="3afcf-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3afcf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3afcf-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3afcf-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3afcf-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3afcf-123">INPUTS</span></span>

### <span data-ttu-id="3afcf-124">ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="3afcf-124">ASRProtectionContainerMapping</span></span>
<span data-ttu-id="3afcf-125">' ProtectionContainerMapping ' parametresi ardışık düzenin ' ASRProtectionContainerMapping ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="3afcf-125">Parameter 'ProtectionContainerMapping' accepts value of type 'ASRProtectionContainerMapping' from the pipeline</span></span>

## <span data-ttu-id="3afcf-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3afcf-126">OUTPUTS</span></span>

### <span data-ttu-id="3afcf-127">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3afcf-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3afcf-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3afcf-128">NOTES</span></span>

## <span data-ttu-id="3afcf-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3afcf-129">RELATED LINKS</span></span>

[<span data-ttu-id="3afcf-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="3afcf-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="3afcf-131">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="3afcf-131">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)
