---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
ms.openlocfilehash: c06442ef9ab4b5f80943da33ed87fc24c276107d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319726"
---
# <span data-ttu-id="6bb48-101">New-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="6bb48-101">New-AzApiManagementGateway</span></span>

## <span data-ttu-id="6bb48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bb48-102">SYNOPSIS</span></span>
<span data-ttu-id="6bb48-103">Yeni ağ geçidi varlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6bb48-103">Creates new Gateway entity.</span></span>

## <span data-ttu-id="6bb48-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6bb48-104">SYNTAX</span></span>

```
New-AzApiManagementGateway -Context <PsApiManagementContext> [-GatewayId <String>] [-Description <String>]
 -LocationData <PsApiManagementResourceLocation> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bb48-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6bb48-105">DESCRIPTION</span></span>
<span data-ttu-id="6bb48-106">**Yeni-Azapsananagementgateway** cmdlet 'ı yeni ağ geçidi varlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6bb48-106">The **New-AzApiManagementGateway** cmdlet creates new Gateway entity.</span></span>

## <span data-ttu-id="6bb48-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6bb48-107">EXAMPLES</span></span>

### <span data-ttu-id="6bb48-108">Örnek 1: ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="6bb48-108">Example 1: Create a gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
PS C:\>New-AzApiManagementGateway -Context $apimContext -GatewayId "123" -Description "desc" -LocationData $location
```

<span data-ttu-id="6bb48-109">Bu komut bir ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6bb48-109">This command creates a gateway.</span></span>

## <span data-ttu-id="6bb48-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6bb48-110">PARAMETERS</span></span>

### <span data-ttu-id="6bb48-111">-Context</span><span class="sxs-lookup"><span data-stu-id="6bb48-111">-Context</span></span>
<span data-ttu-id="6bb48-112">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="6bb48-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6bb48-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="6bb48-113">This parameter is required.</span></span>

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

### <span data-ttu-id="6bb48-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bb48-114">-DefaultProfile</span></span>
<span data-ttu-id="6bb48-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6bb48-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bb48-116">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="6bb48-116">-Description</span></span>
<span data-ttu-id="6bb48-117">Ağ Geçidi açıklaması.</span><span class="sxs-lookup"><span data-stu-id="6bb48-117">Gateway description.</span></span>
<span data-ttu-id="6bb48-118">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="6bb48-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="6bb48-119">-Gatewayıd</span><span class="sxs-lookup"><span data-stu-id="6bb48-119">-GatewayId</span></span>
<span data-ttu-id="6bb48-120">Yeni ağ geçidi tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="6bb48-120">Identifier of new gateway.</span></span>
<span data-ttu-id="6bb48-121">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="6bb48-121">This parameter is optional.</span></span>
<span data-ttu-id="6bb48-122">Belirtilmemişse,.</span><span class="sxs-lookup"><span data-stu-id="6bb48-122">If not specified will be generated.</span></span>

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

### <span data-ttu-id="6bb48-123">-Konumveri</span><span class="sxs-lookup"><span data-stu-id="6bb48-123">-LocationData</span></span>
<span data-ttu-id="6bb48-124">Ağ Geçidi konumu.</span><span class="sxs-lookup"><span data-stu-id="6bb48-124">Gateway location.</span></span>
<span data-ttu-id="6bb48-125">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="6bb48-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bb48-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="6bb48-126">-Confirm</span></span>
<span data-ttu-id="6bb48-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6bb48-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bb48-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bb48-128">-WhatIf</span></span>
<span data-ttu-id="6bb48-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6bb48-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6bb48-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6bb48-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bb48-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bb48-131">CommonParameters</span></span>
<span data-ttu-id="6bb48-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6bb48-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bb48-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6bb48-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bb48-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6bb48-134">INPUTS</span></span>

### <span data-ttu-id="6bb48-135">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="6bb48-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6bb48-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6bb48-136">System.String</span></span>

### <span data-ttu-id="6bb48-137">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementresourcelocation</span><span class="sxs-lookup"><span data-stu-id="6bb48-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="6bb48-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6bb48-138">OUTPUTS</span></span>

### <span data-ttu-id="6bb48-139">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgateway</span><span class="sxs-lookup"><span data-stu-id="6bb48-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="6bb48-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6bb48-140">NOTES</span></span>

## <span data-ttu-id="6bb48-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6bb48-141">RELATED LINKS</span></span>
