---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
ms.openlocfilehash: 8286bdd365f43881f09787dfb051e873d2fdeb9c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933346"
---
# <span data-ttu-id="2bd3f-101">New-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="2bd3f-101">New-AzManagedApplication</span></span>

## <span data-ttu-id="2bd3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bd3f-102">SYNOPSIS</span></span>
<span data-ttu-id="2bd3f-103">Azure yönetilen uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-103">Creates an Azure managed application.</span></span>

## <span data-ttu-id="2bd3f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2bd3f-104">SYNTAX</span></span>

```
New-AzManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bd3f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2bd3f-105">DESCRIPTION</span></span>
<span data-ttu-id="2bd3f-106">**Yeni-AzManagedApplication** cmdlet 'ı Azure yönetilen uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-106">The **New-AzManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="2bd3f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2bd3f-107">EXAMPLES</span></span>

### <span data-ttu-id="2bd3f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2bd3f-108">Example 1</span></span>
```
PS C:\>New-AzManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="2bd3f-109">Bu komut bir yönetilen uygulama oluşturur</span><span class="sxs-lookup"><span data-stu-id="2bd3f-109">This command creates a managed application</span></span>

## <span data-ttu-id="2bd3f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2bd3f-110">PARAMETERS</span></span>

### <span data-ttu-id="2bd3f-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="2bd3f-111">-ApiVersion</span></span>
<span data-ttu-id="2bd3f-112">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="2bd3f-113">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="2bd3f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bd3f-114">-DefaultProfile</span></span>
<span data-ttu-id="2bd3f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bd3f-116">-Tür</span><span class="sxs-lookup"><span data-stu-id="2bd3f-116">-Kind</span></span>
<span data-ttu-id="2bd3f-117">Yönetilen uygulama türü.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-117">The managed application kind.</span></span>
<span data-ttu-id="2bd3f-118">Market veya servicecatalog 'tan biri</span><span class="sxs-lookup"><span data-stu-id="2bd3f-118">One of marketplace or servicecatalog</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationKind
Parameter Sets: (All)
Aliases:
Accepted values: ServiceCatalog, MarketPlace

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bd3f-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="2bd3f-119">-Location</span></span>
<span data-ttu-id="2bd3f-120">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-120">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bd3f-121">-Managedapplicationdefinitionıd</span><span class="sxs-lookup"><span data-stu-id="2bd3f-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="2bd3f-122">Yönetilen kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-122">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bd3f-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bd3f-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="2bd3f-124">Yönetilen kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-124">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bd3f-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="2bd3f-125">-Name</span></span>
<span data-ttu-id="2bd3f-126">Yönetilen uygulama adı.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bd3f-127">-Parametre</span><span class="sxs-lookup"><span data-stu-id="2bd3f-127">-Parameter</span></span>
<span data-ttu-id="2bd3f-128">Yönetilen uygulama için JSON biçimli parametrelerin dizesi.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="2bd3f-129">Bu, parametre içeren bir dosya adı veya URI veya parametre olarak parametre yolu olabilir.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bd3f-130">-Plan</span><span class="sxs-lookup"><span data-stu-id="2bd3f-130">-Plan</span></span>
<span data-ttu-id="2bd3f-131">Yönetilen uygulama planı özelliklerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-131">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bd3f-132">-Pre-</span><span class="sxs-lookup"><span data-stu-id="2bd3f-132">-Pre</span></span>
<span data-ttu-id="2bd3f-133">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2bd3f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bd3f-134">-ResourceGroupName</span></span>
<span data-ttu-id="2bd3f-135">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bd3f-136">Etiketli</span><span class="sxs-lookup"><span data-stu-id="2bd3f-136">-Tag</span></span>
<span data-ttu-id="2bd3f-137">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-137">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bd3f-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="2bd3f-138">-Confirm</span></span>
<span data-ttu-id="2bd3f-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bd3f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bd3f-140">-WhatIf</span></span>
<span data-ttu-id="2bd3f-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bd3f-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bd3f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bd3f-143">CommonParameters</span></span>
<span data-ttu-id="2bd3f-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bd3f-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bd3f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bd3f-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2bd3f-146">INPUTS</span></span>

### <span data-ttu-id="2bd3f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="2bd3f-147">System.String</span></span>

### <span data-ttu-id="2bd3f-148">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2bd3f-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2bd3f-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2bd3f-149">OUTPUTS</span></span>

### <span data-ttu-id="2bd3f-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="2bd3f-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="2bd3f-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2bd3f-151">NOTES</span></span>

## <span data-ttu-id="2bd3f-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2bd3f-152">RELATED LINKS</span></span>
