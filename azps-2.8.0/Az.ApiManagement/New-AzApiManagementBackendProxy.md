---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
ms.openlocfilehash: 2ce3863a546af0f8c9da3c37a75b540d2a859da1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753538"
---
# <span data-ttu-id="04c14-101">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="04c14-101">New-AzApiManagementBackendProxy</span></span>

## <span data-ttu-id="04c14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04c14-102">SYNOPSIS</span></span>
<span data-ttu-id="04c14-103">Yeni bir arka uç proxy nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04c14-103">Creates a new Backend Proxy Object.</span></span>

## <span data-ttu-id="04c14-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="04c14-104">SYNTAX</span></span>

```
New-AzApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04c14-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="04c14-105">DESCRIPTION</span></span>
<span data-ttu-id="04c14-106">Yeni bir arka uç varlığı oluştururken pipbileceğiniz yeni bir arka uç proxy nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04c14-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="04c14-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="04c14-107">EXAMPLES</span></span>

### <span data-ttu-id="04c14-108">Arka uç proxy In-Memory nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="04c14-108">Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="04c14-109">Bir arka uç ara sunucu nesnesi oluşturur ve arka uç 'yi ayarlar</span><span class="sxs-lookup"><span data-stu-id="04c14-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="04c14-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="04c14-110">PARAMETERS</span></span>

### <span data-ttu-id="04c14-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04c14-111">-DefaultProfile</span></span>
<span data-ttu-id="04c14-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="04c14-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04c14-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="04c14-113">-ProxyCredential</span></span>
<span data-ttu-id="04c14-114">Uç ara sunucuya bağlanmak için kullanılan kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="04c14-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="04c14-115">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="04c14-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="04c14-116">-URL</span><span class="sxs-lookup"><span data-stu-id="04c14-116">-Url</span></span>
<span data-ttu-id="04c14-117">Çağrıları arka uca iletirken kullanılacak ara sunucunun URL 'si.</span><span class="sxs-lookup"><span data-stu-id="04c14-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="04c14-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="04c14-118">This parameter is required.</span></span>

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

### <span data-ttu-id="04c14-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04c14-119">CommonParameters</span></span>
<span data-ttu-id="04c14-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="04c14-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04c14-121">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="04c14-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04c14-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="04c14-122">INPUTS</span></span>

### <span data-ttu-id="04c14-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="04c14-123">None</span></span>

## <span data-ttu-id="04c14-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="04c14-124">OUTPUTS</span></span>

### <span data-ttu-id="04c14-125">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="04c14-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="04c14-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="04c14-126">NOTES</span></span>

## <span data-ttu-id="04c14-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="04c14-127">RELATED LINKS</span></span>

[<span data-ttu-id="04c14-128">Get-Azapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="04c14-128">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="04c14-129">Yeni-Azsız arka uç</span><span class="sxs-lookup"><span data-stu-id="04c14-129">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="04c14-130">Yeni-Azapsananagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="04c14-130">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="04c14-131">Set-Azapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="04c14-131">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="04c14-132">Remove-Azapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="04c14-132">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
