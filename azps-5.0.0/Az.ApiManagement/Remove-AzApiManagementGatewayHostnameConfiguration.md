---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: e1999387cc2beb5a55fba3aef771a76440804f22
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278152"
---
# <span data-ttu-id="21628-101">Remove-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="21628-101">Remove-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="21628-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21628-102">SYNOPSIS</span></span>
<span data-ttu-id="21628-103">Var olan ağ geçidinden bir ana bilgisayar yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="21628-103">Removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="21628-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="21628-104">SYNTAX</span></span>

### <span data-ttu-id="21628-105">ContextParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="21628-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21628-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21628-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -InputObject <PsApiManagementGatewayHostnameConfiguration>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21628-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="21628-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21628-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="21628-108">DESCRIPTION</span></span>
<span data-ttu-id="21628-109">**Remove-Azapsananagementgatewayhostnameconfiguration** cmdlet 'ı mevcut ağ geçidinden bir ana bilgisayar yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="21628-109">The **Remove-AzApiManagementGatewayHostnameConfiguration** cmdlet removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="21628-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="21628-110">EXAMPLES</span></span>

### <span data-ttu-id="21628-111">Örnek 1: varolan ağ geçidi konak yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="21628-111">Example 1: Remove an existing gateway hostname configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g0001" -GatewayHostnameConfigurationId "h0001" -Force
```

<span data-ttu-id="21628-112">Bu komut, mevcut ağ geçidi ana bilgisayar yapılandırması 'nı kaldırır ve kullanıcıdan onay istemez.</span><span class="sxs-lookup"><span data-stu-id="21628-112">This command removes an existing gateway hostname configuration and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="21628-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="21628-113">PARAMETERS</span></span>

### <span data-ttu-id="21628-114">-Context</span><span class="sxs-lookup"><span data-stu-id="21628-114">-Context</span></span>
<span data-ttu-id="21628-115">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="21628-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="21628-116">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="21628-116">This parameter is required.</span></span>

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

### <span data-ttu-id="21628-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21628-117">-DefaultProfile</span></span>
<span data-ttu-id="21628-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="21628-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21628-119">-Gatewayhostnameconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="21628-119">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="21628-120">Mevcut ağ geçidi ana bilgisayar yapılandırmasının tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="21628-120">Identifier of existing gateway hostname configuration.</span></span>
<span data-ttu-id="21628-121">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="21628-121">This parameter is required.</span></span>

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

### <span data-ttu-id="21628-122">-Gatewayıd</span><span class="sxs-lookup"><span data-stu-id="21628-122">-GatewayId</span></span>
<span data-ttu-id="21628-123">Mevcut ağ geçidinin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="21628-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="21628-124">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="21628-124">This parameter is required.</span></span>

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

### <span data-ttu-id="21628-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21628-125">-InputObject</span></span>
<span data-ttu-id="21628-126">PsApiManagementGatewayHostnameConfiguration örneği.</span><span class="sxs-lookup"><span data-stu-id="21628-126">Instance of PsApiManagementGatewayHostnameConfiguration.</span></span> <span data-ttu-id="21628-127">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="21628-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21628-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="21628-128">-PassThru</span></span>
<span data-ttu-id="21628-129">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="21628-129">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="21628-130">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="21628-130">This parameter is optional.</span></span>
<span data-ttu-id="21628-131">Varsayılan değer: false.</span><span class="sxs-lookup"><span data-stu-id="21628-131">Default value is false.</span></span>

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

### <span data-ttu-id="21628-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="21628-132">-ResourceId</span></span>
<span data-ttu-id="21628-133">GatewayHostnameConfiguration 'ın Kolonu.</span><span class="sxs-lookup"><span data-stu-id="21628-133">Arm ResourceId of the GatewayHostnameConfiguration.</span></span> <span data-ttu-id="21628-134">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="21628-134">This parameter is required.</span></span>

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

### <span data-ttu-id="21628-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="21628-135">-Confirm</span></span>
<span data-ttu-id="21628-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="21628-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21628-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21628-137">-WhatIf</span></span>
<span data-ttu-id="21628-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="21628-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21628-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="21628-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21628-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21628-140">CommonParameters</span></span>
<span data-ttu-id="21628-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="21628-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21628-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="21628-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21628-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="21628-143">INPUTS</span></span>

### <span data-ttu-id="21628-144">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="21628-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="21628-145">System. String</span><span class="sxs-lookup"><span data-stu-id="21628-145">System.String</span></span>

### <span data-ttu-id="21628-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="21628-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="21628-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="21628-147">OUTPUTS</span></span>

### <span data-ttu-id="21628-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="21628-148">System.Boolean</span></span>

## <span data-ttu-id="21628-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="21628-149">NOTES</span></span>

## <span data-ttu-id="21628-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="21628-150">RELATED LINKS</span></span>
