---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
ms.openlocfilehash: 74bc4fae4dd55a85c4aca811819a0348f5df5f2c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109143"
---
# <span data-ttu-id="b6e96-101">Get-AzCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="b6e96-101">Get-AzCdnProfileSsoUrl</span></span>

## <span data-ttu-id="b6e96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6e96-102">SYNOPSIS</span></span>
<span data-ttu-id="b6e96-103">CDN profilinin çoklu oturum açma URL 'sini alır.</span><span class="sxs-lookup"><span data-stu-id="b6e96-103">Gets the single sign-on URL of a CDN profile.</span></span>

## <span data-ttu-id="b6e96-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b6e96-104">SYNTAX</span></span>

### <span data-ttu-id="b6e96-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b6e96-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6e96-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6e96-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6e96-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b6e96-107">DESCRIPTION</span></span>
<span data-ttu-id="b6e96-108">**Get-AzCdnProfileSsoUrl** cmdlet 'ı, Azure Içerik teslim ağı (CDN) profilinin çoklu oturum açma URL 'sini alır.</span><span class="sxs-lookup"><span data-stu-id="b6e96-108">The **Get-AzCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="b6e96-109">Bu URL, kullanıcıların bir destek portalına bağlanarak CDN 'nin ek özelliklerini kullanmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="b6e96-109">This URL lets users connect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="b6e96-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b6e96-110">EXAMPLES</span></span>

## <span data-ttu-id="b6e96-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b6e96-111">PARAMETERS</span></span>

### <span data-ttu-id="b6e96-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="b6e96-112">-CdnProfile</span></span>
<span data-ttu-id="b6e96-113">CDN profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6e96-113">Specifies the CDN profile.</span></span>

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

### <span data-ttu-id="b6e96-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6e96-114">-DefaultProfile</span></span>
<span data-ttu-id="b6e96-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b6e96-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6e96-116">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="b6e96-116">-ProfileName</span></span>
<span data-ttu-id="b6e96-117">CDN profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6e96-117">Specifies the name of the CDN profile.</span></span>

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

### <span data-ttu-id="b6e96-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6e96-118">-ResourceGroupName</span></span>
<span data-ttu-id="b6e96-119">Profilin ait olduğu kaynak grubu adının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6e96-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

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

### <span data-ttu-id="b6e96-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6e96-120">CommonParameters</span></span>
<span data-ttu-id="b6e96-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b6e96-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6e96-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b6e96-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6e96-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b6e96-123">INPUTS</span></span>

### <span data-ttu-id="b6e96-124">Microsoft. Azure. Commands. CDN. model. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="b6e96-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="b6e96-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b6e96-125">OUTPUTS</span></span>

### <span data-ttu-id="b6e96-126">Microsoft. Azure. Commands. CDN. modeller. Profile. PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="b6e96-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="b6e96-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b6e96-127">NOTES</span></span>

## <span data-ttu-id="b6e96-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b6e96-128">RELATED LINKS</span></span>

[<span data-ttu-id="b6e96-129">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="b6e96-129">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)


