---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRevision.md
ms.openlocfilehash: 2b8db6f5d550c91f806595c80be4beb300a95273
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753480"
---
# <span data-ttu-id="3f62c-101">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="3f62c-101">Remove-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="3f62c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f62c-102">SYNOPSIS</span></span>
<span data-ttu-id="3f62c-103">Belirli bir API düzeltmesi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="3f62c-103">Removed a particular API Revision</span></span>

## <span data-ttu-id="3f62c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3f62c-104">SYNTAX</span></span>

### <span data-ttu-id="3f62c-105">Payapya (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3f62c-105">ByApiId (Default)</span></span>
```
Remove-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f62c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3f62c-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f62c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3f62c-107">DESCRIPTION</span></span>
<span data-ttu-id="3f62c-108">**Remove-Azapsananagementapirevision** cmdlet 'i, belırlı bir API düzeltmesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3f62c-108">The cmdlet **Remove-AzApiManagementApiRevision** removes a particular API revision.</span></span>

## <span data-ttu-id="3f62c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3f62c-109">EXAMPLES</span></span>

### <span data-ttu-id="3f62c-110">Örnek 1: API düzeltmesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="3f62c-110">Example 1: Remove an API Revision</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRevision -Context $apimContext -ApiId "echo-api" -ApiRevision "2"
```

<span data-ttu-id="3f62c-111">Bu komut API `2` Yönetim HIZMETINDEN API 'yi kaldırır `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="3f62c-111">This command removes the `2` revision of the API `echo-api` from API Management service.</span></span>

## <span data-ttu-id="3f62c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3f62c-112">PARAMETERS</span></span>

### <span data-ttu-id="3f62c-113">-Apııd</span><span class="sxs-lookup"><span data-stu-id="3f62c-113">-ApiId</span></span>
<span data-ttu-id="3f62c-114">API tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="3f62c-114">Identifier of the API.</span></span>
<span data-ttu-id="3f62c-115">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="3f62c-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f62c-116">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="3f62c-116">-ApiRevision</span></span>
<span data-ttu-id="3f62c-117">API düzeltmesinin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="3f62c-117">Identifier of the API Revision.</span></span> <span data-ttu-id="3f62c-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="3f62c-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f62c-119">-Context</span><span class="sxs-lookup"><span data-stu-id="3f62c-119">-Context</span></span>
<span data-ttu-id="3f62c-120">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="3f62c-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3f62c-121">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="3f62c-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f62c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f62c-122">-DefaultProfile</span></span>
<span data-ttu-id="3f62c-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3f62c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f62c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f62c-124">-InputObject</span></span>
<span data-ttu-id="3f62c-125">PsApiManagementApiRelease 'in örneği.</span><span class="sxs-lookup"><span data-stu-id="3f62c-125">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="3f62c-126">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="3f62c-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f62c-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3f62c-127">-PassThru</span></span>
<span data-ttu-id="3f62c-128">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="3f62c-128">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="3f62c-129">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="3f62c-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="3f62c-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="3f62c-130">-Confirm</span></span>
<span data-ttu-id="3f62c-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3f62c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f62c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f62c-132">-WhatIf</span></span>
<span data-ttu-id="3f62c-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f62c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f62c-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3f62c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f62c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f62c-135">CommonParameters</span></span>
<span data-ttu-id="3f62c-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3f62c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f62c-137">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3f62c-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f62c-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3f62c-138">INPUTS</span></span>

### <span data-ttu-id="3f62c-139">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="3f62c-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3f62c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3f62c-140">System.String</span></span>

### <span data-ttu-id="3f62c-141">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="3f62c-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="3f62c-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3f62c-142">OUTPUTS</span></span>

### <span data-ttu-id="3f62c-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3f62c-143">System.Boolean</span></span>

## <span data-ttu-id="3f62c-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3f62c-144">NOTES</span></span>

## <span data-ttu-id="3f62c-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3f62c-145">RELATED LINKS</span></span>

[<span data-ttu-id="3f62c-146">Get-Azapsananagementapirevision</span><span class="sxs-lookup"><span data-stu-id="3f62c-146">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="3f62c-147">Yeni-Azapsananagementapirevision</span><span class="sxs-lookup"><span data-stu-id="3f62c-147">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="3f62c-148">Set-Azapsananagementapirevision</span><span class="sxs-lookup"><span data-stu-id="3f62c-148">Set-AzApiManagementApiRevision</span></span>](./Set-AzApiManagementApiRevision.md)