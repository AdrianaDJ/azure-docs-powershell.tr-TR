---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 4f54b361482bad24826d7120e53f96ce8d3b9eef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591844"
---
# <span data-ttu-id="3e21d-101">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3e21d-101">Get-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="3e21d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e21d-102">SYNOPSIS</span></span>
<span data-ttu-id="3e21d-103">Arka ucun ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="3e21d-103">Get the details of the Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e21d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3e21d-104">SYNTAX</span></span>

### <span data-ttu-id="3e21d-105">Tüm backenleri al (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3e21d-105">Get all backends (Default)</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e21d-106">Arka uç KIMLIĞIYLE al</span><span class="sxs-lookup"><span data-stu-id="3e21d-106">Get by backend ID</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e21d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3e21d-107">DESCRIPTION</span></span>
<span data-ttu-id="3e21d-108">Arka ucun ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="3e21d-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="3e21d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3e21d-109">EXAMPLES</span></span>

### <span data-ttu-id="3e21d-110">--------------------------Örnek 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3e21d-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="3e21d-111">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="3e21d-111">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementBackend -Context $apimContext
```

<span data-ttu-id="3e21d-112">Api Yönetim hizmetinde yapılandırılmış tüm Backen'ler listesini alır.</span><span class="sxs-lookup"><span data-stu-id="3e21d-112">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="3e21d-113">--------------------------Örnek 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="3e21d-113">--------------------------  Example 2  --------------------------</span></span>
<span data-ttu-id="3e21d-114">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="3e21d-114">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="3e21d-115">Belirtilen arka ucun ayrıntılarını ' 123 ' tanımlayıcısıyla</span><span class="sxs-lookup"><span data-stu-id="3e21d-115">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="3e21d-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3e21d-116">PARAMETERS</span></span>

### <span data-ttu-id="3e21d-117">-Backenmuydunuz</span><span class="sxs-lookup"><span data-stu-id="3e21d-117">-BackendId</span></span>
<span data-ttu-id="3e21d-118">Arka ucun tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="3e21d-118">Identifier of a backend.</span></span>
<span data-ttu-id="3e21d-119">Belirtilirse, tanımlayıcı tarafından arka uç bulmayı dener.</span><span class="sxs-lookup"><span data-stu-id="3e21d-119">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="3e21d-120">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="3e21d-120">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by backend ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e21d-121">-Context</span><span class="sxs-lookup"><span data-stu-id="3e21d-121">-Context</span></span>
<span data-ttu-id="3e21d-122">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="3e21d-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3e21d-123">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="3e21d-123">This parameter is required.</span></span>

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

### <span data-ttu-id="3e21d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e21d-124">-DefaultProfile</span></span>
<span data-ttu-id="3e21d-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3e21d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e21d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e21d-126">CommonParameters</span></span>
<span data-ttu-id="3e21d-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3e21d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e21d-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e21d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e21d-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3e21d-129">INPUTS</span></span>

## <span data-ttu-id="3e21d-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3e21d-130">OUTPUTS</span></span>

### <span data-ttu-id="3e21d-131">IList<Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementarka uç></span><span class="sxs-lookup"><span data-stu-id="3e21d-131">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend></span></span>

### <span data-ttu-id="3e21d-132">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgünlükçü. Psapimanagementarka uç</span><span class="sxs-lookup"><span data-stu-id="3e21d-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger.PsApiManagementBackend</span></span>

## <span data-ttu-id="3e21d-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3e21d-133">NOTES</span></span>

## <span data-ttu-id="3e21d-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3e21d-134">RELATED LINKS</span></span>

[<span data-ttu-id="3e21d-135">Yeni-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="3e21d-135">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="3e21d-136">Yeni-Azurermapımanagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="3e21d-136">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="3e21d-137">Yeni-Azurermapımanagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="3e21d-137">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="3e21d-138">Set-Azurermapımanaarka uç</span><span class="sxs-lookup"><span data-stu-id="3e21d-138">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="3e21d-139">Remove-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="3e21d-139">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
