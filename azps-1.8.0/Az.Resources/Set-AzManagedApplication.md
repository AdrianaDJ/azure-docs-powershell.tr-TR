---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
ms.openlocfilehash: 83a0e39d5b21aad0d23e4513793b5b9ed00fa0d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759318"
---
# <span data-ttu-id="95c44-101">Set-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="95c44-101">Set-AzManagedApplication</span></span>

## <span data-ttu-id="95c44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95c44-102">SYNOPSIS</span></span>
<span data-ttu-id="95c44-103">Yönetilen uygulamayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="95c44-103">Updates managed application</span></span>

## <span data-ttu-id="95c44-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95c44-104">SYNTAX</span></span>

### <span data-ttu-id="95c44-105">Setbynaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="95c44-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95c44-106">Setbyıd</span><span class="sxs-lookup"><span data-stu-id="95c44-106">SetById</span></span>
```
Set-AzManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95c44-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="95c44-107">DESCRIPTION</span></span>
<span data-ttu-id="95c44-108">**Set-AzManagedApplication** cmdlet 'i yönetilen uygulamaları güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="95c44-108">The **Set-AzManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="95c44-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95c44-109">EXAMPLES</span></span>

### <span data-ttu-id="95c44-110">Örnek 1: yönetilen uygulama tanımı açıklamasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="95c44-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="95c44-111">Bu komut, yönetilen uygulama açıklamasını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="95c44-111">This command updates the managed application description</span></span>

## <span data-ttu-id="95c44-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95c44-112">PARAMETERS</span></span>

### <span data-ttu-id="95c44-113">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="95c44-113">-ApiVersion</span></span>
<span data-ttu-id="95c44-114">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="95c44-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="95c44-115">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="95c44-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="95c44-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95c44-116">-DefaultProfile</span></span>
<span data-ttu-id="95c44-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="95c44-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95c44-118">-ID</span><span class="sxs-lookup"><span data-stu-id="95c44-118">-Id</span></span>
<span data-ttu-id="95c44-119">Abonelik dahil, tam nitelikli yönetilen uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="95c44-119">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="95c44-120">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname</span><span class="sxs-lookup"><span data-stu-id="95c44-120">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95c44-121">-Tür</span><span class="sxs-lookup"><span data-stu-id="95c44-121">-Kind</span></span>
<span data-ttu-id="95c44-122">Yönetilen uygulama türü.</span><span class="sxs-lookup"><span data-stu-id="95c44-122">The managed application kind.</span></span>
<span data-ttu-id="95c44-123">Market veya servicecatalog 'tan biri</span><span class="sxs-lookup"><span data-stu-id="95c44-123">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="95c44-124">-Managedapplicationdefinitionıd</span><span class="sxs-lookup"><span data-stu-id="95c44-124">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="95c44-125">Yönetilen kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="95c44-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="95c44-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95c44-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="95c44-127">Yönetilen kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="95c44-127">The managed resource group name.</span></span>

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

### <span data-ttu-id="95c44-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="95c44-128">-Name</span></span>
<span data-ttu-id="95c44-129">Yönetilen uygulama adı.</span><span class="sxs-lookup"><span data-stu-id="95c44-129">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95c44-130">-Parametre</span><span class="sxs-lookup"><span data-stu-id="95c44-130">-Parameter</span></span>
<span data-ttu-id="95c44-131">Yönetilen uygulama için JSON biçimli parametrelerin dizesi.</span><span class="sxs-lookup"><span data-stu-id="95c44-131">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="95c44-132">Bu, parametre içeren bir dosya adı veya URI veya parametre olarak parametre yolu olabilir.</span><span class="sxs-lookup"><span data-stu-id="95c44-132">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="95c44-133">-Plan</span><span class="sxs-lookup"><span data-stu-id="95c44-133">-Plan</span></span>
<span data-ttu-id="95c44-134">Yönetilen uygulama planı özelliklerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="95c44-134">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="95c44-135">-Pre-</span><span class="sxs-lookup"><span data-stu-id="95c44-135">-Pre</span></span>
<span data-ttu-id="95c44-136">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="95c44-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="95c44-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95c44-137">-ResourceGroupName</span></span>
<span data-ttu-id="95c44-138">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="95c44-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95c44-139">Etiketli</span><span class="sxs-lookup"><span data-stu-id="95c44-139">-Tag</span></span>
<span data-ttu-id="95c44-140">Kaynak etiketlerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="95c44-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="95c44-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="95c44-141">-Confirm</span></span>
<span data-ttu-id="95c44-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="95c44-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95c44-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95c44-143">-WhatIf</span></span>
<span data-ttu-id="95c44-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="95c44-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95c44-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="95c44-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95c44-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95c44-146">CommonParameters</span></span>
<span data-ttu-id="95c44-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="95c44-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95c44-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95c44-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95c44-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95c44-149">INPUTS</span></span>

### <span data-ttu-id="95c44-150">System. String</span><span class="sxs-lookup"><span data-stu-id="95c44-150">System.String</span></span>

### <span data-ttu-id="95c44-151">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="95c44-151">System.Collections.Hashtable</span></span>

## <span data-ttu-id="95c44-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95c44-152">OUTPUTS</span></span>

### <span data-ttu-id="95c44-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="95c44-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="95c44-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95c44-154">NOTES</span></span>

## <span data-ttu-id="95c44-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95c44-155">RELATED LINKS</span></span>
