---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/invoke-azresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
ms.openlocfilehash: 9a971618c205380a4ca2b049563fc8ee4542e681
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932580"
---
# <span data-ttu-id="c1cd5-101">Invoke-AzResourceAction</span><span class="sxs-lookup"><span data-stu-id="c1cd5-101">Invoke-AzResourceAction</span></span>

## <span data-ttu-id="c1cd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1cd5-102">SYNOPSIS</span></span>
<span data-ttu-id="c1cd5-103">Kaynakta bir eylem çağırır.</span><span class="sxs-lookup"><span data-stu-id="c1cd5-103">Invokes an action on a resource.</span></span>

## <span data-ttu-id="c1cd5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c1cd5-104">SYNTAX</span></span>

### <span data-ttu-id="c1cd5-105">Byresourceıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c1cd5-105">ByResourceId (Default)</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1cd5-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="c1cd5-106">BySubscriptionLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1cd5-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="c1cd5-107">ByTenantLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1cd5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1cd5-108">DESCRIPTION</span></span>
<span data-ttu-id="c1cd5-109">**Invoke-Azresourcesaction** cmdlet 'ı belirtilen Azure kaynağında bir eylem çağırır.</span><span class="sxs-lookup"><span data-stu-id="c1cd5-109">The **Invoke-AzResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="c1cd5-110">Desteklenen eylemlerin listesini almak için, Azure Resource Explorer aracını kullanın.</span><span class="sxs-lookup"><span data-stu-id="c1cd5-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="c1cd5-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c1cd5-111">EXAMPLES</span></span>

## <span data-ttu-id="c1cd5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c1cd5-112">PARAMETERS</span></span>

### <span data-ttu-id="c1cd5-113">-Eylem</span><span class="sxs-lookup"><span data-stu-id="c1cd5-113">-Action</span></span>
<span data-ttu-id="c1cd5-114">Çağrılacak eylemin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1cd5-114">Specifies the name of the action to invoke.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ActionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1cd5-115">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="c1cd5-115">-ApiVersion</span></span>
<span data-ttu-id="c1cd5-116">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1cd5-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c1cd5-117">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="c1cd5-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c1cd5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1cd5-118">-DefaultProfile</span></span>
<span data-ttu-id="c1cd5-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c1cd5-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1cd5-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="c1cd5-120">-ExtensionResourceName</span></span>
<span data-ttu-id="c1cd5-121">Bu cmdlet 'in eylem çağırdıkları kaynak için bir uzantı kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1cd5-121">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="c1cd5-122">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın: sunucu adı `/` veritabanı adı</span><span class="sxs-lookup"><span data-stu-id="c1cd5-122">For instance, to specify a database, use the following format: server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1cd5-123">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="c1cd5-123">-ExtensionResourceType</span></span>
<span data-ttu-id="c1cd5-124">Uzantı kaynağının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1cd5-124">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="c1cd5-125">Örneğin: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="c1cd5-125">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1cd5-126">-Force</span><span class="sxs-lookup"><span data-stu-id="c1cd5-126">-Force</span></span>
<span data-ttu-id="c1cd5-127">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="c1cd5-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c1cd5-128">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="c1cd5-128">-ODataQuery</span></span>
<span data-ttu-id="c1cd5-129">Açık bir veri Protokolü (OData) stil filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1cd5-129">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="c1cd5-130">Bu cmdlet, bu değeri diğer tüm filtrelere ek olarak isteğe ekler.</span><span class="sxs-lookup"><span data-stu-id="c1cd5-130">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="c1cd5-131">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="c1cd5-131">-Parameters</span></span>
<span data-ttu-id="c1cd5-132">Bu cmdlet 'in çağırmasına ilişkin eylem için parametreleri karma bir tablo olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1cd5-132">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Object

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1cd5-133">-Pre-</span><span class="sxs-lookup"><span data-stu-id="c1cd5-133">-Pre</span></span>
<span data-ttu-id="c1cd5-134">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c1cd5-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c1cd5-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1cd5-135">-ResourceGroupName</span></span>
<span data-ttu-id="c1cd5-136">Bu cmdlet 'in eylemi çağırdıkları kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1cd5-136">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1cd5-137">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c1cd5-137">-ResourceId</span></span>
<span data-ttu-id="c1cd5-138">Bu cmdlet 'in eylem çağırdıkları kaynağın tam kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1cd5-138">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="c1cd5-139">KIMLIK, aşağıdaki örnekte olduğu gibi aboneliği içerir: `/subscriptions/` ABONELIK kimliği`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="c1cd5-139">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1cd5-140">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c1cd5-140">-ResourceName</span></span>
<span data-ttu-id="c1cd5-141">Bu cmdlet 'in eylem çağırdıkları kaynak kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1cd5-141">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="c1cd5-142">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="c1cd5-142">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1cd5-143">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c1cd5-143">-ResourceType</span></span>
<span data-ttu-id="c1cd5-144">Kaynağın türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1cd5-144">Specifies the type of the resource.</span></span>
<span data-ttu-id="c1cd5-145">Örneğin, veritabanı için kaynak türü aşağıdaki gibidir: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="c1cd5-145">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1cd5-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="c1cd5-146">-TenantLevel</span></span>
<span data-ttu-id="c1cd5-147">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="c1cd5-147">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1cd5-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="c1cd5-148">-Confirm</span></span>
<span data-ttu-id="c1cd5-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c1cd5-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1cd5-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1cd5-150">-WhatIf</span></span>
<span data-ttu-id="c1cd5-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c1cd5-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1cd5-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c1cd5-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1cd5-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1cd5-153">CommonParameters</span></span>
<span data-ttu-id="c1cd5-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c1cd5-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1cd5-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1cd5-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1cd5-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c1cd5-156">INPUTS</span></span>

### <span data-ttu-id="c1cd5-157">System. String</span><span class="sxs-lookup"><span data-stu-id="c1cd5-157">System.String</span></span>

## <span data-ttu-id="c1cd5-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c1cd5-158">OUTPUTS</span></span>

### <span data-ttu-id="c1cd5-159">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c1cd5-159">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c1cd5-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c1cd5-160">NOTES</span></span>

## <span data-ttu-id="c1cd5-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c1cd5-161">RELATED LINKS</span></span>
