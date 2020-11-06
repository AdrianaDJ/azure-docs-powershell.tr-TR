---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
ms.openlocfilehash: 01e4e6b990a35b8573a9ea1d2f2803f6d6fabc1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592585"
---
# <span data-ttu-id="fc1a2-101">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fc1a2-101">Get-AzureRmResource</span></span>

## <span data-ttu-id="fc1a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc1a2-102">SYNOPSIS</span></span>
<span data-ttu-id="fc1a2-103">Kaynakları alır.</span><span class="sxs-lookup"><span data-stu-id="fc1a2-103">Gets resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc1a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc1a2-104">SYNTAX</span></span>

### <span data-ttu-id="fc1a2-105">Tüm kaynakları Listele parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="fc1a2-105">The list all resources parameter set.</span></span> <span data-ttu-id="fc1a2-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="fc1a2-106">(Default)</span></span>
```
Get-AzureRmResource [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc1a2-107">Kimliğini kullanarak tek bir kaynak edinin.</span><span class="sxs-lookup"><span data-stu-id="fc1a2-107">Get a single resource by its Id.</span></span>
```
Get-AzureRmResource -ResourceId <String> [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc1a2-108">Kiracı düzeyinde tek bir kaynak edinin.</span><span class="sxs-lookup"><span data-stu-id="fc1a2-108">Get a single resource at the tenant level.</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc1a2-109">Belirli bir kapsamın kiracı düzeyindeki kaynakları listeler.</span><span class="sxs-lookup"><span data-stu-id="fc1a2-109">Lists the resources based on the specified scope at the tenant level.</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-Top <Int32>] [-ODataQuery <String>]
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc1a2-110">Kaynağa ve gruba göre kaynak al</span><span class="sxs-lookup"><span data-stu-id="fc1a2-110">Get resource by name and group</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc1a2-111">Ada göre bir kaynak alın ve yazın.</span><span class="sxs-lookup"><span data-stu-id="fc1a2-111">Get a resource by name and type.</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc1a2-112">Ada göre kaynak al, Gruplandır ve yaz</span><span class="sxs-lookup"><span data-stu-id="fc1a2-112">Get resource by name, group and type</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-ODataQuery <String>] -ResourceGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc1a2-113">Kaynak toplamayı al</span><span class="sxs-lookup"><span data-stu-id="fc1a2-113">Get resource collection</span></span>
```
Get-AzureRmResource [-ResourceType <String>] [-ExtensionResourceType <String>] [-ExpandProperties]
 [-IsCollection] [-ODataQuery <String>] [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc1a2-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc1a2-114">DESCRIPTION</span></span>
<span data-ttu-id="fc1a2-115">**Get-AzureRmResource** cmdlet 'i Azure kaynaklarını alır.</span><span class="sxs-lookup"><span data-stu-id="fc1a2-115">The **Get-AzureRmResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="fc1a2-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc1a2-116">EXAMPLES</span></span>

### <span data-ttu-id="fc1a2-117">Örnek 1: kaynak alma</span><span class="sxs-lookup"><span data-stu-id="fc1a2-117">Example 1: Get a resource</span></span>
```
PS C:\>Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoWebsite"
```

<span data-ttu-id="fc1a2-118">Bu komut, ResourceGroup11 altında Contosoweb sitesi adlı Microsoft. Web/Sites türünde bir kaynak alır.</span><span class="sxs-lookup"><span data-stu-id="fc1a2-118">This command gets a resource of the type microsoft.web/sites, named ContosoWebsite under ResourceGroup11.</span></span>

## <span data-ttu-id="fc1a2-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc1a2-119">PARAMETERS</span></span>

### <span data-ttu-id="fc1a2-120">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="fc1a2-120">-ApiVersion</span></span>
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

### <span data-ttu-id="fc1a2-121">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="fc1a2-121">-ExpandProperties</span></span>
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

### <span data-ttu-id="fc1a2-122">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="fc1a2-122">-ExtensionResourceName</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource by name, group and type
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc1a2-123">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="fc1a2-123">-ExtensionResourceType</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource by name, group and type
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc1a2-124">-IsCollection</span><span class="sxs-lookup"><span data-stu-id="fc1a2-124">-IsCollection</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc1a2-125">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="fc1a2-125">-ODataQuery</span></span>
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

### <span data-ttu-id="fc1a2-126">-Pre-</span><span class="sxs-lookup"><span data-stu-id="fc1a2-126">-Pre</span></span>
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

### <span data-ttu-id="fc1a2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc1a2-127">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: Get resource by name and group
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource by name, group and type
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc1a2-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fc1a2-128">-ResourceId</span></span>
<span data-ttu-id="fc1a2-129">Aşağıdaki örnekte olduğu gibi, abonelik dahil olmak üzere tam nitelikli kaynak KIMLIĞINI belirtir:</span><span class="sxs-lookup"><span data-stu-id="fc1a2-129">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span> 

<span data-ttu-id="fc1a2-130">`/subscriptions/`abonelik KIMLIĞI`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="fc1a2-130">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

<span data-ttu-id="fc1a2-131">Bu cmdlet, bu KIMLIĞE sahip olan kaynağı alır.</span><span class="sxs-lookup"><span data-stu-id="fc1a2-131">This cmdlet gets the resource that has this ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a single resource by its Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc1a2-132">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="fc1a2-132">-ResourceName</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Get resource by name, group and type
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type.
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc1a2-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="fc1a2-133">-ResourceType</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Get resource by name, group and type
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get a resource by name and type.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc1a2-134">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="fc1a2-134">-TenantLevel</span></span>
<span data-ttu-id="fc1a2-135">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="fc1a2-135">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc1a2-136">-Üst</span><span class="sxs-lookup"><span data-stu-id="fc1a2-136">-Top</span></span>
```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc1a2-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc1a2-137">-DefaultProfile</span></span>
<span data-ttu-id="fc1a2-138">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fc1a2-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc1a2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc1a2-139">CommonParameters</span></span>
<span data-ttu-id="fc1a2-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc1a2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc1a2-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc1a2-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc1a2-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc1a2-142">INPUTS</span></span>

## <span data-ttu-id="fc1a2-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc1a2-143">OUTPUTS</span></span>

### <span data-ttu-id="fc1a2-144">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="fc1a2-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fc1a2-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc1a2-145">NOTES</span></span>

## <span data-ttu-id="fc1a2-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc1a2-146">RELATED LINKS</span></span>

[<span data-ttu-id="fc1a2-147">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fc1a2-147">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="fc1a2-148">Taşı-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fc1a2-148">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="fc1a2-149">Yeni-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fc1a2-149">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="fc1a2-150">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fc1a2-150">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="fc1a2-151">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fc1a2-151">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


