---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 11d832bc74aca4ac274ee17ff0b38de06b77e377
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588657"
---
# <span data-ttu-id="d966d-101">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d966d-101">Get-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="d966d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d966d-102">SYNOPSIS</span></span>
<span data-ttu-id="d966d-103">Arka ucun ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="d966d-103">Get the details of the Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d966d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d966d-104">SYNTAX</span></span>

### <span data-ttu-id="d966d-105">GetAllBackends (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d966d-105">GetAllBackends (Default)</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d966d-106">Getbybackengerçekleşti</span><span class="sxs-lookup"><span data-stu-id="d966d-106">GetByBackendId</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d966d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d966d-107">DESCRIPTION</span></span>
<span data-ttu-id="d966d-108">Arka ucun ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="d966d-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="d966d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d966d-109">EXAMPLES</span></span>

### <span data-ttu-id="d966d-110">Örnek 1: tüm Backenleri alma</span><span class="sxs-lookup"><span data-stu-id="d966d-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext
```

<span data-ttu-id="d966d-111">Api Yönetim hizmetinde yapılandırılmış tüm Backen'ler listesini alır.</span><span class="sxs-lookup"><span data-stu-id="d966d-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="d966d-112">Örnek 2: tanımlayıcı 123 tarafından belirtilen arka uç 'yi alma</span><span class="sxs-lookup"><span data-stu-id="d966d-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="d966d-113">Belirtilen arka ucun ayrıntılarını ' 123 ' tanımlayıcısıyla</span><span class="sxs-lookup"><span data-stu-id="d966d-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="d966d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d966d-114">PARAMETERS</span></span>

### <span data-ttu-id="d966d-115">-Backenmuydunuz</span><span class="sxs-lookup"><span data-stu-id="d966d-115">-BackendId</span></span>
<span data-ttu-id="d966d-116">Arka ucun tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="d966d-116">Identifier of a backend.</span></span>
<span data-ttu-id="d966d-117">Belirtilirse, tanımlayıcı tarafından arka uç bulmayı dener.</span><span class="sxs-lookup"><span data-stu-id="d966d-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="d966d-118">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="d966d-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="d966d-119">-Context</span><span class="sxs-lookup"><span data-stu-id="d966d-119">-Context</span></span>
<span data-ttu-id="d966d-120">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="d966d-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d966d-121">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d966d-121">This parameter is required.</span></span>

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

### <span data-ttu-id="d966d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d966d-122">-DefaultProfile</span></span>
<span data-ttu-id="d966d-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d966d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d966d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d966d-124">CommonParameters</span></span>
<span data-ttu-id="d966d-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d966d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d966d-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d966d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d966d-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d966d-127">INPUTS</span></span>

### <span data-ttu-id="d966d-128">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="d966d-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d966d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d966d-129">System.String</span></span>

## <span data-ttu-id="d966d-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d966d-130">OUTPUTS</span></span>

### <span data-ttu-id="d966d-131">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementarka uç</span><span class="sxs-lookup"><span data-stu-id="d966d-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="d966d-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d966d-132">NOTES</span></span>

## <span data-ttu-id="d966d-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d966d-133">RELATED LINKS</span></span>

[<span data-ttu-id="d966d-134">Yeni-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="d966d-134">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="d966d-135">Yeni-Azurermapımanagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="d966d-135">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="d966d-136">Yeni-Azurermapımanagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="d966d-136">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="d966d-137">Set-Azurermapımanaarka uç</span><span class="sxs-lookup"><span data-stu-id="d966d-137">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="d966d-138">Remove-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="d966d-138">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
