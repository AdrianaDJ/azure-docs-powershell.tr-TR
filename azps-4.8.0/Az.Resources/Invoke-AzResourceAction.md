---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/invoke-azresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
ms.openlocfilehash: 2feb6c48927c1cb5e092414c358b32912892a908
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274679"
---
# <span data-ttu-id="0849d-101">Invoke-AzResourceAction</span><span class="sxs-lookup"><span data-stu-id="0849d-101">Invoke-AzResourceAction</span></span>

## <span data-ttu-id="0849d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0849d-102">SYNOPSIS</span></span>
<span data-ttu-id="0849d-103">Kaynakta bir eylem çağırır.</span><span class="sxs-lookup"><span data-stu-id="0849d-103">Invokes an action on a resource.</span></span>

## <span data-ttu-id="0849d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0849d-104">SYNTAX</span></span>

### <span data-ttu-id="0849d-105">Byresourceıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0849d-105">ByResourceId (Default)</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0849d-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="0849d-106">BySubscriptionLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0849d-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="0849d-107">ByTenantLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0849d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0849d-108">DESCRIPTION</span></span>
<span data-ttu-id="0849d-109">**Invoke-Azresourcesaction** cmdlet 'ı belirtilen Azure kaynağında bir eylem çağırır.</span><span class="sxs-lookup"><span data-stu-id="0849d-109">The **Invoke-AzResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="0849d-110">Desteklenen eylemlerin listesini almak için, Azure Resource Explorer aracını kullanın.</span><span class="sxs-lookup"><span data-stu-id="0849d-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="0849d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0849d-111">EXAMPLES</span></span>

### <span data-ttu-id="0849d-112">Örnek 1: RESOURCEID ile VM başlatma</span><span class="sxs-lookup"><span data-stu-id="0849d-112">Example 1: Invoke starting a VM with ResourceId</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceId /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.Compute/virtualMachines/testVM -Action start

Confirm
Are you sure you want to invoke the 'start' action on the following resource: /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Compute/virtualMachines/testVM
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="0849d-113">Bu komut, sanal makineyi {RESOURCEID} ile başlatır.</span><span class="sxs-lookup"><span data-stu-id="0849d-113">This command starts the Virtual Machine with {ResourceId}.</span></span>

### <span data-ttu-id="0849d-114">Örnek 2: ResourceName ile VM 'yi başlatma</span><span class="sxs-lookup"><span data-stu-id="0849d-114">Example 2: Invoke poweroffing a VM with ResourceName</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceGroupName testGroup -ResourceName testVM -ResourceType Microsoft.Compute/virtualMachines/ -Action Poweroff -Force
```

<span data-ttu-id="0849d-115">Bu komut, {RESOURCEID} ile sanal makineyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="0849d-115">This command stops the Virtual Machine with {ResourceId}.</span></span>
<span data-ttu-id="0849d-116">Komut *Force* parametresini belirtir, bu nedenle sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="0849d-116">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="0849d-117">Örnek 3: RESOURCEID ile kaynak sağlayıcısını kaydettirme</span><span class="sxs-lookup"><span data-stu-id="0849d-117">Example 3: Invoke registering a resource provider with ResourceId</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceId /subscriptions/{subId}/providers/Microsoft.Network -action register -Force

id                : /subscriptions/{subId}/providers/Microsoft.Network
namespace         : Microsoft.Network
authorizations    : {…}
resourceTypes     : {@{resourceType=virtualNetworks; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=publicIPAddresses; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=networkInterfaces; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=privateEndpoints; locations=System.Object[]; apiVersions=System.Object[]}…}
registrationState : Registered
```

<span data-ttu-id="0849d-118">Bu komut, "Microsoft. Network" kaynak sağlayıcısını kaydeder.</span><span class="sxs-lookup"><span data-stu-id="0849d-118">This command registers a resource provider "Microsoft.Network".</span></span>
<span data-ttu-id="0849d-119">Komut *Force* parametresini belirtir, bu nedenle sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="0849d-119">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="0849d-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0849d-120">PARAMETERS</span></span>

### <span data-ttu-id="0849d-121">-Eylem</span><span class="sxs-lookup"><span data-stu-id="0849d-121">-Action</span></span>
<span data-ttu-id="0849d-122">Çağrılacak eylemin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0849d-122">Specifies the name of the action to invoke.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ActionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0849d-123">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="0849d-123">-ApiVersion</span></span>
<span data-ttu-id="0849d-124">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0849d-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0849d-125">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="0849d-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0849d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0849d-126">-DefaultProfile</span></span>
<span data-ttu-id="0849d-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0849d-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0849d-128">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="0849d-128">-ExtensionResourceName</span></span>
<span data-ttu-id="0849d-129">Bu cmdlet 'in eylem çağırdıkları kaynak için bir uzantı kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0849d-129">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="0849d-130">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın: sunucu adı `/` veritabanı adı</span><span class="sxs-lookup"><span data-stu-id="0849d-130">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="0849d-131">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="0849d-131">-ExtensionResourceType</span></span>
<span data-ttu-id="0849d-132">Uzantı kaynağının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0849d-132">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="0849d-133">Örneğin: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="0849d-133">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="0849d-134">-Force</span><span class="sxs-lookup"><span data-stu-id="0849d-134">-Force</span></span>
<span data-ttu-id="0849d-135">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="0849d-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0849d-136">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="0849d-136">-ODataQuery</span></span>
<span data-ttu-id="0849d-137">Açık bir veri Protokolü (OData) stil filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="0849d-137">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="0849d-138">Bu cmdlet, bu değeri diğer tüm filtrelere ek olarak isteğe ekler.</span><span class="sxs-lookup"><span data-stu-id="0849d-138">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="0849d-139">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="0849d-139">-Parameters</span></span>
<span data-ttu-id="0849d-140">Bu cmdlet 'in çağırmasına ilişkin eylem için parametreleri karma bir tablo olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="0849d-140">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Object

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0849d-141">-Pre-</span><span class="sxs-lookup"><span data-stu-id="0849d-141">-Pre</span></span>
<span data-ttu-id="0849d-142">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0849d-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0849d-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0849d-143">-ResourceGroupName</span></span>
<span data-ttu-id="0849d-144">Bu cmdlet 'in eylemi çağırdıkları kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0849d-144">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="0849d-145">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0849d-145">-ResourceId</span></span>
<span data-ttu-id="0849d-146">Bu cmdlet 'in eylem çağırdıkları kaynağın tam kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0849d-146">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="0849d-147">KIMLIK, aşağıdaki örnekte olduğu gibi aboneliği içerir: `/subscriptions/` ABONELIK kimliği`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="0849d-147">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="0849d-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0849d-148">-ResourceName</span></span>
<span data-ttu-id="0849d-149">Bu cmdlet 'in eylem çağırdıkları kaynak kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0849d-149">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="0849d-150">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="0849d-150">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="0849d-151">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0849d-151">-ResourceType</span></span>
<span data-ttu-id="0849d-152">Kaynağın türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0849d-152">Specifies the type of the resource.</span></span>
<span data-ttu-id="0849d-153">Örneğin, veritabanı için kaynak türü aşağıdaki gibidir: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="0849d-153">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="0849d-154">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="0849d-154">-TenantLevel</span></span>
<span data-ttu-id="0849d-155">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="0849d-155">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="0849d-156">-Onay</span><span class="sxs-lookup"><span data-stu-id="0849d-156">-Confirm</span></span>
<span data-ttu-id="0849d-157">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0849d-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0849d-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0849d-158">-WhatIf</span></span>
<span data-ttu-id="0849d-159">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0849d-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0849d-160">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0849d-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0849d-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0849d-161">CommonParameters</span></span>
<span data-ttu-id="0849d-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0849d-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0849d-163">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0849d-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0849d-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0849d-164">INPUTS</span></span>

### <span data-ttu-id="0849d-165">System. String</span><span class="sxs-lookup"><span data-stu-id="0849d-165">System.String</span></span>

## <span data-ttu-id="0849d-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0849d-166">OUTPUTS</span></span>

### <span data-ttu-id="0849d-167">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="0849d-167">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0849d-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0849d-168">NOTES</span></span>

## <span data-ttu-id="0849d-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0849d-169">RELATED LINKS</span></span>
