---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
ms.openlocfilehash: 58f80b6ff1742bfc6360844648d6ad18d12d8389
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591234"
---
# <span data-ttu-id="deb5e-101">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="deb5e-101">New-AzureRmApiManagementBackendCredential</span></span>

## <span data-ttu-id="deb5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="deb5e-102">SYNOPSIS</span></span>
<span data-ttu-id="deb5e-103">Yeni bir arka uç kimlik bilgileri sözleşmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="deb5e-103">Creates a new Backend Credential contract.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="deb5e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="deb5e-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="deb5e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="deb5e-105">DESCRIPTION</span></span>
<span data-ttu-id="deb5e-106">Yeni bir arka uç kimlik bilgileri sözleşmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="deb5e-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="deb5e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="deb5e-107">EXAMPLES</span></span>

### <span data-ttu-id="deb5e-108">In-Memory nesnesi</span><span class="sxs-lookup"><span data-stu-id="deb5e-108">Create a Backend Credentials In-Memory Object</span></span>
```
$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}
```

<span data-ttu-id="deb5e-109">Arka uç kimlik bilgileri sözleşmesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="deb5e-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="deb5e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="deb5e-110">PARAMETERS</span></span>

### <span data-ttu-id="deb5e-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="deb5e-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="deb5e-112">Arka uç için kullanılan yetkilendirme üst bilgisi.</span><span class="sxs-lookup"><span data-stu-id="deb5e-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="deb5e-113">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="deb5e-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="deb5e-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="deb5e-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="deb5e-115">Arka uç için kullanılan yetkilendirme düzeni.</span><span class="sxs-lookup"><span data-stu-id="deb5e-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="deb5e-116">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="deb5e-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="deb5e-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="deb5e-117">-CertificateThumbprint</span></span>
<span data-ttu-id="deb5e-118">İstemci sertifikası parmak Izleri.</span><span class="sxs-lookup"><span data-stu-id="deb5e-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="deb5e-119">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="deb5e-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="deb5e-120">-Üst bilgi</span><span class="sxs-lookup"><span data-stu-id="deb5e-120">-Header</span></span>
<span data-ttu-id="deb5e-121">Arka uç tarafından kabul edilen üst bilgi parametre değerleri.</span><span class="sxs-lookup"><span data-stu-id="deb5e-121">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="deb5e-122">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="deb5e-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="deb5e-123">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="deb5e-123">-Query</span></span>
<span data-ttu-id="deb5e-124">Arka uç tarafından kabul edilen sorgu parametre değerleri.</span><span class="sxs-lookup"><span data-stu-id="deb5e-124">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="deb5e-125">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="deb5e-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="deb5e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deb5e-126">-DefaultProfile</span></span>
<span data-ttu-id="deb5e-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="deb5e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="deb5e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deb5e-128">CommonParameters</span></span>
<span data-ttu-id="deb5e-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="deb5e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deb5e-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deb5e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deb5e-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="deb5e-131">INPUTS</span></span>

## <span data-ttu-id="deb5e-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="deb5e-132">OUTPUTS</span></span>

### <span data-ttu-id="deb5e-133">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="deb5e-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="deb5e-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="deb5e-134">NOTES</span></span>

## <span data-ttu-id="deb5e-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="deb5e-135">RELATED LINKS</span></span>

[<span data-ttu-id="deb5e-136">Get-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="deb5e-136">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="deb5e-137">Yeni-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="deb5e-137">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="deb5e-138">Yeni-Azurermapımanagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="deb5e-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="deb5e-139">Set-Azurermapımanaarka uç</span><span class="sxs-lookup"><span data-stu-id="deb5e-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="deb5e-140">Remove-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="deb5e-140">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
