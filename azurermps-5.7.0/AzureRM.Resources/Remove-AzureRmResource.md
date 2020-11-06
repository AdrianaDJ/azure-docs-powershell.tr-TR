---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
ms.openlocfilehash: 0cf65c33ca5af99be30f7bfa85ad4ad80ff62735
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591623"
---
# <span data-ttu-id="32030-101">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="32030-101">Remove-AzureRmResource</span></span>

## <span data-ttu-id="32030-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32030-102">SYNOPSIS</span></span>
<span data-ttu-id="32030-103">Kaynağı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="32030-103">Removes a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32030-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="32030-104">SYNTAX</span></span>

### <span data-ttu-id="32030-105">Byresourceıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="32030-105">ByResourceId (Default)</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32030-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="32030-106">BySubscriptionLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="32030-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="32030-107">ByTenantLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32030-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="32030-108">DESCRIPTION</span></span>
<span data-ttu-id="32030-109">**Remove-AzureRmResource** cmdlet 'ı bir Azure kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="32030-109">The **Remove-AzureRmResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="32030-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="32030-110">EXAMPLES</span></span>

### <span data-ttu-id="32030-111">Örnek 1: Web sitesi kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="32030-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzureRmResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="32030-112">Bu komut, ContosoSite adlı Web sitesi kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="32030-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="32030-113">Örnekte, abonelik KIMLIĞI için yer tutucu değeri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="32030-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="32030-114">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32030-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="32030-115">Bu nedenle sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="32030-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="32030-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="32030-116">PARAMETERS</span></span>

### <span data-ttu-id="32030-117">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="32030-117">-ApiVersion</span></span>
<span data-ttu-id="32030-118">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="32030-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="32030-119">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="32030-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="32030-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="32030-120">-AsJob</span></span>
<span data-ttu-id="32030-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="32030-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32030-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32030-122">-DefaultProfile</span></span>
<span data-ttu-id="32030-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="32030-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32030-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="32030-124">-ExtensionResourceName</span></span>
<span data-ttu-id="32030-125">Bu cmdlet 'in kaldırdığı kaynağın uzantı kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32030-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="32030-126">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="32030-126">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="32030-127">sunucu adı `/` veritabanı adı</span><span class="sxs-lookup"><span data-stu-id="32030-127">server name`/`database name</span></span>

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

### <span data-ttu-id="32030-128">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="32030-128">-ExtensionResourceType</span></span>
<span data-ttu-id="32030-129">Bir uzantı kaynağı için kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="32030-129">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="32030-130">Kaynağın uzantı kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="32030-130">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="32030-131">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="32030-131">For instance:</span></span> 

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

### <span data-ttu-id="32030-132">-Force</span><span class="sxs-lookup"><span data-stu-id="32030-132">-Force</span></span>
<span data-ttu-id="32030-133">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="32030-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="32030-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="32030-134">-ODataQuery</span></span>
<span data-ttu-id="32030-135">Açık bir veri Protokolü (OData) stil filtresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="32030-135">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="32030-136">Bu cmdlet, bu değeri diğer tüm filtrelere ek olarak isteğe ekler.</span><span class="sxs-lookup"><span data-stu-id="32030-136">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="32030-137">-Pre-</span><span class="sxs-lookup"><span data-stu-id="32030-137">-Pre</span></span>
<span data-ttu-id="32030-138">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="32030-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="32030-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32030-139">-ResourceGroupName</span></span>
<span data-ttu-id="32030-140">Bu cmdlet 'in kaynağı kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32030-140">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="32030-141">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="32030-141">-ResourceId</span></span>
<span data-ttu-id="32030-142">Bu cmdlet 'in kaldırdığı kaynağın tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="32030-142">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="32030-143">KIMLIK, aşağıdaki örnekte olduğu gibi aboneliği içerir:</span><span class="sxs-lookup"><span data-stu-id="32030-143">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="32030-144">`/subscriptions/`abonelik KIMLIĞI`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="32030-144">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="32030-145">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="32030-145">-ResourceName</span></span>
<span data-ttu-id="32030-146">Bu cmdlet 'in kaldırdığı kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32030-146">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="32030-147">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="32030-147">For instance, to specify a database, use the following format:</span></span> 

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

### <span data-ttu-id="32030-148">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="32030-148">-ResourceType</span></span>
<span data-ttu-id="32030-149">Bu cmdlet 'in kaldırdığı kaynağın türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="32030-149">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="32030-150">Örneğin, veritabanı için kaynak türü aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="32030-150">For instance, for a database, the resource type is as follows:</span></span> 

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

### <span data-ttu-id="32030-151">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="32030-151">-TenantLevel</span></span>
<span data-ttu-id="32030-152">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="32030-152">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="32030-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="32030-153">-Confirm</span></span>
<span data-ttu-id="32030-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="32030-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32030-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32030-155">-WhatIf</span></span>
<span data-ttu-id="32030-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="32030-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32030-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="32030-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32030-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32030-158">CommonParameters</span></span>
<span data-ttu-id="32030-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="32030-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32030-160">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32030-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32030-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="32030-161">INPUTS</span></span>

### <span data-ttu-id="32030-162">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="32030-162">None</span></span>
<span data-ttu-id="32030-163">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="32030-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="32030-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="32030-164">OUTPUTS</span></span>

### <span data-ttu-id="32030-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="32030-165">System.Boolean</span></span>

## <span data-ttu-id="32030-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="32030-166">NOTES</span></span>

## <span data-ttu-id="32030-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="32030-167">RELATED LINKS</span></span>

[<span data-ttu-id="32030-168">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="32030-168">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="32030-169">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="32030-169">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="32030-170">Taşı-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="32030-170">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="32030-171">Yeni-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="32030-171">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="32030-172">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="32030-172">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


