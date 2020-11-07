---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/invoke-azurermresourceaction
schema: 2.0.0
ms.openlocfilehash: e29dda3fc5d2b62196d0cc5897ba7a7c9b047a8c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939679"
---
# <span data-ttu-id="09c4f-101">Invoke-AzureRmResourceAction</span><span class="sxs-lookup"><span data-stu-id="09c4f-101">Invoke-AzureRmResourceAction</span></span>

## <span data-ttu-id="09c4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09c4f-102">SYNOPSIS</span></span>
<span data-ttu-id="09c4f-103">Kaynakta bir eylem çağırır.</span><span class="sxs-lookup"><span data-stu-id="09c4f-103">Invokes an action on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09c4f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="09c4f-104">SYNTAX</span></span>

### <span data-ttu-id="09c4f-105">Byresourceıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="09c4f-105">ByResourceId (Default)</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String>
 [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="09c4f-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="09c4f-106">BySubscriptionLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09c4f-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="09c4f-107">ByTenantLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09c4f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="09c4f-108">DESCRIPTION</span></span>
<span data-ttu-id="09c4f-109">**Invoke-AzureRmResourceAction** cmdlet 'ı belirtilen Azure kaynağında bir eylem çağırır.</span><span class="sxs-lookup"><span data-stu-id="09c4f-109">The **Invoke-AzureRmResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="09c4f-110">Desteklenen eylemlerin listesini almak için, Azure Resource Explorer aracını kullanın.</span><span class="sxs-lookup"><span data-stu-id="09c4f-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="09c4f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="09c4f-111">EXAMPLES</span></span>

## <span data-ttu-id="09c4f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="09c4f-112">PARAMETERS</span></span>

### <span data-ttu-id="09c4f-113">-Eylem</span><span class="sxs-lookup"><span data-stu-id="09c4f-113">-Action</span></span>
<span data-ttu-id="09c4f-114">Çağrılacak eylemin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09c4f-114">Specifies the name of the action to invoke.</span></span>

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

### <span data-ttu-id="09c4f-115">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="09c4f-115">-ApiVersion</span></span>
<span data-ttu-id="09c4f-116">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="09c4f-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="09c4f-117">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="09c4f-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="09c4f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09c4f-118">-DefaultProfile</span></span>
<span data-ttu-id="09c4f-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="09c4f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09c4f-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="09c4f-120">-ExtensionResourceName</span></span>
<span data-ttu-id="09c4f-121">Bu cmdlet 'in eylem çağırdıkları kaynak için bir uzantı kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09c4f-121">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="09c4f-122">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın: sunucu adı `/` veritabanı adı</span><span class="sxs-lookup"><span data-stu-id="09c4f-122">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="09c4f-123">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="09c4f-123">-ExtensionResourceType</span></span>
<span data-ttu-id="09c4f-124">Uzantı kaynağının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="09c4f-124">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="09c4f-125">Örneğin: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="09c4f-125">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="09c4f-126">-Force</span><span class="sxs-lookup"><span data-stu-id="09c4f-126">-Force</span></span>
<span data-ttu-id="09c4f-127">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="09c4f-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="09c4f-128">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="09c4f-128">-InformationAction</span></span>
<span data-ttu-id="09c4f-129">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="09c4f-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="09c4f-130">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="09c4f-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="09c4f-131">'A</span><span class="sxs-lookup"><span data-stu-id="09c4f-131">Continue</span></span>
- <span data-ttu-id="09c4f-132">Manıza</span><span class="sxs-lookup"><span data-stu-id="09c4f-132">Ignore</span></span>
- <span data-ttu-id="09c4f-133">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="09c4f-133">Inquire</span></span>
- <span data-ttu-id="09c4f-134">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="09c4f-134">SilentlyContinue</span></span>
- <span data-ttu-id="09c4f-135">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="09c4f-135">Stop</span></span>
- <span data-ttu-id="09c4f-136">Biliriz</span><span class="sxs-lookup"><span data-stu-id="09c4f-136">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09c4f-137">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="09c4f-137">-InformationVariable</span></span>
<span data-ttu-id="09c4f-138">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="09c4f-138">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09c4f-139">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="09c4f-139">-ODataQuery</span></span>
<span data-ttu-id="09c4f-140">Açık bir veri Protokolü (OData) stil filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="09c4f-140">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="09c4f-141">Bu cmdlet, bu değeri diğer tüm filtrelere ek olarak isteğe ekler.</span><span class="sxs-lookup"><span data-stu-id="09c4f-141">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="09c4f-142">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="09c4f-142">-Parameters</span></span>
<span data-ttu-id="09c4f-143">Bu cmdlet 'in çağırmasına ilişkin eylem için parametreleri karma bir tablo olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="09c4f-143">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

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

### <span data-ttu-id="09c4f-144">-Pre-</span><span class="sxs-lookup"><span data-stu-id="09c4f-144">-Pre</span></span>
<span data-ttu-id="09c4f-145">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="09c4f-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="09c4f-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09c4f-146">-ResourceGroupName</span></span>
<span data-ttu-id="09c4f-147">Bu cmdlet 'in eylemi çağırdıkları kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09c4f-147">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="09c4f-148">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="09c4f-148">-ResourceId</span></span>
<span data-ttu-id="09c4f-149">Bu cmdlet 'in eylem çağırdıkları kaynağın tam kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="09c4f-149">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="09c4f-150">KIMLIK, aşağıdaki örnekte olduğu gibi aboneliği içerir: `/subscriptions/` ABONELIK kimliği`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="09c4f-150">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="09c4f-151">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="09c4f-151">-ResourceName</span></span>
<span data-ttu-id="09c4f-152">Bu cmdlet 'in eylem çağırdıkları kaynak kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09c4f-152">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="09c4f-153">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="09c4f-153">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="09c4f-154">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="09c4f-154">-ResourceType</span></span>
<span data-ttu-id="09c4f-155">Kaynağın türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="09c4f-155">Specifies the type of the resource.</span></span>
<span data-ttu-id="09c4f-156">Örneğin, veritabanı için kaynak türü aşağıdaki gibidir: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="09c4f-156">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="09c4f-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="09c4f-157">-TenantLevel</span></span>
<span data-ttu-id="09c4f-158">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="09c4f-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="09c4f-159">-Onay</span><span class="sxs-lookup"><span data-stu-id="09c4f-159">-Confirm</span></span>
<span data-ttu-id="09c4f-160">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="09c4f-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09c4f-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09c4f-161">-WhatIf</span></span>
<span data-ttu-id="09c4f-162">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="09c4f-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09c4f-163">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="09c4f-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09c4f-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09c4f-164">CommonParameters</span></span>
<span data-ttu-id="09c4f-165">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="09c4f-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09c4f-166">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09c4f-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09c4f-167">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="09c4f-167">INPUTS</span></span>

## <span data-ttu-id="09c4f-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="09c4f-168">OUTPUTS</span></span>

## <span data-ttu-id="09c4f-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="09c4f-169">NOTES</span></span>

## <span data-ttu-id="09c4f-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="09c4f-170">RELATED LINKS</span></span>
