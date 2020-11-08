---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
ms.openlocfilehash: 86eb7842bbd0dc29beb8572f4f34d53190ca06e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104159"
---
# <span data-ttu-id="e902c-101">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="e902c-101">Update-AzApiManagementCache</span></span>

## <span data-ttu-id="e902c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e902c-102">SYNOPSIS</span></span>
<span data-ttu-id="e902c-103">API Yönetim hizmetinde bir önbelleği güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e902c-103">updates a cache in Api Management service.</span></span>

## <span data-ttu-id="e902c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e902c-104">SYNTAX</span></span>

### <span data-ttu-id="e902c-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e902c-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e902c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e902c-106">ByInputObject</span></span>
```
Update-AzApiManagementCache -InputObject <PsApiManagementCache> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e902c-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="e902c-107">ByResourceId</span></span>
```
Update-AzApiManagementCache -ResourceId <String> [-ConnectionString <String>] [-AzureRedisResourceId <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e902c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e902c-108">DESCRIPTION</span></span>
<span data-ttu-id="e902c-109">Cmdlet **güncelleştirmesi-Azapsananagementcache** , bir önbelleği bir ön.</span><span class="sxs-lookup"><span data-stu-id="e902c-109">The cmdlet **Update-AzApiManagementCache** updates a cache in the ApiManagement service.</span></span>

## <span data-ttu-id="e902c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e902c-110">EXAMPLES</span></span>

### <span data-ttu-id="e902c-111">Örnek 1: merkezde</span><span class="sxs-lookup"><span data-stu-id="e902c-111">Example 1 : Updates the Description of the Cache in centralus</span></span>
```powershell
PS D:\github\azure-powershell> $context=New-AzApiManagementContext -ResourceGroupName Api-Default-Central-US -ServiceName contoso
PS D:\github\azure-powershell> Update-AzApiManagementCache -Context $context -CacheId centralus -Description "Team new cache" -PassThru


CacheId              : centralus
Description          : Team new cache
ConnectionString     : {{5cc19889e6ed3b0524c3f7d3}}
AzureRedisResourceId :
Id                   : /subscriptions/subid/resourceGroups/Api-Default-Central-US/providers/M
                       icrosoft.ApiManagement/service/contoso/caches/centralus
ResourceGroupName    : Api-Default-Central-US
ServiceName          : contoso
```

<span data-ttu-id="e902c-112">ABD 'deki önbelleğin açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e902c-112">Updates the description of the Cache in Central US.</span></span>

## <span data-ttu-id="e902c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e902c-113">PARAMETERS</span></span>

### <span data-ttu-id="e902c-114">-Azureredisresourceıd</span><span class="sxs-lookup"><span data-stu-id="e902c-114">-AzureRedisResourceId</span></span>
<span data-ttu-id="e902c-115">Azure Redis Cache örneğinin ARM RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="e902c-115">Arm ResourceId of the Azure Redis Cache instance.</span></span>
<span data-ttu-id="e902c-116">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e902c-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e902c-117">-CacheId</span><span class="sxs-lookup"><span data-stu-id="e902c-117">-CacheId</span></span>
<span data-ttu-id="e902c-118">Yeni önbelleğin tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="e902c-118">Identifier of new cache.</span></span>
<span data-ttu-id="e902c-119">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e902c-119">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e902c-120">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="e902c-120">-ConnectionString</span></span>
<span data-ttu-id="e902c-121">Kırmızı bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="e902c-121">Redis Connection String.</span></span>
<span data-ttu-id="e902c-122">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e902c-122">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e902c-123">-Context</span><span class="sxs-lookup"><span data-stu-id="e902c-123">-Context</span></span>
<span data-ttu-id="e902c-124">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="e902c-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e902c-125">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e902c-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e902c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e902c-126">-DefaultProfile</span></span>
<span data-ttu-id="e902c-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e902c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e902c-128">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="e902c-128">-Description</span></span>
<span data-ttu-id="e902c-129">Önbellek açıklaması.</span><span class="sxs-lookup"><span data-stu-id="e902c-129">Cache Description.</span></span>
<span data-ttu-id="e902c-130">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e902c-130">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e902c-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e902c-131">-InputObject</span></span>
<span data-ttu-id="e902c-132">PsApiManagementCache örneği.</span><span class="sxs-lookup"><span data-stu-id="e902c-132">Instance of PsApiManagementCache.</span></span>
<span data-ttu-id="e902c-133">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e902c-133">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e902c-134">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e902c-134">-PassThru</span></span>
<span data-ttu-id="e902c-135">Bu örnekte, belirtilen önbelleği temsil eden Microsoft. Azure. Commands. Apsananad. ServiceManagement. model. Psapsananagementcache türü örneği çıktıya yazılır.</span><span class="sxs-lookup"><span data-stu-id="e902c-135">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache type  representing the modified cache will be written to output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e902c-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e902c-136">-ResourceId</span></span>
<span data-ttu-id="e902c-137">Önbelleğin Kolonu.</span><span class="sxs-lookup"><span data-stu-id="e902c-137">Arm ResourceId of Cache.</span></span>
<span data-ttu-id="e902c-138">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e902c-138">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e902c-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="e902c-139">-Confirm</span></span>
<span data-ttu-id="e902c-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e902c-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e902c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e902c-141">-WhatIf</span></span>
<span data-ttu-id="e902c-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e902c-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e902c-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e902c-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e902c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e902c-144">CommonParameters</span></span>
<span data-ttu-id="e902c-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e902c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e902c-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e902c-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e902c-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e902c-147">INPUTS</span></span>

### <span data-ttu-id="e902c-148">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="e902c-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e902c-149">System. String</span><span class="sxs-lookup"><span data-stu-id="e902c-149">System.String</span></span>

### <span data-ttu-id="e902c-150">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcache</span><span class="sxs-lookup"><span data-stu-id="e902c-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

### <span data-ttu-id="e902c-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e902c-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e902c-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e902c-152">OUTPUTS</span></span>

### <span data-ttu-id="e902c-153">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcache</span><span class="sxs-lookup"><span data-stu-id="e902c-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="e902c-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e902c-154">NOTES</span></span>

## <span data-ttu-id="e902c-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e902c-155">RELATED LINKS</span></span>

[<span data-ttu-id="e902c-156">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="e902c-156">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache)

[<span data-ttu-id="e902c-157">Get-Azapsananagementcache</span><span class="sxs-lookup"><span data-stu-id="e902c-157">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="e902c-158">Remove-Azapsananagementcache</span><span class="sxs-lookup"><span data-stu-id="e902c-158">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)