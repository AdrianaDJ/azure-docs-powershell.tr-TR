---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: 6aadf94ff379df322907be66c73052196de803c5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277873"
---
# <span data-ttu-id="4b4d6-101">New-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b4d6-101">New-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="4b4d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b4d6-102">SYNOPSIS</span></span>
<span data-ttu-id="4b4d6-103">Var olan ağ geçidi için bir ana bilgisayar yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-103">Creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="4b4d6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b4d6-104">SYNTAX</span></span>

```
New-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-GatewayHostnameConfigurationId <String>] -Hostname <String> -CertificateResourceId <String>
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4b4d6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b4d6-105">DESCRIPTION</span></span>
<span data-ttu-id="4b4d6-106">**Yeni-Azapsananagementgatewayhostnameconfiguration** cmdlet 'ı mevcut ağ geçidi için bir ana bilgisayar yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-106">The **New-AzApiManagementGatewayHostnameConfiguration** cmdlet creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="4b4d6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b4d6-107">EXAMPLES</span></span>

### <span data-ttu-id="4b4d6-108">Örnek 1: varolan ağ geçidi için bir ana bilgisayar yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="4b4d6-108">Example 1: Create a hostname configuration for the existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$cert = Get-AzApiManagementCertificate -Context $apimContext -CertificateId "333"
PS C:\>New-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g01" -GatewayHostnameConfigurationId "h01" -Hostname "www.contoso.com" -CertificateResourceId $cert.Id
```

<span data-ttu-id="4b4d6-109">Bu komut, "G01" ağ geçidi için "H01" konak adı yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-109">This command creates a "h01" hostname configuration for a "g01" gateway.</span></span>

## <span data-ttu-id="4b4d6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b4d6-110">PARAMETERS</span></span>

### <span data-ttu-id="4b4d6-111">-CertificateResourceId</span><span class="sxs-lookup"><span data-stu-id="4b4d6-111">-CertificateResourceId</span></span>
<span data-ttu-id="4b4d6-112">Var olan sertifika kimliği için bir kaynak tanımlayıcısı. Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-112">A resource identifier for the existing certificate id. This parameter is required.</span></span>

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

### <span data-ttu-id="4b4d6-113">-Context</span><span class="sxs-lookup"><span data-stu-id="4b4d6-113">-Context</span></span>
<span data-ttu-id="4b4d6-114">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4b4d6-115">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-115">This parameter is required.</span></span>

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

### <span data-ttu-id="4b4d6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b4d6-116">-DefaultProfile</span></span>
<span data-ttu-id="4b4d6-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b4d6-118">-Gatewayhostnameconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="4b4d6-118">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="4b4d6-119">Yeni ağ geçidi ana bilgisayar adı yapılandırması</span><span class="sxs-lookup"><span data-stu-id="4b4d6-119">Identifier of new gateway hostname confiuration.</span></span>
<span data-ttu-id="4b4d6-120">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-120">This parameter is optional.</span></span>
<span data-ttu-id="4b4d6-121">Belirtilmemişse,.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-121">If not specified will be generated.</span></span>

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

### <span data-ttu-id="4b4d6-122">-Gatewayıd</span><span class="sxs-lookup"><span data-stu-id="4b4d6-122">-GatewayId</span></span>
<span data-ttu-id="4b4d6-123">Mevcut ağ geçidinin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="4b4d6-124">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-124">This parameter is required.</span></span>

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

### <span data-ttu-id="4b4d6-125">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="4b4d6-125">-Hostname</span></span>
<span data-ttu-id="4b4d6-126">Hostname.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-126">Hostname.</span></span>
<span data-ttu-id="4b4d6-127">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-127">This parameter is required.</span></span>

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

### <span data-ttu-id="4b4d6-128">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4b4d6-128">-NegotiateClientCertificate</span></span>
<span data-ttu-id="4b4d6-129">NegotiateClientCertificate 'i zorunlu kılma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-129">Flag to enforce NegotiateClientCertificate.</span></span>
<span data-ttu-id="4b4d6-130">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="4b4d6-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="4b4d6-131">-Confirm</span></span>
<span data-ttu-id="4b4d6-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b4d6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b4d6-133">-WhatIf</span></span>
<span data-ttu-id="4b4d6-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b4d6-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b4d6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b4d6-136">CommonParameters</span></span>
<span data-ttu-id="4b4d6-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b4d6-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b4d6-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b4d6-139">INPUTS</span></span>

### <span data-ttu-id="4b4d6-140">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="4b4d6-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4b4d6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4b4d6-141">System.String</span></span>

### <span data-ttu-id="4b4d6-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4b4d6-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4b4d6-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b4d6-143">OUTPUTS</span></span>

### <span data-ttu-id="4b4d6-144">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgatewayhostnameconfiguration</span><span class="sxs-lookup"><span data-stu-id="4b4d6-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="4b4d6-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b4d6-145">NOTES</span></span>

## <span data-ttu-id="4b4d6-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b4d6-146">RELATED LINKS</span></span>
