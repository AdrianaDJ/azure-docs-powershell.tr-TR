---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/Update-AzApiManagementGateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
ms.openlocfilehash: d053bc60390c43c3409bb7adfad5a3ff3720f5b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107984"
---
# <span data-ttu-id="349e7-101">Update-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="349e7-101">Update-AzApiManagementGateway</span></span>

## <span data-ttu-id="349e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="349e7-102">SYNOPSIS</span></span>
<span data-ttu-id="349e7-103">Bir API yönetim ağ geçidi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="349e7-103">Configures an API management Gateway.</span></span>

## <span data-ttu-id="349e7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="349e7-104">SYNTAX</span></span>

### <span data-ttu-id="349e7-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="349e7-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="349e7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="349e7-106">ByInputObject</span></span>
```
Update-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="349e7-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="349e7-107">ByResourceId</span></span>
```
Update-AzApiManagementGateway -ResourceId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="349e7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="349e7-108">DESCRIPTION</span></span>
<span data-ttu-id="349e7-109">**Update-Azapsananagementgateway** cmdlet 'ı bir API yönetim ağ geçidi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="349e7-109">The **Update-AzApiManagementGateway** cmdlet configures an API management Gateway.</span></span>

## <span data-ttu-id="349e7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="349e7-110">EXAMPLES</span></span>

### <span data-ttu-id="349e7-111">Örnek 1: yönetim grubu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="349e7-111">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementGateway -Context $apimContext -GatewayId "0001" -Description "Updated Gateway"
```

<span data-ttu-id="349e7-112">Bu komut ağ geçidini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="349e7-112">This command configures a gateway.</span></span>

## <span data-ttu-id="349e7-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="349e7-113">PARAMETERS</span></span>

### <span data-ttu-id="349e7-114">-Context</span><span class="sxs-lookup"><span data-stu-id="349e7-114">-Context</span></span>
<span data-ttu-id="349e7-115">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="349e7-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="349e7-116">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="349e7-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="349e7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="349e7-117">-DefaultProfile</span></span>
<span data-ttu-id="349e7-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="349e7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="349e7-119">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="349e7-119">-Description</span></span>
<span data-ttu-id="349e7-120">Ağ Geçidi açıklaması.</span><span class="sxs-lookup"><span data-stu-id="349e7-120">Gateway description.</span></span>
<span data-ttu-id="349e7-121">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="349e7-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="349e7-122">-Gatewayıd</span><span class="sxs-lookup"><span data-stu-id="349e7-122">-GatewayId</span></span>
<span data-ttu-id="349e7-123">Mevcut ağ geçidinin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="349e7-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="349e7-124">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="349e7-124">This parameter is required.</span></span>

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

### <span data-ttu-id="349e7-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="349e7-125">-InputObject</span></span>
<span data-ttu-id="349e7-126">PsApiManagementGateway örneği.</span><span class="sxs-lookup"><span data-stu-id="349e7-126">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="349e7-127">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="349e7-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="349e7-128">-Konumveri</span><span class="sxs-lookup"><span data-stu-id="349e7-128">-LocationData</span></span>
<span data-ttu-id="349e7-129">Ağ Geçidi konumu.</span><span class="sxs-lookup"><span data-stu-id="349e7-129">Gateway location.</span></span>
<span data-ttu-id="349e7-130">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="349e7-130">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="349e7-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="349e7-131">-PassThru</span></span>
<span data-ttu-id="349e7-132">Bu sonra, değiştirilmiş ağ geçidini temsil eden Microsoft. Azure. Commands. Apsananaitid.</span><span class="sxs-lookup"><span data-stu-id="349e7-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway type representing the modified gateway.</span></span>

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

### <span data-ttu-id="349e7-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="349e7-133">-ResourceId</span></span>
<span data-ttu-id="349e7-134">Ağ geçidinin Kolonu.</span><span class="sxs-lookup"><span data-stu-id="349e7-134">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="349e7-135">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="349e7-135">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="349e7-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="349e7-136">-Confirm</span></span>
<span data-ttu-id="349e7-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="349e7-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="349e7-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="349e7-138">-WhatIf</span></span>
<span data-ttu-id="349e7-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="349e7-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="349e7-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="349e7-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="349e7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="349e7-141">CommonParameters</span></span>
<span data-ttu-id="349e7-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="349e7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="349e7-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="349e7-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="349e7-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="349e7-144">INPUTS</span></span>

### <span data-ttu-id="349e7-145">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="349e7-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="349e7-146">System. String</span><span class="sxs-lookup"><span data-stu-id="349e7-146">System.String</span></span>

### <span data-ttu-id="349e7-147">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementresourcelocation</span><span class="sxs-lookup"><span data-stu-id="349e7-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

### <span data-ttu-id="349e7-148">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="349e7-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="349e7-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="349e7-149">OUTPUTS</span></span>

### <span data-ttu-id="349e7-150">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgateway</span><span class="sxs-lookup"><span data-stu-id="349e7-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="349e7-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="349e7-151">NOTES</span></span>

## <span data-ttu-id="349e7-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="349e7-152">RELATED LINKS</span></span>
