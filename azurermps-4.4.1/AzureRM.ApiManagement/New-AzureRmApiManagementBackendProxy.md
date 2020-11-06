---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
ms.openlocfilehash: d3699347d21f17452d521afb3bc5524f8e68e40b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591230"
---
# <span data-ttu-id="707e2-101">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="707e2-101">New-AzureRmApiManagementBackendProxy</span></span>

## <span data-ttu-id="707e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="707e2-102">SYNOPSIS</span></span>
<span data-ttu-id="707e2-103">Yeni bir arka uç proxy nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="707e2-103">Creates a new Backend Proxy Object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="707e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="707e2-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendProxy -Url <String> [-UserName <String>] [-Password <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="707e2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="707e2-105">DESCRIPTION</span></span>
<span data-ttu-id="707e2-106">Yeni bir arka uç varlığı oluştururken pipbileceğiniz yeni bir arka uç proxy nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="707e2-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="707e2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="707e2-107">EXAMPLES</span></span>

### <span data-ttu-id="707e2-108">Arka uç proxy In-Memory nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="707e2-108">Create a Backend Proxy In-Memory Object</span></span>
```
$proxy= New-AzureRmApiManagementBackendProxy -Url "https://abbc.def.g" -UserName "apim" -Password "password"
```

<span data-ttu-id="707e2-109">Arka uç proxy nesnesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="707e2-109">Creates a Backend Proxy Object</span></span>

## <span data-ttu-id="707e2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="707e2-110">PARAMETERS</span></span>

### <span data-ttu-id="707e2-111">-Parola</span><span class="sxs-lookup"><span data-stu-id="707e2-111">-Password</span></span>
<span data-ttu-id="707e2-112">Uç ara sunucuya bağlanmak için kullanılan proxy parolası.</span><span class="sxs-lookup"><span data-stu-id="707e2-112">Proxy Password used to connect to Backend Proxy.</span></span>
<span data-ttu-id="707e2-113">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="707e2-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="707e2-114">-URL</span><span class="sxs-lookup"><span data-stu-id="707e2-114">-Url</span></span>
<span data-ttu-id="707e2-115">Çağrıları arka uca iletirken kullanılacak ara sunucunun URL 'si.</span><span class="sxs-lookup"><span data-stu-id="707e2-115">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="707e2-116">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="707e2-116">This parameter is required.</span></span>

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

### <span data-ttu-id="707e2-117">-Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="707e2-117">-UserName</span></span>
<span data-ttu-id="707e2-118">Uç ara sunucuya bağlanmak için kullanılan proxy Kullanıcı adı.</span><span class="sxs-lookup"><span data-stu-id="707e2-118">Proxy UserName used to connect to Backend Proxy.</span></span>
<span data-ttu-id="707e2-119">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="707e2-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="707e2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="707e2-120">-DefaultProfile</span></span>
<span data-ttu-id="707e2-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="707e2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="707e2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="707e2-122">CommonParameters</span></span>
<span data-ttu-id="707e2-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="707e2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="707e2-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="707e2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="707e2-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="707e2-125">INPUTS</span></span>

## <span data-ttu-id="707e2-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="707e2-126">OUTPUTS</span></span>

### <span data-ttu-id="707e2-127">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="707e2-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="707e2-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="707e2-128">NOTES</span></span>

## <span data-ttu-id="707e2-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="707e2-129">RELATED LINKS</span></span>

[<span data-ttu-id="707e2-130">Get-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="707e2-130">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="707e2-131">Yeni-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="707e2-131">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="707e2-132">Yeni-Azurermapımanagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="707e2-132">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="707e2-133">Set-Azurermapımanaarka uç</span><span class="sxs-lookup"><span data-stu-id="707e2-133">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="707e2-134">Remove-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="707e2-134">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
