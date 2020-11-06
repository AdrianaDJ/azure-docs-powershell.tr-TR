---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
ms.openlocfilehash: 3ad44ba1edcec844dcb542defb1baf294aeaa89b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587272"
---
# <span data-ttu-id="0f147-101">Get-AzureRmCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="0f147-101">Get-AzureRmCdnProfileSsoUrl</span></span>

## <span data-ttu-id="0f147-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f147-102">SYNOPSIS</span></span>
<span data-ttu-id="0f147-103">CDN profilinin çoklu oturum açma URL 'sini alır.</span><span class="sxs-lookup"><span data-stu-id="0f147-103">Gets the single sign-on URL of a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f147-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0f147-104">SYNTAX</span></span>

### <span data-ttu-id="0f147-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0f147-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f147-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f147-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f147-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0f147-107">DESCRIPTION</span></span>
<span data-ttu-id="0f147-108">**Get-AzureRmCdnProfileSsoUrl** cmdlet 'ı, Azure Içerik teslim ağı (CDN) profilinin çoklu oturum açma URL 'sini alır.</span><span class="sxs-lookup"><span data-stu-id="0f147-108">The **Get-AzureRmCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="0f147-109">Bu URL, kullanıcıların bir destek portalına ulaşmanızı ve CDN 'nin ek özelliklerini kullanmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="0f147-109">This URL lets users conntect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="0f147-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0f147-110">EXAMPLES</span></span>

## <span data-ttu-id="0f147-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0f147-111">PARAMETERS</span></span>

### <span data-ttu-id="0f147-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="0f147-112">-CdnProfile</span></span>
<span data-ttu-id="0f147-113">CDN profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f147-113">Specifies the CDN profile.</span></span>

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

### <span data-ttu-id="0f147-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f147-114">-DefaultProfile</span></span>
<span data-ttu-id="0f147-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0f147-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f147-116">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="0f147-116">-ProfileName</span></span>
<span data-ttu-id="0f147-117">CDN profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f147-117">Specifies the name of the CDN profile.</span></span>

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

### <span data-ttu-id="0f147-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f147-118">-ResourceGroupName</span></span>
<span data-ttu-id="0f147-119">Profilin ait olduğu kaynak grubu adının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f147-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

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

### <span data-ttu-id="0f147-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f147-120">CommonParameters</span></span>
<span data-ttu-id="0f147-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0f147-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f147-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f147-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f147-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0f147-123">INPUTS</span></span>

### <span data-ttu-id="0f147-124">Microsoft. Azure. Commands. CDN. model. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="0f147-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="0f147-125">Parametreler: Cdnprofıle (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0f147-125">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="0f147-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0f147-126">OUTPUTS</span></span>

### <span data-ttu-id="0f147-127">Microsoft. Azure. Commands. CDN. modeller. Profile. PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="0f147-127">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="0f147-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0f147-128">NOTES</span></span>

## <span data-ttu-id="0f147-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0f147-129">RELATED LINKS</span></span>

[<span data-ttu-id="0f147-130">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="0f147-130">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)


