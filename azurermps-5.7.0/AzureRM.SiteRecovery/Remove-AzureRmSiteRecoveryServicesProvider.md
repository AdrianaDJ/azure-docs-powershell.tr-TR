---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2FB62869-FF83-4D92-B08B-07AF3C393159
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 88b6b83f24edb06871fd87f61fec1732893b0f41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573265"
---
# <span data-ttu-id="7e39c-101">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="7e39c-101">Remove-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="7e39c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e39c-102">SYNOPSIS</span></span>
<span data-ttu-id="7e39c-103">Azure Site Recovery Hizmetleri sağlayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7e39c-103">Removes an Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e39c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e39c-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e39c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e39c-105">DESCRIPTION</span></span>
<span data-ttu-id="7e39c-106">**Remove-AzureRmSiteRecoveryServicesProvider** cmdlet 'i, kasadan bir Azure Site Recovery Hizmetleri sağlayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7e39c-106">The **Remove-AzureRmSiteRecoveryServicesProvider** cmdlet removes an Azure Site Recovery Services Provider from the vault.</span></span>

## <span data-ttu-id="7e39c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e39c-107">EXAMPLES</span></span>

## <span data-ttu-id="7e39c-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e39c-108">PARAMETERS</span></span>

### <span data-ttu-id="7e39c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e39c-109">-DefaultProfile</span></span>
<span data-ttu-id="7e39c-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7e39c-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e39c-111">-Force</span><span class="sxs-lookup"><span data-stu-id="7e39c-111">-Force</span></span>
<span data-ttu-id="7e39c-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="7e39c-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7e39c-113">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="7e39c-113">-ServicesProvider</span></span>
<span data-ttu-id="7e39c-114">Hizmetler sağlayıcısı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e39c-114">Specifies the Services Provider object.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e39c-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="7e39c-115">-Confirm</span></span>
<span data-ttu-id="7e39c-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7e39c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e39c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e39c-117">-WhatIf</span></span>
<span data-ttu-id="7e39c-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7e39c-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="7e39c-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7e39c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e39c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e39c-120">CommonParameters</span></span>
<span data-ttu-id="7e39c-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e39c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e39c-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e39c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e39c-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e39c-123">INPUTS</span></span>

### <span data-ttu-id="7e39c-124">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="7e39c-124">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="7e39c-125">Parametre ' Hizmetsağlayıcısı ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="7e39c-125">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="7e39c-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e39c-126">OUTPUTS</span></span>

### <span data-ttu-id="7e39c-127">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRJob, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7e39c-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRJob, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7e39c-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e39c-128">NOTES</span></span>

## <span data-ttu-id="7e39c-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e39c-129">RELATED LINKS</span></span>

[<span data-ttu-id="7e39c-130">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="7e39c-130">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="7e39c-131">Güncelleştirme-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="7e39c-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
