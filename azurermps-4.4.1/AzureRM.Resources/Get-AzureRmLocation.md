---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmLocation.md
ms.openlocfilehash: 62acee0398c9530a54e02c2347bf384498b07196
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594180"
---
# <span data-ttu-id="ece15-101">Get-AzureRmLocation</span><span class="sxs-lookup"><span data-stu-id="ece15-101">Get-AzureRmLocation</span></span>

## <span data-ttu-id="ece15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ece15-102">SYNOPSIS</span></span>
<span data-ttu-id="ece15-103">Her konum için tüm konumları ve desteklenen kaynak sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="ece15-103">Gets all locations and the supported resource providers for each location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ece15-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ece15-104">SYNTAX</span></span>

```
Get-AzureRmLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ece15-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ece15-105">DESCRIPTION</span></span>
<span data-ttu-id="ece15-106">**Get-AzureRmLocation** cmdlet 'i her konum için tüm konumları ve desteklenen kaynak sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="ece15-106">The **Get-AzureRmLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="ece15-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ece15-107">EXAMPLES</span></span>

### <span data-ttu-id="ece15-108">Örnek 1: tüm konumları ve desteklenen kaynak sağlayıcılarını alma</span><span class="sxs-lookup"><span data-stu-id="ece15-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzureRmLocation
```

<span data-ttu-id="ece15-109">Bu komut, her konum için tüm konumları ve desteklenen kaynak sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="ece15-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="ece15-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ece15-110">PARAMETERS</span></span>

### <span data-ttu-id="ece15-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="ece15-111">-ApiVersion</span></span>
<span data-ttu-id="ece15-112">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ece15-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="ece15-113">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ece15-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="ece15-114">-Pre-</span><span class="sxs-lookup"><span data-stu-id="ece15-114">-Pre</span></span>
<span data-ttu-id="ece15-115">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ece15-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ece15-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ece15-116">-DefaultProfile</span></span>
<span data-ttu-id="ece15-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ece15-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ece15-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece15-118">CommonParameters</span></span>
<span data-ttu-id="ece15-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ece15-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece15-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ece15-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece15-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ece15-121">INPUTS</span></span>

## <span data-ttu-id="ece15-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ece15-122">OUTPUTS</span></span>

### <span data-ttu-id="ece15-123">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodel. PSResourceProviderLocation]</span><span class="sxs-lookup"><span data-stu-id="ece15-123">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation]</span></span>

## <span data-ttu-id="ece15-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ece15-124">NOTES</span></span>

## <span data-ttu-id="ece15-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ece15-125">RELATED LINKS</span></span>

