---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
ms.openlocfilehash: 6f6653c9ba7f69c6bf2cc91d2517edb06fae7523
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933273"
---
# <span data-ttu-id="9e28a-101">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="9e28a-101">Remove-AzSearchService</span></span>

## <span data-ttu-id="9e28a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e28a-102">SYNOPSIS</span></span>
<span data-ttu-id="9e28a-103">Azure Search hizmetini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="9e28a-103">Remove an Azure Search service.</span></span>

## <span data-ttu-id="9e28a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e28a-104">SYNTAX</span></span>

### <span data-ttu-id="9e28a-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9e28a-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e28a-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="9e28a-106">InputObjectParameterSet</span></span>
```
Remove-AzSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e28a-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="9e28a-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchService [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e28a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e28a-108">DESCRIPTION</span></span>
<span data-ttu-id="9e28a-109">**Remove-AzSearchService** cmdlet 'ı, Azure Search hizmetini belirtilen parametrelerle kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9e28a-109">The **Remove-AzSearchService** cmdlet removes an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="9e28a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e28a-110">EXAMPLES</span></span>

### <span data-ttu-id="9e28a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9e28a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="9e28a-112">Örnek, bir Azure Search hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9e28a-112">The example removes an Azure Search service.</span></span>

## <span data-ttu-id="9e28a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e28a-113">PARAMETERS</span></span>

### <span data-ttu-id="9e28a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e28a-114">-DefaultProfile</span></span>
<span data-ttu-id="9e28a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9e28a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e28a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="9e28a-116">-Force</span></span>
<span data-ttu-id="9e28a-117">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="9e28a-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9e28a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e28a-118">-InputObject</span></span>
<span data-ttu-id="9e28a-119">Arama hizmeti giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9e28a-119">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e28a-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="9e28a-120">-Name</span></span>
<span data-ttu-id="9e28a-121">Arama hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="9e28a-121">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e28a-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9e28a-122">-PassThru</span></span>
<span data-ttu-id="9e28a-123">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="9e28a-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="9e28a-124">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="9e28a-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9e28a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e28a-125">-ResourceGroupName</span></span>
<span data-ttu-id="9e28a-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9e28a-126">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e28a-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9e28a-127">-ResourceId</span></span>
<span data-ttu-id="9e28a-128">Arama hizmeti kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="9e28a-128">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e28a-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="9e28a-129">-Confirm</span></span>
<span data-ttu-id="9e28a-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9e28a-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e28a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e28a-131">-WhatIf</span></span>
<span data-ttu-id="9e28a-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9e28a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e28a-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9e28a-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e28a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e28a-134">CommonParameters</span></span>
<span data-ttu-id="9e28a-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e28a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e28a-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e28a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e28a-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e28a-137">INPUTS</span></span>

### <span data-ttu-id="9e28a-138">Microsoft. Azure. Commands. Management. Search. model. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="9e28a-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="9e28a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9e28a-139">System.String</span></span>

## <span data-ttu-id="9e28a-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e28a-140">OUTPUTS</span></span>

### <span data-ttu-id="9e28a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9e28a-141">System.Boolean</span></span>

## <span data-ttu-id="9e28a-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e28a-142">NOTES</span></span>

## <span data-ttu-id="9e28a-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e28a-143">RELATED LINKS</span></span>

[<span data-ttu-id="9e28a-144">Yeni-Azaramahizmeti</span><span class="sxs-lookup"><span data-stu-id="9e28a-144">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="9e28a-145">Get-Azaramahizmeti</span><span class="sxs-lookup"><span data-stu-id="9e28a-145">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="9e28a-146">Set-Azaramahizmeti</span><span class="sxs-lookup"><span data-stu-id="9e28a-146">Set-AzSearchService</span></span>](./Set-AzSearchService.md)
