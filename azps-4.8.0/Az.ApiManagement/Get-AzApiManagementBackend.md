---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: 4781800ea9a6f8526ddee5e06b90b73ea676bf88
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109259"
---
# <span data-ttu-id="196c0-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="196c0-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="196c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="196c0-102">SYNOPSIS</span></span>
<span data-ttu-id="196c0-103">Arka ucun ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="196c0-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="196c0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="196c0-104">SYNTAX</span></span>

### <span data-ttu-id="196c0-105">ContextParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="196c0-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="196c0-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="196c0-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementBackend [-BackendId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="196c0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="196c0-107">DESCRIPTION</span></span>
<span data-ttu-id="196c0-108">Arka ucun ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="196c0-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="196c0-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="196c0-109">EXAMPLES</span></span>

### <span data-ttu-id="196c0-110">Örnek 1: tüm Backenleri alma</span><span class="sxs-lookup"><span data-stu-id="196c0-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="196c0-111">Api Yönetim hizmetinde yapılandırılmış tüm Backen'ler listesini alır.</span><span class="sxs-lookup"><span data-stu-id="196c0-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="196c0-112">Örnek 2: tanımlayıcı 123 tarafından belirtilen arka uç 'yi alma</span><span class="sxs-lookup"><span data-stu-id="196c0-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="196c0-113">Belirtilen arka ucun ayrıntılarını ' 123 ' tanımlayıcısıyla</span><span class="sxs-lookup"><span data-stu-id="196c0-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="196c0-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="196c0-114">PARAMETERS</span></span>

### <span data-ttu-id="196c0-115">-Backenmuydunuz</span><span class="sxs-lookup"><span data-stu-id="196c0-115">-BackendId</span></span>
<span data-ttu-id="196c0-116">Arka ucun tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="196c0-116">Identifier of a backend.</span></span>
<span data-ttu-id="196c0-117">Belirtilirse, tanımlayıcı tarafından arka uç bulmayı dener.</span><span class="sxs-lookup"><span data-stu-id="196c0-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="196c0-118">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="196c0-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="196c0-119">-Context</span><span class="sxs-lookup"><span data-stu-id="196c0-119">-Context</span></span>
<span data-ttu-id="196c0-120">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="196c0-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="196c0-121">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="196c0-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="196c0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="196c0-122">-DefaultProfile</span></span>
<span data-ttu-id="196c0-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="196c0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="196c0-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="196c0-124">-ResourceId</span></span>
<span data-ttu-id="196c0-125">Arka ucun ARM kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="196c0-125">Arm Resource Identifier of the backend.</span></span> <span data-ttu-id="196c0-126">Belirtilirse, tanımlayıcı tarafından arka uç bulmayı dener.</span><span class="sxs-lookup"><span data-stu-id="196c0-126">If specified will try to find backend by the identifier.</span></span> <span data-ttu-id="196c0-127">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="196c0-127">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="196c0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="196c0-128">CommonParameters</span></span>
<span data-ttu-id="196c0-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="196c0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="196c0-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="196c0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="196c0-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="196c0-131">INPUTS</span></span>

### <span data-ttu-id="196c0-132">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="196c0-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="196c0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="196c0-133">System.String</span></span>

## <span data-ttu-id="196c0-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="196c0-134">OUTPUTS</span></span>

### <span data-ttu-id="196c0-135">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementarka uç</span><span class="sxs-lookup"><span data-stu-id="196c0-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="196c0-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="196c0-136">NOTES</span></span>

## <span data-ttu-id="196c0-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="196c0-137">RELATED LINKS</span></span>

[<span data-ttu-id="196c0-138">Yeni-Azsız arka uç</span><span class="sxs-lookup"><span data-stu-id="196c0-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="196c0-139">Yeni-Azapsananagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="196c0-139">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="196c0-140">Yeni-Azapsananagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="196c0-140">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="196c0-141">Set-Azapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="196c0-141">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="196c0-142">Remove-Azapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="196c0-142">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
