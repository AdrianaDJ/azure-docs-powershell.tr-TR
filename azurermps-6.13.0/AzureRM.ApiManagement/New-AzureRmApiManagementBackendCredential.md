---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
ms.openlocfilehash: d34a7666e10fe678d49194887d9b58e7c1ba0aa7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588644"
---
# <span data-ttu-id="0250d-101">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="0250d-101">New-AzureRmApiManagementBackendCredential</span></span>

## <span data-ttu-id="0250d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0250d-102">SYNOPSIS</span></span>
<span data-ttu-id="0250d-103">Yeni bir arka uç kimlik bilgileri sözleşmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0250d-103">Creates a new Backend Credential contract.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0250d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0250d-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0250d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0250d-105">DESCRIPTION</span></span>
<span data-ttu-id="0250d-106">Yeni bir arka uç kimlik bilgileri sözleşmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0250d-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="0250d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0250d-107">EXAMPLES</span></span>

### <span data-ttu-id="0250d-108">In-Memory nesnesi</span><span class="sxs-lookup"><span data-stu-id="0250d-108">Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="0250d-109">Arka uç kimlik bilgileri sözleşmesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="0250d-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="0250d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0250d-110">PARAMETERS</span></span>

### <span data-ttu-id="0250d-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="0250d-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="0250d-112">Arka uç için kullanılan yetkilendirme üst bilgisi.</span><span class="sxs-lookup"><span data-stu-id="0250d-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="0250d-113">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="0250d-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="0250d-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="0250d-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="0250d-115">Arka uç için kullanılan yetkilendirme düzeni.</span><span class="sxs-lookup"><span data-stu-id="0250d-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="0250d-116">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="0250d-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="0250d-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="0250d-117">-CertificateThumbprint</span></span>
<span data-ttu-id="0250d-118">İstemci sertifikası parmak Izleri.</span><span class="sxs-lookup"><span data-stu-id="0250d-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="0250d-119">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="0250d-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="0250d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0250d-120">-DefaultProfile</span></span>
<span data-ttu-id="0250d-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0250d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0250d-122">-Üst bilgi</span><span class="sxs-lookup"><span data-stu-id="0250d-122">-Header</span></span>
<span data-ttu-id="0250d-123">Arka uç tarafından kabul edilen üst bilgi parametre değerleri.</span><span class="sxs-lookup"><span data-stu-id="0250d-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="0250d-124">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="0250d-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="0250d-125">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="0250d-125">-Query</span></span>
<span data-ttu-id="0250d-126">Arka uç tarafından kabul edilen sorgu parametre değerleri.</span><span class="sxs-lookup"><span data-stu-id="0250d-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="0250d-127">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="0250d-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="0250d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0250d-128">CommonParameters</span></span>
<span data-ttu-id="0250d-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0250d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0250d-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0250d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0250d-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0250d-131">INPUTS</span></span>

### <span data-ttu-id="0250d-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0250d-132">None</span></span>

## <span data-ttu-id="0250d-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0250d-133">OUTPUTS</span></span>

### <span data-ttu-id="0250d-134">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="0250d-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="0250d-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0250d-135">NOTES</span></span>

## <span data-ttu-id="0250d-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0250d-136">RELATED LINKS</span></span>

[<span data-ttu-id="0250d-137">Get-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="0250d-137">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="0250d-138">Yeni-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="0250d-138">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="0250d-139">Yeni-Azurermapımanagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="0250d-139">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="0250d-140">Set-Azurermapımanaarka uç</span><span class="sxs-lookup"><span data-stu-id="0250d-140">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="0250d-141">Remove-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="0250d-141">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
