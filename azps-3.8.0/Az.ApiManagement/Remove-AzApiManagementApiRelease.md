---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
ms.openlocfilehash: 073f93cdb13e39925ef92dc556fb06a0ac96bcae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098383"
---
# <span data-ttu-id="abda9-101">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="abda9-101">Remove-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="abda9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abda9-102">SYNOPSIS</span></span>
<span data-ttu-id="abda9-103">Belirli bir API sürümünü kaldırır</span><span class="sxs-lookup"><span data-stu-id="abda9-103">Removes a particular API Release</span></span>

## <span data-ttu-id="abda9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="abda9-104">SYNTAX</span></span>

### <span data-ttu-id="abda9-105">Byapıreleaseıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="abda9-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abda9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="abda9-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abda9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="abda9-107">DESCRIPTION</span></span>

<span data-ttu-id="abda9-108">**Remove-AzAzureRmApiManagementApiRelease** cmdlet 'i var olan bir API sürümünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="abda9-108">The **Remove-AzAzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="abda9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="abda9-109">EXAMPLES</span></span>

### <span data-ttu-id="abda9-110">Örnek 1: bir API sürümünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="abda9-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="abda9-111">Bu komut belirtilen Apııd ve ReleaseID ile API 'YI kaldırır.</span><span class="sxs-lookup"><span data-stu-id="abda9-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="abda9-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="abda9-112">PARAMETERS</span></span>

### <span data-ttu-id="abda9-113">-Apııd</span><span class="sxs-lookup"><span data-stu-id="abda9-113">-ApiId</span></span>
<span data-ttu-id="abda9-114">API tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="abda9-114">Identifier of the API.</span></span>
<span data-ttu-id="abda9-115">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="abda9-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abda9-116">-Context</span><span class="sxs-lookup"><span data-stu-id="abda9-116">-Context</span></span>
<span data-ttu-id="abda9-117">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="abda9-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="abda9-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="abda9-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abda9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abda9-119">-DefaultProfile</span></span>
<span data-ttu-id="abda9-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="abda9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abda9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abda9-121">-InputObject</span></span>
<span data-ttu-id="abda9-122">PsApiManagementApiRelease 'in örneği.</span><span class="sxs-lookup"><span data-stu-id="abda9-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="abda9-123">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="abda9-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abda9-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="abda9-124">-PassThru</span></span>
<span data-ttu-id="abda9-125">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="abda9-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="abda9-126">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="abda9-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="abda9-127">-ReleaseID</span><span class="sxs-lookup"><span data-stu-id="abda9-127">-ReleaseId</span></span>
<span data-ttu-id="abda9-128">API sürümünün tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="abda9-128">Identifier of the API Release.</span></span>
<span data-ttu-id="abda9-129">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="abda9-129">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abda9-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="abda9-130">-Confirm</span></span>
<span data-ttu-id="abda9-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="abda9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abda9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abda9-132">-WhatIf</span></span>
<span data-ttu-id="abda9-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="abda9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abda9-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="abda9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abda9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abda9-135">CommonParameters</span></span>
<span data-ttu-id="abda9-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="abda9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abda9-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="abda9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abda9-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="abda9-138">INPUTS</span></span>

### <span data-ttu-id="abda9-139">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="abda9-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="abda9-140">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapirelease</span><span class="sxs-lookup"><span data-stu-id="abda9-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

### <span data-ttu-id="abda9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="abda9-141">System.String</span></span>

## <span data-ttu-id="abda9-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="abda9-142">OUTPUTS</span></span>

### <span data-ttu-id="abda9-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="abda9-143">System.Boolean</span></span>

## <span data-ttu-id="abda9-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="abda9-144">NOTES</span></span>

## <span data-ttu-id="abda9-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="abda9-145">RELATED LINKS</span></span>

[<span data-ttu-id="abda9-146">Get-Azapimpırelease</span><span class="sxs-lookup"><span data-stu-id="abda9-146">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="abda9-147">Yeni-Azapimpırelease</span><span class="sxs-lookup"><span data-stu-id="abda9-147">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

[<span data-ttu-id="abda9-148">Set-Azapsananagementapirelease</span><span class="sxs-lookup"><span data-stu-id="abda9-148">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)