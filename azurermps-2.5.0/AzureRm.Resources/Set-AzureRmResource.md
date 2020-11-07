---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresource
schema: 2.0.0
ms.openlocfilehash: 6d243cccb5f5a64ef0275da1020222416c491ee3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939239"
---
# <span data-ttu-id="51b92-101">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="51b92-101">Set-AzureRmResource</span></span>

## <span data-ttu-id="51b92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51b92-102">SYNOPSIS</span></span>
<span data-ttu-id="51b92-103">Bir kaynağı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="51b92-103">Modifies a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51b92-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="51b92-104">SYNTAX</span></span>

### <span data-ttu-id="51b92-105">Byresourceıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="51b92-105">ByResourceId (Default)</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51b92-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="51b92-106">ByInputObject</span></span>
```
Set-AzureRmResource -InputObject <PSResource> [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51b92-107">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="51b92-107">BySubscriptionLevel</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51b92-108">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="51b92-108">ByTenantLevel</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="51b92-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="51b92-109">DESCRIPTION</span></span>
<span data-ttu-id="51b92-110">**Set-AzureRmResource** cmdlet 'i, mevcut bir Azure kaynağını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="51b92-110">The **Set-AzureRmResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="51b92-111">Ada göre değiştirmek ve KIMLIK yazmak için kaynak belirtin.</span><span class="sxs-lookup"><span data-stu-id="51b92-111">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="51b92-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="51b92-112">EXAMPLES</span></span>

### <span data-ttu-id="51b92-113">Örnek 1: kaynağı değiştirme</span><span class="sxs-lookup"><span data-stu-id="51b92-113">Example 1: Modify a resource</span></span>
```
PS C:\> $Resource = Get-AzureRmResource -ResourceType Microsoft.Web/sites -ResourceGroupName ResourceGroup11 -ResourceName ContosoSite
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzureRmResource -Force
```

<span data-ttu-id="51b92-114">İlk komut, Get-AzureRmResource cmdlet 'ini kullanarak ContosoSite adlı kaynağı alır ve $Resource değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="51b92-114">The first command gets the resource named ContosoSite by using the Get-AzureRmResource cmdlet, and then stores it in the $Resource variable.</span></span>
<span data-ttu-id="51b92-115">İkinci komut $Resource özelliğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="51b92-115">The second command modifies a property of $Resource.</span></span>
<span data-ttu-id="51b92-116">Son komutu $Resource eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="51b92-116">The final command updates the resource to match $Resource.</span></span>

### <span data-ttu-id="51b92-117">Örnek 2: belirli bir kaynak grubundaki tüm kaynakları değiştirme</span><span class="sxs-lookup"><span data-stu-id="51b92-117">Example 2: Modify all resources in a given resource group</span></span>
```
PS C:\> $Resource = Get-AzureRmResource -ResourceGroupName testrg
PS C:\> $Resource | ForEach-Object { $_.Tags.Add("testkey", "testval") }
PS C:\> $Resource | Set-AzureRmResource -Force

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

<span data-ttu-id="51b92-118">İlk komut, testrg kaynak grubundaki kaynakları alır ve $Resource değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="51b92-118">The first command gets the resources in the testrg resource group, and then stores them in the $Resource variable.</span></span>

<span data-ttu-id="51b92-119">İkinci komut, kaynak grubundaki bu kaynakların her birinin üzerinde dolaşır ve bunlara yeni bir etiket ekler.</span><span class="sxs-lookup"><span data-stu-id="51b92-119">The second command iterates over each of these resources in the resource group and adds a new tag to them.</span></span>

<span data-ttu-id="51b92-120">Son komutu bu kaynakların her birini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="51b92-120">The final command updates each of these resources.</span></span>

## <span data-ttu-id="51b92-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="51b92-121">PARAMETERS</span></span>

### <span data-ttu-id="51b92-122">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="51b92-122">-ApiVersion</span></span>
<span data-ttu-id="51b92-123">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="51b92-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="51b92-124">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="51b92-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="51b92-125">-Iş</span><span class="sxs-lookup"><span data-stu-id="51b92-125">-AsJob</span></span>
<span data-ttu-id="51b92-126">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="51b92-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51b92-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51b92-127">-DefaultProfile</span></span>
<span data-ttu-id="51b92-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="51b92-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51b92-129">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="51b92-129">-ExtensionResourceName</span></span>
<span data-ttu-id="51b92-130">Kaynak için bir uzantı kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="51b92-130">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="51b92-131">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın: sunucu adı `/` veritabanı adı</span><span class="sxs-lookup"><span data-stu-id="51b92-131">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="51b92-132">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="51b92-132">-ExtensionResourceType</span></span>
<span data-ttu-id="51b92-133">Bir uzantı kaynağı için kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="51b92-133">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="51b92-134">Örneğin, uzantı kaynağı bir veritabanıdır, aşağıdakileri belirtin: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="51b92-134">For instance, if the extension resource is a database specify the following: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="51b92-135">-Force</span><span class="sxs-lookup"><span data-stu-id="51b92-135">-Force</span></span>
<span data-ttu-id="51b92-136">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="51b92-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="51b92-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51b92-137">-InputObject</span></span>
<span data-ttu-id="51b92-138">Güncelleştirilecek kaynağın nesne gösterimi.</span><span class="sxs-lookup"><span data-stu-id="51b92-138">The object representation of the resource to update.</span></span>

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

### <span data-ttu-id="51b92-139">-Tür</span><span class="sxs-lookup"><span data-stu-id="51b92-139">-Kind</span></span>
<span data-ttu-id="51b92-140">Kaynağın kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="51b92-140">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="51b92-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="51b92-141">-ODataQuery</span></span>
<span data-ttu-id="51b92-142">Açık bir veri Protokolü (OData) stil filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="51b92-142">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="51b92-143">Bu cmdlet, bu değeri diğer tüm filtrelere ek olarak isteğe ekler.</span><span class="sxs-lookup"><span data-stu-id="51b92-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="51b92-144">-Plan</span><span class="sxs-lookup"><span data-stu-id="51b92-144">-Plan</span></span>
<span data-ttu-id="51b92-145">Kaynak için kaynak planı özelliklerini karma tablo olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="51b92-145">Specifies resource plan properties, as a hash table, for the resource.</span></span>

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

### <span data-ttu-id="51b92-146">-Pre-</span><span class="sxs-lookup"><span data-stu-id="51b92-146">-Pre</span></span>
<span data-ttu-id="51b92-147">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="51b92-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="51b92-148">-Özellikler</span><span class="sxs-lookup"><span data-stu-id="51b92-148">-Properties</span></span>
<span data-ttu-id="51b92-149">Kaynağın kaynak özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="51b92-149">Specifies resource properties for the resource.</span></span>

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

### <span data-ttu-id="51b92-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51b92-150">-ResourceGroupName</span></span>
<span data-ttu-id="51b92-151">Bu cmdlet 'in kaynağı değiştirdiği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="51b92-151">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="51b92-152">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="51b92-152">-ResourceId</span></span>
<span data-ttu-id="51b92-153">Aşağıdaki örnekte olduğu gibi, abonelik dahil olmak üzere tam nitelikli kaynak KIMLIĞINI belirtir: `/subscriptions/` ABONELIK kimliği`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="51b92-153">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="51b92-154">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="51b92-154">-ResourceName</span></span>
<span data-ttu-id="51b92-155">Kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="51b92-155">Specifies the name of the resource.</span></span>
<span data-ttu-id="51b92-156">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="51b92-156">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="51b92-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="51b92-157">-ResourceType</span></span>
<span data-ttu-id="51b92-158">Kaynağın türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="51b92-158">Specifies the type of the resource.</span></span>
<span data-ttu-id="51b92-159">Örneğin, veritabanı için kaynak türü aşağıdaki gibidir: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="51b92-159">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="51b92-160">-SKU</span><span class="sxs-lookup"><span data-stu-id="51b92-160">-Sku</span></span>
<span data-ttu-id="51b92-161">Kaynağın SKU nesnesini karma tablo olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="51b92-161">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="51b92-162">Etiketli</span><span class="sxs-lookup"><span data-stu-id="51b92-162">-Tag</span></span>
<span data-ttu-id="51b92-163">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="51b92-163">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="51b92-164">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="51b92-164">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="51b92-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="51b92-165">-TenantLevel</span></span>
<span data-ttu-id="51b92-166">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="51b92-166">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="51b92-167">-Usepatchsemantiği</span><span class="sxs-lookup"><span data-stu-id="51b92-167">-UsePatchSemantics</span></span>
<span data-ttu-id="51b92-168">Bu cmdlet 'in, HTTP yerıne nesneyi güncelleştirmek için bir HTTP düzeltme eki kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="51b92-168">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="51b92-169">-Onay</span><span class="sxs-lookup"><span data-stu-id="51b92-169">-Confirm</span></span>
<span data-ttu-id="51b92-170">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="51b92-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51b92-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51b92-171">-WhatIf</span></span>
<span data-ttu-id="51b92-172">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="51b92-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51b92-173">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="51b92-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51b92-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51b92-174">CommonParameters</span></span>
<span data-ttu-id="51b92-175">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="51b92-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51b92-176">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51b92-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51b92-177">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="51b92-177">INPUTS</span></span>

### <span data-ttu-id="51b92-178">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="51b92-178">None</span></span>

## <span data-ttu-id="51b92-179">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="51b92-179">OUTPUTS</span></span>

### <span data-ttu-id="51b92-180">Microsoft. Azure. Commands. ResourceManager. model. PSResource</span><span class="sxs-lookup"><span data-stu-id="51b92-180">Microsoft.Azure.Commands.ResourceManager.Models.PSResource</span></span>

## <span data-ttu-id="51b92-181">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="51b92-181">NOTES</span></span>

## <span data-ttu-id="51b92-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="51b92-182">RELATED LINKS</span></span>



[<span data-ttu-id="51b92-183">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="51b92-183">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="51b92-184">Taşı-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="51b92-184">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="51b92-185">Yeni-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="51b92-185">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="51b92-186">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="51b92-186">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)
