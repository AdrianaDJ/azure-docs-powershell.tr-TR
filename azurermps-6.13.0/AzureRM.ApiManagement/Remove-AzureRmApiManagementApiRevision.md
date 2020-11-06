---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: cd32f29a0202fa8c38abed43075a8623efe068a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573070"
---
# <span data-ttu-id="23dcd-101">Remove-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="23dcd-101">Remove-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="23dcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23dcd-102">SYNOPSIS</span></span>
<span data-ttu-id="23dcd-103">Belirli bir API düzeltmesi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="23dcd-103">Removed a particular API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23dcd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="23dcd-104">SYNTAX</span></span>

### <span data-ttu-id="23dcd-105">Payapya (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="23dcd-105">ByApiId (Default)</span></span>
```
Remove-AzureRmApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23dcd-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="23dcd-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiRevision -InputObject <PsApiManagementApi> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23dcd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="23dcd-107">DESCRIPTION</span></span>
<span data-ttu-id="23dcd-108">**Remove-Azurermapsananagementapirevision** cmdlet 'i, belırlı bir API düzeltmesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="23dcd-108">The cmdlet **Remove-AzureRmApiManagementApiRevision** removes a particular API revision.</span></span>

## <span data-ttu-id="23dcd-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="23dcd-109">EXAMPLES</span></span>

### <span data-ttu-id="23dcd-110">Örnek 1: API düzeltmesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="23dcd-110">Example 1: Remove an API Revision</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiRevision -Context $apimContext -ApiId "echo-api" -ApiRevision "2"
```

<span data-ttu-id="23dcd-111">Bu komut API `2` Yönetim HIZMETINDEN API 'yi kaldırır `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="23dcd-111">This command removes the `2` revision of the API `echo-api` from API Management service.</span></span>

## <span data-ttu-id="23dcd-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="23dcd-112">PARAMETERS</span></span>

### <span data-ttu-id="23dcd-113">-Apııd</span><span class="sxs-lookup"><span data-stu-id="23dcd-113">-ApiId</span></span>
<span data-ttu-id="23dcd-114">API tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="23dcd-114">Identifier of the API.</span></span>
<span data-ttu-id="23dcd-115">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="23dcd-115">This parameter is required.</span></span>

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

### <span data-ttu-id="23dcd-116">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="23dcd-116">-ApiRevision</span></span>
<span data-ttu-id="23dcd-117">API düzeltmesinin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="23dcd-117">Identifier of the API Revision.</span></span> <span data-ttu-id="23dcd-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="23dcd-118">This parameter is required.</span></span>

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

### <span data-ttu-id="23dcd-119">-Context</span><span class="sxs-lookup"><span data-stu-id="23dcd-119">-Context</span></span>
<span data-ttu-id="23dcd-120">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="23dcd-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="23dcd-121">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="23dcd-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23dcd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23dcd-122">-DefaultProfile</span></span>
<span data-ttu-id="23dcd-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="23dcd-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23dcd-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23dcd-124">-InputObject</span></span>
<span data-ttu-id="23dcd-125">PsApiManagementApiRelease 'in örneği.</span><span class="sxs-lookup"><span data-stu-id="23dcd-125">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="23dcd-126">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="23dcd-126">This parameter is required.</span></span>

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

### <span data-ttu-id="23dcd-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="23dcd-127">-PassThru</span></span>
<span data-ttu-id="23dcd-128">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="23dcd-128">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="23dcd-129">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="23dcd-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="23dcd-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="23dcd-130">-Confirm</span></span>
<span data-ttu-id="23dcd-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="23dcd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23dcd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23dcd-132">-WhatIf</span></span>
<span data-ttu-id="23dcd-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="23dcd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23dcd-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="23dcd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23dcd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23dcd-135">CommonParameters</span></span>
<span data-ttu-id="23dcd-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="23dcd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23dcd-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23dcd-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23dcd-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="23dcd-138">INPUTS</span></span>

### <span data-ttu-id="23dcd-139">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="23dcd-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="23dcd-140">System. String</span><span class="sxs-lookup"><span data-stu-id="23dcd-140">System.String</span></span>

### <span data-ttu-id="23dcd-141">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="23dcd-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="23dcd-142">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="23dcd-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="23dcd-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="23dcd-143">OUTPUTS</span></span>

### <span data-ttu-id="23dcd-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="23dcd-144">System.Boolean</span></span>

## <span data-ttu-id="23dcd-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="23dcd-145">NOTES</span></span>

## <span data-ttu-id="23dcd-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="23dcd-146">RELATED LINKS</span></span>

[<span data-ttu-id="23dcd-147">Get-Azurermapımanagementapirevision</span><span class="sxs-lookup"><span data-stu-id="23dcd-147">Get-AzureRmApiManagementApiRevision</span></span>](./Get-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="23dcd-148">New-Azurermapımanagementapirevision</span><span class="sxs-lookup"><span data-stu-id="23dcd-148">New-AzureRmApiManagementApiRevision</span></span>](./New-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="23dcd-149">Set-Azurermapımanagementapirevision</span><span class="sxs-lookup"><span data-stu-id="23dcd-149">Set-AzureRmApiManagementApiRevision</span></span>](./Set-AzureRmApiManagementApiRevision.md)
