---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
ms.openlocfilehash: ffca6c1bc32d809f7bbb93c3b76dd9490f9fafb8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324028"
---
# <span data-ttu-id="c5e1c-101">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="c5e1c-101">Remove-AzApiManagementCache</span></span>

## <span data-ttu-id="c5e1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="c5e1c-103">Önbellek varlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c5e1c-103">Removes the cache entity.</span></span>

## <span data-ttu-id="c5e1c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c5e1c-104">SYNTAX</span></span>

### <span data-ttu-id="c5e1c-105">ContextParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c5e1c-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5e1c-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5e1c-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementCache -InputObject <PsApiManagementCache> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5e1c-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c5e1c-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementCache -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5e1c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c5e1c-108">DESCRIPTION</span></span>
<span data-ttu-id="c5e1c-109">**Remove-Azapsananagementcache** cmdlet 'ini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c5e1c-109">The cmdlet **Remove-AzApiManagementCache** removes the cache entity.</span></span>

## <span data-ttu-id="c5e1c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c5e1c-110">EXAMPLES</span></span>

### <span data-ttu-id="c5e1c-111">Örnek 1: önbellek varlığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="c5e1c-111">Example 1 : Remove the Cache entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCache -Context $apimContext -CacheId "centralus"
```

<span data-ttu-id="c5e1c-112">Bu cmdlet, önbelleği `centralus` API yönetim hizmetinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c5e1c-112">This cmdlet remove the cache `centralus` from Api Management service.</span></span>

## <span data-ttu-id="c5e1c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c5e1c-113">PARAMETERS</span></span>

### <span data-ttu-id="c5e1c-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="c5e1c-114">-CacheId</span></span>
<span data-ttu-id="c5e1c-115">Mevcut CacheId 'nin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="c5e1c-115">Identifier of existing cacheId.</span></span>
<span data-ttu-id="c5e1c-116">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="c5e1c-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e1c-117">-Context</span><span class="sxs-lookup"><span data-stu-id="c5e1c-117">-Context</span></span>
<span data-ttu-id="c5e1c-118">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="c5e1c-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c5e1c-119">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="c5e1c-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e1c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5e1c-120">-DefaultProfile</span></span>
<span data-ttu-id="c5e1c-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c5e1c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5e1c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5e1c-122">-InputObject</span></span>
<span data-ttu-id="c5e1c-123">PsApiManagementCache örneği.</span><span class="sxs-lookup"><span data-stu-id="c5e1c-123">Instance of PsApiManagementCache.</span></span> <span data-ttu-id="c5e1c-124">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="c5e1c-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e1c-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c5e1c-125">-PassThru</span></span>
<span data-ttu-id="c5e1c-126">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="c5e1c-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="c5e1c-127">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="c5e1c-127">This parameter is optional.</span></span>
<span data-ttu-id="c5e1c-128">Varsayılan değer: false.</span><span class="sxs-lookup"><span data-stu-id="c5e1c-128">Default value is false.</span></span>

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

### <span data-ttu-id="c5e1c-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c5e1c-129">-ResourceId</span></span>
<span data-ttu-id="c5e1c-130">Önbelleğin Kolonu.</span><span class="sxs-lookup"><span data-stu-id="c5e1c-130">Arm ResourceId of Cache.</span></span> <span data-ttu-id="c5e1c-131">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="c5e1c-131">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e1c-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="c5e1c-132">-Confirm</span></span>
<span data-ttu-id="c5e1c-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c5e1c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5e1c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5e1c-134">-WhatIf</span></span>
<span data-ttu-id="c5e1c-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c5e1c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5e1c-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c5e1c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5e1c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5e1c-137">CommonParameters</span></span>
<span data-ttu-id="c5e1c-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c5e1c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5e1c-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c5e1c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5e1c-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c5e1c-140">INPUTS</span></span>

### <span data-ttu-id="c5e1c-141">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="c5e1c-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c5e1c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c5e1c-142">System.String</span></span>

### <span data-ttu-id="c5e1c-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c5e1c-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c5e1c-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c5e1c-144">OUTPUTS</span></span>

### <span data-ttu-id="c5e1c-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c5e1c-145">System.Boolean</span></span>

## <span data-ttu-id="c5e1c-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c5e1c-146">NOTES</span></span>

## <span data-ttu-id="c5e1c-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c5e1c-147">RELATED LINKS</span></span>

[<span data-ttu-id="c5e1c-148">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="c5e1c-148">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="c5e1c-149">Get-Azapsananagementcache</span><span class="sxs-lookup"><span data-stu-id="c5e1c-149">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="c5e1c-150">Güncelleştirme-Azapsananagementcache</span><span class="sxs-lookup"><span data-stu-id="c5e1c-150">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
