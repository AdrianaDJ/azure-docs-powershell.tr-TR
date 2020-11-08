---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
ms.openlocfilehash: 341d46e5dd4ceefaf8baa76a71de462559115a5d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267911"
---
# <span data-ttu-id="27c7b-101">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="27c7b-101">Set-AzCdnProfile</span></span>

## <span data-ttu-id="27c7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27c7b-102">SYNOPSIS</span></span>
<span data-ttu-id="27c7b-103">CDN profilini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="27c7b-103">Updates a CDN profile.</span></span>

## <span data-ttu-id="27c7b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="27c7b-104">SYNTAX</span></span>

```
Set-AzCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="27c7b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="27c7b-105">DESCRIPTION</span></span>
<span data-ttu-id="27c7b-106">**Set-AzCdnProfile** cmdlet 'i, bir Azure Içerik teslim ağı (CDN) profilini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="27c7b-106">The **Set-AzCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="27c7b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="27c7b-107">EXAMPLES</span></span>

## <span data-ttu-id="27c7b-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="27c7b-108">PARAMETERS</span></span>

### <span data-ttu-id="27c7b-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="27c7b-109">-CdnProfile</span></span>
<span data-ttu-id="27c7b-110">Bu cmdlet 'in güncelleştirdiği profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="27c7b-110">Specifies the profile that this cmdlet updates.</span></span>

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

### <span data-ttu-id="27c7b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27c7b-111">-DefaultProfile</span></span>
<span data-ttu-id="27c7b-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="27c7b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c7b-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="27c7b-113">-Confirm</span></span>
<span data-ttu-id="27c7b-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="27c7b-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27c7b-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27c7b-115">-WhatIf</span></span>
<span data-ttu-id="27c7b-116">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="27c7b-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27c7b-117">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="27c7b-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27c7b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27c7b-118">CommonParameters</span></span>
<span data-ttu-id="27c7b-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="27c7b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27c7b-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="27c7b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27c7b-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="27c7b-121">INPUTS</span></span>

### <span data-ttu-id="27c7b-122">Microsoft. Azure. Commands. CDN. model. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="27c7b-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="27c7b-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="27c7b-123">OUTPUTS</span></span>

### <span data-ttu-id="27c7b-124">Microsoft. Azure. Commands. CDN. model. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="27c7b-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="27c7b-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="27c7b-125">NOTES</span></span>

## <span data-ttu-id="27c7b-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="27c7b-126">RELATED LINKS</span></span>

[<span data-ttu-id="27c7b-127">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="27c7b-127">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="27c7b-128">New-Azcıdnprofile</span><span class="sxs-lookup"><span data-stu-id="27c7b-128">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="27c7b-129">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="27c7b-129">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)


