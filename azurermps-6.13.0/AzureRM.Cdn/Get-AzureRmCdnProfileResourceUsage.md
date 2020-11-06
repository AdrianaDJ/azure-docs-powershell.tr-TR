---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
ms.openlocfilehash: 3d0f93a732739b94832a5e411580fb80958b27c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587273"
---
# <span data-ttu-id="f1d42-101">Get-AzureRmCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="f1d42-101">Get-AzureRmCdnProfileResourceUsage</span></span>

## <span data-ttu-id="f1d42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1d42-102">SYNOPSIS</span></span>
<span data-ttu-id="f1d42-103">CDN profilinin kaynak kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="f1d42-103">Gets the resource usage of a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1d42-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1d42-104">SYNTAX</span></span>

### <span data-ttu-id="f1d42-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f1d42-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1d42-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1d42-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1d42-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1d42-107">DESCRIPTION</span></span>
<span data-ttu-id="f1d42-108">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="f1d42-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="f1d42-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1d42-109">EXAMPLES</span></span>

### <span data-ttu-id="f1d42-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f1d42-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="f1d42-111">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="f1d42-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="f1d42-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1d42-112">PARAMETERS</span></span>

### <span data-ttu-id="f1d42-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="f1d42-113">-CdnProfile</span></span>
<span data-ttu-id="f1d42-114">Azure CDN profil nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f1d42-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="f1d42-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1d42-115">-DefaultProfile</span></span>
<span data-ttu-id="f1d42-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f1d42-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1d42-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="f1d42-117">-ProfileName</span></span>
<span data-ttu-id="f1d42-118">Profilin adı.</span><span class="sxs-lookup"><span data-stu-id="f1d42-118">The name of the profile.</span></span>

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

### <span data-ttu-id="f1d42-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1d42-119">-ResourceGroupName</span></span>
<span data-ttu-id="f1d42-120">Profilin ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="f1d42-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="f1d42-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1d42-121">CommonParameters</span></span>
<span data-ttu-id="f1d42-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1d42-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1d42-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1d42-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1d42-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1d42-124">INPUTS</span></span>

### <span data-ttu-id="f1d42-125">Microsoft. Azure. Commands. CDN. model. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="f1d42-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="f1d42-126">Parametreler: Cdnprofıle (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f1d42-126">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="f1d42-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1d42-127">OUTPUTS</span></span>

### <span data-ttu-id="f1d42-128">Microsoft. Azure. Commands. CDN. model. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="f1d42-128">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="f1d42-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1d42-129">NOTES</span></span>

## <span data-ttu-id="f1d42-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1d42-130">RELATED LINKS</span></span>
