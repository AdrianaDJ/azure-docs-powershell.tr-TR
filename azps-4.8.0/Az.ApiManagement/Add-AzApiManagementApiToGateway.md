---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitogateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
ms.openlocfilehash: 6bb40d46c80e609824b1c56d05091ade5716f7f8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110128"
---
# <span data-ttu-id="6aa96-101">Add-AzApiManagementApiToGateway</span><span class="sxs-lookup"><span data-stu-id="6aa96-101">Add-AzApiManagementApiToGateway</span></span>

## <span data-ttu-id="6aa96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6aa96-102">SYNOPSIS</span></span>
<span data-ttu-id="6aa96-103">Ağ geçidine bir API ekler.</span><span class="sxs-lookup"><span data-stu-id="6aa96-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="6aa96-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6aa96-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-ProvisioningState <PsApiManagementGatewayApiProvisioningState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6aa96-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6aa96-105">DESCRIPTION</span></span>
<span data-ttu-id="6aa96-106">**Add-Azapsananagementapitogateway** cmdlet 'Ine BIR Azure API yönetim API 'si ekler.</span><span class="sxs-lookup"><span data-stu-id="6aa96-106">The **Add-AzApiManagementApiToGateway** cmdlet adds an Azure API Management API to a Gateway.</span></span>

## <span data-ttu-id="6aa96-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6aa96-107">EXAMPLES</span></span>

### <span data-ttu-id="6aa96-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6aa96-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001"
```

<span data-ttu-id="6aa96-109">Bu komut belirtilen ağ geçidine belirtilen API 'yi ekler.</span><span class="sxs-lookup"><span data-stu-id="6aa96-109">This command adds the specified API to the specified Gateway.</span></span>

## <span data-ttu-id="6aa96-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6aa96-110">PARAMETERS</span></span>

### <span data-ttu-id="6aa96-111">-Apııd</span><span class="sxs-lookup"><span data-stu-id="6aa96-111">-ApiId</span></span>
<span data-ttu-id="6aa96-112">Var olan API tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="6aa96-112">Identifier of existing API.</span></span>
<span data-ttu-id="6aa96-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="6aa96-113">This parameter is required.</span></span>

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

### <span data-ttu-id="6aa96-114">-Context</span><span class="sxs-lookup"><span data-stu-id="6aa96-114">-Context</span></span>
<span data-ttu-id="6aa96-115">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="6aa96-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6aa96-116">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="6aa96-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aa96-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aa96-117">-DefaultProfile</span></span>
<span data-ttu-id="6aa96-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6aa96-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6aa96-119">-Gatewayıd</span><span class="sxs-lookup"><span data-stu-id="6aa96-119">-GatewayId</span></span>
<span data-ttu-id="6aa96-120">Mevcut ağ geçidinin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="6aa96-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="6aa96-121">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="6aa96-121">This parameter is required.</span></span>

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

### <span data-ttu-id="6aa96-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6aa96-122">-PassThru</span></span>
<span data-ttu-id="6aa96-123">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="6aa96-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="6aa96-124">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="6aa96-124">This parameter is optional.</span></span>
<span data-ttu-id="6aa96-125">Varsayılan değer: false.</span><span class="sxs-lookup"><span data-stu-id="6aa96-125">Default value is false.</span></span>

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

### <span data-ttu-id="6aa96-126">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="6aa96-126">-ProvisioningState</span></span>
<span data-ttu-id="6aa96-127">Hazırlama durumu (oluşturuldu).</span><span class="sxs-lookup"><span data-stu-id="6aa96-127">Provisioning State (Created).</span></span>
<span data-ttu-id="6aa96-128">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="6aa96-128">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState]
Parameter Sets: (All)
Aliases:
Accepted values: Created

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aa96-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="6aa96-129">-Confirm</span></span>
<span data-ttu-id="6aa96-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6aa96-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6aa96-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6aa96-131">-WhatIf</span></span>
<span data-ttu-id="6aa96-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6aa96-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6aa96-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6aa96-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6aa96-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aa96-134">CommonParameters</span></span>
<span data-ttu-id="6aa96-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6aa96-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aa96-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6aa96-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aa96-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6aa96-137">INPUTS</span></span>

### <span data-ttu-id="6aa96-138">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="6aa96-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6aa96-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6aa96-139">System.String</span></span>

### <span data-ttu-id="6aa96-140">System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapimanagementgatewayapıprovisioningstate, Microsoft. Azure. PowerShell. cmdlet. Apsananayöneti. ServiceManagement, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6aa96-140">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="6aa96-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6aa96-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6aa96-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6aa96-142">OUTPUTS</span></span>

### <span data-ttu-id="6aa96-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6aa96-143">System.Boolean</span></span>

## <span data-ttu-id="6aa96-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6aa96-144">NOTES</span></span>

## <span data-ttu-id="6aa96-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6aa96-145">RELATED LINKS</span></span>

[<span data-ttu-id="6aa96-146">Remove-Azapsananagementapifromgateway</span><span class="sxs-lookup"><span data-stu-id="6aa96-146">Remove-AzApiManagementApiFromGateway</span></span>](./Remove-AzApiManagementApiFromGateway.md)