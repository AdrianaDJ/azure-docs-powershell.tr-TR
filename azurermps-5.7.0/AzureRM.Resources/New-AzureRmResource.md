---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
ms.openlocfilehash: c7a98f6fba2c690fb296c42f4f6eca902d7678bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588797"
---
# <span data-ttu-id="c5e70-101">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c5e70-101">New-AzureRmResource</span></span>

## <span data-ttu-id="c5e70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5e70-102">SYNOPSIS</span></span>
<span data-ttu-id="c5e70-103">Kaynak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c5e70-103">Creates a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5e70-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c5e70-104">SYNTAX</span></span>

### <span data-ttu-id="c5e70-105">Byresourceıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c5e70-105">ByResourceId (Default)</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5e70-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="c5e70-106">BySubscriptionLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5e70-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="c5e70-107">ByTenantLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c5e70-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c5e70-108">DESCRIPTION</span></span>
<span data-ttu-id="c5e70-109">**Yeni-AzureRmResource** cmdlet 'i, bir kaynak grubundaki Web sitesi, Azure SQL veritabanı sunucusu veya Azure SQL veritabanı gibi bir Azure kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c5e70-109">The **New-AzureRmResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="c5e70-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c5e70-110">EXAMPLES</span></span>

### <span data-ttu-id="c5e70-111">Örnek 1: kaynak oluşturma</span><span class="sxs-lookup"><span data-stu-id="c5e70-111">Example 1: Create a resource</span></span>
```
PS> New-AzureRmResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="c5e70-112">Bu komut, ResourceGroup11 'da Web sitesi olan bir kaynak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c5e70-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="c5e70-113">Örnek 2: splatın kullanarak kaynak oluşturma</span><span class="sxs-lookup"><span data-stu-id="c5e70-113">Example 2: Create a resource using splatting</span></span>
```
PS> $prop = @{
    Location          = "West US" 
    Properties        = @{test = "test"} 
    ResourceName      = "TestSite06" 
    ResourceType      = "microsoft.web/sites" 
    ResourceGroupName = "ResourceGroup11" 
    Force             = $true
}

PS> New-AzureRmResource @prop
```

<span data-ttu-id="c5e70-114">Bu komut, ResourceGroup11 'da Web sitesi olan bir kaynak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c5e70-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="c5e70-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c5e70-115">PARAMETERS</span></span>

### <span data-ttu-id="c5e70-116">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="c5e70-116">-ApiVersion</span></span>
<span data-ttu-id="c5e70-117">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5e70-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="c5e70-118">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="c5e70-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c5e70-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="c5e70-119">-AsJob</span></span>
<span data-ttu-id="c5e70-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c5e70-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c5e70-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5e70-121">-DefaultProfile</span></span>
<span data-ttu-id="c5e70-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c5e70-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5e70-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="c5e70-123">-ExtensionResourceName</span></span>
<span data-ttu-id="c5e70-124">Kaynak için bir uzantı kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5e70-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="c5e70-125">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="c5e70-125">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="c5e70-126">sunucu adı `/` veritabanı adı</span><span class="sxs-lookup"><span data-stu-id="c5e70-126">server name`/`database name</span></span>

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

### <span data-ttu-id="c5e70-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="c5e70-127">-ExtensionResourceType</span></span>
<span data-ttu-id="c5e70-128">Bir uzantı kaynağı için kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5e70-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="c5e70-129">Örneğin, uzantı kaynağı bir veritabanıdır, aşağıdaki türü belirtin:</span><span class="sxs-lookup"><span data-stu-id="c5e70-129">For instance, if the extension resource is a database, specify the following type:</span></span>

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

### <span data-ttu-id="c5e70-130">-Force</span><span class="sxs-lookup"><span data-stu-id="c5e70-130">-Force</span></span>
<span data-ttu-id="c5e70-131">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="c5e70-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c5e70-132">-Isfullobject</span><span class="sxs-lookup"><span data-stu-id="c5e70-132">-IsFullObject</span></span>
<span data-ttu-id="c5e70-133">*Özellikler* parametresinin belirttiği nesnenin tam nesne olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="c5e70-133">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="c5e70-134">-Tür</span><span class="sxs-lookup"><span data-stu-id="c5e70-134">-Kind</span></span>
<span data-ttu-id="c5e70-135">Kaynağın kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5e70-135">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="c5e70-136">-Konum</span><span class="sxs-lookup"><span data-stu-id="c5e70-136">-Location</span></span>
<span data-ttu-id="c5e70-137">Kaynağın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5e70-137">Specifies the location of the resource.</span></span>
<span data-ttu-id="c5e70-138">Orta ABD veya Güneydoğu Asya gibi veri merkezi konumunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="c5e70-138">Specify data center location, such as Central US or Southeast Asia.</span></span>

<span data-ttu-id="c5e70-139">Kaynağı, bu türdeki kaynakları destekleyen herhangi bir konuma yerleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c5e70-139">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="c5e70-140">Kaynak gruplarında farklı konumlardaki kaynaklar bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="c5e70-140">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="c5e70-141">Hangi konumların her kaynak türünü desteklerini belirlemek için Get-AzureLocation cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c5e70-141">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

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

### <span data-ttu-id="c5e70-142">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="c5e70-142">-ODataQuery</span></span>
<span data-ttu-id="c5e70-143">Açık bir veri Protokolü (OData) stil filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5e70-143">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="c5e70-144">Bu cmdlet, bu değeri diğer tüm filtrelere ek olarak isteğe ekler.</span><span class="sxs-lookup"><span data-stu-id="c5e70-144">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="c5e70-145">-Plan</span><span class="sxs-lookup"><span data-stu-id="c5e70-145">-Plan</span></span>
<span data-ttu-id="c5e70-146">Kaynak planı özelliklerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="c5e70-146">A hash table that represents resource plan properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e70-147">-Pre-</span><span class="sxs-lookup"><span data-stu-id="c5e70-147">-Pre</span></span>
<span data-ttu-id="c5e70-148">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c5e70-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c5e70-149">-Özellikler</span><span class="sxs-lookup"><span data-stu-id="c5e70-149">-Properties</span></span>
<span data-ttu-id="c5e70-150">Kaynağın kaynak özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5e70-150">Specifies resource properties for the resource.</span></span> <span data-ttu-id="c5e70-151">Bir kaynak türüne özgü özelliklerin değerlerini belirtmek için bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="c5e70-151">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e70-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5e70-152">-ResourceGroupName</span></span>
<span data-ttu-id="c5e70-153">Bu cmdlet 'in kaynağı oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5e70-153">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="c5e70-154">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c5e70-154">-ResourceId</span></span>
<span data-ttu-id="c5e70-155">Aşağıdaki örnekte olduğu gibi, abonelik dahil olmak üzere tam nitelikli kaynak KIMLIĞINI belirtir:</span><span class="sxs-lookup"><span data-stu-id="c5e70-155">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="c5e70-156">`/subscriptions/`abonelik KIMLIĞI`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="c5e70-156">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="c5e70-157">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c5e70-157">-ResourceName</span></span>
<span data-ttu-id="c5e70-158">Kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5e70-158">Specifies the name of the resource.</span></span> <span data-ttu-id="c5e70-159">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="c5e70-159">For instance, to specify a database, use the following format:</span></span>

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

### <span data-ttu-id="c5e70-160">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c5e70-160">-ResourceType</span></span>
<span data-ttu-id="c5e70-161">Kaynağın türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5e70-161">Specifies the type of the resource.</span></span>
<span data-ttu-id="c5e70-162">Örneğin, veritabanı için kaynak türü aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="c5e70-162">For instance, for a database, the resource type is as follows:</span></span>

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

### <span data-ttu-id="c5e70-163">-SKU</span><span class="sxs-lookup"><span data-stu-id="c5e70-163">-Sku</span></span>
<span data-ttu-id="c5e70-164">SKU özelliklerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="c5e70-164">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="c5e70-165">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c5e70-165">-Tag</span></span>
<span data-ttu-id="c5e70-166">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="c5e70-166">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c5e70-167">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="c5e70-167">For example:</span></span>

<span data-ttu-id="c5e70-168">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="c5e70-168">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e70-169">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="c5e70-169">-TenantLevel</span></span>
<span data-ttu-id="c5e70-170">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="c5e70-170">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="c5e70-171">-Onay</span><span class="sxs-lookup"><span data-stu-id="c5e70-171">-Confirm</span></span>
<span data-ttu-id="c5e70-172">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c5e70-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5e70-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5e70-173">-WhatIf</span></span>
<span data-ttu-id="c5e70-174">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c5e70-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5e70-175">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c5e70-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5e70-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5e70-176">CommonParameters</span></span>
<span data-ttu-id="c5e70-177">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c5e70-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5e70-178">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5e70-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5e70-179">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c5e70-179">INPUTS</span></span>

### <span data-ttu-id="c5e70-180">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c5e70-180">None</span></span>
<span data-ttu-id="c5e70-181">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="c5e70-181">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c5e70-182">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c5e70-182">OUTPUTS</span></span>

### <span data-ttu-id="c5e70-183">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c5e70-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c5e70-184">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c5e70-184">NOTES</span></span>

## <span data-ttu-id="c5e70-185">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c5e70-185">RELATED LINKS</span></span>

[<span data-ttu-id="c5e70-186">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c5e70-186">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="c5e70-187">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c5e70-187">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="c5e70-188">Taşı-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c5e70-188">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="c5e70-189">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c5e70-189">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="c5e70-190">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c5e70-190">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
