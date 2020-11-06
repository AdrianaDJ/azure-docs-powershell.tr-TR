---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
ms.openlocfilehash: 890f169c3fd497f7045522133e1e9e1f1d509aca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594517"
---
# <span data-ttu-id="e0a60-101">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="e0a60-101">New-AzureRmApiManagementBackendProxy</span></span>

## <span data-ttu-id="e0a60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0a60-102">SYNOPSIS</span></span>
<span data-ttu-id="e0a60-103">Yeni bir arka uç proxy nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e0a60-103">Creates a new Backend Proxy Object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0a60-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0a60-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0a60-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0a60-105">DESCRIPTION</span></span>
<span data-ttu-id="e0a60-106">Yeni bir arka uç varlığı oluştururken pipbileceğiniz yeni bir arka uç proxy nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e0a60-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="e0a60-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0a60-107">EXAMPLES</span></span>

### <span data-ttu-id="e0a60-108">Arka uç proxy In-Memory nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="e0a60-108">Create a Backend Proxy In-Memory Object</span></span>
```
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzureRmApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds
```

<span data-ttu-id="e0a60-109">Arka uç proxy nesnesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="e0a60-109">Creates a Backend Proxy Object</span></span>

## <span data-ttu-id="e0a60-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0a60-110">PARAMETERS</span></span>

### <span data-ttu-id="e0a60-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0a60-111">-DefaultProfile</span></span>
<span data-ttu-id="e0a60-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e0a60-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="e0a60-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="e0a60-113">-ProxyCredential</span></span>
<span data-ttu-id="e0a60-114">Uç ara sunucuya bağlanmak için kullanılan kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="e0a60-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="e0a60-115">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e0a60-115">This parameter is optional.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0a60-116">-URL</span><span class="sxs-lookup"><span data-stu-id="e0a60-116">-Url</span></span>
<span data-ttu-id="e0a60-117">Çağrıları arka uca iletirken kullanılacak ara sunucunun URL 'si.</span><span class="sxs-lookup"><span data-stu-id="e0a60-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="e0a60-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e0a60-118">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0a60-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0a60-119">CommonParameters</span></span>
<span data-ttu-id="e0a60-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0a60-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0a60-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0a60-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0a60-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0a60-122">INPUTS</span></span>

### <span data-ttu-id="e0a60-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e0a60-123">None</span></span>
<span data-ttu-id="e0a60-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="e0a60-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e0a60-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0a60-125">OUTPUTS</span></span>

### <span data-ttu-id="e0a60-126">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="e0a60-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="e0a60-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0a60-127">NOTES</span></span>

## <span data-ttu-id="e0a60-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0a60-128">RELATED LINKS</span></span>

[<span data-ttu-id="e0a60-129">Get-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="e0a60-129">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="e0a60-130">Yeni-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="e0a60-130">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="e0a60-131">Yeni-Azurermapımanagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="e0a60-131">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="e0a60-132">Set-Azurermapımanaarka uç</span><span class="sxs-lookup"><span data-stu-id="e0a60-132">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="e0a60-133">Remove-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="e0a60-133">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
