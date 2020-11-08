---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
ms.openlocfilehash: 506287812f684a778fdb96e750aac34049912b58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279727"
---
# <span data-ttu-id="91c93-101">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="91c93-101">Remove-AzApiManagementApiFromGateway</span></span>

## <span data-ttu-id="91c93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91c93-102">SYNOPSIS</span></span>
<span data-ttu-id="91c93-103">Ağ geçidine bir API ekler.</span><span class="sxs-lookup"><span data-stu-id="91c93-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="91c93-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="91c93-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91c93-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="91c93-105">DESCRIPTION</span></span>
<span data-ttu-id="91c93-106">**Remove-Azapsananagementapifromgateway** cmdlet 'INE bir API ekler.</span><span class="sxs-lookup"><span data-stu-id="91c93-106">The **Remove-AzApiManagementApiFromGateway** cmdlet attaches an API to a gateway.</span></span>

## <span data-ttu-id="91c93-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="91c93-107">EXAMPLES</span></span>

### <span data-ttu-id="91c93-108">Örnek 1: ağ geçidinden API kaldırma</span><span class="sxs-lookup"><span data-stu-id="91c93-108">Example 1: Remove an API from a gateway</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="91c93-109">Bu komut ağ geçidinden belirtilen API 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="91c93-109">This command removes the specified API from a gateway.</span></span>

## <span data-ttu-id="91c93-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="91c93-110">PARAMETERS</span></span>

### <span data-ttu-id="91c93-111">-Apııd</span><span class="sxs-lookup"><span data-stu-id="91c93-111">-ApiId</span></span>
<span data-ttu-id="91c93-112">Ağ geçidinden kaldırılacak mevcut API 'lerin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="91c93-112">Identifier of existing APIs to remove from the Gateway.</span></span>
<span data-ttu-id="91c93-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="91c93-113">This parameter is required.</span></span>

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

### <span data-ttu-id="91c93-114">-Context</span><span class="sxs-lookup"><span data-stu-id="91c93-114">-Context</span></span>
<span data-ttu-id="91c93-115">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="91c93-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="91c93-116">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="91c93-116">This parameter is required.</span></span>

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

### <span data-ttu-id="91c93-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91c93-117">-DefaultProfile</span></span>
<span data-ttu-id="91c93-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="91c93-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91c93-119">-Gatewayıd</span><span class="sxs-lookup"><span data-stu-id="91c93-119">-GatewayId</span></span>
<span data-ttu-id="91c93-120">API 'yi kaldırmak için mevcut ağ geçidinin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="91c93-120">Identifier of existing Gateway to remove API from.</span></span>
<span data-ttu-id="91c93-121">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="91c93-121">This parameter is required.</span></span>

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

### <span data-ttu-id="91c93-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="91c93-122">-PassThru</span></span>
<span data-ttu-id="91c93-123">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="91c93-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="91c93-124">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="91c93-124">This parameter is optional.</span></span>
<span data-ttu-id="91c93-125">Varsayılan değer: false.</span><span class="sxs-lookup"><span data-stu-id="91c93-125">Default value is false.</span></span>

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

### <span data-ttu-id="91c93-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="91c93-126">-Confirm</span></span>
<span data-ttu-id="91c93-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="91c93-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91c93-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91c93-128">-WhatIf</span></span>
<span data-ttu-id="91c93-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="91c93-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91c93-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="91c93-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91c93-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91c93-131">CommonParameters</span></span>
<span data-ttu-id="91c93-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="91c93-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91c93-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="91c93-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91c93-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="91c93-134">INPUTS</span></span>

### <span data-ttu-id="91c93-135">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="91c93-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="91c93-136">System. String</span><span class="sxs-lookup"><span data-stu-id="91c93-136">System.String</span></span>

### <span data-ttu-id="91c93-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="91c93-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="91c93-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="91c93-138">OUTPUTS</span></span>

### <span data-ttu-id="91c93-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="91c93-139">System.Boolean</span></span>

## <span data-ttu-id="91c93-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="91c93-140">NOTES</span></span>

## <span data-ttu-id="91c93-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="91c93-141">RELATED LINKS</span></span>
