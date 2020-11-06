---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: EFBBFB60-D972-47B8-997E-B737F0CA007E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
ms.openlocfilehash: 029404938ba7a253b5130f5c807e4b66c3847d43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589127"
---
# <span data-ttu-id="a1464-101">Find-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a1464-101">Find-AzureRmResourceGroup</span></span>

## <span data-ttu-id="a1464-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1464-102">SYNOPSIS</span></span>
<span data-ttu-id="a1464-103">Kaynak gruplarını arar.</span><span class="sxs-lookup"><span data-stu-id="a1464-103">Searches for resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1464-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1464-104">SYNTAX</span></span>

```
Find-AzureRmResourceGroup [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1464-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1464-105">DESCRIPTION</span></span>
<span data-ttu-id="a1464-106">**Find-AzureRmResourceGroup** cmdlet 'i belirtilen parametreleri kullanarak kaynak gruplarını arar.</span><span class="sxs-lookup"><span data-stu-id="a1464-106">The **Find-AzureRmResourceGroup** cmdlet searches for resource groups using the specified parameters.</span></span>

## <span data-ttu-id="a1464-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1464-107">EXAMPLES</span></span>

### <span data-ttu-id="a1464-108">Örnek 1: tüm kaynak gruplarını bulma</span><span class="sxs-lookup"><span data-stu-id="a1464-108">Example 1: Find all resource groups</span></span>
```
PS C:\>Find-AzureRmResourceGroup
```

<span data-ttu-id="a1464-109">Bu komut tüm kaynak gruplarını bulur.</span><span class="sxs-lookup"><span data-stu-id="a1464-109">This command finds all resource groups.</span></span>

### <span data-ttu-id="a1464-110">Örnek 2: etiket adına göre kaynak gruplarını bulma</span><span class="sxs-lookup"><span data-stu-id="a1464-110">Example 2: Find resource groups by tag name</span></span>
```
PS C:\>Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
```

<span data-ttu-id="a1464-111">Bu komut testtag adlı etikete sahip tüm kaynak gruplarını bulur.</span><span class="sxs-lookup"><span data-stu-id="a1464-111">This command finds all resource groups that have a tag named testtag.</span></span>

### <span data-ttu-id="a1464-112">Örnek 3: etiket adına göre kaynak gruplarını bulma</span><span class="sxs-lookup"><span data-stu-id="a1464-112">Example 3: Find resource groups by tag name and value</span></span>
```
PS C:\>Find-AzureRmResourceGroup -Tag @{"testtag" = "testval" }
```

<span data-ttu-id="a1464-113">Bu komut testtag adlı etikete ve TestVal değerine sahip tüm kaynak gruplarını bulur.</span><span class="sxs-lookup"><span data-stu-id="a1464-113">This command finds all resource groups that have a tag named testtag and the value testval.</span></span>

## <span data-ttu-id="a1464-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1464-114">PARAMETERS</span></span>

### <span data-ttu-id="a1464-115">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="a1464-115">-ApiVersion</span></span>
<span data-ttu-id="a1464-116">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1464-116">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="a1464-117">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="a1464-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a1464-118">-Pre-</span><span class="sxs-lookup"><span data-stu-id="a1464-118">-Pre</span></span>
<span data-ttu-id="a1464-119">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a1464-119">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a1464-120">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a1464-120">-Tag</span></span>
<span data-ttu-id="a1464-121">Sonuçlarınızı filtrelemek için etiket bilgilerini karma tablo olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1464-121">Specifies tag information, as a hash table, to filter your results.</span></span> <span data-ttu-id="a1464-122">Aşağıdaki biçimleri kullanın:</span><span class="sxs-lookup"><span data-stu-id="a1464-122">Use the following formats:</span></span>

<span data-ttu-id="a1464-123">@ {tagName = $null} veya @ {tagName = ' tagValue '}.</span><span class="sxs-lookup"><span data-stu-id="a1464-123">@{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1464-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1464-124">-DefaultProfile</span></span>
<span data-ttu-id="a1464-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a1464-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1464-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1464-126">CommonParameters</span></span>
<span data-ttu-id="a1464-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1464-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1464-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1464-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1464-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1464-129">INPUTS</span></span>

## <span data-ttu-id="a1464-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1464-130">OUTPUTS</span></span>

### <span data-ttu-id="a1464-131">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a1464-131">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a1464-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1464-132">NOTES</span></span>

## <span data-ttu-id="a1464-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1464-133">RELATED LINKS</span></span>

