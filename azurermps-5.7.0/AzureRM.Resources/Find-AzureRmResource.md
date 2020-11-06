---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BB90E6BB-7F53-4441-A7B2-EDA940621D49
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/find-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
ms.openlocfilehash: 67389829eb5edc5ea7ac21fcc891cc85787b5e9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591636"
---
# <span data-ttu-id="974e5-101">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="974e5-101">Find-AzureRmResource</span></span>

## <span data-ttu-id="974e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="974e5-102">SYNOPSIS</span></span>
<span data-ttu-id="974e5-103">Kaynakları belirtilen parametrelere göre arar.</span><span class="sxs-lookup"><span data-stu-id="974e5-103">Searches for resources based on specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="974e5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="974e5-104">SYNTAX</span></span>

### <span data-ttu-id="974e5-105">Getbybelirtilmediscope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="974e5-105">GetBySpecifiedScope (Default)</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] [-ResourceType <String>]
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="974e5-106">Getbybelirtilmediscopeattenantlevel</span><span class="sxs-lookup"><span data-stu-id="974e5-106">GetBySpecifiedScopeAtTenantLevel</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ExpandProperties] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="974e5-107">GetByMultiSubscriptionQuery</span><span class="sxs-lookup"><span data-stu-id="974e5-107">GetByMultiSubscriptionQuery</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="974e5-108">GetByTagObject</span><span class="sxs-lookup"><span data-stu-id="974e5-108">GetByTagObject</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-Tag <Hashtable>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="974e5-109">GetByTagNameValue</span><span class="sxs-lookup"><span data-stu-id="974e5-109">GetByTagNameValue</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-TagName <String>] [-TagValue <String>]
 [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="974e5-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="974e5-110">DESCRIPTION</span></span>
<span data-ttu-id="974e5-111">**Find-AzureRmResource** cmdlet 'i belirtilen parametrelere göre kaynakları arar.</span><span class="sxs-lookup"><span data-stu-id="974e5-111">The **Find-AzureRmResource** cmdlet searches for resources based on specified parameters.</span></span>

## <span data-ttu-id="974e5-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="974e5-112">EXAMPLES</span></span>

### <span data-ttu-id="974e5-113">Örnek 1: türe ve kaynak grubu adına göre kaynakları arama</span><span class="sxs-lookup"><span data-stu-id="974e5-113">Example 1: Search for resources by type and resource group name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupNameContains "ResourceGroup"
```

<span data-ttu-id="974e5-114">Bu komut, dize kaynak kaynağı ile eşleşen adları olan kaynak grupları altında Microsoft. Web/siteleri türündeki kaynakları arar.</span><span class="sxs-lookup"><span data-stu-id="974e5-114">This command searches for resources of the type microsoft.web/sites under resource groups that have names that match the string ResourceGroup.</span></span>

### <span data-ttu-id="974e5-115">Örnek 2: türe ve kaynak adına göre kaynakları arama</span><span class="sxs-lookup"><span data-stu-id="974e5-115">Example 2: Search for resources by type and resource name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceNameContains "test"
```

<span data-ttu-id="974e5-116">Bu komut, dize testiyle eşleşen bir kaynak adı olan Microsoft. Web/Sites türündeki kaynakları arar.</span><span class="sxs-lookup"><span data-stu-id="974e5-116">This command searches for resources of the type microsoft.web/sites that have a resource name that matches the string test.</span></span>

## <span data-ttu-id="974e5-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="974e5-117">PARAMETERS</span></span>

### <span data-ttu-id="974e5-118">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="974e5-118">-ApiVersion</span></span>
<span data-ttu-id="974e5-119">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="974e5-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="974e5-120">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="974e5-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="974e5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="974e5-121">-DefaultProfile</span></span>
<span data-ttu-id="974e5-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="974e5-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="974e5-123">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="974e5-123">-ExpandProperties</span></span>
<span data-ttu-id="974e5-124">Bu cmdlet 'in kaynağın özelliklerini genişletdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="974e5-124">Indicates that this cmdlet expands the properties of the resource.</span></span>

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

### <span data-ttu-id="974e5-125">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="974e5-125">-ExtensionResourceType</span></span>
<span data-ttu-id="974e5-126">Bu cmdlet 'in aradığı kaynaklar için uzantı kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="974e5-126">Specifies the extension resource type for the resources for which this cmdlet searches.</span></span>
<span data-ttu-id="974e5-127">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="974e5-127">For instance:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="974e5-128">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="974e5-128">-InformationAction</span></span>
<span data-ttu-id="974e5-129">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="974e5-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="974e5-130">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="974e5-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="974e5-131">'A</span><span class="sxs-lookup"><span data-stu-id="974e5-131">Continue</span></span>
- <span data-ttu-id="974e5-132">Manıza</span><span class="sxs-lookup"><span data-stu-id="974e5-132">Ignore</span></span>
- <span data-ttu-id="974e5-133">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="974e5-133">Inquire</span></span>
- <span data-ttu-id="974e5-134">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="974e5-134">SilentlyContinue</span></span>
- <span data-ttu-id="974e5-135">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="974e5-135">Stop</span></span>
- <span data-ttu-id="974e5-136">Biliriz</span><span class="sxs-lookup"><span data-stu-id="974e5-136">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="974e5-137">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="974e5-137">-InformationVariable</span></span>
<span data-ttu-id="974e5-138">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="974e5-138">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="974e5-139">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="974e5-139">-ODataQuery</span></span>
<span data-ttu-id="974e5-140">Açık bir veri Protokolü (OData) stil filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="974e5-140">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="974e5-141">Bu cmdlet, bu değeri diğer tüm filtrelere ek olarak isteğe ekler.</span><span class="sxs-lookup"><span data-stu-id="974e5-141">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="974e5-142">-Pre-</span><span class="sxs-lookup"><span data-stu-id="974e5-142">-Pre</span></span>
<span data-ttu-id="974e5-143">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="974e5-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="974e5-144">-ResourceGroupNameContains</span><span class="sxs-lookup"><span data-stu-id="974e5-144">-ResourceGroupNameContains</span></span>
<span data-ttu-id="974e5-145">Kaynak grubunun kısmi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="974e5-145">Specifies a partial name of a resource group.</span></span>
<span data-ttu-id="974e5-146">Bu cmdlet, bu değerin alt dize olduğu kaynak gruplarıyla eşleşir.</span><span class="sxs-lookup"><span data-stu-id="974e5-146">This cmdlet matches resource groups of which this value is a substring.</span></span>
<span data-ttu-id="974e5-147">Cmdlet, bu kaynak gruplarındaki kaynakları arar.</span><span class="sxs-lookup"><span data-stu-id="974e5-147">The cmdlet searches for resources in those resource groups.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetByMultiSubscriptionQuery
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="974e5-148">-ResourceGroupNameEquals</span><span class="sxs-lookup"><span data-stu-id="974e5-148">-ResourceGroupNameEquals</span></span>
<span data-ttu-id="974e5-149">Tam eşleşme için kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="974e5-149">The resource group name for a full match.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="974e5-150">-ResourceNameContains</span><span class="sxs-lookup"><span data-stu-id="974e5-150">-ResourceNameContains</span></span>
<span data-ttu-id="974e5-151">Kaynağın kısmi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="974e5-151">Specifies a partial name of a resource.</span></span>
<span data-ttu-id="974e5-152">Cmdlet, bu değeri alt dize olarak içeren kaynakları arar.</span><span class="sxs-lookup"><span data-stu-id="974e5-152">The cmdlet searches for resources which contain this value as a substring.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="974e5-153">-Resourcenameeşittir</span><span class="sxs-lookup"><span data-stu-id="974e5-153">-ResourceNameEquals</span></span>
<span data-ttu-id="974e5-154">Tam eşleşme için kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="974e5-154">The resource name for a full match.</span></span> <span data-ttu-id="974e5-155">Örneğin, kaynak adınız testResource ise testResource belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="974e5-155">e.g. if your resource name is testResource, you can specify testResource.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="974e5-156">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="974e5-156">-ResourceType</span></span>
<span data-ttu-id="974e5-157">Kaynağın türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="974e5-157">Specifies the type of a resource.</span></span>
<span data-ttu-id="974e5-158">Örneğin, veritabanı için kaynak türü aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="974e5-158">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

<span data-ttu-id="974e5-159">Bu cmdlet belirtilen türde kaynakları arar.</span><span class="sxs-lookup"><span data-stu-id="974e5-159">This cmdlet searches for resources of the specified type.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="974e5-160">Etiketli</span><span class="sxs-lookup"><span data-stu-id="974e5-160">-Tag</span></span>
<span data-ttu-id="974e5-161">OData sorgusunun etiket filtresi.</span><span class="sxs-lookup"><span data-stu-id="974e5-161">The tag filter for the OData query.</span></span> <span data-ttu-id="974e5-162">Beklenen biçim @ {tagName = $null} veya @ {tagName = ' tagValue '}.</span><span class="sxs-lookup"><span data-stu-id="974e5-162">The expected format is @{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: Hashtable
Parameter Sets: GetByTagObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="974e5-163">-TagName</span><span class="sxs-lookup"><span data-stu-id="974e5-163">-TagName</span></span>
```yaml
Type: String
Parameter Sets: GetByTagNameValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="974e5-164">-TagValue</span><span class="sxs-lookup"><span data-stu-id="974e5-164">-TagValue</span></span>
```yaml
Type: String
Parameter Sets: GetByTagNameValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="974e5-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="974e5-165">-TenantLevel</span></span>
<span data-ttu-id="974e5-166">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="974e5-166">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="974e5-167">-Üst</span><span class="sxs-lookup"><span data-stu-id="974e5-167">-Top</span></span>
<span data-ttu-id="974e5-168">Alınacak kaynak sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="974e5-168">Specifies the number of resources to retrieve.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="974e5-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="974e5-169">CommonParameters</span></span>
<span data-ttu-id="974e5-170">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="974e5-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="974e5-171">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="974e5-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="974e5-172">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="974e5-172">INPUTS</span></span>

### <span data-ttu-id="974e5-173">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="974e5-173">None</span></span>
<span data-ttu-id="974e5-174">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="974e5-174">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="974e5-175">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="974e5-175">OUTPUTS</span></span>

### <span data-ttu-id="974e5-176">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="974e5-176">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="974e5-177">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="974e5-177">NOTES</span></span>

## <span data-ttu-id="974e5-178">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="974e5-178">RELATED LINKS</span></span>

[<span data-ttu-id="974e5-179">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="974e5-179">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="974e5-180">Taşı-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="974e5-180">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="974e5-181">Yeni-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="974e5-181">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="974e5-182">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="974e5-182">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="974e5-183">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="974e5-183">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
