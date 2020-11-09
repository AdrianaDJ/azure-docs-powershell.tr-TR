---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscriptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
ms.openlocfilehash: 74362c511abde8baed24f1b484a916a9e9851426
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323473"
---
# <span data-ttu-id="3e6a2-101">Get-AzApiManagementSubscriptionKey</span><span class="sxs-lookup"><span data-stu-id="3e6a2-101">Get-AzApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="3e6a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e6a2-102">SYNOPSIS</span></span>
<span data-ttu-id="3e6a2-103">Abonelik anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="3e6a2-103">Gets subscription keys.</span></span>

## <span data-ttu-id="3e6a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3e6a2-104">SYNTAX</span></span>

```
Get-AzApiManagementSubscriptionKey -Context <PsApiManagementContext> -SubscriptionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e6a2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3e6a2-105">DESCRIPTION</span></span>
<span data-ttu-id="3e6a2-106">**Get-Azapsananagementsubscriptionkey** cmdlet 'i belirtilen aboneliğin anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="3e6a2-106">The **Get-AzApiManagementSubscriptionKey** cmdlet gets a keys of a specified subscription.</span></span>

## <span data-ttu-id="3e6a2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3e6a2-107">EXAMPLES</span></span>

### <span data-ttu-id="3e6a2-108">Örnek 1: belirtilen KIMLIĞE sahip abonelik anahtarlarını alma</span><span class="sxs-lookup"><span data-stu-id="3e6a2-108">Example 1: Get a subscription keys with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscriptionKey -Context $apimContext -SubscriptionId "0123456789"

PrimaryKey        : 5e48532634114fe999a6979ce0d63a64
SecondaryKey      : 0a8efaf85a664aa0a412241015c7c8f6
```

<span data-ttu-id="3e6a2-109">Bu komut, KIMLIĞI bir abonelik alır.</span><span class="sxs-lookup"><span data-stu-id="3e6a2-109">This command gets a subscription by ID.</span></span>

## <span data-ttu-id="3e6a2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3e6a2-110">PARAMETERS</span></span>

### <span data-ttu-id="3e6a2-111">-Context</span><span class="sxs-lookup"><span data-stu-id="3e6a2-111">-Context</span></span>
<span data-ttu-id="3e6a2-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e6a2-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e6a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e6a2-113">-DefaultProfile</span></span>
<span data-ttu-id="3e6a2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3e6a2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e6a2-115">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="3e6a2-115">-SubscriptionId</span></span>
<span data-ttu-id="3e6a2-116">Abonelik tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e6a2-116">Specifies a subscription identifier.</span></span>
<span data-ttu-id="3e6a2-117">Belirtilmişse, bu cmdlet tanımlayıcının tanımlayıcısını bulur.</span><span class="sxs-lookup"><span data-stu-id="3e6a2-117">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e6a2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e6a2-118">CommonParameters</span></span>
<span data-ttu-id="3e6a2-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3e6a2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e6a2-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3e6a2-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e6a2-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3e6a2-121">INPUTS</span></span>

### <span data-ttu-id="3e6a2-122">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="3e6a2-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3e6a2-123">System. String</span><span class="sxs-lookup"><span data-stu-id="3e6a2-123">System.String</span></span>

## <span data-ttu-id="3e6a2-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3e6a2-124">OUTPUTS</span></span>

### <span data-ttu-id="3e6a2-125">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsubscriptionkey</span><span class="sxs-lookup"><span data-stu-id="3e6a2-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="3e6a2-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3e6a2-126">NOTES</span></span>

## <span data-ttu-id="3e6a2-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3e6a2-127">RELATED LINKS</span></span>

[<span data-ttu-id="3e6a2-128">Yeni-Azsız abonelik</span><span class="sxs-lookup"><span data-stu-id="3e6a2-128">New-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="3e6a2-129">Yeni-Azsız abonelik</span><span class="sxs-lookup"><span data-stu-id="3e6a2-129">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="3e6a2-130">Remove-Azapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="3e6a2-130">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="3e6a2-131">Set-Azapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="3e6a2-131">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


