---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplication.md
ms.openlocfilehash: 830b1ed91f8e6148886be9fa3d0c49d48d52d369
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594576"
---
# <span data-ttu-id="82e40-101">New-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="82e40-101">New-AzureRmManagedApplication</span></span>

## <span data-ttu-id="82e40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82e40-102">SYNOPSIS</span></span>
<span data-ttu-id="82e40-103">Azure yönetilen uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="82e40-103">Creates an Azure managed application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82e40-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="82e40-104">SYNTAX</span></span>

```
New-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82e40-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="82e40-105">DESCRIPTION</span></span>
<span data-ttu-id="82e40-106">**Yeni-AzureRmManagedApplication** cmdlet 'ı Azure yönetilen uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="82e40-106">The **New-AzureRmManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="82e40-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="82e40-107">EXAMPLES</span></span>

### <span data-ttu-id="82e40-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="82e40-108">Example 1</span></span>
```
PS C:\>New-AzureRmManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="82e40-109">Bu komut bir yönetilen uygulama oluşturur</span><span class="sxs-lookup"><span data-stu-id="82e40-109">This command creates a managed application</span></span>

## <span data-ttu-id="82e40-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="82e40-110">PARAMETERS</span></span>

### <span data-ttu-id="82e40-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="82e40-111">-ApiVersion</span></span>
<span data-ttu-id="82e40-112">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="82e40-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="82e40-113">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="82e40-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="82e40-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82e40-114">-DefaultProfile</span></span>
<span data-ttu-id="82e40-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="82e40-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82e40-116">-Tür</span><span class="sxs-lookup"><span data-stu-id="82e40-116">-Kind</span></span>
<span data-ttu-id="82e40-117">Yönetilen uygulama türü.</span><span class="sxs-lookup"><span data-stu-id="82e40-117">The managed application kind.</span></span>
<span data-ttu-id="82e40-118">Market veya servicecatalog 'tan biri</span><span class="sxs-lookup"><span data-stu-id="82e40-118">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="82e40-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="82e40-119">-Location</span></span>
<span data-ttu-id="82e40-120">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="82e40-120">The resource location.</span></span>

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

### <span data-ttu-id="82e40-121">-Managedapplicationdefinitionıd</span><span class="sxs-lookup"><span data-stu-id="82e40-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="82e40-122">Yönetilen kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="82e40-122">The managed resource group name.</span></span>

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

### <span data-ttu-id="82e40-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82e40-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="82e40-124">Yönetilen kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="82e40-124">The managed resource group name.</span></span>

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

### <span data-ttu-id="82e40-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="82e40-125">-Name</span></span>
<span data-ttu-id="82e40-126">Yönetilen uygulama adı.</span><span class="sxs-lookup"><span data-stu-id="82e40-126">The managed application name.</span></span>

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

### <span data-ttu-id="82e40-127">-Parametre</span><span class="sxs-lookup"><span data-stu-id="82e40-127">-Parameter</span></span>
<span data-ttu-id="82e40-128">Yönetilen uygulama için JSON biçimli parametrelerin dizesi.</span><span class="sxs-lookup"><span data-stu-id="82e40-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="82e40-129">Bu, parametre içeren bir dosya adı veya URI veya parametre olarak parametre yolu olabilir.</span><span class="sxs-lookup"><span data-stu-id="82e40-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="82e40-130">-Plan</span><span class="sxs-lookup"><span data-stu-id="82e40-130">-Plan</span></span>
<span data-ttu-id="82e40-131">Yönetilen uygulama planı özelliklerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="82e40-131">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="82e40-132">-Pre-</span><span class="sxs-lookup"><span data-stu-id="82e40-132">-Pre</span></span>
<span data-ttu-id="82e40-133">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="82e40-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="82e40-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82e40-134">-ResourceGroupName</span></span>
<span data-ttu-id="82e40-135">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="82e40-135">The resource group name.</span></span>

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

### <span data-ttu-id="82e40-136">Etiketli</span><span class="sxs-lookup"><span data-stu-id="82e40-136">-Tag</span></span>
<span data-ttu-id="82e40-137">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="82e40-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="82e40-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="82e40-138">-Confirm</span></span>
<span data-ttu-id="82e40-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="82e40-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82e40-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82e40-140">-WhatIf</span></span>
<span data-ttu-id="82e40-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="82e40-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82e40-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="82e40-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82e40-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82e40-143">CommonParameters</span></span>
<span data-ttu-id="82e40-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="82e40-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82e40-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82e40-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82e40-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="82e40-146">INPUTS</span></span>

### <span data-ttu-id="82e40-147">System. String</span><span class="sxs-lookup"><span data-stu-id="82e40-147">System.String</span></span>
<span data-ttu-id="82e40-148">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="82e40-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="82e40-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="82e40-149">OUTPUTS</span></span>

### <span data-ttu-id="82e40-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="82e40-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="82e40-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="82e40-151">NOTES</span></span>

## <span data-ttu-id="82e40-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="82e40-152">RELATED LINKS</span></span>

