---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: 4aedbb502780a08d0ce5556af84a445ab44552f5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936450"
---
# <span data-ttu-id="c0c26-101">Get-AzLocation</span><span class="sxs-lookup"><span data-stu-id="c0c26-101">Get-AzLocation</span></span>

## <span data-ttu-id="c0c26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0c26-102">SYNOPSIS</span></span>
<span data-ttu-id="c0c26-103">Her konum için tüm konumları ve desteklenen kaynak sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="c0c26-103">Gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="c0c26-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c0c26-104">SYNTAX</span></span>

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0c26-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c0c26-105">DESCRIPTION</span></span>
<span data-ttu-id="c0c26-106">**Get-AzLocation** cmdlet 'i her konum için tüm konumları ve desteklenen kaynak sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="c0c26-106">The **Get-AzLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="c0c26-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c0c26-107">EXAMPLES</span></span>

### <span data-ttu-id="c0c26-108">Örnek 1: tüm konumları ve desteklenen kaynak sağlayıcılarını alma</span><span class="sxs-lookup"><span data-stu-id="c0c26-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzLocation
```

<span data-ttu-id="c0c26-109">Bu komut, her konum için tüm konumları ve desteklenen kaynak sağlayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="c0c26-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="c0c26-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c0c26-110">PARAMETERS</span></span>

### <span data-ttu-id="c0c26-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="c0c26-111">-ApiVersion</span></span>
<span data-ttu-id="c0c26-112">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0c26-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="c0c26-113">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c0c26-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="c0c26-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0c26-114">-DefaultProfile</span></span>
<span data-ttu-id="c0c26-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c0c26-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c26-116">-Pre-</span><span class="sxs-lookup"><span data-stu-id="c0c26-116">-Pre</span></span>
<span data-ttu-id="c0c26-117">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c0c26-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c0c26-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0c26-118">CommonParameters</span></span>
<span data-ttu-id="c0c26-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c0c26-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0c26-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0c26-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0c26-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c0c26-121">INPUTS</span></span>

## <span data-ttu-id="c0c26-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c0c26-122">OUTPUTS</span></span>

## <span data-ttu-id="c0c26-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c0c26-123">NOTES</span></span>

## <span data-ttu-id="c0c26-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c0c26-124">RELATED LINKS</span></span>
