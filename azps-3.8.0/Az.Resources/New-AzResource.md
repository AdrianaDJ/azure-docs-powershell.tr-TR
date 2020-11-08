---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
ms.openlocfilehash: 37561ecc57f5b729a33b2011c26a297bcb2bf52b
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107419"
---
# <span data-ttu-id="aeac3-101">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="aeac3-101">New-AzResource</span></span>

## <span data-ttu-id="aeac3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aeac3-102">SYNOPSIS</span></span>
<span data-ttu-id="aeac3-103">Kaynak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aeac3-103">Creates a resource.</span></span>

## <span data-ttu-id="aeac3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aeac3-104">SYNTAX</span></span>

### <span data-ttu-id="aeac3-105">Byresourceıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="aeac3-105">ByResourceId (Default)</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aeac3-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="aeac3-106">BySubscriptionLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aeac3-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="aeac3-107">ByTenantLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aeac3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="aeac3-108">DESCRIPTION</span></span>
<span data-ttu-id="aeac3-109">**New-AzResource** cmdlet 'i, bir kaynak grubundaki Web sitesi, Azure SQL veritabanı sunucusu veya Azure SQL veritabanı gibi bir Azure kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aeac3-109">The **New-AzResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="aeac3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aeac3-110">EXAMPLES</span></span>

### <span data-ttu-id="aeac3-111">Örnek 1: kaynak oluşturma</span><span class="sxs-lookup"><span data-stu-id="aeac3-111">Example 1: Create a resource</span></span>
```
PS> New-AzResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="aeac3-112">Bu komut, ResourceGroup11 'da Web sitesi olan bir kaynak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aeac3-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="aeac3-113">Örnek 2: splatın kullanarak kaynak oluşturma</span><span class="sxs-lookup"><span data-stu-id="aeac3-113">Example 2: Create a resource using splatting</span></span>
```
PS> $prop = @{
    Location          = "West US"
    Properties        = @{test = "test"}
    ResourceName      = "TestSite06"
    ResourceType      = "microsoft.web/sites"
    ResourceGroupName = "ResourceGroup11"
    Force             = $true
}

PS> New-AzResource @prop
```

<span data-ttu-id="aeac3-114">Bu komut, ResourceGroup11 'da Web sitesi olan bir kaynak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aeac3-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="aeac3-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aeac3-115">PARAMETERS</span></span>

### <span data-ttu-id="aeac3-116">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="aeac3-116">-ApiVersion</span></span>
<span data-ttu-id="aeac3-117">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeac3-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="aeac3-118">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="aeac3-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="aeac3-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="aeac3-119">-AsJob</span></span>
<span data-ttu-id="aeac3-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="aeac3-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aeac3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeac3-121">-DefaultProfile</span></span>
<span data-ttu-id="aeac3-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="aeac3-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aeac3-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="aeac3-123">-ExtensionResourceName</span></span>
<span data-ttu-id="aeac3-124">Kaynak için bir uzantı kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeac3-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="aeac3-125">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın: sunucu adı `/` veritabanı adı</span><span class="sxs-lookup"><span data-stu-id="aeac3-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="aeac3-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="aeac3-126">-ExtensionResourceType</span></span>
<span data-ttu-id="aeac3-127">Bir uzantı kaynağı için kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeac3-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="aeac3-128">Örneğin, uzantı kaynağı bir veritabanıdır, aşağıdaki türü belirtin: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="aeac3-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="aeac3-129">-Force</span><span class="sxs-lookup"><span data-stu-id="aeac3-129">-Force</span></span>
<span data-ttu-id="aeac3-130">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="aeac3-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aeac3-131">-Isfullobject</span><span class="sxs-lookup"><span data-stu-id="aeac3-131">-IsFullObject</span></span>
<span data-ttu-id="aeac3-132">*Özellikler* parametresinin belirttiği nesnenin tam nesne olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="aeac3-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="aeac3-133">-Tür</span><span class="sxs-lookup"><span data-stu-id="aeac3-133">-Kind</span></span>
<span data-ttu-id="aeac3-134">Kaynağın kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeac3-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="aeac3-135">-Konum</span><span class="sxs-lookup"><span data-stu-id="aeac3-135">-Location</span></span>
<span data-ttu-id="aeac3-136">Kaynağın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeac3-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="aeac3-137">Orta ABD veya Güneydoğu Asya gibi veri merkezi konumunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="aeac3-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="aeac3-138">Kaynağı, bu türdeki kaynakları destekleyen herhangi bir konuma yerleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aeac3-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="aeac3-139">Kaynak gruplarında farklı konumlardaki kaynaklar bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="aeac3-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="aeac3-140">Hangi konumların her kaynak türünü desteklerini belirlemek için Get-AzLocation cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="aeac3-140">To determine which locations support each resource type, use the Get-AzLocation cmdlet.</span></span>

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

### <span data-ttu-id="aeac3-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="aeac3-141">-ODataQuery</span></span>
<span data-ttu-id="aeac3-142">Açık bir veri Protokolü (OData) stil filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeac3-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="aeac3-143">Bu cmdlet, bu değeri diğer tüm filtrelere ek olarak isteğe ekler.</span><span class="sxs-lookup"><span data-stu-id="aeac3-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="aeac3-144">-Plan</span><span class="sxs-lookup"><span data-stu-id="aeac3-144">-Plan</span></span>
<span data-ttu-id="aeac3-145">Kaynak planı özelliklerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="aeac3-145">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="aeac3-146">-Pre-</span><span class="sxs-lookup"><span data-stu-id="aeac3-146">-Pre</span></span>
<span data-ttu-id="aeac3-147">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="aeac3-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="aeac3-148">-Özellikler</span><span class="sxs-lookup"><span data-stu-id="aeac3-148">-Properties</span></span>
<span data-ttu-id="aeac3-149">Kaynağın kaynak özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeac3-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="aeac3-150">Bir kaynak türüne özgü özelliklerin değerlerini belirtmek için bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="aeac3-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="aeac3-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aeac3-151">-ResourceGroupName</span></span>
<span data-ttu-id="aeac3-152">Bu cmdlet 'in kaynağı oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeac3-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="aeac3-153">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="aeac3-153">-ResourceId</span></span>
<span data-ttu-id="aeac3-154">Aşağıdaki örnekte olduğu gibi, abonelik dahil olmak üzere tam nitelikli kaynak KIMLIĞINI belirtir: `/subscriptions/` ABONELIK kimliği`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="aeac3-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="aeac3-155">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="aeac3-155">-ResourceName</span></span>
<span data-ttu-id="aeac3-156">Kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeac3-156">Specifies the name of the resource.</span></span> <span data-ttu-id="aeac3-157">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="aeac3-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="aeac3-158">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="aeac3-158">-ResourceType</span></span>
<span data-ttu-id="aeac3-159">Kaynağın türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeac3-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="aeac3-160">Örneğin, veritabanı için kaynak türü aşağıdaki gibidir: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="aeac3-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="aeac3-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="aeac3-161">-Sku</span></span>
<span data-ttu-id="aeac3-162">SKU özelliklerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="aeac3-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="aeac3-163">Etiketli</span><span class="sxs-lookup"><span data-stu-id="aeac3-163">-Tag</span></span>
<span data-ttu-id="aeac3-164">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="aeac3-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="aeac3-165">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="aeac3-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="aeac3-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="aeac3-166">-TenantLevel</span></span>
<span data-ttu-id="aeac3-167">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="aeac3-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="aeac3-168">-Onay</span><span class="sxs-lookup"><span data-stu-id="aeac3-168">-Confirm</span></span>
<span data-ttu-id="aeac3-169">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="aeac3-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aeac3-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aeac3-170">-WhatIf</span></span>
<span data-ttu-id="aeac3-171">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aeac3-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aeac3-172">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="aeac3-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aeac3-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeac3-173">CommonParameters</span></span>
<span data-ttu-id="aeac3-174">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aeac3-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeac3-175">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="aeac3-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeac3-176">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aeac3-176">INPUTS</span></span>

### <span data-ttu-id="aeac3-177">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="aeac3-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="aeac3-178">System. String</span><span class="sxs-lookup"><span data-stu-id="aeac3-178">System.String</span></span>

## <span data-ttu-id="aeac3-179">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aeac3-179">OUTPUTS</span></span>

### <span data-ttu-id="aeac3-180">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="aeac3-180">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="aeac3-181">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aeac3-181">NOTES</span></span>

## <span data-ttu-id="aeac3-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aeac3-182">RELATED LINKS</span></span>

[<span data-ttu-id="aeac3-183">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="aeac3-183">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="aeac3-184">Taşı-Azkaynak</span><span class="sxs-lookup"><span data-stu-id="aeac3-184">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="aeac3-185">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="aeac3-185">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="aeac3-186">Set-Azkaynak</span><span class="sxs-lookup"><span data-stu-id="aeac3-186">Set-AzResource</span></span>](./Set-AzResource.md)
