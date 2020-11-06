---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmLocation.md
ms.openlocfilehash: 6052a621b43cd0b51170e9a502a38df46d38e17d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590053"
---
# <span data-ttu-id="9f5be-101">Get-AzureRmLocation</span><span class="sxs-lookup"><span data-stu-id="9f5be-101">Get-AzureRmLocation</span></span>

## <span data-ttu-id="9f5be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f5be-102">SYNOPSIS</span></span>
<span data-ttu-id="9f5be-103">Her konum için tüm konumları ve desteklenen kaynak sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="9f5be-103">Gets all locations and the supported resource providers for each location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f5be-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9f5be-104">SYNTAX</span></span>

```
Get-AzureRmLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f5be-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9f5be-105">DESCRIPTION</span></span>
<span data-ttu-id="9f5be-106">**Get-AzureRmLocation** cmdlet 'i her konum için tüm konumları ve desteklenen kaynak sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="9f5be-106">The **Get-AzureRmLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="9f5be-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9f5be-107">EXAMPLES</span></span>

### <span data-ttu-id="9f5be-108">Örnek 1: tüm konumları ve desteklenen kaynak sağlayıcılarını alma</span><span class="sxs-lookup"><span data-stu-id="9f5be-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzureRmLocation
```

<span data-ttu-id="9f5be-109">Bu komut, her konum için tüm konumları ve desteklenen kaynak sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="9f5be-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="9f5be-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9f5be-110">PARAMETERS</span></span>

### <span data-ttu-id="9f5be-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="9f5be-111">-ApiVersion</span></span>
<span data-ttu-id="9f5be-112">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f5be-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="9f5be-113">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9f5be-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="9f5be-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f5be-114">-DefaultProfile</span></span>
<span data-ttu-id="9f5be-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9f5be-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f5be-116">-Pre-</span><span class="sxs-lookup"><span data-stu-id="9f5be-116">-Pre</span></span>
<span data-ttu-id="9f5be-117">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="9f5be-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9f5be-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f5be-118">CommonParameters</span></span>
<span data-ttu-id="9f5be-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9f5be-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f5be-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f5be-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f5be-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9f5be-121">INPUTS</span></span>

## <span data-ttu-id="9f5be-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9f5be-122">OUTPUTS</span></span>

## <span data-ttu-id="9f5be-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9f5be-123">NOTES</span></span>

## <span data-ttu-id="9f5be-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9f5be-124">RELATED LINKS</span></span>
