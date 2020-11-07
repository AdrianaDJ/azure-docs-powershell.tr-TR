---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: 2cde898622c870dc0598639addb1e8b30e438076
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753539"
---
# <span data-ttu-id="7d727-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="7d727-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="7d727-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d727-102">SYNOPSIS</span></span>
<span data-ttu-id="7d727-103">Yeni bir arka uç kimlik bilgileri sözleşmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7d727-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="7d727-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7d727-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d727-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7d727-105">DESCRIPTION</span></span>
<span data-ttu-id="7d727-106">Yeni bir arka uç kimlik bilgileri sözleşmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7d727-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="7d727-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7d727-107">EXAMPLES</span></span>

### <span data-ttu-id="7d727-108">In-Memory nesnesi</span><span class="sxs-lookup"><span data-stu-id="7d727-108">Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="7d727-109">Arka uç kimlik bilgileri sözleşmesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="7d727-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="7d727-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7d727-110">PARAMETERS</span></span>

### <span data-ttu-id="7d727-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="7d727-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="7d727-112">Arka uç için kullanılan yetkilendirme üst bilgisi.</span><span class="sxs-lookup"><span data-stu-id="7d727-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="7d727-113">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7d727-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="7d727-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="7d727-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="7d727-115">Arka uç için kullanılan yetkilendirme düzeni.</span><span class="sxs-lookup"><span data-stu-id="7d727-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="7d727-116">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7d727-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="7d727-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="7d727-117">-CertificateThumbprint</span></span>
<span data-ttu-id="7d727-118">İstemci sertifikası parmak Izleri.</span><span class="sxs-lookup"><span data-stu-id="7d727-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="7d727-119">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7d727-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="7d727-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d727-120">-DefaultProfile</span></span>
<span data-ttu-id="7d727-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7d727-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d727-122">-Üst bilgi</span><span class="sxs-lookup"><span data-stu-id="7d727-122">-Header</span></span>
<span data-ttu-id="7d727-123">Arka uç tarafından kabul edilen üst bilgi parametre değerleri.</span><span class="sxs-lookup"><span data-stu-id="7d727-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="7d727-124">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7d727-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="7d727-125">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="7d727-125">-Query</span></span>
<span data-ttu-id="7d727-126">Arka uç tarafından kabul edilen sorgu parametre değerleri.</span><span class="sxs-lookup"><span data-stu-id="7d727-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="7d727-127">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7d727-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="7d727-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d727-128">CommonParameters</span></span>
<span data-ttu-id="7d727-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7d727-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d727-130">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7d727-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d727-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7d727-131">INPUTS</span></span>

### <span data-ttu-id="7d727-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7d727-132">None</span></span>

## <span data-ttu-id="7d727-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7d727-133">OUTPUTS</span></span>

### <span data-ttu-id="7d727-134">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="7d727-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="7d727-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7d727-135">NOTES</span></span>

## <span data-ttu-id="7d727-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7d727-136">RELATED LINKS</span></span>

[<span data-ttu-id="7d727-137">Get-Azapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="7d727-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="7d727-138">Yeni-Azsız arka uç</span><span class="sxs-lookup"><span data-stu-id="7d727-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="7d727-139">Yeni-Azapsananagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="7d727-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="7d727-140">Set-Azapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="7d727-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="7d727-141">Remove-Azapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="7d727-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
