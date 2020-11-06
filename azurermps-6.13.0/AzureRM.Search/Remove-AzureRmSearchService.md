---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/remove-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchService.md
ms.openlocfilehash: c558a5d7228253e0a76b0d47fb21f581b4e06f11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592259"
---
# <span data-ttu-id="4153b-101">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="4153b-101">Remove-AzureRmSearchService</span></span>

## <span data-ttu-id="4153b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4153b-102">SYNOPSIS</span></span>
<span data-ttu-id="4153b-103">Azure Search hizmetini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="4153b-103">Remove an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4153b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4153b-104">SYNTAX</span></span>

### <span data-ttu-id="4153b-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4153b-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzureRmSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4153b-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="4153b-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4153b-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="4153b-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmSearchService [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4153b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4153b-108">DESCRIPTION</span></span>
<span data-ttu-id="4153b-109">**Remove-AzureRmSearchService** cmdlet 'i, bir Azure Search hizmetini belirtilen parametre ile kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4153b-109">The **Remove-AzureRmSearchService** cmdlet removes an Azure Search service with specified paramters.</span></span>

## <span data-ttu-id="4153b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4153b-110">EXAMPLES</span></span>

### <span data-ttu-id="4153b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4153b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="4153b-112">Örnek, bir Azure Search hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4153b-112">The example removes an Azure Search service.</span></span>

## <span data-ttu-id="4153b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4153b-113">PARAMETERS</span></span>

### <span data-ttu-id="4153b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4153b-114">-DefaultProfile</span></span>
<span data-ttu-id="4153b-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4153b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4153b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4153b-116">-Force</span></span>
<span data-ttu-id="4153b-117">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="4153b-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4153b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4153b-118">-InputObject</span></span>
<span data-ttu-id="4153b-119">Arama hizmeti giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4153b-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="4153b-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="4153b-120">-Name</span></span>
<span data-ttu-id="4153b-121">Arama hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="4153b-121">Search Service name.</span></span>

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

### <span data-ttu-id="4153b-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4153b-122">-PassThru</span></span>
<span data-ttu-id="4153b-123">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="4153b-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="4153b-124">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="4153b-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4153b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4153b-125">-ResourceGroupName</span></span>
<span data-ttu-id="4153b-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4153b-126">Resource Group name.</span></span>

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

### <span data-ttu-id="4153b-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4153b-127">-ResourceId</span></span>
<span data-ttu-id="4153b-128">Arama hizmeti kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="4153b-128">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="4153b-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="4153b-129">-Confirm</span></span>
<span data-ttu-id="4153b-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4153b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4153b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4153b-131">-WhatIf</span></span>
<span data-ttu-id="4153b-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4153b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4153b-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4153b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4153b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4153b-134">CommonParameters</span></span>
<span data-ttu-id="4153b-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4153b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4153b-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4153b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4153b-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4153b-137">INPUTS</span></span>

### <span data-ttu-id="4153b-138">Microsoft. Azure. Commands. Management. Search. model. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="4153b-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="4153b-139">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4153b-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="4153b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4153b-140">System.String</span></span>

## <span data-ttu-id="4153b-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4153b-141">OUTPUTS</span></span>

### <span data-ttu-id="4153b-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4153b-142">System.Boolean</span></span>

## <span data-ttu-id="4153b-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4153b-143">NOTES</span></span>

## <span data-ttu-id="4153b-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4153b-144">RELATED LINKS</span></span>

[<span data-ttu-id="4153b-145">Yeni-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="4153b-145">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="4153b-146">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="4153b-146">Get-AzureRmSearchService</span></span>](./Get-AzureRmSearchService.md)

[<span data-ttu-id="4153b-147">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="4153b-147">Set-AzureRmSearchService</span></span>](./Set-AzureRmSearchService.md)

