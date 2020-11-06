---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
ms.openlocfilehash: eb75c1afc0b0fa82c0fee6b734ded951fdfa519f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593019"
---
# <span data-ttu-id="b4bf4-101">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b4bf4-101">New-AzureRmResource</span></span>

## <span data-ttu-id="b4bf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="b4bf4-103">Kaynak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-103">Creates a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4bf4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4bf4-104">SYNTAX</span></span>

### <span data-ttu-id="b4bf4-105">Kaynak kimliği. (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b4bf4-105">The resource Id. (Default)</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4bf4-106">Abonelik düzeyinde bulunan kaynaktır.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-106">Resource that resides at the subscription level.</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4bf4-107">Kiracı düzeyinde bulunan kaynaktır.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-107">Resource that resides at the tenant level.</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4bf4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4bf4-108">DESCRIPTION</span></span>
<span data-ttu-id="b4bf4-109">**Yeni-AzureRmResource** cmdlet 'i, bir kaynak grubundaki Web sitesi, Azure SQL veritabanı sunucusu veya Azure SQL veritabanı gibi bir Azure kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-109">The **New-AzureRmResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="b4bf4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4bf4-110">EXAMPLES</span></span>

### <span data-ttu-id="b4bf4-111">Örnek 1: kaynak oluşturma</span><span class="sxs-lookup"><span data-stu-id="b4bf4-111">Example 1: Create a resource</span></span>
```
PS C:\>New-AzureRmResource -Location "West US" -Properties @{"test"="test"} -ResourceName "TestSite06" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -Force
```

<span data-ttu-id="b4bf4-112">Bu komut, ResourceGroup11 'da Web sitesi olan bir kaynak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="b4bf4-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4bf4-113">PARAMETERS</span></span>

### <span data-ttu-id="b4bf4-114">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="b4bf4-114">-ApiVersion</span></span>
<span data-ttu-id="b4bf4-115">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-115">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="b4bf4-116">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b4bf4-117">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="b4bf4-117">-ExtensionResourceName</span></span>
<span data-ttu-id="b4bf4-118">Kaynak için bir uzantı kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-118">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="b4bf4-119">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="b4bf4-119">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="b4bf4-120">sunucu adı `/` veritabanı adı</span><span class="sxs-lookup"><span data-stu-id="b4bf4-120">server name`/`database name</span></span>

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

### <span data-ttu-id="b4bf4-121">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="b4bf4-121">-ExtensionResourceType</span></span>
<span data-ttu-id="b4bf4-122">Bir uzantı kaynağı için kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-122">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="b4bf4-123">Örneğin, uzantı kaynağı bir veritabanıdır, aşağıdaki türü belirtin:</span><span class="sxs-lookup"><span data-stu-id="b4bf4-123">For instance, if the extension resource is a database, specify the following type:</span></span>

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

### <span data-ttu-id="b4bf4-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b4bf4-124">-Force</span></span>
<span data-ttu-id="b4bf4-125">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b4bf4-126">-Isfullobject</span><span class="sxs-lookup"><span data-stu-id="b4bf4-126">-IsFullObject</span></span>
<span data-ttu-id="b4bf4-127">*Özellikler* parametresinin belirttiği nesnenin tam nesne olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-127">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="b4bf4-128">-Tür</span><span class="sxs-lookup"><span data-stu-id="b4bf4-128">-Kind</span></span>
<span data-ttu-id="b4bf4-129">Kaynağın kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-129">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="b4bf4-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="b4bf4-130">-Location</span></span>
<span data-ttu-id="b4bf4-131">Kaynağın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-131">Specifies the location of the resource.</span></span>
<span data-ttu-id="b4bf4-132">Orta ABD veya Güneydoğu Asya gibi veri merkezi konumunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-132">Specify data center location, such as Central US or Southeast Asia.</span></span>

<span data-ttu-id="b4bf4-133">Kaynağı, bu türdeki kaynakları destekleyen herhangi bir konuma yerleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-133">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="b4bf4-134">Kaynak gruplarında farklı konumlardaki kaynaklar bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-134">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="b4bf4-135">Hangi konumların her kaynak türünü desteklerini belirlemek için Get-AzureLocation cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-135">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

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

### <span data-ttu-id="b4bf4-136">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="b4bf4-136">-ODataQuery</span></span>
<span data-ttu-id="b4bf4-137">Açık bir veri Protokolü (OData) stil filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-137">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="b4bf4-138">Bu cmdlet, bu değeri diğer tüm filtrelere ek olarak isteğe ekler.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-138">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="b4bf4-139">-Plan</span><span class="sxs-lookup"><span data-stu-id="b4bf4-139">-Plan</span></span>
<span data-ttu-id="b4bf4-140">Kaynak planı özelliklerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-140">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="b4bf4-141">-Pre-</span><span class="sxs-lookup"><span data-stu-id="b4bf4-141">-Pre</span></span>
<span data-ttu-id="b4bf4-142">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b4bf4-143">-Özellikler</span><span class="sxs-lookup"><span data-stu-id="b4bf4-143">-Properties</span></span>
<span data-ttu-id="b4bf4-144">Kaynağın kaynak özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-144">Specifies resource properties for the resource.</span></span> <span data-ttu-id="b4bf4-145">Bir kaynak türüne özgü özelliklerin değerlerini belirtmek için bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-145">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bf4-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4bf4-146">-ResourceGroupName</span></span>
<span data-ttu-id="b4bf4-147">Bu cmdlet 'in kaynağı oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-147">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="b4bf4-148">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b4bf4-148">-ResourceId</span></span>
<span data-ttu-id="b4bf4-149">Aşağıdaki örnekte olduğu gibi, abonelik dahil olmak üzere tam nitelikli kaynak KIMLIĞINI belirtir:</span><span class="sxs-lookup"><span data-stu-id="b4bf4-149">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="b4bf4-150">`/subscriptions/`abonelik KIMLIĞI`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="b4bf4-150">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="b4bf4-151">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b4bf4-151">-ResourceName</span></span>
<span data-ttu-id="b4bf4-152">Kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-152">Specifies the name of the resource.</span></span> <span data-ttu-id="b4bf4-153">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="b4bf4-153">For instance, to specify a database, use the following format:</span></span>

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

### <span data-ttu-id="b4bf4-154">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b4bf4-154">-ResourceType</span></span>
<span data-ttu-id="b4bf4-155">Kaynağın türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-155">Specifies the type of the resource.</span></span>
<span data-ttu-id="b4bf4-156">Örneğin, veritabanı için kaynak türü aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="b4bf4-156">For instance, for a database, the resource type is as follows:</span></span>

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

### <span data-ttu-id="b4bf4-157">-SKU</span><span class="sxs-lookup"><span data-stu-id="b4bf4-157">-Sku</span></span>
<span data-ttu-id="b4bf4-158">SKU özelliklerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-158">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="b4bf4-159">Etiketli</span><span class="sxs-lookup"><span data-stu-id="b4bf4-159">-Tag</span></span>
<span data-ttu-id="b4bf4-160">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-160">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b4bf4-161">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="b4bf4-161">For example:</span></span>

<span data-ttu-id="b4bf4-162">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="b4bf4-162">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bf4-163">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="b4bf4-163">-TenantLevel</span></span>
<span data-ttu-id="b4bf4-164">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-164">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="b4bf4-165">-Onay</span><span class="sxs-lookup"><span data-stu-id="b4bf4-165">-Confirm</span></span>
<span data-ttu-id="b4bf4-166">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4bf4-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4bf4-167">-WhatIf</span></span>
<span data-ttu-id="b4bf4-168">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4bf4-169">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4bf4-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4bf4-170">-DefaultProfile</span></span>
<span data-ttu-id="b4bf4-171">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4bf4-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4bf4-172">CommonParameters</span></span>
<span data-ttu-id="b4bf4-173">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4bf4-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4bf4-174">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4bf4-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4bf4-175">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4bf4-175">INPUTS</span></span>

## <span data-ttu-id="b4bf4-176">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4bf4-176">OUTPUTS</span></span>

### <span data-ttu-id="b4bf4-177">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="b4bf4-177">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b4bf4-178">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4bf4-178">NOTES</span></span>

## <span data-ttu-id="b4bf4-179">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4bf4-179">RELATED LINKS</span></span>

[<span data-ttu-id="b4bf4-180">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b4bf4-180">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="b4bf4-181">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b4bf4-181">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="b4bf4-182">Taşı-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b4bf4-182">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="b4bf4-183">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b4bf4-183">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="b4bf4-184">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b4bf4-184">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
