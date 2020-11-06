---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BB90E6BB-7F53-4441-A7B2-EDA940621D49
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
ms.openlocfilehash: e626a57088a9c726bfe9040f76157f0b011a6405
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589130"
---
# <span data-ttu-id="cbc15-101">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="cbc15-101">Find-AzureRmResource</span></span>

## <span data-ttu-id="cbc15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbc15-102">SYNOPSIS</span></span>
<span data-ttu-id="cbc15-103">Kaynakları belirtilen parametrelere göre arar.</span><span class="sxs-lookup"><span data-stu-id="cbc15-103">Searches for resources based on specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbc15-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cbc15-104">SYNTAX</span></span>

### <span data-ttu-id="cbc15-105">Belirtilen kapsamı temel alan kaynakları listeler.</span><span class="sxs-lookup"><span data-stu-id="cbc15-105">Lists the resources based on the specified scope.</span></span> <span data-ttu-id="cbc15-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="cbc15-106">(Default)</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] [-ResourceType <String>]
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cbc15-107">Belirli bir kapsamın kiracı düzeyindeki kaynakları listeler.</span><span class="sxs-lookup"><span data-stu-id="cbc15-107">Lists the resources based on the specified scope at the tenant level.</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ExpandProperties] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cbc15-108">Çok birimli sorgu kullanarak bir kaynak alın.</span><span class="sxs-lookup"><span data-stu-id="cbc15-108">Get a resources using a multi-subscription query.</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cbc15-109">Kaynakları bir diyez kümesi olarak belirtilen etiket nesnesiyle listeler.</span><span class="sxs-lookup"><span data-stu-id="cbc15-109">Lists resources by a tag object specified as a hashset.</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-Tag <Hashtable>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cbc15-110">Kaynakları tek tek ad ve değer parametreleri olarak belirtilen etikete göre listeler.</span><span class="sxs-lookup"><span data-stu-id="cbc15-110">Lists resources by a tag specified as a individual name and value parameters.</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-TagName <String>] [-TagValue <String>]
 [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cbc15-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="cbc15-111">DESCRIPTION</span></span>
<span data-ttu-id="cbc15-112">**Find-AzureRmResource** cmdlet 'i belirtilen parametrelere göre kaynakları arar.</span><span class="sxs-lookup"><span data-stu-id="cbc15-112">The **Find-AzureRmResource** cmdlet searches for resources based on specified parameters.</span></span>

## <span data-ttu-id="cbc15-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cbc15-113">EXAMPLES</span></span>

### <span data-ttu-id="cbc15-114">Örnek 1: türe ve kaynak grubu adına göre kaynakları arama</span><span class="sxs-lookup"><span data-stu-id="cbc15-114">Example 1: Search for resources by type and resource group name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupNameContains "ResourceGroup"
```

<span data-ttu-id="cbc15-115">Bu komut, dize kaynak kaynağı ile eşleşen adları olan kaynak grupları altında Microsoft. Web/siteleri türündeki kaynakları arar.</span><span class="sxs-lookup"><span data-stu-id="cbc15-115">This command searches for resources of the type microsoft.web/sites under resource groups that have names that match the string ResourceGroup.</span></span>

### <span data-ttu-id="cbc15-116">Örnek 2: türe ve kaynak adına göre kaynakları arama</span><span class="sxs-lookup"><span data-stu-id="cbc15-116">Example 2: Search for resources by type and resource name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceNameContains "test"
```

<span data-ttu-id="cbc15-117">Bu komut, dize testiyle eşleşen bir kaynak adı olan Microsoft. Web/Sites türündeki kaynakları arar.</span><span class="sxs-lookup"><span data-stu-id="cbc15-117">This command searches for resources of the type microsoft.web/sites that have a resource name that matches the string test.</span></span>

## <span data-ttu-id="cbc15-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cbc15-118">PARAMETERS</span></span>

### <span data-ttu-id="cbc15-119">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="cbc15-119">-ApiVersion</span></span>
<span data-ttu-id="cbc15-120">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="cbc15-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="cbc15-121">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="cbc15-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="cbc15-122">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="cbc15-122">-ExpandProperties</span></span>
<span data-ttu-id="cbc15-123">Bu cmdlet 'in kaynağın özelliklerini genişletdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cbc15-123">Indicates that this cmdlet expands the properties of the resource.</span></span>

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

### <span data-ttu-id="cbc15-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="cbc15-124">-ExtensionResourceType</span></span>
<span data-ttu-id="cbc15-125">Bu cmdlet 'in aradığı kaynaklar için uzantı kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="cbc15-125">Specifies the extension resource type for the resources for which this cmdlet searches.</span></span>
<span data-ttu-id="cbc15-126">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="cbc15-126">For instance:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbc15-127">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="cbc15-127">-InformationAction</span></span>
<span data-ttu-id="cbc15-128">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cbc15-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cbc15-129">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="cbc15-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cbc15-130">'A</span><span class="sxs-lookup"><span data-stu-id="cbc15-130">Continue</span></span>
- <span data-ttu-id="cbc15-131">Manıza</span><span class="sxs-lookup"><span data-stu-id="cbc15-131">Ignore</span></span>
- <span data-ttu-id="cbc15-132">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="cbc15-132">Inquire</span></span>
- <span data-ttu-id="cbc15-133">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="cbc15-133">SilentlyContinue</span></span>
- <span data-ttu-id="cbc15-134">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="cbc15-134">Stop</span></span>
- <span data-ttu-id="cbc15-135">Biliriz</span><span class="sxs-lookup"><span data-stu-id="cbc15-135">Suspend</span></span>

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

### <span data-ttu-id="cbc15-136">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="cbc15-136">-InformationVariable</span></span>
<span data-ttu-id="cbc15-137">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="cbc15-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="cbc15-138">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="cbc15-138">-ODataQuery</span></span>
<span data-ttu-id="cbc15-139">Açık bir veri Protokolü (OData) stil filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="cbc15-139">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="cbc15-140">Bu cmdlet, bu değeri diğer tüm filtrelere ek olarak isteğe ekler.</span><span class="sxs-lookup"><span data-stu-id="cbc15-140">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="cbc15-141">-Pre-</span><span class="sxs-lookup"><span data-stu-id="cbc15-141">-Pre</span></span>
<span data-ttu-id="cbc15-142">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="cbc15-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="cbc15-143">-ResourceGroupNameContains</span><span class="sxs-lookup"><span data-stu-id="cbc15-143">-ResourceGroupNameContains</span></span>
<span data-ttu-id="cbc15-144">Kaynak grubunun kısmi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cbc15-144">Specifies a partial name of a resource group.</span></span>
<span data-ttu-id="cbc15-145">Bu cmdlet, bu değerin alt dize olduğu kaynak gruplarıyla eşleşir.</span><span class="sxs-lookup"><span data-stu-id="cbc15-145">This cmdlet matches resource groups of which this value is a substring.</span></span>
<span data-ttu-id="cbc15-146">Cmdlet, bu kaynak gruplarındaki kaynakları arar.</span><span class="sxs-lookup"><span data-stu-id="cbc15-146">The cmdlet searches for resources in those resource groups.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Get a resources using a multi-subscription query.
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbc15-147">-ResourceGroupNameEquals</span><span class="sxs-lookup"><span data-stu-id="cbc15-147">-ResourceGroupNameEquals</span></span>
<span data-ttu-id="cbc15-148">Tam eşleşme için kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="cbc15-148">The resource group name for a full match.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbc15-149">-ResourceNameContains</span><span class="sxs-lookup"><span data-stu-id="cbc15-149">-ResourceNameContains</span></span>
<span data-ttu-id="cbc15-150">Kaynağın kısmi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cbc15-150">Specifies a partial name of a resource.</span></span>
<span data-ttu-id="cbc15-151">Cmdlet, bu değeri alt dize olarak içeren kaynakları arar.</span><span class="sxs-lookup"><span data-stu-id="cbc15-151">The cmdlet searches for resources which contain this value as a substring.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbc15-152">-Resourcenameeşittir</span><span class="sxs-lookup"><span data-stu-id="cbc15-152">-ResourceNameEquals</span></span>
<span data-ttu-id="cbc15-153">Tam eşleşme için kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="cbc15-153">The resource name for a full match.</span></span> <span data-ttu-id="cbc15-154">Örneğin, kaynak adınız testResource ise testResource belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cbc15-154">e.g. if your resource name is testResource, you can specify testResource.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbc15-155">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="cbc15-155">-ResourceType</span></span>
<span data-ttu-id="cbc15-156">Kaynağın türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="cbc15-156">Specifies the type of a resource.</span></span>
<span data-ttu-id="cbc15-157">Örneğin, veritabanı için kaynak türü aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="cbc15-157">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

<span data-ttu-id="cbc15-158">Bu cmdlet belirtilen türde kaynakları arar.</span><span class="sxs-lookup"><span data-stu-id="cbc15-158">This cmdlet searches for resources of the specified type.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbc15-159">Etiketli</span><span class="sxs-lookup"><span data-stu-id="cbc15-159">-Tag</span></span>
<span data-ttu-id="cbc15-160">OData sorgusunun etiket filtresi.</span><span class="sxs-lookup"><span data-stu-id="cbc15-160">The tag filter for the OData query.</span></span> <span data-ttu-id="cbc15-161">Beklenen biçim @ {tagName = $null} veya @ {tagName = ' tagValue '}.</span><span class="sxs-lookup"><span data-stu-id="cbc15-161">The expected format is @{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Lists resources by a tag object specified as a hashset.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbc15-162">-TagName</span><span class="sxs-lookup"><span data-stu-id="cbc15-162">-TagName</span></span>
```yaml
Type: System.String
Parameter Sets: Lists resources by a tag specified as a individual name and value parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc15-163">-TagValue</span><span class="sxs-lookup"><span data-stu-id="cbc15-163">-TagValue</span></span>
```yaml
Type: System.String
Parameter Sets: Lists resources by a tag specified as a individual name and value parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc15-164">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="cbc15-164">-TenantLevel</span></span>
<span data-ttu-id="cbc15-165">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="cbc15-165">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc15-166">-Üst</span><span class="sxs-lookup"><span data-stu-id="cbc15-166">-Top</span></span>
<span data-ttu-id="cbc15-167">Alınacak kaynak sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cbc15-167">Specifies the number of resources to retrieve.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc15-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbc15-168">-DefaultProfile</span></span>
<span data-ttu-id="cbc15-169">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cbc15-169">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbc15-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbc15-170">CommonParameters</span></span>
<span data-ttu-id="cbc15-171">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cbc15-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbc15-172">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbc15-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbc15-173">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cbc15-173">INPUTS</span></span>

## <span data-ttu-id="cbc15-174">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cbc15-174">OUTPUTS</span></span>

### <span data-ttu-id="cbc15-175">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="cbc15-175">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="cbc15-176">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cbc15-176">NOTES</span></span>

## <span data-ttu-id="cbc15-177">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cbc15-177">RELATED LINKS</span></span>

[<span data-ttu-id="cbc15-178">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="cbc15-178">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="cbc15-179">Taşı-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="cbc15-179">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="cbc15-180">Yeni-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="cbc15-180">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="cbc15-181">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="cbc15-181">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="cbc15-182">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="cbc15-182">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
