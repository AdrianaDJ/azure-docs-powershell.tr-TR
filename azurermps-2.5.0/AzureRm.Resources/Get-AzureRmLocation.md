---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermlocation
schema: 2.0.0
ms.openlocfilehash: c5d9d2131ff144f04794d2cf283aaf51ed1450e9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939490"
---
# <span data-ttu-id="5a876-101">Get-AzureRmLocation</span><span class="sxs-lookup"><span data-stu-id="5a876-101">Get-AzureRmLocation</span></span>

## <span data-ttu-id="5a876-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a876-102">SYNOPSIS</span></span>
<span data-ttu-id="5a876-103">Her konum için tüm konumları ve desteklenen kaynak sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="5a876-103">Gets all locations and the supported resource providers for each location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a876-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5a876-104">SYNTAX</span></span>

```
Get-AzureRmLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a876-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5a876-105">DESCRIPTION</span></span>
<span data-ttu-id="5a876-106">**Get-AzureRmLocation** cmdlet 'i her konum için tüm konumları ve desteklenen kaynak sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="5a876-106">The **Get-AzureRmLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="5a876-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5a876-107">EXAMPLES</span></span>

### <span data-ttu-id="5a876-108">Örnek 1: tüm konumları ve desteklenen kaynak sağlayıcılarını alma</span><span class="sxs-lookup"><span data-stu-id="5a876-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzureRmLocation
```

<span data-ttu-id="5a876-109">Bu komut, her konum için tüm konumları ve desteklenen kaynak sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="5a876-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="5a876-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5a876-110">PARAMETERS</span></span>

### <span data-ttu-id="5a876-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="5a876-111">-ApiVersion</span></span>
<span data-ttu-id="5a876-112">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a876-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="5a876-113">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5a876-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="5a876-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a876-114">-DefaultProfile</span></span>
<span data-ttu-id="5a876-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5a876-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a876-116">-Pre-</span><span class="sxs-lookup"><span data-stu-id="5a876-116">-Pre</span></span>
<span data-ttu-id="5a876-117">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5a876-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5a876-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a876-118">CommonParameters</span></span>
<span data-ttu-id="5a876-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5a876-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a876-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a876-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a876-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5a876-121">INPUTS</span></span>

## <span data-ttu-id="5a876-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5a876-122">OUTPUTS</span></span>

## <span data-ttu-id="5a876-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5a876-123">NOTES</span></span>

## <span data-ttu-id="5a876-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5a876-124">RELATED LINKS</span></span>