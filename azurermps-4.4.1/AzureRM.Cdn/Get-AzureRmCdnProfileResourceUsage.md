---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
ms.openlocfilehash: f8b85088ac05cb118cf443eb54f28508727bd335
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595020"
---
# <span data-ttu-id="cba6f-101">Get-AzureRmCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="cba6f-101">Get-AzureRmCdnProfileResourceUsage</span></span>

## <span data-ttu-id="cba6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cba6f-102">SYNOPSIS</span></span>
<span data-ttu-id="cba6f-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="cba6f-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cba6f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cba6f-104">SYNTAX</span></span>

### <span data-ttu-id="cba6f-105">Alanlar parametrelerinin parametre kümesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cba6f-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cba6f-106">Nesne parametreleri için parametre kümesi</span><span class="sxs-lookup"><span data-stu-id="cba6f-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cba6f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cba6f-107">DESCRIPTION</span></span>
<span data-ttu-id="cba6f-108">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="cba6f-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="cba6f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cba6f-109">EXAMPLES</span></span>

### <span data-ttu-id="cba6f-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cba6f-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="cba6f-111">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="cba6f-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="cba6f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cba6f-112">PARAMETERS</span></span>

### <span data-ttu-id="cba6f-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="cba6f-113">-CdnProfile</span></span>
<span data-ttu-id="cba6f-114">Azure CDN profil nesnesi.</span><span class="sxs-lookup"><span data-stu-id="cba6f-114">The Azure CDN profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cba6f-115">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="cba6f-115">-ProfileName</span></span>
<span data-ttu-id="cba6f-116">Profilin adı.</span><span class="sxs-lookup"><span data-stu-id="cba6f-116">The name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba6f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cba6f-117">-ResourceGroupName</span></span>
<span data-ttu-id="cba6f-118">Profilin ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="cba6f-118">The resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba6f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cba6f-119">-DefaultProfile</span></span>
<span data-ttu-id="cba6f-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cba6f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cba6f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cba6f-121">CommonParameters</span></span>
<span data-ttu-id="cba6f-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cba6f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cba6f-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cba6f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cba6f-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cba6f-124">INPUTS</span></span>

### <span data-ttu-id="cba6f-125">Microsoft. Azure. Commands. CDN. model. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="cba6f-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="cba6f-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cba6f-126">OUTPUTS</span></span>

### <span data-ttu-id="cba6f-127">Microsoft. Azure. Commands. CDN. model. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="cba6f-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="cba6f-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cba6f-128">NOTES</span></span>

## <span data-ttu-id="cba6f-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cba6f-129">RELATED LINKS</span></span>

