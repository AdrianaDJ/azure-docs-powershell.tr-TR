---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
ms.openlocfilehash: ef81674d75ee2f5f79988875e70764df91d23d2c
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93765231"
---
# <span data-ttu-id="2db32-101">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="2db32-101">Remove-AzResource</span></span>

## <span data-ttu-id="2db32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2db32-102">SYNOPSIS</span></span>
<span data-ttu-id="2db32-103">Kaynağı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2db32-103">Removes a resource.</span></span>

## <span data-ttu-id="2db32-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2db32-104">SYNTAX</span></span>

### <span data-ttu-id="2db32-105">Byresourceıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2db32-105">ByResourceId (Default)</span></span>
```
Remove-AzResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2db32-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="2db32-106">BySubscriptionLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2db32-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="2db32-107">ByTenantLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2db32-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2db32-108">DESCRIPTION</span></span>
<span data-ttu-id="2db32-109">**Remove-AzResource** cmdlet 'ı bir Azure kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2db32-109">The **Remove-AzResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="2db32-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2db32-110">EXAMPLES</span></span>

### <span data-ttu-id="2db32-111">Örnek 1: Web sitesi kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="2db32-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="2db32-112">Bu komut, ContosoSite adlı Web sitesi kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2db32-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="2db32-113">Örnekte, abonelik KIMLIĞI için yer tutucu değeri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2db32-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="2db32-114">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2db32-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="2db32-115">Bu nedenle sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="2db32-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="2db32-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2db32-116">PARAMETERS</span></span>

### <span data-ttu-id="2db32-117">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="2db32-117">-ApiVersion</span></span>
<span data-ttu-id="2db32-118">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2db32-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="2db32-119">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="2db32-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="2db32-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="2db32-120">-AsJob</span></span>
<span data-ttu-id="2db32-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2db32-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2db32-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2db32-122">-DefaultProfile</span></span>
<span data-ttu-id="2db32-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2db32-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2db32-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="2db32-124">-ExtensionResourceName</span></span>
<span data-ttu-id="2db32-125">Bu cmdlet 'in kaldırdığı kaynağın uzantı kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2db32-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="2db32-126">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın: sunucu adı `/` veritabanı adı</span><span class="sxs-lookup"><span data-stu-id="2db32-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="2db32-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="2db32-127">-ExtensionResourceType</span></span>
<span data-ttu-id="2db32-128">Bir uzantı kaynağı için kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2db32-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="2db32-129">Kaynağın uzantı kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2db32-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="2db32-130">Örneğin: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="2db32-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="2db32-131">-Force</span><span class="sxs-lookup"><span data-stu-id="2db32-131">-Force</span></span>
<span data-ttu-id="2db32-132">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="2db32-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2db32-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="2db32-133">-ODataQuery</span></span>
<span data-ttu-id="2db32-134">Açık bir veri Protokolü (OData) stil filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="2db32-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="2db32-135">Bu cmdlet, bu değeri diğer tüm filtrelere ek olarak isteğe ekler.</span><span class="sxs-lookup"><span data-stu-id="2db32-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="2db32-136">-Pre-</span><span class="sxs-lookup"><span data-stu-id="2db32-136">-Pre</span></span>
<span data-ttu-id="2db32-137">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2db32-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2db32-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2db32-138">-ResourceGroupName</span></span>
<span data-ttu-id="2db32-139">Bu cmdlet 'in kaynağı kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2db32-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="2db32-140">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2db32-140">-ResourceId</span></span>
<span data-ttu-id="2db32-141">Bu cmdlet 'in kaldırdığı kaynağın tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2db32-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="2db32-142">KIMLIK, aşağıdaki örnekte olduğu gibi aboneliği içerir: `/subscriptions/` ABONELIK kimliği`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="2db32-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="2db32-143">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="2db32-143">-ResourceName</span></span>
<span data-ttu-id="2db32-144">Bu cmdlet 'in kaldırdığı kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2db32-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="2db32-145">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="2db32-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="2db32-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="2db32-146">-ResourceType</span></span>
<span data-ttu-id="2db32-147">Bu cmdlet 'in kaldırdığı kaynağın türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2db32-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="2db32-148">Örneğin, veritabanı için kaynak türü aşağıdaki gibidir: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="2db32-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="2db32-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="2db32-149">-TenantLevel</span></span>
<span data-ttu-id="2db32-150">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="2db32-150">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="2db32-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="2db32-151">-Confirm</span></span>
<span data-ttu-id="2db32-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2db32-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2db32-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2db32-153">-WhatIf</span></span>
<span data-ttu-id="2db32-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2db32-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2db32-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2db32-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2db32-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2db32-156">CommonParameters</span></span>
<span data-ttu-id="2db32-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2db32-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2db32-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2db32-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2db32-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2db32-159">INPUTS</span></span>

### <span data-ttu-id="2db32-160">System. String</span><span class="sxs-lookup"><span data-stu-id="2db32-160">System.String</span></span>

## <span data-ttu-id="2db32-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2db32-161">OUTPUTS</span></span>

### <span data-ttu-id="2db32-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2db32-162">System.Boolean</span></span>

## <span data-ttu-id="2db32-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2db32-163">NOTES</span></span>

## <span data-ttu-id="2db32-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2db32-164">RELATED LINKS</span></span>

[<span data-ttu-id="2db32-165">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="2db32-165">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="2db32-166">Taşı-Azkaynak</span><span class="sxs-lookup"><span data-stu-id="2db32-166">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="2db32-167">Yeni-aza kaynağı</span><span class="sxs-lookup"><span data-stu-id="2db32-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="2db32-168">Set-Azkaynak</span><span class="sxs-lookup"><span data-stu-id="2db32-168">Set-AzResource</span></span>](./Set-AzResource.md)

