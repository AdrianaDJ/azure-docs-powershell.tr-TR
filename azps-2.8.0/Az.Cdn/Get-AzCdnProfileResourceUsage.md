---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: 689604037c709496f0ccc5208599f7151eaf2c55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753076"
---
# <span data-ttu-id="2c620-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="2c620-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="2c620-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c620-102">SYNOPSIS</span></span>
<span data-ttu-id="2c620-103">CDN profilinin kaynak kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="2c620-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="2c620-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2c620-104">SYNTAX</span></span>

### <span data-ttu-id="2c620-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2c620-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c620-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c620-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2c620-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2c620-107">DESCRIPTION</span></span>
<span data-ttu-id="2c620-108">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="2c620-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="2c620-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2c620-109">EXAMPLES</span></span>

### <span data-ttu-id="2c620-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2c620-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="2c620-111">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="2c620-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="2c620-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2c620-112">PARAMETERS</span></span>

### <span data-ttu-id="2c620-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="2c620-113">-CdnProfile</span></span>
<span data-ttu-id="2c620-114">Azure CDN profil nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2c620-114">The Azure CDN profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c620-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c620-115">-DefaultProfile</span></span>
<span data-ttu-id="2c620-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2c620-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c620-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2c620-117">-ProfileName</span></span>
<span data-ttu-id="2c620-118">Profilin adı.</span><span class="sxs-lookup"><span data-stu-id="2c620-118">The name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c620-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c620-119">-ResourceGroupName</span></span>
<span data-ttu-id="2c620-120">Profilin ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="2c620-120">The resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c620-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c620-121">CommonParameters</span></span>
<span data-ttu-id="2c620-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2c620-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c620-123">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2c620-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c620-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2c620-124">INPUTS</span></span>

### <span data-ttu-id="2c620-125">Microsoft. Azure. Commands. CDN. model. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="2c620-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="2c620-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2c620-126">OUTPUTS</span></span>

### <span data-ttu-id="2c620-127">Microsoft. Azure. Commands. CDN. model. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="2c620-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="2c620-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2c620-128">NOTES</span></span>

## <span data-ttu-id="2c620-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2c620-129">RELATED LINKS</span></span>
