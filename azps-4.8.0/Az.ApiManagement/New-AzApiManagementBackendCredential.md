---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: 069bf57b62d6834a1509adb551d15ce5082b2dc3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109892"
---
# <span data-ttu-id="95eb9-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="95eb9-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="95eb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="95eb9-103">Yeni bir arka uç kimlik bilgileri sözleşmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="95eb9-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="95eb9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95eb9-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95eb9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="95eb9-105">DESCRIPTION</span></span>
<span data-ttu-id="95eb9-106">Yeni bir arka uç kimlik bilgileri sözleşmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="95eb9-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="95eb9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95eb9-107">EXAMPLES</span></span>

### <span data-ttu-id="95eb9-108">Örnek 1: arka uç kimlik bilgileri In-Memory nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="95eb9-108">Example 1: Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="95eb9-109">Arka uç kimlik bilgileri sözleşmesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="95eb9-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="95eb9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95eb9-110">PARAMETERS</span></span>

### <span data-ttu-id="95eb9-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="95eb9-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="95eb9-112">Arka uç için kullanılan yetkilendirme üst bilgisi.</span><span class="sxs-lookup"><span data-stu-id="95eb9-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="95eb9-113">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="95eb9-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95eb9-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="95eb9-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="95eb9-115">Arka uç için kullanılan yetkilendirme düzeni.</span><span class="sxs-lookup"><span data-stu-id="95eb9-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="95eb9-116">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="95eb9-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95eb9-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="95eb9-117">-CertificateThumbprint</span></span>
<span data-ttu-id="95eb9-118">İstemci sertifikası parmak Izleri.</span><span class="sxs-lookup"><span data-stu-id="95eb9-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="95eb9-119">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="95eb9-119">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95eb9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95eb9-120">-DefaultProfile</span></span>
<span data-ttu-id="95eb9-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="95eb9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95eb9-122">-Üst bilgi</span><span class="sxs-lookup"><span data-stu-id="95eb9-122">-Header</span></span>
<span data-ttu-id="95eb9-123">Arka uç tarafından kabul edilen üst bilgi parametre değerleri.</span><span class="sxs-lookup"><span data-stu-id="95eb9-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="95eb9-124">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="95eb9-124">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95eb9-125">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="95eb9-125">-Query</span></span>
<span data-ttu-id="95eb9-126">Arka uç tarafından kabul edilen sorgu parametre değerleri.</span><span class="sxs-lookup"><span data-stu-id="95eb9-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="95eb9-127">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="95eb9-127">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95eb9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95eb9-128">CommonParameters</span></span>
<span data-ttu-id="95eb9-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="95eb9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95eb9-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="95eb9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95eb9-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95eb9-131">INPUTS</span></span>

### <span data-ttu-id="95eb9-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="95eb9-132">None</span></span>

## <span data-ttu-id="95eb9-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95eb9-133">OUTPUTS</span></span>

### <span data-ttu-id="95eb9-134">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="95eb9-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="95eb9-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95eb9-135">NOTES</span></span>

## <span data-ttu-id="95eb9-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95eb9-136">RELATED LINKS</span></span>

[<span data-ttu-id="95eb9-137">Get-Azapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="95eb9-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="95eb9-138">Yeni-Azsız arka uç</span><span class="sxs-lookup"><span data-stu-id="95eb9-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="95eb9-139">Yeni-Azapsananagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="95eb9-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="95eb9-140">Set-Azapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="95eb9-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="95eb9-141">Remove-Azapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="95eb9-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
