---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
ms.openlocfilehash: 1861b048a1782f8962708ae5ed2bbd16ebc178b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762197"
---
# <span data-ttu-id="08b3e-101">Invoke-AzureRmResourceAction</span><span class="sxs-lookup"><span data-stu-id="08b3e-101">Invoke-AzureRmResourceAction</span></span>

## <span data-ttu-id="08b3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08b3e-102">SYNOPSIS</span></span>
<span data-ttu-id="08b3e-103">Kaynakta bir eylem çağırır.</span><span class="sxs-lookup"><span data-stu-id="08b3e-103">Invokes an action on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08b3e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="08b3e-104">SYNTAX</span></span>

### <span data-ttu-id="08b3e-105">Kaynak kimliği. (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="08b3e-105">The resource Id. (Default)</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String>
 [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08b3e-106">Abonelik düzeyinde bulunan kaynaktır.</span><span class="sxs-lookup"><span data-stu-id="08b3e-106">Resource that resides at the subscription level.</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08b3e-107">Kiracı düzeyinde bulunan kaynaktır.</span><span class="sxs-lookup"><span data-stu-id="08b3e-107">Resource that resides at the tenant level.</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08b3e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="08b3e-108">DESCRIPTION</span></span>
<span data-ttu-id="08b3e-109">**Invoke-AzureRmResourceAction** cmdlet 'ı belirtilen Azure kaynağında bir eylem çağırır.</span><span class="sxs-lookup"><span data-stu-id="08b3e-109">The **Invoke-AzureRmResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>

<span data-ttu-id="08b3e-110">Desteklenen eylemlerin listesini almak için, Azure Resource Explorer aracını kullanın.</span><span class="sxs-lookup"><span data-stu-id="08b3e-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="08b3e-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="08b3e-111">EXAMPLES</span></span>

## <span data-ttu-id="08b3e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="08b3e-112">PARAMETERS</span></span>

### <span data-ttu-id="08b3e-113">-Eylem</span><span class="sxs-lookup"><span data-stu-id="08b3e-113">-Action</span></span>
<span data-ttu-id="08b3e-114">Çağrılacak eylemin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="08b3e-114">Specifies the name of the action to invoke.</span></span>

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

### <span data-ttu-id="08b3e-115">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="08b3e-115">-ApiVersion</span></span>
<span data-ttu-id="08b3e-116">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="08b3e-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="08b3e-117">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="08b3e-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="08b3e-118">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="08b3e-118">-ExtensionResourceName</span></span>
<span data-ttu-id="08b3e-119">Bu cmdlet 'in eylem çağırdıkları kaynak için bir uzantı kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="08b3e-119">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="08b3e-120">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="08b3e-120">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="08b3e-121">sunucu adı `/` veritabanı adı</span><span class="sxs-lookup"><span data-stu-id="08b3e-121">server name`/`database name</span></span>

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

### <span data-ttu-id="08b3e-122">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="08b3e-122">-ExtensionResourceType</span></span>
<span data-ttu-id="08b3e-123">Uzantı kaynağının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="08b3e-123">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="08b3e-124">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="08b3e-124">For instance:</span></span> 

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

### <span data-ttu-id="08b3e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="08b3e-125">-Force</span></span>
<span data-ttu-id="08b3e-126">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="08b3e-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="08b3e-127">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="08b3e-127">-InformationAction</span></span>
<span data-ttu-id="08b3e-128">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="08b3e-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="08b3e-129">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="08b3e-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="08b3e-130">'A</span><span class="sxs-lookup"><span data-stu-id="08b3e-130">Continue</span></span>
- <span data-ttu-id="08b3e-131">Manıza</span><span class="sxs-lookup"><span data-stu-id="08b3e-131">Ignore</span></span>
- <span data-ttu-id="08b3e-132">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="08b3e-132">Inquire</span></span>
- <span data-ttu-id="08b3e-133">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="08b3e-133">SilentlyContinue</span></span>
- <span data-ttu-id="08b3e-134">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="08b3e-134">Stop</span></span>
- <span data-ttu-id="08b3e-135">Biliriz</span><span class="sxs-lookup"><span data-stu-id="08b3e-135">Suspend</span></span>

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

### <span data-ttu-id="08b3e-136">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="08b3e-136">-InformationVariable</span></span>
<span data-ttu-id="08b3e-137">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="08b3e-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="08b3e-138">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="08b3e-138">-ODataQuery</span></span>
<span data-ttu-id="08b3e-139">Açık bir veri Protokolü (OData) stil filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="08b3e-139">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="08b3e-140">Bu cmdlet, bu değeri diğer tüm filtrelere ek olarak isteğe ekler.</span><span class="sxs-lookup"><span data-stu-id="08b3e-140">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="08b3e-141">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="08b3e-141">-Parameters</span></span>
<span data-ttu-id="08b3e-142">Bu cmdlet 'in çağırmasına ilişkin eylem için parametreleri karma bir tablo olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="08b3e-142">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

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

### <span data-ttu-id="08b3e-143">-Pre-</span><span class="sxs-lookup"><span data-stu-id="08b3e-143">-Pre</span></span>
<span data-ttu-id="08b3e-144">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="08b3e-144">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="08b3e-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08b3e-145">-ResourceGroupName</span></span>
<span data-ttu-id="08b3e-146">Bu cmdlet 'in eylemi çağırdıkları kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="08b3e-146">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="08b3e-147">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="08b3e-147">-ResourceId</span></span>
<span data-ttu-id="08b3e-148">Bu cmdlet 'in eylem çağırdıkları kaynağın tam kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="08b3e-148">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="08b3e-149">KIMLIK, aşağıdaki örnekte olduğu gibi aboneliği içerir:</span><span class="sxs-lookup"><span data-stu-id="08b3e-149">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="08b3e-150">`/subscriptions/`abonelik KIMLIĞI`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="08b3e-150">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="08b3e-151">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="08b3e-151">-ResourceName</span></span>
<span data-ttu-id="08b3e-152">Bu cmdlet 'in eylem çağırdıkları kaynak kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="08b3e-152">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="08b3e-153">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="08b3e-153">For instance, to specify a database, use the following format:</span></span> 

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

### <span data-ttu-id="08b3e-154">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="08b3e-154">-ResourceType</span></span>
<span data-ttu-id="08b3e-155">Kaynağın türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="08b3e-155">Specifies the type of the resource.</span></span>
<span data-ttu-id="08b3e-156">Örneğin, veritabanı için kaynak türü aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="08b3e-156">For instance, for a database, the resource type is as follows:</span></span> 

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

### <span data-ttu-id="08b3e-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="08b3e-157">-TenantLevel</span></span>
<span data-ttu-id="08b3e-158">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="08b3e-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="08b3e-159">-Onay</span><span class="sxs-lookup"><span data-stu-id="08b3e-159">-Confirm</span></span>
<span data-ttu-id="08b3e-160">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="08b3e-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08b3e-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08b3e-161">-WhatIf</span></span>
<span data-ttu-id="08b3e-162">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="08b3e-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08b3e-163">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="08b3e-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08b3e-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08b3e-164">-DefaultProfile</span></span>
<span data-ttu-id="08b3e-165">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="08b3e-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08b3e-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08b3e-166">CommonParameters</span></span>
<span data-ttu-id="08b3e-167">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="08b3e-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08b3e-168">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08b3e-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08b3e-169">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="08b3e-169">INPUTS</span></span>

## <span data-ttu-id="08b3e-170">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="08b3e-170">OUTPUTS</span></span>

### <span data-ttu-id="08b3e-171">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="08b3e-171">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="08b3e-172">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="08b3e-172">NOTES</span></span>

## <span data-ttu-id="08b3e-173">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="08b3e-173">RELATED LINKS</span></span>

