---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 71256ab72d8c5c6042aa6c17b184066f96b3a813
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573074"
---
# <span data-ttu-id="b38f3-101">Remove-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b38f3-101">Remove-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="b38f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b38f3-102">SYNOPSIS</span></span>
<span data-ttu-id="b38f3-103">Belirli bir API sürümünü kaldırır</span><span class="sxs-lookup"><span data-stu-id="b38f3-103">Removes a particular API Release</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b38f3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b38f3-104">SYNTAX</span></span>

### <span data-ttu-id="b38f3-105">Byapıreleaseıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b38f3-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b38f3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b38f3-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b38f3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b38f3-107">DESCRIPTION</span></span>

<span data-ttu-id="b38f3-108">**Remove-Azurermapsananagementapırelease** cmdlet 'i var olan bir API sürümünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b38f3-108">The **Remove-AzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="b38f3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b38f3-109">EXAMPLES</span></span>

### <span data-ttu-id="b38f3-110">Örnek 1: bir API sürümünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="b38f3-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="b38f3-111">Bu komut belirtilen Apııd ve ReleaseID ile API 'YI kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b38f3-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="b38f3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b38f3-112">PARAMETERS</span></span>

### <span data-ttu-id="b38f3-113">-Apııd</span><span class="sxs-lookup"><span data-stu-id="b38f3-113">-ApiId</span></span>
<span data-ttu-id="b38f3-114">API tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="b38f3-114">Identifier of the API.</span></span>
<span data-ttu-id="b38f3-115">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="b38f3-115">This parameter is required.</span></span>

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

### <span data-ttu-id="b38f3-116">-Context</span><span class="sxs-lookup"><span data-stu-id="b38f3-116">-Context</span></span>
<span data-ttu-id="b38f3-117">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="b38f3-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b38f3-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="b38f3-118">This parameter is required.</span></span>

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

### <span data-ttu-id="b38f3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b38f3-119">-DefaultProfile</span></span>
<span data-ttu-id="b38f3-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b38f3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b38f3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b38f3-121">-InputObject</span></span>
<span data-ttu-id="b38f3-122">PsApiManagementApiRelease 'in örneği.</span><span class="sxs-lookup"><span data-stu-id="b38f3-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="b38f3-123">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="b38f3-123">This parameter is required.</span></span>

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

### <span data-ttu-id="b38f3-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b38f3-124">-PassThru</span></span>
<span data-ttu-id="b38f3-125">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="b38f3-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="b38f3-126">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="b38f3-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="b38f3-127">-ReleaseID</span><span class="sxs-lookup"><span data-stu-id="b38f3-127">-ReleaseId</span></span>
<span data-ttu-id="b38f3-128">API sürümünün tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="b38f3-128">Identifier of the API Release.</span></span>
<span data-ttu-id="b38f3-129">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="b38f3-129">This parameter is required.</span></span>

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

### <span data-ttu-id="b38f3-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="b38f3-130">-Confirm</span></span>
<span data-ttu-id="b38f3-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b38f3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b38f3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b38f3-132">-WhatIf</span></span>
<span data-ttu-id="b38f3-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b38f3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b38f3-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b38f3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b38f3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b38f3-135">CommonParameters</span></span>
<span data-ttu-id="b38f3-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b38f3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b38f3-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b38f3-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b38f3-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b38f3-138">INPUTS</span></span>

### <span data-ttu-id="b38f3-139">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="b38f3-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b38f3-140">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapirelease</span><span class="sxs-lookup"><span data-stu-id="b38f3-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>
<span data-ttu-id="b38f3-141">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b38f3-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="b38f3-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b38f3-142">System.String</span></span>

## <span data-ttu-id="b38f3-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b38f3-143">OUTPUTS</span></span>

### <span data-ttu-id="b38f3-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b38f3-144">System.Boolean</span></span>

## <span data-ttu-id="b38f3-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b38f3-145">NOTES</span></span>

## <span data-ttu-id="b38f3-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b38f3-146">RELATED LINKS</span></span>

[<span data-ttu-id="b38f3-147">Get-Azurermapımanagementapirelease</span><span class="sxs-lookup"><span data-stu-id="b38f3-147">Get-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="b38f3-148">Yeni-Azurermapımanagementapirelease</span><span class="sxs-lookup"><span data-stu-id="b38f3-148">New-AzureRmApiManagementApiRelease</span></span>](./New-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="b38f3-149">Set-Azurermapımanagementapirelease</span><span class="sxs-lookup"><span data-stu-id="b38f3-149">Set-AzureRmApiManagementApiRelease</span></span>](./Set-AzureRmApiManagementApiRelease.md)
