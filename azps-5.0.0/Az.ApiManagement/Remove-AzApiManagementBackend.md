---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
ms.openlocfilehash: 073b32936be1e1614e495ca680a250498742ba66
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322723"
---
# <span data-ttu-id="735df-101">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="735df-101">Remove-AzApiManagementBackend</span></span>

## <span data-ttu-id="735df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="735df-102">SYNOPSIS</span></span>
<span data-ttu-id="735df-103">Arka uç 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="735df-103">Removes a Backend.</span></span>

## <span data-ttu-id="735df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="735df-104">SYNTAX</span></span>

```
Remove-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="735df-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="735df-105">DESCRIPTION</span></span>
<span data-ttu-id="735df-106">Tanımlayıcının belirttiği arka uç API yönetiminden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="735df-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="735df-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="735df-107">EXAMPLES</span></span>

### <span data-ttu-id="735df-108">Örnek 1: arka uç 123</span><span class="sxs-lookup"><span data-stu-id="735df-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="735df-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="735df-109">PARAMETERS</span></span>

### <span data-ttu-id="735df-110">-Backenmuydunuz</span><span class="sxs-lookup"><span data-stu-id="735df-110">-BackendId</span></span>
<span data-ttu-id="735df-111">Var olan arka ucun tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="735df-111">Identifier of existing backend.</span></span>
<span data-ttu-id="735df-112">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="735df-112">This parameter is required.</span></span>

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

### <span data-ttu-id="735df-113">-Context</span><span class="sxs-lookup"><span data-stu-id="735df-113">-Context</span></span>
<span data-ttu-id="735df-114">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="735df-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="735df-115">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="735df-115">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="735df-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="735df-116">-DefaultProfile</span></span>
<span data-ttu-id="735df-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="735df-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="735df-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="735df-118">-PassThru</span></span>
<span data-ttu-id="735df-119">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="735df-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="735df-120">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="735df-120">This parameter is optional.</span></span>
<span data-ttu-id="735df-121">Varsayılan değer: false.</span><span class="sxs-lookup"><span data-stu-id="735df-121">Default value is false.</span></span>

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

### <span data-ttu-id="735df-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="735df-122">-Confirm</span></span>
<span data-ttu-id="735df-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="735df-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="735df-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="735df-124">-WhatIf</span></span>
<span data-ttu-id="735df-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="735df-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="735df-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="735df-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="735df-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="735df-127">CommonParameters</span></span>
<span data-ttu-id="735df-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="735df-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="735df-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="735df-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="735df-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="735df-130">INPUTS</span></span>

### <span data-ttu-id="735df-131">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="735df-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="735df-132">System. String</span><span class="sxs-lookup"><span data-stu-id="735df-132">System.String</span></span>

### <span data-ttu-id="735df-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="735df-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="735df-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="735df-134">OUTPUTS</span></span>

### <span data-ttu-id="735df-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="735df-135">System.Boolean</span></span>

## <span data-ttu-id="735df-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="735df-136">NOTES</span></span>

## <span data-ttu-id="735df-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="735df-137">RELATED LINKS</span></span>

[<span data-ttu-id="735df-138">Get-Azapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="735df-138">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="735df-139">Yeni-Azsız arka uç</span><span class="sxs-lookup"><span data-stu-id="735df-139">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="735df-140">Yeni-Azapsananagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="735df-140">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="735df-141">Yeni-Azapsananagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="735df-141">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="735df-142">Set-Azapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="735df-142">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)
