---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: 784480b56a868f84f8f79a35bf7ab2c1ba2e9fbf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753551"
---
# <span data-ttu-id="19df0-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="19df0-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="19df0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19df0-102">SYNOPSIS</span></span>
<span data-ttu-id="19df0-103">API düzeltmesinin API sürümünü oluşturur</span><span class="sxs-lookup"><span data-stu-id="19df0-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="19df0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19df0-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19df0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="19df0-105">DESCRIPTION</span></span>

<span data-ttu-id="19df0-106">**Yeni-Azapsananagementapırelease** CMDLET 'ı API yönetim BAĞLAMıNDA bir API düzeltmesi IÇIN bir API sürümü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="19df0-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span> <span data-ttu-id="19df0-107">Bir sürüm, geçerli düzeltme olarak API düzeltmesini oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="19df0-107">A Release is used to make the Api Revision as Current Revision.</span></span>

## <span data-ttu-id="19df0-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19df0-108">EXAMPLES</span></span>

### <span data-ttu-id="19df0-109">Örnek 1: API düzeltmesi için API sürümü oluşturma</span><span class="sxs-lookup"><span data-stu-id="19df0-109">Example 1: Create an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRelease -Context $context  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6 -Note "Releasing version 6"


ReleaseId         : 7e4d3fbb43c146c4bf406499ef9411f4
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 1:16:29 AM
UpdatedDateTime   : 5/17/2018 1:16:29 AM
Notes             : Releasing version 6
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/7e4d3fbb43c146c4bf40649
                    9ef9411f4
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="19df0-110">Bu komut, uygulamasının düzeltilmesinde bir API sürümü oluşturur `2` `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="19df0-110">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="19df0-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19df0-111">PARAMETERS</span></span>

### <span data-ttu-id="19df0-112">-Apııd</span><span class="sxs-lookup"><span data-stu-id="19df0-112">-ApiId</span></span>
<span data-ttu-id="19df0-113">Yeni API için tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="19df0-113">Identifier for new API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19df0-114">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="19df0-114">-ApiRevision</span></span>
<span data-ttu-id="19df0-115">API düzeltmesine yönelik tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="19df0-115">Identifier for the Api Revision.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19df0-116">-Context</span><span class="sxs-lookup"><span data-stu-id="19df0-116">-Context</span></span>
<span data-ttu-id="19df0-117">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="19df0-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="19df0-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="19df0-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19df0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19df0-119">-DefaultProfile</span></span>
<span data-ttu-id="19df0-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="19df0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19df0-121">Not</span><span class="sxs-lookup"><span data-stu-id="19df0-121">-Note</span></span>
<span data-ttu-id="19df0-122">API sürüm notları.</span><span class="sxs-lookup"><span data-stu-id="19df0-122">Api Release Notes.</span></span> <span data-ttu-id="19df0-123">Bu parametre isteğe bağlıdır</span><span class="sxs-lookup"><span data-stu-id="19df0-123">This parameter is optional</span></span>

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

### <span data-ttu-id="19df0-124">-ReleaseID</span><span class="sxs-lookup"><span data-stu-id="19df0-124">-ReleaseId</span></span>
<span data-ttu-id="19df0-125">API sürümü için tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="19df0-125">Identifier for the Api Release.</span></span>
<span data-ttu-id="19df0-126">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="19df0-126">This parameter is optional.</span></span>
<span data-ttu-id="19df0-127">Belirtilmemişse, tanımlayıcı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="19df0-127">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="19df0-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="19df0-128">-Confirm</span></span>
<span data-ttu-id="19df0-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="19df0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19df0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19df0-130">-WhatIf</span></span>
<span data-ttu-id="19df0-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="19df0-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19df0-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="19df0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19df0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19df0-133">CommonParameters</span></span>
<span data-ttu-id="19df0-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19df0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19df0-135">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="19df0-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19df0-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19df0-136">INPUTS</span></span>

### <span data-ttu-id="19df0-137">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="19df0-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="19df0-138">System. String</span><span class="sxs-lookup"><span data-stu-id="19df0-138">System.String</span></span>

## <span data-ttu-id="19df0-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19df0-139">OUTPUTS</span></span>

### <span data-ttu-id="19df0-140">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapirelease</span><span class="sxs-lookup"><span data-stu-id="19df0-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="19df0-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19df0-141">NOTES</span></span>

## <span data-ttu-id="19df0-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19df0-142">RELATED LINKS</span></span>

[<span data-ttu-id="19df0-143">Get-Azapimpırelease</span><span class="sxs-lookup"><span data-stu-id="19df0-143">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="19df0-144">Remove-Azapsananagementapırelease</span><span class="sxs-lookup"><span data-stu-id="19df0-144">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="19df0-145">Set-Azapsananagementapirelease</span><span class="sxs-lookup"><span data-stu-id="19df0-145">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)