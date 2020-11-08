---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: ecdae500b0c1d81635e23ca6ca4bc4c803665912
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274640"
---
# <span data-ttu-id="2f257-101">Get-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f257-101">Get-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="2f257-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f257-102">SYNOPSIS</span></span>
<span data-ttu-id="2f257-103">Var olan ağ geçidi için tüm veya belirli ana bilgisayar yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="2f257-103">Gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="2f257-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2f257-104">SYNTAX</span></span>

### <span data-ttu-id="2f257-105">Getbygatewayıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2f257-105">GetByGatewayId (Default)</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f257-106">Getbygatewayhostnameıd</span><span class="sxs-lookup"><span data-stu-id="2f257-106">GetByGatewayHostnameId</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f257-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f257-107">DESCRIPTION</span></span>
<span data-ttu-id="2f257-108">**Get-Azapsananagementgatewayhostnameconfiguration** cmdlet 'i, mevcut ağ geçidi için tüm veya belirli ana bilgisayar yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="2f257-108">The **Get-AzApiManagementGatewayHostnameConfiguration** cmdlet gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="2f257-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2f257-109">EXAMPLES</span></span>

### <span data-ttu-id="2f257-110">Örnek 1: ağ geçidi için tüm ana bilgisayar yapılandırmalarını alma</span><span class="sxs-lookup"><span data-stu-id="2f257-110">Example 1: Get all hostname configurations for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext  -GatewayId "0123456789"
```

<span data-ttu-id="2f257-111">Bu komut, "0123456789" ağ geçidi için tüm ana bilgisayar yapılandırmalarını alır.</span><span class="sxs-lookup"><span data-stu-id="2f257-111">This command gets all hostname configurations for a "0123456789" gateway.</span></span>

### <span data-ttu-id="2f257-112">Örnek 2: ağ geçidi için bir ana bilgisayar yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="2f257-112">Example 2: Get a hostname configuration for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "0123456789" -GatewayHostnameConfigurationId "123"
```

<span data-ttu-id="2f257-113">Bu komut "0123456789" ağ geçidi için "123" hostname yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="2f257-113">This command gets "123" hostname configuration for a "0123456789" gateway.</span></span>

## <span data-ttu-id="2f257-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2f257-114">PARAMETERS</span></span>

### <span data-ttu-id="2f257-115">-Context</span><span class="sxs-lookup"><span data-stu-id="2f257-115">-Context</span></span>
<span data-ttu-id="2f257-116">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="2f257-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2f257-117">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2f257-117">This parameter is required.</span></span>

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

### <span data-ttu-id="2f257-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f257-118">-DefaultProfile</span></span>
<span data-ttu-id="2f257-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2f257-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f257-120">-Gatewayhostnameconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="2f257-120">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="2f257-121">Ana bilgisayar yapılandırma tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="2f257-121">Hostname Configuration identifier.</span></span>
<span data-ttu-id="2f257-122">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="2f257-122">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayHostnameId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f257-123">-Gatewayıd</span><span class="sxs-lookup"><span data-stu-id="2f257-123">-GatewayId</span></span>
<span data-ttu-id="2f257-124">Ağ Geçidi tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="2f257-124">Gateway identifier.</span></span>
<span data-ttu-id="2f257-125">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2f257-125">This parameter is required.</span></span>

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

### <span data-ttu-id="2f257-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f257-126">CommonParameters</span></span>
<span data-ttu-id="2f257-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2f257-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f257-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2f257-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f257-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2f257-129">INPUTS</span></span>

### <span data-ttu-id="2f257-130">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="2f257-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2f257-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2f257-131">System.String</span></span>

## <span data-ttu-id="2f257-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2f257-132">OUTPUTS</span></span>

### <span data-ttu-id="2f257-133">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgatewayhostnameconfiguration</span><span class="sxs-lookup"><span data-stu-id="2f257-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="2f257-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2f257-134">NOTES</span></span>

## <span data-ttu-id="2f257-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2f257-135">RELATED LINKS</span></span>
