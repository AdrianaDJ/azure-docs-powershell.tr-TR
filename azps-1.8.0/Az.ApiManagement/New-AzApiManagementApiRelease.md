---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: f816488e6334c0e9c410bb1c24f46501a1fefe85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751125"
---
# <span data-ttu-id="0b3d1-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="0b3d1-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="0b3d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b3d1-102">SYNOPSIS</span></span>
<span data-ttu-id="0b3d1-103">API düzeltmesinin API sürümünü oluşturur</span><span class="sxs-lookup"><span data-stu-id="0b3d1-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="0b3d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b3d1-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b3d1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b3d1-105">DESCRIPTION</span></span>

<span data-ttu-id="0b3d1-106">**Yeni-Azapsananagementapırelease** CMDLET 'ı API yönetim BAĞLAMıNDA bir API düzeltmesi IÇIN bir API sürümü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b3d1-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span>

## <span data-ttu-id="0b3d1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b3d1-107">EXAMPLES</span></span>

### <span data-ttu-id="0b3d1-108">Örnek 1: API düzeltmesi için API sürümü oluşturma</span><span class="sxs-lookup"><span data-stu-id="0b3d1-108">Example 1: Create an API Release for an API Revision</span></span>
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

<span data-ttu-id="0b3d1-109">Bu komut, uygulamasının düzeltilmesinde bir API sürümü oluşturur `2` `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="0b3d1-109">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="0b3d1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b3d1-110">PARAMETERS</span></span>

### <span data-ttu-id="0b3d1-111">-Apııd</span><span class="sxs-lookup"><span data-stu-id="0b3d1-111">-ApiId</span></span>
<span data-ttu-id="0b3d1-112">Yeni API için tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="0b3d1-112">Identifier for new API.</span></span>

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

### <span data-ttu-id="0b3d1-113">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="0b3d1-113">-ApiRevision</span></span>
<span data-ttu-id="0b3d1-114">API düzeltmesine yönelik tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="0b3d1-114">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="0b3d1-115">-Context</span><span class="sxs-lookup"><span data-stu-id="0b3d1-115">-Context</span></span>
<span data-ttu-id="0b3d1-116">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="0b3d1-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0b3d1-117">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="0b3d1-117">This parameter is required.</span></span>

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

### <span data-ttu-id="0b3d1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b3d1-118">-DefaultProfile</span></span>
<span data-ttu-id="0b3d1-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b3d1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b3d1-120">Not</span><span class="sxs-lookup"><span data-stu-id="0b3d1-120">-Note</span></span>
<span data-ttu-id="0b3d1-121">API sürüm notları.</span><span class="sxs-lookup"><span data-stu-id="0b3d1-121">Api Release Notes.</span></span> <span data-ttu-id="0b3d1-122">Bu parametre isteğe bağlıdır</span><span class="sxs-lookup"><span data-stu-id="0b3d1-122">This parameter is optional</span></span>

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

### <span data-ttu-id="0b3d1-123">-ReleaseID</span><span class="sxs-lookup"><span data-stu-id="0b3d1-123">-ReleaseId</span></span>
<span data-ttu-id="0b3d1-124">API sürümü için tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="0b3d1-124">Identifier for the Api Release.</span></span>
<span data-ttu-id="0b3d1-125">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="0b3d1-125">This parameter is optional.</span></span>
<span data-ttu-id="0b3d1-126">Belirtilmemişse, tanımlayıcı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="0b3d1-126">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="0b3d1-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="0b3d1-127">-Confirm</span></span>
<span data-ttu-id="0b3d1-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0b3d1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b3d1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b3d1-129">-WhatIf</span></span>
<span data-ttu-id="0b3d1-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b3d1-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b3d1-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0b3d1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b3d1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b3d1-132">CommonParameters</span></span>
<span data-ttu-id="0b3d1-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b3d1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b3d1-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b3d1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b3d1-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b3d1-135">INPUTS</span></span>

### <span data-ttu-id="0b3d1-136">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="0b3d1-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0b3d1-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0b3d1-137">System.String</span></span>

## <span data-ttu-id="0b3d1-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b3d1-138">OUTPUTS</span></span>

### <span data-ttu-id="0b3d1-139">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapirelease</span><span class="sxs-lookup"><span data-stu-id="0b3d1-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="0b3d1-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b3d1-140">NOTES</span></span>

## <span data-ttu-id="0b3d1-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b3d1-141">RELATED LINKS</span></span>

[<span data-ttu-id="0b3d1-142">Get-Azapimpırelease</span><span class="sxs-lookup"><span data-stu-id="0b3d1-142">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="0b3d1-143">Remove-Azapsananagementapırelease</span><span class="sxs-lookup"><span data-stu-id="0b3d1-143">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="0b3d1-144">Set-Azapsananagementapirelease</span><span class="sxs-lookup"><span data-stu-id="0b3d1-144">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)