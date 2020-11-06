---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 2FB62869-FF83-4D92-B08B-07AF3C393159
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: e7ee32974ef87b86d443d90b7dc628f9c9f1072f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589071"
---
# <span data-ttu-id="edd5f-101">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="edd5f-101">Remove-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="edd5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edd5f-102">SYNOPSIS</span></span>
<span data-ttu-id="edd5f-103">Azure Site Recovery Hizmetleri sağlayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="edd5f-103">Removes an Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edd5f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="edd5f-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edd5f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="edd5f-105">DESCRIPTION</span></span>
<span data-ttu-id="edd5f-106">**Remove-AzureRmSiteRecoveryServicesProvider** cmdlet 'i, kasadan bir Azure Site Recovery Hizmetleri sağlayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="edd5f-106">The **Remove-AzureRmSiteRecoveryServicesProvider** cmdlet removes an Azure Site Recovery Services Provider from the vault.</span></span>

## <span data-ttu-id="edd5f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="edd5f-107">EXAMPLES</span></span>

## <span data-ttu-id="edd5f-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="edd5f-108">PARAMETERS</span></span>

### <span data-ttu-id="edd5f-109">-Force</span><span class="sxs-lookup"><span data-stu-id="edd5f-109">-Force</span></span>
<span data-ttu-id="edd5f-110">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="edd5f-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="edd5f-111">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="edd5f-111">-ServicesProvider</span></span>
<span data-ttu-id="edd5f-112">Hizmetler sağlayıcısı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="edd5f-112">Specifies the Services Provider object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edd5f-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="edd5f-113">-Confirm</span></span>
<span data-ttu-id="edd5f-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="edd5f-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edd5f-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edd5f-115">-WhatIf</span></span>
<span data-ttu-id="edd5f-116">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="edd5f-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="edd5f-117">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="edd5f-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edd5f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edd5f-118">-DefaultProfile</span></span>
<span data-ttu-id="edd5f-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="edd5f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edd5f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edd5f-120">CommonParameters</span></span>
<span data-ttu-id="edd5f-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="edd5f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edd5f-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edd5f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edd5f-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="edd5f-123">INPUTS</span></span>

### <span data-ttu-id="edd5f-124">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="edd5f-124">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="edd5f-125">Parametre ' Hizmetsağlayıcısı ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="edd5f-125">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="edd5f-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="edd5f-126">OUTPUTS</span></span>

### <span data-ttu-id="edd5f-127">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRJob, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="edd5f-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRJob, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="edd5f-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="edd5f-128">NOTES</span></span>

## <span data-ttu-id="edd5f-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="edd5f-129">RELATED LINKS</span></span>

[<span data-ttu-id="edd5f-130">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="edd5f-130">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="edd5f-131">Güncelleştirme-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="edd5f-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
