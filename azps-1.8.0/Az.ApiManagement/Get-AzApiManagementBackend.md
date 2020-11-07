---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: 88a48edf3ae7e576aa78e989a5fda7515499a7f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751165"
---
# <span data-ttu-id="32822-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="32822-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="32822-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32822-102">SYNOPSIS</span></span>
<span data-ttu-id="32822-103">Arka ucun ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="32822-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="32822-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="32822-104">SYNTAX</span></span>

### <span data-ttu-id="32822-105">GetAllBackends (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="32822-105">GetAllBackends (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="32822-106">Getbybackengerçekleşti</span><span class="sxs-lookup"><span data-stu-id="32822-106">GetByBackendId</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32822-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="32822-107">DESCRIPTION</span></span>
<span data-ttu-id="32822-108">Arka ucun ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="32822-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="32822-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="32822-109">EXAMPLES</span></span>

### <span data-ttu-id="32822-110">Örnek 1: tüm Backenleri alma</span><span class="sxs-lookup"><span data-stu-id="32822-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="32822-111">Api Yönetim hizmetinde yapılandırılmış tüm Backen'ler listesini alır.</span><span class="sxs-lookup"><span data-stu-id="32822-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="32822-112">Örnek 2: tanımlayıcı 123 tarafından belirtilen arka uç 'yi alma</span><span class="sxs-lookup"><span data-stu-id="32822-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="32822-113">Belirtilen arka ucun ayrıntılarını ' 123 ' tanımlayıcısıyla</span><span class="sxs-lookup"><span data-stu-id="32822-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="32822-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="32822-114">PARAMETERS</span></span>

### <span data-ttu-id="32822-115">-Backenmuydunuz</span><span class="sxs-lookup"><span data-stu-id="32822-115">-BackendId</span></span>
<span data-ttu-id="32822-116">Arka ucun tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="32822-116">Identifier of a backend.</span></span>
<span data-ttu-id="32822-117">Belirtilirse, tanımlayıcı tarafından arka uç bulmayı dener.</span><span class="sxs-lookup"><span data-stu-id="32822-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="32822-118">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="32822-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByBackendId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32822-119">-Context</span><span class="sxs-lookup"><span data-stu-id="32822-119">-Context</span></span>
<span data-ttu-id="32822-120">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="32822-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="32822-121">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="32822-121">This parameter is required.</span></span>

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

### <span data-ttu-id="32822-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32822-122">-DefaultProfile</span></span>
<span data-ttu-id="32822-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="32822-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32822-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32822-124">CommonParameters</span></span>
<span data-ttu-id="32822-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="32822-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32822-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32822-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32822-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="32822-127">INPUTS</span></span>

### <span data-ttu-id="32822-128">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="32822-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="32822-129">System. String</span><span class="sxs-lookup"><span data-stu-id="32822-129">System.String</span></span>

## <span data-ttu-id="32822-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="32822-130">OUTPUTS</span></span>

### <span data-ttu-id="32822-131">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementarka uç</span><span class="sxs-lookup"><span data-stu-id="32822-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="32822-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="32822-132">NOTES</span></span>

## <span data-ttu-id="32822-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="32822-133">RELATED LINKS</span></span>

[<span data-ttu-id="32822-134">Yeni-Azsız arka uç</span><span class="sxs-lookup"><span data-stu-id="32822-134">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="32822-135">Yeni-Azapsananagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="32822-135">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="32822-136">Yeni-Azapsananagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="32822-136">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="32822-137">Set-Azapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="32822-137">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="32822-138">Remove-Azapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="32822-138">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
