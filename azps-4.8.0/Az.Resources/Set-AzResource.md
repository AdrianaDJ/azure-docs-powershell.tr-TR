---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
ms.openlocfilehash: 7a4929ffff531bb11b19b44ca9c0914c71662c8d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107646"
---
# <span data-ttu-id="189d1-101">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="189d1-101">Set-AzResource</span></span>

## <span data-ttu-id="189d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="189d1-102">SYNOPSIS</span></span>
<span data-ttu-id="189d1-103">Bir kaynağı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="189d1-103">Modifies a resource.</span></span>

## <span data-ttu-id="189d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="189d1-104">SYNTAX</span></span>

### <span data-ttu-id="189d1-105">Byresourceıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="189d1-105">ByResourceId (Default)</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="189d1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="189d1-106">ByInputObject</span></span>
```
Set-AzResource -InputObject <PSResource> [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="189d1-107">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="189d1-107">BySubscriptionLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="189d1-108">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="189d1-108">ByTenantLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="189d1-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="189d1-109">DESCRIPTION</span></span>
<span data-ttu-id="189d1-110">**Set-Azkaynak** cmdlet 'i mevcut bir Azure kaynağını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="189d1-110">The **Set-AzResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="189d1-111">Ada göre değiştirmek ve KIMLIK yazmak için kaynak belirtin.</span><span class="sxs-lookup"><span data-stu-id="189d1-111">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="189d1-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="189d1-112">EXAMPLES</span></span>

### <span data-ttu-id="189d1-113">Örnek 1: kaynağı değiştirme</span><span class="sxs-lookup"><span data-stu-id="189d1-113">Example 1: Modify a resource</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceType Microsoft.Web/sites -ResourceGroupName ResourceGroup11 -ResourceName ContosoSite
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzResource -Force
```

<span data-ttu-id="189d1-114">İlk komut, Get-AzResource cmdlet 'ini kullanarak ContosoSite adlı kaynağı alır ve $Resource değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="189d1-114">The first command gets the resource named ContosoSite by using the Get-AzResource cmdlet, and then stores it in the $Resource variable.</span></span>
<span data-ttu-id="189d1-115">İkinci komut $Resource özelliğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="189d1-115">The second command modifies a property of $Resource.</span></span>
<span data-ttu-id="189d1-116">Son komutu $Resource eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="189d1-116">The final command updates the resource to match $Resource.</span></span>

### <span data-ttu-id="189d1-117">Örnek 2: belirli bir kaynak grubundaki tüm kaynakları değiştirme</span><span class="sxs-lookup"><span data-stu-id="189d1-117">Example 2: Modify all resources in a given resource group</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceGroupName testrg
PS C:\> $Resource | ForEach-Object { $_.Tags.Add("testkey", "testval") }
PS C:\> $Resource | Set-AzResource -Force

Name              : kv-test
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.KeyVault/vaults/kv-test
ResourceName      : kv-test
ResourceType      : Microsoft.KeyVault/vaults
ResourceGroupName : testrg
Location          : westus
SubscriptionId    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags              : {testrgkey, key}
Properties        : @{}

Name              : testresource
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Providers.Test/statefulResources/testresource
ResourceName      : testresource
ResourceType      : Providers.Test/statefulResources
ResourceGroupName : testrg
Location          : West US 2
SubscriptionId    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags              : {testrgkey, anothertesttag}
Properties        : @{key=value}
Sku               : @{name=A0}
```

<span data-ttu-id="189d1-118">İlk komut, testrg kaynak grubundaki kaynakları alır ve $Resource değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="189d1-118">The first command gets the resources in the testrg resource group, and then stores them in the $Resource variable.</span></span>

<span data-ttu-id="189d1-119">İkinci komut, kaynak grubundaki bu kaynakların her birinin üzerinde dolaşır ve bunlara yeni bir etiket ekler.</span><span class="sxs-lookup"><span data-stu-id="189d1-119">The second command iterates over each of these resources in the resource group and adds a new tag to them.</span></span>

<span data-ttu-id="189d1-120">Son komutu bu kaynakların her birini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="189d1-120">The final command updates each of these resources.</span></span>

## <span data-ttu-id="189d1-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="189d1-121">PARAMETERS</span></span>

### <span data-ttu-id="189d1-122">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="189d1-122">-ApiVersion</span></span>
<span data-ttu-id="189d1-123">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="189d1-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="189d1-124">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="189d1-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="189d1-125">-Iş</span><span class="sxs-lookup"><span data-stu-id="189d1-125">-AsJob</span></span>
<span data-ttu-id="189d1-126">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="189d1-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="189d1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="189d1-127">-DefaultProfile</span></span>
<span data-ttu-id="189d1-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="189d1-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="189d1-129">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="189d1-129">-ExtensionResourceName</span></span>
<span data-ttu-id="189d1-130">Kaynak için bir uzantı kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="189d1-130">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="189d1-131">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın: sunucu adı `/` veritabanı adı</span><span class="sxs-lookup"><span data-stu-id="189d1-131">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="189d1-132">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="189d1-132">-ExtensionResourceType</span></span>
<span data-ttu-id="189d1-133">Bir uzantı kaynağı için kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="189d1-133">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="189d1-134">Örneğin, uzantı kaynağı bir veritabanıdır, aşağıdakileri belirtin: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="189d1-134">For instance, if the extension resource is a database specify the following: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="189d1-135">-Force</span><span class="sxs-lookup"><span data-stu-id="189d1-135">-Force</span></span>
<span data-ttu-id="189d1-136">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="189d1-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="189d1-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="189d1-137">-InputObject</span></span>
<span data-ttu-id="189d1-138">Güncelleştirilecek kaynağın nesne gösterimi.</span><span class="sxs-lookup"><span data-stu-id="189d1-138">The object representation of the resource to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="189d1-139">-Tür</span><span class="sxs-lookup"><span data-stu-id="189d1-139">-Kind</span></span>
<span data-ttu-id="189d1-140">Kaynağın kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="189d1-140">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="189d1-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="189d1-141">-ODataQuery</span></span>
<span data-ttu-id="189d1-142">Açık bir veri Protokolü (OData) stil filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="189d1-142">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="189d1-143">Bu cmdlet, bu değeri diğer tüm filtrelere ek olarak isteğe ekler.</span><span class="sxs-lookup"><span data-stu-id="189d1-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="189d1-144">-Plan</span><span class="sxs-lookup"><span data-stu-id="189d1-144">-Plan</span></span>
<span data-ttu-id="189d1-145">Kaynak için kaynak planı özelliklerini karma tablo olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="189d1-145">Specifies resource plan properties, as a hash table, for the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="189d1-146">-Pre-</span><span class="sxs-lookup"><span data-stu-id="189d1-146">-Pre</span></span>
<span data-ttu-id="189d1-147">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="189d1-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="189d1-148">-Özellikler</span><span class="sxs-lookup"><span data-stu-id="189d1-148">-Properties</span></span>
<span data-ttu-id="189d1-149">Kaynağın kaynak özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="189d1-149">Specifies resource properties for the resource.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="189d1-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="189d1-150">-ResourceGroupName</span></span>
<span data-ttu-id="189d1-151">Bu cmdlet 'in kaynağı değiştirdiği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="189d1-151">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="189d1-152">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="189d1-152">-ResourceId</span></span>
<span data-ttu-id="189d1-153">Aşağıdaki örnekte olduğu gibi, abonelik dahil olmak üzere tam nitelikli kaynak KIMLIĞINI belirtir: `/subscriptions/` ABONELIK kimliği`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="189d1-153">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="189d1-154">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="189d1-154">-ResourceName</span></span>
<span data-ttu-id="189d1-155">Kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="189d1-155">Specifies the name of the resource.</span></span>
<span data-ttu-id="189d1-156">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="189d1-156">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="189d1-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="189d1-157">-ResourceType</span></span>
<span data-ttu-id="189d1-158">Kaynağın türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="189d1-158">Specifies the type of the resource.</span></span>
<span data-ttu-id="189d1-159">Örneğin, veritabanı için kaynak türü aşağıdaki gibidir: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="189d1-159">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="189d1-160">-SKU</span><span class="sxs-lookup"><span data-stu-id="189d1-160">-Sku</span></span>
<span data-ttu-id="189d1-161">Kaynağın SKU nesnesini karma tablo olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="189d1-161">Specifies the SKU object of the resource as a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="189d1-162">Etiketli</span><span class="sxs-lookup"><span data-stu-id="189d1-162">-Tag</span></span>
<span data-ttu-id="189d1-163">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="189d1-163">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="189d1-164">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="189d1-164">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="189d1-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="189d1-165">-TenantLevel</span></span>
<span data-ttu-id="189d1-166">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="189d1-166">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="189d1-167">-Usepatchsemantiği</span><span class="sxs-lookup"><span data-stu-id="189d1-167">-UsePatchSemantics</span></span>
<span data-ttu-id="189d1-168">Bu cmdlet 'in, HTTP yerıne nesneyi güncelleştirmek için bir HTTP düzeltme eki kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="189d1-168">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="189d1-169">-Onay</span><span class="sxs-lookup"><span data-stu-id="189d1-169">-Confirm</span></span>
<span data-ttu-id="189d1-170">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="189d1-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="189d1-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="189d1-171">-WhatIf</span></span>
<span data-ttu-id="189d1-172">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="189d1-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="189d1-173">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="189d1-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="189d1-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="189d1-174">CommonParameters</span></span>
<span data-ttu-id="189d1-175">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="189d1-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="189d1-176">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="189d1-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="189d1-177">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="189d1-177">INPUTS</span></span>

### <span data-ttu-id="189d1-178">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSResource</span><span class="sxs-lookup"><span data-stu-id="189d1-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

### <span data-ttu-id="189d1-179">System. String</span><span class="sxs-lookup"><span data-stu-id="189d1-179">System.String</span></span>

### <span data-ttu-id="189d1-180">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="189d1-180">System.Management.Automation.PSObject</span></span>

### <span data-ttu-id="189d1-181">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="189d1-181">System.Collections.Hashtable</span></span>

## <span data-ttu-id="189d1-182">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="189d1-182">OUTPUTS</span></span>

### <span data-ttu-id="189d1-183">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="189d1-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="189d1-184">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="189d1-184">NOTES</span></span>

## <span data-ttu-id="189d1-185">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="189d1-185">RELATED LINKS</span></span>

[<span data-ttu-id="189d1-186">Find-AzResource</span><span class="sxs-lookup"><span data-stu-id="189d1-186">Find-AzResource</span></span>](./Find-AzResource.md)

[<span data-ttu-id="189d1-187">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="189d1-187">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="189d1-188">Taşı-Azkaynak</span><span class="sxs-lookup"><span data-stu-id="189d1-188">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="189d1-189">Yeni-aza kaynağı</span><span class="sxs-lookup"><span data-stu-id="189d1-189">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="189d1-190">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="189d1-190">Remove-AzResource</span></span>](./Remove-AzResource.md)
