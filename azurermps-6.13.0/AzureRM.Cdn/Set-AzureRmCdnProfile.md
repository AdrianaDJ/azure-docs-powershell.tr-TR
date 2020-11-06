---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
ms.openlocfilehash: e80b82f567dd1c0935dd56d8e3996a63bcce72e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591381"
---
# <span data-ttu-id="d3ad2-101">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="d3ad2-101">Set-AzureRmCdnProfile</span></span>

## <span data-ttu-id="d3ad2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3ad2-102">SYNOPSIS</span></span>
<span data-ttu-id="d3ad2-103">CDN profilini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d3ad2-103">Updates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3ad2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3ad2-104">SYNTAX</span></span>

```
Set-AzureRmCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d3ad2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3ad2-105">DESCRIPTION</span></span>
<span data-ttu-id="d3ad2-106">**Set-AzureRmCdnProfile** cmdlet 'i, bir Azure Içerik teslim ağı (CDN) profilini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d3ad2-106">The **Set-AzureRmCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="d3ad2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3ad2-107">EXAMPLES</span></span>

## <span data-ttu-id="d3ad2-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3ad2-108">PARAMETERS</span></span>

### <span data-ttu-id="d3ad2-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="d3ad2-109">-CdnProfile</span></span>
<span data-ttu-id="d3ad2-110">Bu cmdlet 'in güncelleştirdiği profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3ad2-110">Specifies the profile that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3ad2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3ad2-111">-DefaultProfile</span></span>
<span data-ttu-id="d3ad2-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d3ad2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3ad2-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="d3ad2-113">-Confirm</span></span>
<span data-ttu-id="d3ad2-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d3ad2-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3ad2-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3ad2-115">-WhatIf</span></span>
<span data-ttu-id="d3ad2-116">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d3ad2-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3ad2-117">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d3ad2-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3ad2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3ad2-118">CommonParameters</span></span>
<span data-ttu-id="d3ad2-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3ad2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3ad2-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3ad2-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3ad2-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3ad2-121">INPUTS</span></span>

### <span data-ttu-id="d3ad2-122">Microsoft. Azure. Commands. CDN. model. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="d3ad2-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="d3ad2-123">Parametreler: Cdnprofıle (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d3ad2-123">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="d3ad2-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3ad2-124">OUTPUTS</span></span>

### <span data-ttu-id="d3ad2-125">Microsoft. Azure. Commands. CDN. model. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="d3ad2-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="d3ad2-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3ad2-126">NOTES</span></span>

## <span data-ttu-id="d3ad2-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3ad2-127">RELATED LINKS</span></span>

[<span data-ttu-id="d3ad2-128">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="d3ad2-128">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="d3ad2-129">Yeni-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="d3ad2-129">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="d3ad2-130">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="d3ad2-130">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)


