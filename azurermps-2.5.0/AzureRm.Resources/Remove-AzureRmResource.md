---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresource
schema: 2.0.0
ms.openlocfilehash: 29cdde4d48ca782abd680647ed895945062c055d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939990"
---
# <span data-ttu-id="e887b-101">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e887b-101">Remove-AzureRmResource</span></span>

## <span data-ttu-id="e887b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e887b-102">SYNOPSIS</span></span>
<span data-ttu-id="e887b-103">Kaynağı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e887b-103">Removes a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e887b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e887b-104">SYNTAX</span></span>

### <span data-ttu-id="e887b-105">Byresourceıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e887b-105">ByResourceId (Default)</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e887b-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="e887b-106">BySubscriptionLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e887b-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="e887b-107">ByTenantLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e887b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e887b-108">DESCRIPTION</span></span>
<span data-ttu-id="e887b-109">**Remove-AzureRmResource** cmdlet 'ı bir Azure kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e887b-109">The **Remove-AzureRmResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="e887b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e887b-110">EXAMPLES</span></span>

### <span data-ttu-id="e887b-111">Örnek 1: Web sitesi kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="e887b-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzureRmResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="e887b-112">Bu komut, ContosoSite adlı Web sitesi kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e887b-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="e887b-113">Örnekte, abonelik KIMLIĞI için yer tutucu değeri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e887b-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="e887b-114">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e887b-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="e887b-115">Bu nedenle sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="e887b-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e887b-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e887b-116">PARAMETERS</span></span>

### <span data-ttu-id="e887b-117">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="e887b-117">-ApiVersion</span></span>
<span data-ttu-id="e887b-118">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e887b-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e887b-119">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="e887b-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e887b-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="e887b-120">-AsJob</span></span>
<span data-ttu-id="e887b-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e887b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e887b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e887b-122">-DefaultProfile</span></span>
<span data-ttu-id="e887b-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e887b-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e887b-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="e887b-124">-ExtensionResourceName</span></span>
<span data-ttu-id="e887b-125">Bu cmdlet 'in kaldırdığı kaynağın uzantı kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e887b-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="e887b-126">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın: sunucu adı `/` veritabanı adı</span><span class="sxs-lookup"><span data-stu-id="e887b-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="e887b-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="e887b-127">-ExtensionResourceType</span></span>
<span data-ttu-id="e887b-128">Bir uzantı kaynağı için kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e887b-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="e887b-129">Kaynağın uzantı kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e887b-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="e887b-130">Örneğin: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="e887b-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="e887b-131">-Force</span><span class="sxs-lookup"><span data-stu-id="e887b-131">-Force</span></span>
<span data-ttu-id="e887b-132">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e887b-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e887b-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="e887b-133">-ODataQuery</span></span>
<span data-ttu-id="e887b-134">Açık bir veri Protokolü (OData) stil filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e887b-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="e887b-135">Bu cmdlet, bu değeri diğer tüm filtrelere ek olarak isteğe ekler.</span><span class="sxs-lookup"><span data-stu-id="e887b-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="e887b-136">-Pre-</span><span class="sxs-lookup"><span data-stu-id="e887b-136">-Pre</span></span>
<span data-ttu-id="e887b-137">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e887b-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e887b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e887b-138">-ResourceGroupName</span></span>
<span data-ttu-id="e887b-139">Bu cmdlet 'in kaynağı kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e887b-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="e887b-140">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e887b-140">-ResourceId</span></span>
<span data-ttu-id="e887b-141">Bu cmdlet 'in kaldırdığı kaynağın tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e887b-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="e887b-142">KIMLIK, aşağıdaki örnekte olduğu gibi aboneliği içerir: `/subscriptions/` ABONELIK kimliği`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="e887b-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="e887b-143">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e887b-143">-ResourceName</span></span>
<span data-ttu-id="e887b-144">Bu cmdlet 'in kaldırdığı kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e887b-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="e887b-145">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="e887b-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="e887b-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e887b-146">-ResourceType</span></span>
<span data-ttu-id="e887b-147">Bu cmdlet 'in kaldırdığı kaynağın türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e887b-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="e887b-148">Örneğin, veritabanı için kaynak türü aşağıdaki gibidir: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="e887b-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="e887b-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="e887b-149">-TenantLevel</span></span>
<span data-ttu-id="e887b-150">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="e887b-150">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="e887b-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="e887b-151">-Confirm</span></span>
<span data-ttu-id="e887b-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e887b-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e887b-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e887b-153">-WhatIf</span></span>
<span data-ttu-id="e887b-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e887b-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e887b-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e887b-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e887b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e887b-156">CommonParameters</span></span>
<span data-ttu-id="e887b-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e887b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e887b-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e887b-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e887b-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e887b-159">INPUTS</span></span>

### <span data-ttu-id="e887b-160">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e887b-160">None</span></span>

## <span data-ttu-id="e887b-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e887b-161">OUTPUTS</span></span>

### <span data-ttu-id="e887b-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e887b-162">System.Boolean</span></span>

## <span data-ttu-id="e887b-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e887b-163">NOTES</span></span>

## <span data-ttu-id="e887b-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e887b-164">RELATED LINKS</span></span>



[<span data-ttu-id="e887b-165">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e887b-165">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="e887b-166">Taşı-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e887b-166">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="e887b-167">Yeni-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e887b-167">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="e887b-168">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e887b-168">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


