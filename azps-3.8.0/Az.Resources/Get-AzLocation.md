---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: f14da4760f70c8e4ba95136b81a884f830f4f44a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097801"
---
# <span data-ttu-id="db450-101">Get-AzLocation</span><span class="sxs-lookup"><span data-stu-id="db450-101">Get-AzLocation</span></span>

## <span data-ttu-id="db450-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db450-102">SYNOPSIS</span></span>
<span data-ttu-id="db450-103">Her konum için tüm konumları ve desteklenen kaynak sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="db450-103">Gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="db450-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="db450-104">SYNTAX</span></span>

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db450-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="db450-105">DESCRIPTION</span></span>
<span data-ttu-id="db450-106">**Get-AzLocation** cmdlet 'i her konum için tüm konumları ve desteklenen kaynak sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="db450-106">The **Get-AzLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="db450-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="db450-107">EXAMPLES</span></span>

### <span data-ttu-id="db450-108">Örnek 1: tüm konumları ve desteklenen kaynak sağlayıcılarını alma</span><span class="sxs-lookup"><span data-stu-id="db450-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzLocation
```

<span data-ttu-id="db450-109">Bu komut, her konum için tüm konumları ve desteklenen kaynak sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="db450-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="db450-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="db450-110">PARAMETERS</span></span>

### <span data-ttu-id="db450-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="db450-111">-ApiVersion</span></span>
<span data-ttu-id="db450-112">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="db450-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="db450-113">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="db450-113">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db450-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db450-114">-DefaultProfile</span></span>
<span data-ttu-id="db450-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="db450-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db450-116">-Pre-</span><span class="sxs-lookup"><span data-stu-id="db450-116">-Pre</span></span>
<span data-ttu-id="db450-117">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="db450-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="db450-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db450-118">CommonParameters</span></span>
<span data-ttu-id="db450-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="db450-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db450-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="db450-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db450-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="db450-121">INPUTS</span></span>

### <span data-ttu-id="db450-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="db450-122">None</span></span>

## <span data-ttu-id="db450-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="db450-123">OUTPUTS</span></span>

### <span data-ttu-id="db450-124">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSResourceProviderLocation</span><span class="sxs-lookup"><span data-stu-id="db450-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span></span>

## <span data-ttu-id="db450-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="db450-125">NOTES</span></span>

## <span data-ttu-id="db450-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="db450-126">RELATED LINKS</span></span>
