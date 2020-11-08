---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
ms.openlocfilehash: 80b059a82264cf7d0adedbfca477616abcaa232d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277886"
---
# <span data-ttu-id="9ff8f-101">Get-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="9ff8f-101">Get-AzApiManagementGateway</span></span>

## <span data-ttu-id="9ff8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ff8f-102">SYNOPSIS</span></span>
<span data-ttu-id="9ff8f-103">Tüm veya belirli API Yönetimi ağ geçidini alır.</span><span class="sxs-lookup"><span data-stu-id="9ff8f-103">Gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="9ff8f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9ff8f-104">SYNTAX</span></span>

### <span data-ttu-id="9ff8f-105">Getallgeçitleri (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9ff8f-105">GetAllGateways (Default)</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ff8f-106">Getbygatewayıd</span><span class="sxs-lookup"><span data-stu-id="9ff8f-106">GetByGatewayId</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ff8f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9ff8f-107">DESCRIPTION</span></span>
<span data-ttu-id="9ff8f-108">**Get-Azapsananagementgateway** cmdlet 'i ya da belirli API yönetim ağ geçidini alır.</span><span class="sxs-lookup"><span data-stu-id="9ff8f-108">The **Get-AzApiManagementGateway** cmdlet gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="9ff8f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9ff8f-109">EXAMPLES</span></span>

### <span data-ttu-id="9ff8f-110">Örnek 1: tüm ağ geçitlerini al</span><span class="sxs-lookup"><span data-stu-id="9ff8f-110">Example 1: Get all gateways</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext
```

<span data-ttu-id="9ff8f-111">Bu komut tüm ağ geçitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="9ff8f-111">This command gets all gateways.</span></span>

### <span data-ttu-id="9ff8f-112">Örnek 2: KIMLIĞE göre ağ geçidi alma</span><span class="sxs-lookup"><span data-stu-id="9ff8f-112">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="9ff8f-113">Bu komut, 0123456789 ağ geçidini alır.</span><span class="sxs-lookup"><span data-stu-id="9ff8f-113">This command gets the gateway 0123456789.</span></span>

## <span data-ttu-id="9ff8f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9ff8f-114">PARAMETERS</span></span>

### <span data-ttu-id="9ff8f-115">-Context</span><span class="sxs-lookup"><span data-stu-id="9ff8f-115">-Context</span></span>
<span data-ttu-id="9ff8f-116">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="9ff8f-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9ff8f-117">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="9ff8f-117">This parameter is required.</span></span>

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

### <span data-ttu-id="9ff8f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ff8f-118">-DefaultProfile</span></span>
<span data-ttu-id="9ff8f-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9ff8f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ff8f-120">-Gatewayıd</span><span class="sxs-lookup"><span data-stu-id="9ff8f-120">-GatewayId</span></span>
<span data-ttu-id="9ff8f-121">Ağ geçidinin tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="9ff8f-121">Identifier of a gateway.</span></span>
<span data-ttu-id="9ff8f-122">Belirtilmişse tanımlayıcı tarafından ağ geçidini bulmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="9ff8f-122">If specified will try to find gateway by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ff8f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ff8f-123">CommonParameters</span></span>
<span data-ttu-id="9ff8f-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9ff8f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ff8f-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9ff8f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ff8f-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9ff8f-126">INPUTS</span></span>

### <span data-ttu-id="9ff8f-127">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="9ff8f-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9ff8f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9ff8f-128">System.String</span></span>

## <span data-ttu-id="9ff8f-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9ff8f-129">OUTPUTS</span></span>

### <span data-ttu-id="9ff8f-130">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgateway</span><span class="sxs-lookup"><span data-stu-id="9ff8f-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="9ff8f-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9ff8f-131">NOTES</span></span>

## <span data-ttu-id="9ff8f-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9ff8f-132">RELATED LINKS</span></span>
