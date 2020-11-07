---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: 4ff48709b02cdd0270c559ea8be2f4e269dbce2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93761994"
---
# <span data-ttu-id="1b38f-101">Remove-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1b38f-101">Remove-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="1b38f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b38f-102">SYNOPSIS</span></span>
<span data-ttu-id="1b38f-103">Belirli bir API sürüm kümesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="1b38f-103">Removes a particular Api Version Set</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b38f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b38f-104">SYNTAX</span></span>

### <span data-ttu-id="1b38f-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1b38f-105">ExpandedParameter (Default)</span></span>
```
Remove-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b38f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1b38f-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b38f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b38f-107">DESCRIPTION</span></span>

<span data-ttu-id="1b38f-108">**Remove-Azurermapsananagementapiversionset** cmdlet 'i var olan bir API sürümü kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1b38f-108">The **Remove-AzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="1b38f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b38f-109">EXAMPLES</span></span>

### <span data-ttu-id="1b38f-110">Örnek 1: API sürüm kümesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="1b38f-110">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="1b38f-111">Bu komut belirtilen Apıversionsetid ile API sürüm kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1b38f-111">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="1b38f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b38f-112">PARAMETERS</span></span>

### <span data-ttu-id="1b38f-113">-Apıversionsetid</span><span class="sxs-lookup"><span data-stu-id="1b38f-113">-ApiVersionSetId</span></span>
<span data-ttu-id="1b38f-114">API sürüm kümesinin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="1b38f-114">Identifier of the API Version Set.</span></span>
<span data-ttu-id="1b38f-115">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1b38f-115">This parameter is required.</span></span>

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

### <span data-ttu-id="1b38f-116">-Context</span><span class="sxs-lookup"><span data-stu-id="1b38f-116">-Context</span></span>
<span data-ttu-id="1b38f-117">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="1b38f-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1b38f-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1b38f-118">This parameter is required.</span></span>

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

### <span data-ttu-id="1b38f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b38f-119">-DefaultProfile</span></span>
<span data-ttu-id="1b38f-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1b38f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b38f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b38f-121">-InputObject</span></span>
<span data-ttu-id="1b38f-122">Psapimanagementapıversionset 'in örneği.</span><span class="sxs-lookup"><span data-stu-id="1b38f-122">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="1b38f-123">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1b38f-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b38f-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1b38f-124">-PassThru</span></span>
<span data-ttu-id="1b38f-125">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="1b38f-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="1b38f-126">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="1b38f-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="1b38f-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="1b38f-127">-Confirm</span></span>
<span data-ttu-id="1b38f-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1b38f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b38f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b38f-129">-WhatIf</span></span>
<span data-ttu-id="1b38f-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1b38f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b38f-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1b38f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b38f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b38f-132">CommonParameters</span></span>
<span data-ttu-id="1b38f-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b38f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b38f-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b38f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b38f-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b38f-135">INPUTS</span></span>

### <span data-ttu-id="1b38f-136">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="1b38f-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="1b38f-137">Parametreler: bağlam (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1b38f-137">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="1b38f-138">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="1b38f-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>
<span data-ttu-id="1b38f-139">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1b38f-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="1b38f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1b38f-140">System.String</span></span>

## <span data-ttu-id="1b38f-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b38f-141">OUTPUTS</span></span>

### <span data-ttu-id="1b38f-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1b38f-142">System.Boolean</span></span>

## <span data-ttu-id="1b38f-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b38f-143">NOTES</span></span>

## <span data-ttu-id="1b38f-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b38f-144">RELATED LINKS</span></span>

[<span data-ttu-id="1b38f-145">Get-Azurermapımanagementapiversionset</span><span class="sxs-lookup"><span data-stu-id="1b38f-145">Get-AzureRmApiManagementApiVersionSet</span></span>](./Get-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="1b38f-146">New-Azurermapımanagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="1b38f-146">New-AzureRmApiManagementApiVersionSet</span></span>](./New-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="1b38f-147">Set-Azurermapımanagementapiversionset</span><span class="sxs-lookup"><span data-stu-id="1b38f-147">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiVersionSet.md)
