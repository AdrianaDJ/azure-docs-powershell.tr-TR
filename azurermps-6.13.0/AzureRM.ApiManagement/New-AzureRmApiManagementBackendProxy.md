---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
ms.openlocfilehash: d5ff2fd4f9bd3360974d93c457e541cb2f96dc5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588643"
---
# <span data-ttu-id="b3863-101">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="b3863-101">New-AzureRmApiManagementBackendProxy</span></span>

## <span data-ttu-id="b3863-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3863-102">SYNOPSIS</span></span>
<span data-ttu-id="b3863-103">Yeni bir arka uç proxy nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b3863-103">Creates a new Backend Proxy Object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3863-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3863-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3863-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3863-105">DESCRIPTION</span></span>
<span data-ttu-id="b3863-106">Yeni bir arka uç varlığı oluştururken pipbileceğiniz yeni bir arka uç proxy nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b3863-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="b3863-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3863-107">EXAMPLES</span></span>

### <span data-ttu-id="b3863-108">Arka uç proxy In-Memory nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="b3863-108">Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzureRmApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="b3863-109">Bir arka uç ara sunucu nesnesi oluşturur ve arka uç 'yi ayarlar</span><span class="sxs-lookup"><span data-stu-id="b3863-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="b3863-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3863-110">PARAMETERS</span></span>

### <span data-ttu-id="b3863-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3863-111">-DefaultProfile</span></span>
<span data-ttu-id="b3863-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b3863-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3863-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="b3863-113">-ProxyCredential</span></span>
<span data-ttu-id="b3863-114">Uç ara sunucuya bağlanmak için kullanılan kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="b3863-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="b3863-115">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="b3863-115">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3863-116">-URL</span><span class="sxs-lookup"><span data-stu-id="b3863-116">-Url</span></span>
<span data-ttu-id="b3863-117">Çağrıları arka uca iletirken kullanılacak ara sunucunun URL 'si.</span><span class="sxs-lookup"><span data-stu-id="b3863-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="b3863-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="b3863-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3863-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3863-119">CommonParameters</span></span>
<span data-ttu-id="b3863-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3863-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3863-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3863-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3863-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3863-122">INPUTS</span></span>

### <span data-ttu-id="b3863-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b3863-123">None</span></span>

## <span data-ttu-id="b3863-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3863-124">OUTPUTS</span></span>

### <span data-ttu-id="b3863-125">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="b3863-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="b3863-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3863-126">NOTES</span></span>

## <span data-ttu-id="b3863-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3863-127">RELATED LINKS</span></span>

[<span data-ttu-id="b3863-128">Get-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="b3863-128">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="b3863-129">Yeni-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="b3863-129">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="b3863-130">Yeni-Azurermapımanagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="b3863-130">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="b3863-131">Set-Azurermapımanaarka uç</span><span class="sxs-lookup"><span data-stu-id="b3863-131">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="b3863-132">Remove-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="b3863-132">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
