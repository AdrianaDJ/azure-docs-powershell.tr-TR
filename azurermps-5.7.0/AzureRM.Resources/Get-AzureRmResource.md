---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
ms.openlocfilehash: 2161c3c4bc81721c0d99b88ab0adfc43beac8eee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589689"
---
# <span data-ttu-id="8581b-101">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8581b-101">Get-AzureRmResource</span></span>

## <span data-ttu-id="8581b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8581b-102">SYNOPSIS</span></span>
<span data-ttu-id="8581b-103">Kaynakları alır.</span><span class="sxs-lookup"><span data-stu-id="8581b-103">Gets resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8581b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8581b-104">SYNTAX</span></span>

### <span data-ttu-id="8581b-105">GetAllResources (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8581b-105">GetAllResources (Default)</span></span>
```
Get-AzureRmResource [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8581b-106">Getbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="8581b-106">GetByResourceId</span></span>
```
Get-AzureRmResource -ResourceId <String> [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8581b-107">GetByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="8581b-107">GetByTenantLevel</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8581b-108">Getbybelirtilmediscopeattenantlevel</span><span class="sxs-lookup"><span data-stu-id="8581b-108">GetBySpecifiedScopeAtTenantLevel</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-Top <Int32>] [-ODataQuery <String>]
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8581b-109">Grup</span><span class="sxs-lookup"><span data-stu-id="8581b-109">GetByNameAndGroup</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8581b-110">Getbyresourcenadeniz Vseçtype</span><span class="sxs-lookup"><span data-stu-id="8581b-110">GetByResourceNameAndType</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8581b-111">GetByNameGroupAndType</span><span class="sxs-lookup"><span data-stu-id="8581b-111">GetByNameGroupAndType</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-ODataQuery <String>] -ResourceGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8581b-112">GetResourceCollection</span><span class="sxs-lookup"><span data-stu-id="8581b-112">GetResourceCollection</span></span>
```
Get-AzureRmResource [-ResourceType <String>] [-ExtensionResourceType <String>] [-ExpandProperties]
 [-IsCollection] [-ODataQuery <String>] [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8581b-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="8581b-113">DESCRIPTION</span></span>
<span data-ttu-id="8581b-114">**Get-AzureRmResource** cmdlet 'i Azure kaynaklarını alır.</span><span class="sxs-lookup"><span data-stu-id="8581b-114">The **Get-AzureRmResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="8581b-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8581b-115">EXAMPLES</span></span>

### <span data-ttu-id="8581b-116">Örnek 1: belirli türdeki tüm kaynakları alma</span><span class="sxs-lookup"><span data-stu-id="8581b-116">Example 1: Get all the resources of a particular type</span></span>
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceType microsoft.web/sites
```

<span data-ttu-id="8581b-117">Bu komut, ResourceGroup11 altında Microsoft. Web/Sites türünde bir kaynak alır.</span><span class="sxs-lookup"><span data-stu-id="8581b-117">This command gets a resource of the type microsoft.web/sites under ResourceGroup11.</span></span>

### <span data-ttu-id="8581b-118">Örnek 2: ada göre kaynak alma</span><span class="sxs-lookup"><span data-stu-id="8581b-118">Example 2: Get a resource by name</span></span>
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceName ContosoWebsite
```

<span data-ttu-id="8581b-119">Bu komut, ResourceGroup11 altında Contosoweb sitesi adlı bir kaynak alır.</span><span class="sxs-lookup"><span data-stu-id="8581b-119">This command gets a resource  named ContosoWebsite under ResourceGroup11.</span></span>

### <span data-ttu-id="8581b-120">Örnek 3: kaynak grubundaki depolama hesaplarının tüm durumunu gösterme</span><span class="sxs-lookup"><span data-stu-id="8581b-120">Example 3: Show all the status of storage accounts in a Resource Group</span></span>
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceType Microsoft.ClassicStorage/storageAccounts -ExpandProperties |
   Select * -Expand Properties |
   Sort Name |
   Format-Table Name,Status*
```

## <span data-ttu-id="8581b-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8581b-121">PARAMETERS</span></span>

### <span data-ttu-id="8581b-122">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="8581b-122">-ApiVersion</span></span>
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

### <span data-ttu-id="8581b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8581b-123">-DefaultProfile</span></span>
<span data-ttu-id="8581b-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8581b-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8581b-125">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="8581b-125">-ExpandProperties</span></span>
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

### <span data-ttu-id="8581b-126">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="8581b-126">-ExtensionResourceName</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetByNameGroupAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8581b-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="8581b-127">-ExtensionResourceType</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetByNameGroupAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8581b-128">-IsCollection</span><span class="sxs-lookup"><span data-stu-id="8581b-128">-IsCollection</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8581b-129">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="8581b-129">-ODataQuery</span></span>
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

### <span data-ttu-id="8581b-130">-Pre-</span><span class="sxs-lookup"><span data-stu-id="8581b-130">-Pre</span></span>
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

### <span data-ttu-id="8581b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8581b-131">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: GetByNameAndGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByNameGroupAndType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8581b-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8581b-132">-ResourceId</span></span>
<span data-ttu-id="8581b-133">Aşağıdaki örnekte olduğu gibi, abonelik dahil olmak üzere tam nitelikli kaynak KIMLIĞINI belirtir:</span><span class="sxs-lookup"><span data-stu-id="8581b-133">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span> 

<span data-ttu-id="8581b-134">`/subscriptions/`abonelik KIMLIĞI`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="8581b-134">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

<span data-ttu-id="8581b-135">Bu cmdlet, bu KIMLIĞE sahip olan kaynağı alır.</span><span class="sxs-lookup"><span data-stu-id="8581b-135">This cmdlet gets the resource that has this ID.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8581b-136">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8581b-136">-ResourceName</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetByNameGroupAndType
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8581b-137">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8581b-137">-ResourceType</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetByNameGroupAndType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByResourceNameAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8581b-138">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="8581b-138">-TenantLevel</span></span>
<span data-ttu-id="8581b-139">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="8581b-139">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8581b-140">-Üst</span><span class="sxs-lookup"><span data-stu-id="8581b-140">-Top</span></span>
```yaml
Type: Int32
Parameter Sets: GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8581b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8581b-141">CommonParameters</span></span>
<span data-ttu-id="8581b-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8581b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8581b-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8581b-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8581b-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8581b-144">INPUTS</span></span>

### <span data-ttu-id="8581b-145">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8581b-145">None</span></span>
<span data-ttu-id="8581b-146">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="8581b-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8581b-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8581b-147">OUTPUTS</span></span>

### <span data-ttu-id="8581b-148">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="8581b-148">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8581b-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8581b-149">NOTES</span></span>

## <span data-ttu-id="8581b-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8581b-150">RELATED LINKS</span></span>

[<span data-ttu-id="8581b-151">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8581b-151">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="8581b-152">Taşı-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8581b-152">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="8581b-153">Yeni-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8581b-153">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="8581b-154">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8581b-154">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="8581b-155">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8581b-155">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


