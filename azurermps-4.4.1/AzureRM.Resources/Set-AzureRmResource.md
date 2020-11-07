---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
ms.openlocfilehash: d3e7a1e947eb03c52c2cd8e032a359eb7765be03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764234"
---
# <span data-ttu-id="0411f-101">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0411f-101">Set-AzureRmResource</span></span>

## <span data-ttu-id="0411f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0411f-102">SYNOPSIS</span></span>
<span data-ttu-id="0411f-103">Bir kaynağı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0411f-103">Modifies a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0411f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0411f-104">SYNTAX</span></span>

### <span data-ttu-id="0411f-105">Kaynak kimliği. (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0411f-105">The resource Id. (Default)</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0411f-106">Abonelik düzeyinde bulunan kaynaktır.</span><span class="sxs-lookup"><span data-stu-id="0411f-106">Resource that resides at the subscription level.</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0411f-107">Kiracı düzeyinde bulunan kaynaktır.</span><span class="sxs-lookup"><span data-stu-id="0411f-107">Resource that resides at the tenant level.</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0411f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0411f-108">DESCRIPTION</span></span>
<span data-ttu-id="0411f-109">**Set-AzureRmResource** cmdlet 'i, mevcut bir Azure kaynağını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0411f-109">The **Set-AzureRmResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="0411f-110">Ada göre değiştirmek ve KIMLIK yazmak için kaynak belirtin.</span><span class="sxs-lookup"><span data-stu-id="0411f-110">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="0411f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0411f-111">EXAMPLES</span></span>

### <span data-ttu-id="0411f-112">Örnek 1: kaynağı değiştirme</span><span class="sxs-lookup"><span data-stu-id="0411f-112">Example 1: Modify a resource</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoSite"
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzureRmResource -Force
```

<span data-ttu-id="0411f-113">İlk komut, Get-AzureRmResource cmdlet 'ini kullanarak ContosoSite adlı kaynağı alır ve $Resource değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0411f-113">The first command gets the resource named ContosoSite by using the Get-AzureRmResource cmdlet, and then stores it in the $Resource variable.</span></span>

<span data-ttu-id="0411f-114">İkinci komut $Resource özelliğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0411f-114">The second command modifies a property of $Resource.</span></span>

<span data-ttu-id="0411f-115">Son komutu $Resource eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0411f-115">The final command updates the resource to match $Resource.</span></span>

## <span data-ttu-id="0411f-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0411f-116">PARAMETERS</span></span>

### <span data-ttu-id="0411f-117">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="0411f-117">-ApiVersion</span></span>
<span data-ttu-id="0411f-118">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0411f-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0411f-119">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="0411f-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0411f-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="0411f-120">-ExtensionResourceName</span></span>
<span data-ttu-id="0411f-121">Kaynak için bir uzantı kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0411f-121">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="0411f-122">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="0411f-122">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="0411f-123">sunucu adı `/` veritabanı adı</span><span class="sxs-lookup"><span data-stu-id="0411f-123">server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0411f-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="0411f-124">-ExtensionResourceType</span></span>
<span data-ttu-id="0411f-125">Bir uzantı kaynağı için kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0411f-125">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="0411f-126">Örneğin, uzantı kaynağı bir veritabanıdır, aşağıdakileri belirtin:</span><span class="sxs-lookup"><span data-stu-id="0411f-126">For instance, if the extension resource is a database specify the following:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0411f-127">-Force</span><span class="sxs-lookup"><span data-stu-id="0411f-127">-Force</span></span>
<span data-ttu-id="0411f-128">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="0411f-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0411f-129">-Tür</span><span class="sxs-lookup"><span data-stu-id="0411f-129">-Kind</span></span>
<span data-ttu-id="0411f-130">Kaynağın kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0411f-130">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="0411f-131">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="0411f-131">-ODataQuery</span></span>
<span data-ttu-id="0411f-132">Açık bir veri Protokolü (OData) stil filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="0411f-132">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="0411f-133">Bu cmdlet, bu değeri diğer tüm filtrelere ek olarak isteğe ekler.</span><span class="sxs-lookup"><span data-stu-id="0411f-133">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="0411f-134">-Plan</span><span class="sxs-lookup"><span data-stu-id="0411f-134">-Plan</span></span>
<span data-ttu-id="0411f-135">Kaynak için kaynak planı özelliklerini karma tablo olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="0411f-135">Specifies resource plan properties, as a hash table, for the resource.</span></span>

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

### <span data-ttu-id="0411f-136">-Pre-</span><span class="sxs-lookup"><span data-stu-id="0411f-136">-Pre</span></span>
<span data-ttu-id="0411f-137">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0411f-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0411f-138">-Özellikler</span><span class="sxs-lookup"><span data-stu-id="0411f-138">-Properties</span></span>
<span data-ttu-id="0411f-139">Kaynağın kaynak özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0411f-139">Specifies resource properties for the resource.</span></span>

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

### <span data-ttu-id="0411f-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0411f-140">-ResourceGroupName</span></span>
<span data-ttu-id="0411f-141">Bu cmdlet 'in kaynağı değiştirdiği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0411f-141">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0411f-142">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0411f-142">-ResourceId</span></span>
<span data-ttu-id="0411f-143">Aşağıdaki örnekte olduğu gibi, abonelik dahil olmak üzere tam nitelikli kaynak KIMLIĞINI belirtir:</span><span class="sxs-lookup"><span data-stu-id="0411f-143">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="0411f-144">`/subscriptions/`abonelik KIMLIĞI`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="0411f-144">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: The resource Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0411f-145">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0411f-145">-ResourceName</span></span>
<span data-ttu-id="0411f-146">Kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0411f-146">Specifies the name of the resource.</span></span>
<span data-ttu-id="0411f-147">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="0411f-147">For instance, to specify a database, use the following format:</span></span>

`ContosoServer/ContosoDatabase`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0411f-148">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0411f-148">-ResourceType</span></span>
<span data-ttu-id="0411f-149">Kaynağın türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0411f-149">Specifies the type of the resource.</span></span>
<span data-ttu-id="0411f-150">Örneğin, veritabanı için kaynak türü aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="0411f-150">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0411f-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="0411f-151">-Sku</span></span>
<span data-ttu-id="0411f-152">Kaynağın SKU nesnesini karma tablo olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="0411f-152">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="0411f-153">Etiketli</span><span class="sxs-lookup"><span data-stu-id="0411f-153">-Tag</span></span>
<span data-ttu-id="0411f-154">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="0411f-154">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0411f-155">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="0411f-155">For example:</span></span>

<span data-ttu-id="0411f-156">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="0411f-156">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0411f-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="0411f-157">-TenantLevel</span></span>
<span data-ttu-id="0411f-158">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="0411f-158">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0411f-159">-Usepatchsemantiği</span><span class="sxs-lookup"><span data-stu-id="0411f-159">-UsePatchSemantics</span></span>
<span data-ttu-id="0411f-160">Bu cmdlet 'in, HTTP yerıne nesneyi güncelleştirmek için bir HTTP düzeltme eki kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0411f-160">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="0411f-161">-Onay</span><span class="sxs-lookup"><span data-stu-id="0411f-161">-Confirm</span></span>
<span data-ttu-id="0411f-162">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0411f-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0411f-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0411f-163">-WhatIf</span></span>
<span data-ttu-id="0411f-164">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0411f-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0411f-165">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0411f-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0411f-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0411f-166">-DefaultProfile</span></span>
<span data-ttu-id="0411f-167">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0411f-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0411f-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0411f-168">CommonParameters</span></span>
<span data-ttu-id="0411f-169">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0411f-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0411f-170">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0411f-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0411f-171">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0411f-171">INPUTS</span></span>

## <span data-ttu-id="0411f-172">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0411f-172">OUTPUTS</span></span>

### <span data-ttu-id="0411f-173">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="0411f-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0411f-174">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0411f-174">NOTES</span></span>

## <span data-ttu-id="0411f-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0411f-175">RELATED LINKS</span></span>

[<span data-ttu-id="0411f-176">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0411f-176">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="0411f-177">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0411f-177">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="0411f-178">Taşı-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0411f-178">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="0411f-179">Yeni-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0411f-179">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="0411f-180">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0411f-180">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)
