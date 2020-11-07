---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/invoke-azurermresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
ms.openlocfilehash: 7f2aa8299e3e4dcbdc6d326dfedf76092a65f351
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763233"
---
# <span data-ttu-id="02327-101">Invoke-AzureRmResourceAction</span><span class="sxs-lookup"><span data-stu-id="02327-101">Invoke-AzureRmResourceAction</span></span>

## <span data-ttu-id="02327-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02327-102">SYNOPSIS</span></span>
<span data-ttu-id="02327-103">Kaynakta bir eylem çağırır.</span><span class="sxs-lookup"><span data-stu-id="02327-103">Invokes an action on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02327-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02327-104">SYNTAX</span></span>

### <span data-ttu-id="02327-105">Byresourceıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="02327-105">ByResourceId (Default)</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String>
 [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02327-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="02327-106">BySubscriptionLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02327-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="02327-107">ByTenantLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02327-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="02327-108">DESCRIPTION</span></span>
<span data-ttu-id="02327-109">**Invoke-AzureRmResourceAction** cmdlet 'ı belirtilen Azure kaynağında bir eylem çağırır.</span><span class="sxs-lookup"><span data-stu-id="02327-109">The **Invoke-AzureRmResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>

<span data-ttu-id="02327-110">Desteklenen eylemlerin listesini almak için, Azure Resource Explorer aracını kullanın.</span><span class="sxs-lookup"><span data-stu-id="02327-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="02327-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02327-111">EXAMPLES</span></span>

## <span data-ttu-id="02327-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02327-112">PARAMETERS</span></span>

### <span data-ttu-id="02327-113">-Eylem</span><span class="sxs-lookup"><span data-stu-id="02327-113">-Action</span></span>
<span data-ttu-id="02327-114">Çağrılacak eylemin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="02327-114">Specifies the name of the action to invoke.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ActionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02327-115">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="02327-115">-ApiVersion</span></span>
<span data-ttu-id="02327-116">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="02327-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="02327-117">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="02327-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="02327-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02327-118">-DefaultProfile</span></span>
<span data-ttu-id="02327-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="02327-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02327-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="02327-120">-ExtensionResourceName</span></span>
<span data-ttu-id="02327-121">Bu cmdlet 'in eylem çağırdıkları kaynak için bir uzantı kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="02327-121">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="02327-122">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="02327-122">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="02327-123">sunucu adı `/` veritabanı adı</span><span class="sxs-lookup"><span data-stu-id="02327-123">server name`/`database name</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02327-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="02327-124">-ExtensionResourceType</span></span>
<span data-ttu-id="02327-125">Uzantı kaynağının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="02327-125">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="02327-126">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="02327-126">For instance:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02327-127">-Force</span><span class="sxs-lookup"><span data-stu-id="02327-127">-Force</span></span>
<span data-ttu-id="02327-128">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="02327-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="02327-129">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="02327-129">-InformationAction</span></span>
<span data-ttu-id="02327-130">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="02327-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="02327-131">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="02327-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="02327-132">'A</span><span class="sxs-lookup"><span data-stu-id="02327-132">Continue</span></span>
- <span data-ttu-id="02327-133">Manıza</span><span class="sxs-lookup"><span data-stu-id="02327-133">Ignore</span></span>
- <span data-ttu-id="02327-134">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="02327-134">Inquire</span></span>
- <span data-ttu-id="02327-135">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="02327-135">SilentlyContinue</span></span>
- <span data-ttu-id="02327-136">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="02327-136">Stop</span></span>
- <span data-ttu-id="02327-137">Biliriz</span><span class="sxs-lookup"><span data-stu-id="02327-137">Suspend</span></span>

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

### <span data-ttu-id="02327-138">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="02327-138">-InformationVariable</span></span>
<span data-ttu-id="02327-139">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="02327-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="02327-140">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="02327-140">-ODataQuery</span></span>
<span data-ttu-id="02327-141">Açık bir veri Protokolü (OData) stil filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="02327-141">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="02327-142">Bu cmdlet, bu değeri diğer tüm filtrelere ek olarak isteğe ekler.</span><span class="sxs-lookup"><span data-stu-id="02327-142">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="02327-143">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="02327-143">-Parameters</span></span>
<span data-ttu-id="02327-144">Bu cmdlet 'in çağırmasına ilişkin eylem için parametreleri karma bir tablo olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="02327-144">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Object

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02327-145">-Pre-</span><span class="sxs-lookup"><span data-stu-id="02327-145">-Pre</span></span>
<span data-ttu-id="02327-146">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="02327-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="02327-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02327-147">-ResourceGroupName</span></span>
<span data-ttu-id="02327-148">Bu cmdlet 'in eylemi çağırdıkları kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="02327-148">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02327-149">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="02327-149">-ResourceId</span></span>
<span data-ttu-id="02327-150">Bu cmdlet 'in eylem çağırdıkları kaynağın tam kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="02327-150">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="02327-151">KIMLIK, aşağıdaki örnekte olduğu gibi aboneliği içerir:</span><span class="sxs-lookup"><span data-stu-id="02327-151">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="02327-152">`/subscriptions/`abonelik KIMLIĞI`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="02327-152">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02327-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="02327-153">-ResourceName</span></span>
<span data-ttu-id="02327-154">Bu cmdlet 'in eylem çağırdıkları kaynak kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="02327-154">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="02327-155">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="02327-155">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02327-156">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="02327-156">-ResourceType</span></span>
<span data-ttu-id="02327-157">Kaynağın türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="02327-157">Specifies the type of the resource.</span></span>
<span data-ttu-id="02327-158">Örneğin, veritabanı için kaynak türü aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="02327-158">For instance, for a database, the resource type is as follows:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02327-159">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="02327-159">-TenantLevel</span></span>
<span data-ttu-id="02327-160">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="02327-160">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02327-161">-Onay</span><span class="sxs-lookup"><span data-stu-id="02327-161">-Confirm</span></span>
<span data-ttu-id="02327-162">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="02327-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02327-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02327-163">-WhatIf</span></span>
<span data-ttu-id="02327-164">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="02327-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02327-165">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="02327-165">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02327-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02327-166">CommonParameters</span></span>
<span data-ttu-id="02327-167">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02327-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02327-168">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02327-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02327-169">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02327-169">INPUTS</span></span>

### <span data-ttu-id="02327-170">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="02327-170">None</span></span>
<span data-ttu-id="02327-171">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="02327-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="02327-172">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02327-172">OUTPUTS</span></span>

### <span data-ttu-id="02327-173">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="02327-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="02327-174">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02327-174">NOTES</span></span>

## <span data-ttu-id="02327-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02327-175">RELATED LINKS</span></span>
