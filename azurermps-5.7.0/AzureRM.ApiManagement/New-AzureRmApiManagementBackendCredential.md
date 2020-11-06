---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
ms.openlocfilehash: 4453b7fc3e13f4de2632c41cea966fdada1d84f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594518"
---
# <span data-ttu-id="b9c1f-101">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="b9c1f-101">New-AzureRmApiManagementBackendCredential</span></span>

## <span data-ttu-id="b9c1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c1f-103">Yeni bir arka uç kimlik bilgileri sözleşmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b9c1f-103">Creates a new Backend Credential contract.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9c1f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b9c1f-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9c1f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b9c1f-105">DESCRIPTION</span></span>
<span data-ttu-id="b9c1f-106">Yeni bir arka uç kimlik bilgileri sözleşmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b9c1f-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="b9c1f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b9c1f-107">EXAMPLES</span></span>

### <span data-ttu-id="b9c1f-108">In-Memory nesnesi</span><span class="sxs-lookup"><span data-stu-id="b9c1f-108">Create a Backend Credentials In-Memory Object</span></span>
```
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}
```

<span data-ttu-id="b9c1f-109">Arka uç kimlik bilgileri sözleşmesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="b9c1f-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="b9c1f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b9c1f-110">PARAMETERS</span></span>

### <span data-ttu-id="b9c1f-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="b9c1f-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="b9c1f-112">Arka uç için kullanılan yetkilendirme üst bilgisi.</span><span class="sxs-lookup"><span data-stu-id="b9c1f-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="b9c1f-113">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="b9c1f-113">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c1f-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="b9c1f-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="b9c1f-115">Arka uç için kullanılan yetkilendirme düzeni.</span><span class="sxs-lookup"><span data-stu-id="b9c1f-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="b9c1f-116">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="b9c1f-116">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c1f-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="b9c1f-117">-CertificateThumbprint</span></span>
<span data-ttu-id="b9c1f-118">İstemci sertifikası parmak Izleri.</span><span class="sxs-lookup"><span data-stu-id="b9c1f-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="b9c1f-119">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="b9c1f-119">This parameter is optional.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c1f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c1f-120">-DefaultProfile</span></span>
<span data-ttu-id="b9c1f-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b9c1f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c1f-122">-Üst bilgi</span><span class="sxs-lookup"><span data-stu-id="b9c1f-122">-Header</span></span>
<span data-ttu-id="b9c1f-123">Arka uç tarafından kabul edilen üst bilgi parametre değerleri.</span><span class="sxs-lookup"><span data-stu-id="b9c1f-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="b9c1f-124">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="b9c1f-124">This parameter is optional.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c1f-125">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="b9c1f-125">-Query</span></span>
<span data-ttu-id="b9c1f-126">Arka uç tarafından kabul edilen sorgu parametre değerleri.</span><span class="sxs-lookup"><span data-stu-id="b9c1f-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="b9c1f-127">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="b9c1f-127">This parameter is optional.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c1f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c1f-128">CommonParameters</span></span>
<span data-ttu-id="b9c1f-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b9c1f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c1f-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9c1f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c1f-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b9c1f-131">INPUTS</span></span>

### <span data-ttu-id="b9c1f-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b9c1f-132">None</span></span>
<span data-ttu-id="b9c1f-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b9c1f-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b9c1f-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b9c1f-134">OUTPUTS</span></span>

### <span data-ttu-id="b9c1f-135">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="b9c1f-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="b9c1f-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b9c1f-136">NOTES</span></span>

## <span data-ttu-id="b9c1f-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b9c1f-137">RELATED LINKS</span></span>

[<span data-ttu-id="b9c1f-138">Get-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="b9c1f-138">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="b9c1f-139">Yeni-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="b9c1f-139">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="b9c1f-140">Yeni-Azurermapımanagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="b9c1f-140">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="b9c1f-141">Set-Azurermapımanaarka uç</span><span class="sxs-lookup"><span data-stu-id="b9c1f-141">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="b9c1f-142">Remove-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="b9c1f-142">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
