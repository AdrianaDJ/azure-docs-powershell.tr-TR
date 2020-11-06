---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
ms.openlocfilehash: 92d6fc81536568b2654fb72a1d6462830c05923e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592558"
---
# <span data-ttu-id="c4981-101">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c4981-101">Remove-AzureRmResource</span></span>

## <span data-ttu-id="c4981-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4981-102">SYNOPSIS</span></span>
<span data-ttu-id="c4981-103">Kaynağı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c4981-103">Removes a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4981-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c4981-104">SYNTAX</span></span>

### <span data-ttu-id="c4981-105">Kaynak kimliği. (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c4981-105">The resource Id. (Default)</span></span>
```
Remove-AzureRmResource -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4981-106">Abonelik düzeyinde bulunan kaynaktır.</span><span class="sxs-lookup"><span data-stu-id="c4981-106">Resource that resides at the subscription level.</span></span>
```
Remove-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4981-107">Kiracı düzeyinde bulunan kaynaktır.</span><span class="sxs-lookup"><span data-stu-id="c4981-107">Resource that resides at the tenant level.</span></span>
```
Remove-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4981-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c4981-108">DESCRIPTION</span></span>
<span data-ttu-id="c4981-109">**Remove-AzureRmResource** cmdlet 'ı bir Azure kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c4981-109">The **Remove-AzureRmResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="c4981-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c4981-110">EXAMPLES</span></span>

### <span data-ttu-id="c4981-111">Örnek 1: Web sitesi kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="c4981-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzureRmResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="c4981-112">Bu komut, ContosoSite adlı Web sitesi kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c4981-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="c4981-113">Örnekte, abonelik KIMLIĞI için yer tutucu değeri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c4981-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="c4981-114">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4981-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c4981-115">Bu nedenle sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="c4981-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c4981-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c4981-116">PARAMETERS</span></span>

### <span data-ttu-id="c4981-117">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="c4981-117">-ApiVersion</span></span>
<span data-ttu-id="c4981-118">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4981-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c4981-119">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="c4981-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c4981-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="c4981-120">-ExtensionResourceName</span></span>
<span data-ttu-id="c4981-121">Bu cmdlet 'in kaldırdığı kaynağın uzantı kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4981-121">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="c4981-122">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="c4981-122">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="c4981-123">sunucu adı `/` veritabanı adı</span><span class="sxs-lookup"><span data-stu-id="c4981-123">server name`/`database name</span></span>

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

### <span data-ttu-id="c4981-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="c4981-124">-ExtensionResourceType</span></span>
<span data-ttu-id="c4981-125">Bir uzantı kaynağı için kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4981-125">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="c4981-126">Kaynağın uzantı kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4981-126">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="c4981-127">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="c4981-127">For instance:</span></span> 

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

### <span data-ttu-id="c4981-128">-Force</span><span class="sxs-lookup"><span data-stu-id="c4981-128">-Force</span></span>
<span data-ttu-id="c4981-129">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="c4981-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c4981-130">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="c4981-130">-ODataQuery</span></span>
<span data-ttu-id="c4981-131">Açık bir veri Protokolü (OData) stil filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4981-131">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="c4981-132">Bu cmdlet, bu değeri diğer tüm filtrelere ek olarak isteğe ekler.</span><span class="sxs-lookup"><span data-stu-id="c4981-132">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="c4981-133">-Pre-</span><span class="sxs-lookup"><span data-stu-id="c4981-133">-Pre</span></span>
<span data-ttu-id="c4981-134">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c4981-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c4981-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4981-135">-ResourceGroupName</span></span>
<span data-ttu-id="c4981-136">Bu cmdlet 'in kaynağı kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4981-136">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="c4981-137">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c4981-137">-ResourceId</span></span>
<span data-ttu-id="c4981-138">Bu cmdlet 'in kaldırdığı kaynağın tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4981-138">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="c4981-139">KIMLIK, aşağıdaki örnekte olduğu gibi aboneliği içerir:</span><span class="sxs-lookup"><span data-stu-id="c4981-139">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="c4981-140">`/subscriptions/`abonelik KIMLIĞI`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="c4981-140">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="c4981-141">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c4981-141">-ResourceName</span></span>
<span data-ttu-id="c4981-142">Bu cmdlet 'in kaldırdığı kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4981-142">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="c4981-143">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="c4981-143">For instance, to specify a database, use the following format:</span></span> 

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

### <span data-ttu-id="c4981-144">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c4981-144">-ResourceType</span></span>
<span data-ttu-id="c4981-145">Bu cmdlet 'in kaldırdığı kaynağın türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4981-145">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="c4981-146">Örneğin, veritabanı için kaynak türü aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="c4981-146">For instance, for a database, the resource type is as follows:</span></span> 

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

### <span data-ttu-id="c4981-147">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="c4981-147">-TenantLevel</span></span>
<span data-ttu-id="c4981-148">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="c4981-148">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="c4981-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="c4981-149">-Confirm</span></span>
<span data-ttu-id="c4981-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c4981-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4981-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4981-151">-WhatIf</span></span>
<span data-ttu-id="c4981-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c4981-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4981-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c4981-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4981-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4981-154">-DefaultProfile</span></span>
<span data-ttu-id="c4981-155">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c4981-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4981-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4981-156">CommonParameters</span></span>
<span data-ttu-id="c4981-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c4981-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4981-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4981-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4981-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c4981-159">INPUTS</span></span>

## <span data-ttu-id="c4981-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c4981-160">OUTPUTS</span></span>

### <span data-ttu-id="c4981-161">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c4981-161">System.Boolean</span></span>

## <span data-ttu-id="c4981-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c4981-162">NOTES</span></span>

## <span data-ttu-id="c4981-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c4981-163">RELATED LINKS</span></span>

[<span data-ttu-id="c4981-164">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c4981-164">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="c4981-165">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c4981-165">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="c4981-166">Taşı-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c4981-166">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="c4981-167">Yeni-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c4981-167">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="c4981-168">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c4981-168">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


