---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
ms.openlocfilehash: 9b6eac7a0c0c994797de51c936840da515ef3f4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108550"
---
# <span data-ttu-id="66d79-101">Remove-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="66d79-101">Remove-AzApiManagementGateway</span></span>

## <span data-ttu-id="66d79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66d79-102">SYNOPSIS</span></span>
<span data-ttu-id="66d79-103">Bir ağ geçidinden API ayırır.</span><span class="sxs-lookup"><span data-stu-id="66d79-103">Detaches an API from a Gateway.</span></span>

## <span data-ttu-id="66d79-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66d79-104">SYNTAX</span></span>

### <span data-ttu-id="66d79-105">ContextParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="66d79-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66d79-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66d79-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66d79-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="66d79-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGateway -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66d79-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="66d79-108">DESCRIPTION</span></span>
<span data-ttu-id="66d79-109">**Remove-Azapsananagementgateway** cmdlet 'ı bir ağ geçidinden API ayırır.</span><span class="sxs-lookup"><span data-stu-id="66d79-109">The **Remove-AzApiManagementGateway** cmdlet detaches an API from a Gateway.</span></span>

## <span data-ttu-id="66d79-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66d79-110">EXAMPLES</span></span>

### <span data-ttu-id="66d79-111">Örnek 1: varolan ağ geçidini kaldırma</span><span class="sxs-lookup"><span data-stu-id="66d79-111">Example 1: Remove an existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGateway -Context $apimContext -GatewayId "g0001" -Force
```

<span data-ttu-id="66d79-112">Bu komut, mevcut ağ geçidini kaldırır ve kullanıcıdan onay istemez.</span><span class="sxs-lookup"><span data-stu-id="66d79-112">This command removes an existing gateway and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="66d79-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66d79-113">PARAMETERS</span></span>

### <span data-ttu-id="66d79-114">-Context</span><span class="sxs-lookup"><span data-stu-id="66d79-114">-Context</span></span>
<span data-ttu-id="66d79-115">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="66d79-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="66d79-116">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="66d79-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66d79-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66d79-117">-DefaultProfile</span></span>
<span data-ttu-id="66d79-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="66d79-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66d79-119">-Gatewayıd</span><span class="sxs-lookup"><span data-stu-id="66d79-119">-GatewayId</span></span>
<span data-ttu-id="66d79-120">Mevcut ağ geçidinin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="66d79-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="66d79-121">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="66d79-121">This parameter is required.</span></span>

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

### <span data-ttu-id="66d79-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66d79-122">-InputObject</span></span>
<span data-ttu-id="66d79-123">PsApiManagementGateway örneği.</span><span class="sxs-lookup"><span data-stu-id="66d79-123">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="66d79-124">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="66d79-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66d79-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="66d79-125">-PassThru</span></span>
<span data-ttu-id="66d79-126">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="66d79-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="66d79-127">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="66d79-127">This parameter is optional.</span></span>
<span data-ttu-id="66d79-128">Varsayılan değer: false.</span><span class="sxs-lookup"><span data-stu-id="66d79-128">Default value is false.</span></span>

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

### <span data-ttu-id="66d79-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="66d79-129">-ResourceId</span></span>
<span data-ttu-id="66d79-130">Ağ geçidinin Kolonu.</span><span class="sxs-lookup"><span data-stu-id="66d79-130">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="66d79-131">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="66d79-131">This parameter is required.</span></span>

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

### <span data-ttu-id="66d79-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="66d79-132">-Confirm</span></span>
<span data-ttu-id="66d79-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="66d79-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66d79-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66d79-134">-WhatIf</span></span>
<span data-ttu-id="66d79-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="66d79-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66d79-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="66d79-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66d79-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66d79-137">CommonParameters</span></span>
<span data-ttu-id="66d79-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66d79-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66d79-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="66d79-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66d79-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66d79-140">INPUTS</span></span>

### <span data-ttu-id="66d79-141">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="66d79-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="66d79-142">System. String</span><span class="sxs-lookup"><span data-stu-id="66d79-142">System.String</span></span>

### <span data-ttu-id="66d79-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="66d79-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="66d79-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66d79-144">OUTPUTS</span></span>

### <span data-ttu-id="66d79-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="66d79-145">System.Boolean</span></span>

## <span data-ttu-id="66d79-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66d79-146">NOTES</span></span>

## <span data-ttu-id="66d79-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66d79-147">RELATED LINKS</span></span>
