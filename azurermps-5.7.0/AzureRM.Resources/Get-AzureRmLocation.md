---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmLocation.md
ms.openlocfilehash: a3169a78747a34a831ed6bd738e5647c3a4d9eb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592415"
---
# <span data-ttu-id="dc937-101">Get-AzureRmLocation</span><span class="sxs-lookup"><span data-stu-id="dc937-101">Get-AzureRmLocation</span></span>

## <span data-ttu-id="dc937-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc937-102">SYNOPSIS</span></span>
<span data-ttu-id="dc937-103">Her konum için tüm konumları ve desteklenen kaynak sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="dc937-103">Gets all locations and the supported resource providers for each location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc937-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dc937-104">SYNTAX</span></span>

```
Get-AzureRmLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc937-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dc937-105">DESCRIPTION</span></span>
<span data-ttu-id="dc937-106">**Get-AzureRmLocation** cmdlet 'i her konum için tüm konumları ve desteklenen kaynak sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="dc937-106">The **Get-AzureRmLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="dc937-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dc937-107">EXAMPLES</span></span>

### <span data-ttu-id="dc937-108">Örnek 1: tüm konumları ve desteklenen kaynak sağlayıcılarını alma</span><span class="sxs-lookup"><span data-stu-id="dc937-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzureRmLocation
```

<span data-ttu-id="dc937-109">Bu komut, her konum için tüm konumları ve desteklenen kaynak sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="dc937-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="dc937-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dc937-110">PARAMETERS</span></span>

### <span data-ttu-id="dc937-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="dc937-111">-ApiVersion</span></span>
<span data-ttu-id="dc937-112">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="dc937-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="dc937-113">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc937-113">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc937-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc937-114">-DefaultProfile</span></span>
<span data-ttu-id="dc937-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="dc937-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc937-116">-Pre-</span><span class="sxs-lookup"><span data-stu-id="dc937-116">-Pre</span></span>
<span data-ttu-id="dc937-117">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="dc937-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc937-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc937-118">CommonParameters</span></span>
<span data-ttu-id="dc937-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dc937-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc937-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc937-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc937-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dc937-121">INPUTS</span></span>

### <span data-ttu-id="dc937-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="dc937-122">None</span></span>
<span data-ttu-id="dc937-123">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="dc937-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dc937-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dc937-124">OUTPUTS</span></span>

### <span data-ttu-id="dc937-125">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodel. PSResourceProviderLocation]</span><span class="sxs-lookup"><span data-stu-id="dc937-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation]</span></span>

## <span data-ttu-id="dc937-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dc937-126">NOTES</span></span>

## <span data-ttu-id="dc937-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dc937-127">RELATED LINKS</span></span>
