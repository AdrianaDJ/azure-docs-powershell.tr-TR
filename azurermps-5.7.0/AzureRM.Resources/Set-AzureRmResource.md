---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
ms.openlocfilehash: 9b1f12060ca7cc161f4f7fbe7c99948d9ddd10f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764000"
---
# <span data-ttu-id="3d6fb-101">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="3d6fb-101">Set-AzureRmResource</span></span>

## <span data-ttu-id="3d6fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d6fb-102">SYNOPSIS</span></span>
<span data-ttu-id="3d6fb-103">Bir kaynağı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-103">Modifies a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d6fb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3d6fb-104">SYNTAX</span></span>

### <span data-ttu-id="3d6fb-105">Byresourceıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3d6fb-105">ByResourceId (Default)</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d6fb-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="3d6fb-106">BySubscriptionLevel</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d6fb-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="3d6fb-107">ByTenantLevel</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d6fb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d6fb-108">DESCRIPTION</span></span>
<span data-ttu-id="3d6fb-109">**Set-AzureRmResource** cmdlet 'i, mevcut bir Azure kaynağını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-109">The **Set-AzureRmResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="3d6fb-110">Ada göre değiştirmek ve KIMLIK yazmak için kaynak belirtin.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-110">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="3d6fb-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3d6fb-111">EXAMPLES</span></span>

### <span data-ttu-id="3d6fb-112">Örnek 1: kaynağı değiştirme</span><span class="sxs-lookup"><span data-stu-id="3d6fb-112">Example 1: Modify a resource</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoSite"
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzureRmResource -Force
```

<span data-ttu-id="3d6fb-113">İlk komut, Get-AzureRmResource cmdlet 'ini kullanarak ContosoSite adlı kaynağı alır ve $Resource değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-113">The first command gets the resource named ContosoSite by using the Get-AzureRmResource cmdlet, and then stores it in the $Resource variable.</span></span>

<span data-ttu-id="3d6fb-114">İkinci komut $Resource özelliğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-114">The second command modifies a property of $Resource.</span></span>

<span data-ttu-id="3d6fb-115">Son komutu $Resource eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-115">The final command updates the resource to match $Resource.</span></span>

## <span data-ttu-id="3d6fb-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3d6fb-116">PARAMETERS</span></span>

### <span data-ttu-id="3d6fb-117">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="3d6fb-117">-ApiVersion</span></span>
<span data-ttu-id="3d6fb-118">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="3d6fb-119">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6fb-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="3d6fb-120">-AsJob</span></span>
<span data-ttu-id="3d6fb-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3d6fb-121">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6fb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d6fb-122">-DefaultProfile</span></span>
<span data-ttu-id="3d6fb-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3d6fb-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6fb-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="3d6fb-124">-ExtensionResourceName</span></span>
<span data-ttu-id="3d6fb-125">Kaynak için bir uzantı kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-125">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="3d6fb-126">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="3d6fb-126">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="3d6fb-127">sunucu adı `/` veritabanı adı</span><span class="sxs-lookup"><span data-stu-id="3d6fb-127">server name`/`database name</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6fb-128">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="3d6fb-128">-ExtensionResourceType</span></span>
<span data-ttu-id="3d6fb-129">Bir uzantı kaynağı için kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-129">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="3d6fb-130">Örneğin, uzantı kaynağı bir veritabanıdır, aşağıdakileri belirtin:</span><span class="sxs-lookup"><span data-stu-id="3d6fb-130">For instance, if the extension resource is a database specify the following:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6fb-131">-Force</span><span class="sxs-lookup"><span data-stu-id="3d6fb-131">-Force</span></span>
<span data-ttu-id="3d6fb-132">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-132">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6fb-133">-Tür</span><span class="sxs-lookup"><span data-stu-id="3d6fb-133">-Kind</span></span>
<span data-ttu-id="3d6fb-134">Kaynağın kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-134">Specifies the resource kind for the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6fb-135">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="3d6fb-135">-ODataQuery</span></span>
<span data-ttu-id="3d6fb-136">Açık bir veri Protokolü (OData) stil filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-136">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="3d6fb-137">Bu cmdlet, bu değeri diğer tüm filtrelere ek olarak isteğe ekler.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-137">This cmdlet appends this value to the request in addition to any other filters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6fb-138">-Plan</span><span class="sxs-lookup"><span data-stu-id="3d6fb-138">-Plan</span></span>
<span data-ttu-id="3d6fb-139">Kaynak için kaynak planı özelliklerini karma tablo olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-139">Specifies resource plan properties, as a hash table, for the resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6fb-140">-Pre-</span><span class="sxs-lookup"><span data-stu-id="3d6fb-140">-Pre</span></span>
<span data-ttu-id="3d6fb-141">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6fb-142">-Özellikler</span><span class="sxs-lookup"><span data-stu-id="3d6fb-142">-Properties</span></span>
<span data-ttu-id="3d6fb-143">Kaynağın kaynak özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-143">Specifies resource properties for the resource.</span></span>

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6fb-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d6fb-144">-ResourceGroupName</span></span>
<span data-ttu-id="3d6fb-145">Bu cmdlet 'in kaynağı değiştirdiği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-145">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6fb-146">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3d6fb-146">-ResourceId</span></span>
<span data-ttu-id="3d6fb-147">Aşağıdaki örnekte olduğu gibi, abonelik dahil olmak üzere tam nitelikli kaynak KIMLIĞINI belirtir:</span><span class="sxs-lookup"><span data-stu-id="3d6fb-147">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="3d6fb-148">`/subscriptions/`abonelik KIMLIĞI`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="3d6fb-148">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6fb-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="3d6fb-149">-ResourceName</span></span>
<span data-ttu-id="3d6fb-150">Kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-150">Specifies the name of the resource.</span></span>
<span data-ttu-id="3d6fb-151">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="3d6fb-151">For instance, to specify a database, use the following format:</span></span>

`ContosoServer/ContosoDatabase`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6fb-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="3d6fb-152">-ResourceType</span></span>
<span data-ttu-id="3d6fb-153">Kaynağın türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-153">Specifies the type of the resource.</span></span>
<span data-ttu-id="3d6fb-154">Örneğin, veritabanı için kaynak türü aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="3d6fb-154">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6fb-155">-SKU</span><span class="sxs-lookup"><span data-stu-id="3d6fb-155">-Sku</span></span>
<span data-ttu-id="3d6fb-156">Kaynağın SKU nesnesini karma tablo olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-156">Specifies the SKU object of the resource as a hash table.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6fb-157">Etiketli</span><span class="sxs-lookup"><span data-stu-id="3d6fb-157">-Tag</span></span>
<span data-ttu-id="3d6fb-158">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3d6fb-159">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="3d6fb-159">For example:</span></span>

<span data-ttu-id="3d6fb-160">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="3d6fb-160">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6fb-161">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="3d6fb-161">-TenantLevel</span></span>
<span data-ttu-id="3d6fb-162">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-162">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6fb-163">-Usepatchsemantiği</span><span class="sxs-lookup"><span data-stu-id="3d6fb-163">-UsePatchSemantics</span></span>
<span data-ttu-id="3d6fb-164">Bu cmdlet 'in, HTTP yerıne nesneyi güncelleştirmek için bir HTTP düzeltme eki kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-164">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6fb-165">-Onay</span><span class="sxs-lookup"><span data-stu-id="3d6fb-165">-Confirm</span></span>
<span data-ttu-id="3d6fb-166">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-166">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6fb-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d6fb-167">-WhatIf</span></span>
<span data-ttu-id="3d6fb-168">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d6fb-169">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-169">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6fb-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d6fb-170">CommonParameters</span></span>
<span data-ttu-id="3d6fb-171">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d6fb-172">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d6fb-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d6fb-173">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3d6fb-173">INPUTS</span></span>

### <span data-ttu-id="3d6fb-174">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3d6fb-174">None</span></span>
<span data-ttu-id="3d6fb-175">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="3d6fb-175">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3d6fb-176">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3d6fb-176">OUTPUTS</span></span>

### <span data-ttu-id="3d6fb-177">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="3d6fb-177">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="3d6fb-178">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3d6fb-178">NOTES</span></span>

## <span data-ttu-id="3d6fb-179">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3d6fb-179">RELATED LINKS</span></span>

[<span data-ttu-id="3d6fb-180">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="3d6fb-180">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="3d6fb-181">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="3d6fb-181">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="3d6fb-182">Taşı-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="3d6fb-182">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="3d6fb-183">Yeni-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="3d6fb-183">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="3d6fb-184">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="3d6fb-184">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)
